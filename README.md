# 🏛️ Hacienda Explained

> Plataforma de análisis de la contratación pública de la Agencia Estatal de Administración Tributaria (AEAT) construida a partir de datos abiertos de la Plataforma de Contratación del Sector Público (PLACSP).

---

## 🎯 Objetivo

La Agencia Tributaria publica miles de anuncios y actualizaciones de contratación cada año. Sin embargo, la información se encuentra dispersa entre expedientes, modificaciones, correcciones y publicaciones técnicas difíciles de analizar de forma global.

Este proyecto transforma esos datos abiertos en una plataforma que permite responder preguntas como:

- 💰 ¿En qué gasta el dinero la Agencia Tributaria?
- 📈 ¿Cómo ha evolucionado el gasto entre 2012 y 2026?
- 💻 ¿Cuánto se invierte en tecnología?
- 🏗️ ¿Cuáles son las mayores obras públicas?
- 🚁 ¿Cuánto cuesta mantener la flota aérea y marítima?
- 📡 ¿Cómo evolucionan los grandes contratos de telecomunicaciones?
- 🚨 ¿Existen patrones o anomalías interesantes?

---

## 📊 Resultados obtenidos

| Métrica | Valor |
|----------|----------:|
| 📅 Periodo analizado | 2012-2026 |
| 📄 Publicaciones procesadas | 3.184 |
| 📋 Licitaciones únicas | 746 |
| 💰 Importe analizado | 1.155 M€ |
| 🏢 Órganos de contratación | 4 |
| 📂 Categorías de gasto | 10 |

---

## 🏗️ Arquitectura del proyecto

```text
🐍 data_collector.py
         ↓
📊 data_clean.xlsx
         ↓
🌐 data_visualization.html
```

### 🐍 Data Collector

Obtiene automáticamente los datos desde la Plataforma de Contratación del Sector Público:

- Descarga ficheros ATOM
- Procesa XML oficiales
- Filtra expedientes AEAT
- Normaliza información
- Genera dataset consolidado

---

### 📊 Dataset

Dataset estructurado utilizado por el dashboard.

Información disponible:

- Expediente
- Objeto del contrato
- Órgano de contratación
- Procedimiento
- Tipo de contrato
- CPV
- Importe
- Fechas
- URL oficial

---

### 🌐 Dashboard

Aplicación interactiva para explorar los datos.

Permite visualizar:

#### 📈 Evolución temporal

- Importe anual
- Número de expedientes
- Cambios de tendencia

#### 💸 Distribución del gasto

- 💻 Tecnología
- 📡 Telecomunicaciones
- 🚁 Flota aérea y marítima
- 🏗️ Obras
- ☎️ Atención al contribuyente
- 🧹 Limpieza
- 🔒 Seguridad

#### 🏢 Órganos de contratación

Comparación entre:

- Servicios Centrales
- Cataluña
- Castilla-La Mancha
- Murcia

#### 🏆 Grandes proyectos

Identificación automática de los mayores contratos.

Ejemplos:

| Proyecto | Importe |
|-----------|----------:|
| Mainframe IBM | 77,6 M€ |
| Nueva sede Valencia | 74,4 M€ |
| Nuevo DIT Madrid | 69,9 M€ |
| Telecomunicaciones AEAT | 53,6 M€ |

#### 🚨 Análisis de anomalías

Detección automática de:

- Posibles duplicidades
- Importes repetidos
- Contratos próximos a umbrales legales
- Expedientes con múltiples modificaciones

---

## 🌍 Fuente de datos

Todos los datos económicos proceden de fuentes oficiales de contratación pública:

🔗 https://contrataciondelestado.es

---

## 📚 Documentación de referencia

Los siguientes documentos se utilizan únicamente para comprender el funcionamiento y los procesos gestionados por la Agencia Tributaria.

### 👤 Impuesto sobre la Renta (IRPF)

- [ManualRenta2025Parte1_es_es.pdf](https://github.com/basketmoreno/Hacienda-explained/blob/main/ManualRenta2025Parte1_es_es.pdf)
- [ManualRenta2025Parte2_es_es.pdf](https://github.com/basketmoreno/Hacienda-explained/blob/main/ManualRenta2025Parte2_es_es.pdf)

### 💶 IVA

- [Manual_IVA_2025.pdf](https://github.com/basketmoreno/Hacienda-explained/blob/main/Manual_IVA_2025.pdf)

### 🏢 Impuesto sobre Sociedades

- [Manual_Sociedades_2025.pdf](https://github.com/basketmoreno/Hacienda-explained/blob/main/Manual_Sociedades_2025.pdf)

### 🏠 Impuesto sobre el Patrimonio

- [ManualPatrimonio2025_es_es.pdf](https://github.com/basketmoreno/Hacienda-explained/blob/main/ManualPatrimonio2025_es_es.pdf)

---

## ⚠️ Nota importante

Los análisis económicos, importes y expedientes mostrados en el proyecto proceden exclusivamente de la Plataforma de Contratación del Sector Público.

Los manuales tributarios incluidos en el repositorio se utilizan únicamente como documentación contextual y referencia funcional.
