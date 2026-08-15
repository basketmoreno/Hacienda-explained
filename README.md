# 🏛️ AEAT Procurement Analytics

> Análisis de las licitaciones públicas de la Agencia Estatal de Administración Tributaria (AEAT) utilizando datos abiertos de la Plataforma de Contratación del Sector Público (PLACSP).

---

# 📂 Estructura del proyecto

```text
📦 Proyecto
├── 📄 README.md
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

## 📄 Fichero

```text
data_collector.py
```

## 🎯 Objetivo

Automatizar la descarga y procesamiento de licitaciones AEAT desde la PLACSP.

## ⚙️ Funcionalidades

✅ Descarga datos históricos (2012-2026)

✅ Extrae ficheros ATOM

✅ Filtra únicamente expedientes AEAT

✅ Normaliza datos

✅ Elimina ruido y registros innecesarios

✅ Genera dataset consolidado

✅ Prepara la información para el dashboard

---

# 📊 Dataset

## 📄 Fichero

```text
data_clean.xlsx
```

## 📈 Contenido

Contiene:

| 📋 Campo |
|-----------|
| Año |
| Expediente |
| Objeto |
| Órgano de contratación |
| Importe sin IVA |
| Importe con IVA |
| Procedimiento |
| Tipo de contrato |
| Código CPV |
| Fecha publicación |
| Fecha actualización |
| URL oficial |

---

## 📦 Volumen de datos

### 📄 Publicaciones procesadas

```text
3.184 registros
```

### 🏷️ Licitaciones únicas

```text
746 expedientes
```

### 💰 Importe total analizado

```text
1.155.927.992 €
```

Más de:

```text
1.155 millones €
```

---

# 🌐 Dashboard

## 📄 Fichero

```text
data_visualization.html
```

## 🎯 Objetivo

Convertir los datos brutos en información útil y visual.

---

## 📈 ¿Qué se puede visualizar?

### 🗓️ Evolución anual

- Importe contratado por año
- Número de expedientes
- Tendencias históricas

---

### 💰 Distribución del gasto

- 💻 Tecnología
- 📡 Telecomunicaciones
- 🚁 Flota aérea
- 🚢 Flota marítima
- 🏗️ Obras
- 🧹 Limpieza
- 🔒 Seguridad

---

### 🏢 Órganos de contratación

- Dirección General (SSCC)
- Cataluña
- Castilla-La Mancha
- Murcia

---

### 📑 Procedimientos

- Abierto
- Abierto simplificado
- Negociado
- Acuerdo marco

---

### 🏆 Grandes contratos

Identifica automáticamente:

- Contratos más caros
- Proyectos estratégicos
- Principales inversiones

Ejemplos:

```text
💻 Mainframe IBM
🏗️ Nueva sede Valencia
🏢 Nuevo DIT Madrid
📡 Telecomunicaciones AEAT
```

---

### 📉 Evolución de costes

Seguimiento de contratos recurrentes:

- IBM Mainframe
- Telecomunicaciones
- Atención telefónica
- Limpieza
- Seguridad
- Motores MTU

---

### 🚨 Detección de anomalías

El dashboard resalta automáticamente:

✅ Posibles duplicidades

✅ Importes repetidos

✅ Contratos cercanos a umbrales legales

✅ Expedientes con demasiadas modificaciones

✅ Patrones de contratación relevantes

---

### 🔍 Buscador avanzado

Permite filtrar por:

```text
🔎 Texto
🏢 Órgano
📑 Procedimiento
📂 Categoría
📆 Año
```

Con acceso directo al expediente oficial.

---

# 📚 Documentación utilizada

Los siguientes documentos oficiales se utilizan como referencia documental para comprender la actividad y los servicios gestionados por la Agencia Tributaria:

## 👤 IRPF

📄 ManualRenta2025Parte1_es_es.pdf

📄 ManualRenta2025Parte2_es_es.pdf

---

## 💶 IVA

📄 Manual_IVA_2025.pdf

---

## 🏢 Impuesto sobre Sociedades

📄 Manual_Sociedades_2025.pdf

---

## 🏠 Impuesto sobre el Patrimonio

📄 ManualPatrimonio2025_es_es.pdf

---

# 🌍 Fuente de datos

## Plataforma de Contratación del Sector Público

🔗 https://contrataciondelestado.es

Los datos proceden de:

- Licitaciones públicas
- Actualizaciones de expedientes
- Anuncios de contratación
- Procedimientos de adjudicación

---

# 🚀 Resultado final

El proyecto transforma datos abiertos de contratación pública en una plataforma de análisis compuesta por:

```text
🐍 data_collector.py
       ↓
📊 data_clean.xlsx
       ↓
🌐 data_visualization.html
```

Permitiendo analizar más de:

```text
💰 1.155 millones de euros
📋 746 licitaciones
📅 2012-2026
```

de contratación pública de la Agencia Estatal de Administración Tributaria.
