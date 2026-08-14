# PLACSP - Exportador AEAT

Este script descarga los datos abiertos de la Plataforma de Contratación del Sector Público (PLACSP), filtra las licitaciones relacionadas con la Agencia Tributaria y genera un único fichero Excel con una hoja por año.

---

# Parámetros de búsqueda

## Años a consultar

Define el rango de años a descargar.

```python
YEARS = range(2012, 2027)
```

### Ejemplos

Solo 2026:

```python
YEARS = [2026]
```

Últimos 5 años:

```python
YEARS = range(2022, 2027)
```

Años concretos:

```python
YEARS = [2018, 2020, 2023, 2026]
```

---

## Filtro por órgano de contratación

El filtro principal se realiza sobre el campo **Órgano de contratación**.

```python
PATRONES_ORGANO = [
    r"Agencia Estatal de Administración Tributaria",
    r"\bAEAT\b",
    r"Departamento de Informática Tributaria",
    r"Delegación Especial de la AEAT",
]
```

### Añadir nuevos organismos

Por ejemplo:

```python
PATRONES_ORGANO = [
    r"Agencia Estatal de Administración Tributaria",
    r"\bAEAT\b",
    r"Departamento de Informática Tributaria",
    r"Delegación Especial de la AEAT",
    r"Dirección General del Catastro",
]
```

---

## Validación SSL

Permite activar o desactivar la validación de certificados HTTPS.

```python
VERIFY_SSL = True
```

### Desactivar SSL

Solo si se producen errores de certificado:

```python
VERIFY_SSL = False
```

---

# Ubicación de los archivos

## Carpeta principal

```python
WORK_DIR = DOWNLOADS_DIR / "PLACSP_AEAT"
```

Resultado:

```text
C:\Users\<usuario>\Downloads\PLACSP_AEAT
```

---

## ZIP descargados

```python
ZIP_DIR = WORK_DIR / "zips_descargados"
```

Contiene:

```text
licitaciones_2012.zip
licitaciones_2013.zip
...
licitaciones_2026.zip
```

---

## Ficheros ATOM extraídos

```python
ATOM_DIR = WORK_DIR / "atom_extraidos"
```

Contiene:

```text
atom_extraidos
 ├─ 2012
 ├─ 2013
 ├─ 2014
 ...
 └─ 2026
```

Los ficheros ATOM se conservan para evitar volver a descomprimir los ZIP en futuras ejecuciones.

---

## Excel generado

```python
OUTPUT_FILE = WORK_DIR / "licitaciones_aeat_2012_2026.xlsx"
```

Resultado:

```text
C:\Users\<usuario>\Downloads\PLACSP_AEAT\licitaciones_aeat_2012_2026.xlsx
```

---

# Campos exportados

El Excel contiene las siguientes columnas:

```python
COLUMNAS = [
    "Año fuente",
    "Expediente",
    "Objeto",
    "Órgano de contratación",
    "Coincidencia filtro",
    "Estado",
    "Importe sin IVA",
    "Importe con IVA",
    "Tipo de contrato",
    "Procedimiento",
    "CPV",
    "Fecha publicación",
    "Fecha actualización",
    "URL",
]
```

---

# Formato del Excel

## Hojas

Se crea una worksheet independiente para cada año.

Ejemplo:

```text
2012
2013
2014
...
2026
```

---

## Tipos de datos

### Importes

```text
12.345,67 €
```

Se almacenan como números Excel.

---

### Fechas

```text
31-12-2025
```

Formato:

```text
DD-MM-AAAA
```

---

### CPV

Se almacena como texto para conservar ceros iniciales.

---

# Reutilización de datos

## ZIP ya descargado

Si existe:

```text
zips_descargados\licitaciones_2025.zip
```

el script lo reutiliza y no vuelve a descargarlo.

---

## ATOM ya extraído

Si existe:

```text
atom_extraidos\2025
```

el script reutiliza los ficheros extraídos y no vuelve a descomprimir el ZIP.

---

# Cómo ampliar la búsqueda

## Buscar varios organismos

```python
PATRONES_ORGANO = [
    r"AEAT",
    r"Agencia Tributaria",
    r"Dirección General del Catastro",
    r"Tesoro Público",
]
```

---

## Buscar cualquier contrato de Hacienda

```python
PATRONES_ORGANO = [
    r"Hacienda",
    r"Tributaria",
    r"AEAT",
]
```

---

# Salida esperada

Al finalizar se obtiene:

```text
Downloads
 └─ PLACSP_AEAT
     ├─ licitaciones_aeat_2012_2026.xlsx
     ├─ zips_descargados
     └─ atom_extraidos
```

El Excel contiene únicamente los expedientes cuyo órgano de contratación coincide con alguno de los patrones definidos en `PATRONES_ORGANO`.
