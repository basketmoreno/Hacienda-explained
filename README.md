# 🏛️ Hacienda Explained

> Plataforma de análisis de contratación pública de la Agencia Estatal de Administración Tributaria (AEAT) basada en datos abiertos de la Plataforma de Contratación del Sector Público (PLACSP).

El objetivo del proyecto es transformar miles de publicaciones de contratación pública en información comprensible, visual e investigable para ciudadanos, periodistas, investigadores, desarrolladores y profesionales del sector público.

---

# 🔗 Enlaces rápidos

## 📊 Datos y aplicación

- 🌐 Dashboard interactivo: `data_visualization.html`
- 📊 Dataset consolidado: `data_clean.xlsx`
- 🐍 Recolector de datos: `data_collector.py`

---

## 📚 Documentación oficial utilizada

### 👤 IRPF

- 📄 https://github.com/basketmoreno/Hacienda-explained/blob/main/ManualRenta2025Parte1_es_es.pdf
- 📄 https://github.com/basketmoreno/Hacienda-explained/blob/main/ManualRenta2025Parte2_es_es.pdf

### 💶 IVA

- 📄 https://github.com/basketmoreno/Hacienda-explained/blob/main/Manual_IVA_2025.pdf

### 🏢 Impuesto sobre Sociedades

- 📄 https://github.com/basketmoreno/Hacienda-explained/blob/main/Manual_Sociedades_2025.pdf

### 🏠 Impuesto sobre el Patrimonio

- 📄 https://github.com/basketmoreno/Hacienda-explained/blob/main/ManualPatrimonio2025_es_es.pdf

---

# 📂 Estructura del proyecto

```text
📦 Hacienda-explained
│
├── 📄 README.md
│
├── 🐍 data_collector.py
├── 📊 data_clean.xlsx
├── 🌐 data_visualization.html
│
├── 📚 ManualRenta2025Parte1_es_es.pdf
├── 📚 ManualRenta2025Parte2_es_es.pdf
├── 📚 Manual_IVA_2025.pdf
├── 📚 Manual_Sociedades_2025.pdf
└── 📚 ManualPatrimonio2025_es_es.pdf
```

---

# 🐍 Data Collector

## 📄 Archivo

```text
data_collector.py
```

## 🎯 Función

Automatiza la descarga y procesamiento de licitaciones de la Agencia Tributaria desde la Plataforma de Contratación del Sector Público.

---

## ⚙️ Qué hace

✅ Descarga datos históricos de contratación

✅ Procesa ficheros ATOM publicados por la PLACSP

✅ Filtra únicamente licitaciones relacionadas con la AEAT

✅ Extrae información estructurada

✅ Normaliza formatos

✅ Consolida resultados

✅ Genera el dataset utilizado por el dashboard

---

## 📥 Datos obtenidos

Para cada expediente se recopilan:

- 📋 Expediente
- 📝 Objeto del contrato
- 🏢 Órgano de contratación
- 💰 Importe sin IVA
- 💵 Importe con IVA
- 📑 Procedimiento
- 📦 Tipo de contrato
- 🏷️ Código CPV
- 📅 Fecha de publicación
- 🔄 Fecha de actualización
- 🔗 URL oficial

---

# 📊 Dataset

## 📄 Archivo

```text
data_clean.xlsx
```

---

## 📈 Cobertura temporal

```text
2012 – 2026
```

---

## 📦 Volumen analizado

### 📄 Publicaciones procesadas

```text
3.184 registros
```

Cada fila representa una publicación o actualización en la plataforma.

---

### 🏷️ Licitaciones únicas

```text
746 expedientes
```

Tras eliminar duplicados y actualizaciones repetidas.

---

### 💰 Importe total analizado

```text
1.155.927.992 €
```

Más de:

```text
1.155 millones de euros
```

de contratación pública.

---

## 🏢 Órganos analizados

### 🏛️ Dirección General (Servicios Centrales)

Grandes contratos nacionales:

- 💻 Informática
- 📡 Telecomunicaciones
- 🏗️ Grandes obras
- 🚁 Flota aérea
- 🚢 Flota marítima

---

### 🌍 Delegación Especial de Cataluña

Incluye:

- Barcelona
- Girona
- Lleida
- Tarragona

---

### 🌍 Delegación Especial de Castilla-La Mancha

Incluye:

- Albacete
- Ciudad Real
- Cuenca
- Guadalajara
- Toledo

---

### 🌍 Delegación Especial de Murcia

Incluye:

- Murcia
- Cartagena
- Vigilancia Aduanera

---

# 🌐 Dashboard

## 📄 Archivo

```text
data_visualization.html
```

## 🎯 Objetivo

Transformar datos complejos de contratación pública en información visual e interactiva.

---

# 📈 ¿Qué se puede visualizar?

## 🗓️ Evolución anual

Visualización de:

- 💰 Importe licitado por año
- 📋 Número de expedientes
- 📈 Tendencias de gasto

---

## 💸 Distribución del gasto

Clasificación automática por categorías:

### 💻 Tecnología y Sistemas

≈ 454 M€

### 🏗️ Obras y Construcción

≈ 198 M€

### 🚁 Flota Aérea y Marítima

≈ 177 M€

### 📡 Telecomunicaciones

≈ 162 M€

### ☎️ Atención al Contribuyente

≈ 70 M€

### 🧹 Limpieza

≈ 40 M€

### 🔒 Seguridad

≈ 27 M€

---

## 🏢 Órganos de contratación

Comparativa entre:

- Dirección General
- Cataluña
- Castilla-La Mancha
- Murcia

Mostrando:

✅ Importe total

✅ Número de contratos

✅ Mediana por expediente

✅ Peso relativo del gasto

---

## 📑 Procedimientos de contratación

Análisis histórico de:

- 📖 Abierto
- 📖 Abierto simplificado
- 🤝 Negociado con publicidad
- 🤝 Negociado sin publicidad
- 📋 Acuerdo marco

---

## 🏆 Grandes contratos

Identificación automática de los proyectos más relevantes.

Ejemplos:

### 💻 Mainframe IBM

```text
77,6 M€
```

### 🏗️ Nueva sede AEAT Valencia

```text
74,4 M€
```

### 🏢 Nuevo edificio DIT Madrid

```text
69,9 M€
```

### 📡 Telecomunicaciones AEAT

```text
53,6 M€
```

---

## 📉 Evolución de costes

Seguimiento histórico de contratos recurrentes:

- 💻 Mainframe IBM
- 📡 Telecomunicaciones
- ☎️ Información Tributaria
- 🧹 Limpieza
- 🔒 Vigilancia
- 🚢 Motores MTU

Permite detectar tendencias y evolución de precios.

---

## 🚨 Detección de anomalías

El sistema destaca automáticamente situaciones que pueden resultar interesantes para una revisión posterior.

### 🔁 Posibles duplicidades

Contratos prácticamente idénticos publicados más de una vez.

---

### 💰 Importes repetidos

Presupuestos que aparecen exactamente iguales en distintos ejercicios.

---

### 📏 Contratos próximos a límites legales

Expedientes muy cercanos a determinados umbrales económicos.

---

### 🔄 Exceso de modificaciones

Procedimientos con gran número de actualizaciones.

---

### 📊 Patrones llamativos

Cambios significativos en contratación o gasto.

---

## 🔍 Explorador completo

Consulta interactiva de las:

```text
746 licitaciones únicas
```

mediante filtros por:

- 🔎 Texto libre
- 🏢 Órgano
- 📂 Categoría
- 📑 Procedimiento
- 📅 Año

Cada expediente enlaza directamente con la publicación oficial.

---

# 📚 Documentación de referencia

Los siguientes manuales oficiales se utilizan para comprender el funcionamiento de la Agencia Tributaria y contextualizar sus necesidades operativas.

## 👤 IRPF

- ManualRenta2025Parte1_es_es.pdf
- ManualRenta2025Parte2_es_es.pdf

---

## 💶 IVA

- Manual_IVA_2025.pdf

---

## 🏢 Impuesto sobre Sociedades

- Manual_Sociedades_2025.pdf

---

## 🏠 Impuesto sobre el Patrimonio

- ManualPatrimonio2025_es_es.pdf

---

## 🎯 Utilidad de esta documentación

✅ Comprender los servicios prestados por la AEAT

✅ Entender procesos tributarios reales

✅ Relacionar contratos con funciones de negocio

✅ Contextualizar proyectos tecnológicos

✅ Analizar la transformación digital de la Agencia Tributaria

---

# 🌍 Fuente principal de datos

## Plataforma de Contratación del Sector Público

🔗 https://contrataciondelestado.es

Los datos proceden de publicaciones oficiales relativas a:

- Licitaciones
- Modificaciones
- Actualizaciones
- Procedimientos de contratación
- Expedientes administrativos

---

# ⚠️ Importante

Los importes, licitaciones, expedientes y análisis económicos proceden exclusivamente de los datos abiertos de la Plataforma de Contratación del Sector Público.

Los manuales tributarios incluidos en el repositorio se utilizan únicamente como material documental de referencia y contextualización.

---

# 🚀 Resultado final

```text
🐍 data_collector.py
          ↓
📊 data_clean.xlsx
          ↓
🌐 data_visualization.html
```

El proyecto permite explorar de forma visual e interactiva:

```text
💰 1.155 millones de euros
📋 746 licitaciones únicas
📄 3.184 publicaciones procesadas
📅 Periodo 2012-2026
🏛️ Agencia Estatal de Administración Tributaria
```

convirtiendo datos abiertos de contratación pública en información accesible, auditable y fácil de comprender.
