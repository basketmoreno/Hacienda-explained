# Estructura del proyecto

## Código fuente

### data_collector.py

Script encargado de:

- Descargar datos abiertos de la Plataforma de Contratación del Sector Público (PLACSP).
- Extraer los ficheros ATOM publicados por la plataforma.
- Filtrar únicamente las licitaciones relacionadas con la Agencia Estatal de Administración Tributaria (AEAT).
- Procesar y normalizar los datos.
- Generar el conjunto de datos consolidado utilizado por el dashboard.

### data_visualization.html

Aplicación web de análisis y visualización.

Permite:

- Explorar las licitaciones de la AEAT.
- Analizar la evolución temporal del gasto.
- Visualizar las principales categorías de contratación.
- Identificar órganos de contratación.
- Revisar contratos relevantes.
- Detectar posibles anomalías.
- Consultar cada expediente con enlace directo a la Plataforma de Contratación del Sector Público.

---

## Dataset generado

### data_clean.xlsx

Base de datos consolidada obtenida a partir de los datos abiertos de la PLACSP.

Contiene información estructurada de las licitaciones de la Agencia Estatal de Administración Tributaria entre 2012 y 2026.

Campos principales:

- Año fuente
- Expediente
- Objeto del contrato
- Órgano de contratación
- Importe sin IVA
- Importe con IVA
- Tipo de contrato
- Procedimiento
- Código CPV
- Fecha de publicación
- Fecha de actualización
- URL oficial del expediente

---

# Fuentes documentales utilizadas

Además de los datos abiertos obtenidos de la Plataforma de Contratación del Sector Público, se han utilizado documentos oficiales de la Agencia Estatal de Administración Tributaria (AEAT) y de la Agencia Tributaria Española para contextualizar y validar los análisis.

## Manuales tributarios

### ManualRenta2025Parte1_es_es.pdf

Manual oficial del Impuesto sobre la Renta de las Personas Físicas (IRPF) 2025.

Utilizado para:

- Comprender los procesos de atención al contribuyente.
- Analizar servicios de asistencia tributaria.
- Contextualizar contratos relacionados con campañas de Renta.

### ManualRenta2025Parte2_es_es.pdf

Segunda parte del Manual de IRPF 2025.

Utilizado para:

- Identificar necesidades funcionales y operativas de la AEAT.
- Comprender procedimientos administrativos y servicios prestados al ciudadano.

### Manual_IVA_2025.pdf

Manual oficial del Impuesto sobre el Valor Añadido (IVA).

Utilizado para:

- Contextualizar procesos operativos gestionados por la Agencia Tributaria.
- Analizar posibles necesidades de sistemas y herramientas informáticas asociadas.

### Manual_Sociedades_2025.pdf

Manual oficial del Impuesto sobre Sociedades.

Utilizado para:

- Entender procesos de gestión tributaria empresarial.
- Relacionar contratos tecnológicos con necesidades operativas de la AEAT.

### ManualPatrimonio2025_es_es.pdf

Manual oficial del Impuesto sobre el Patrimonio.

Utilizado como referencia para comprender servicios tributarios específicos y su posible impacto en los sistemas de información de la Agencia Tributaria.

---

# Origen de los datos

## Plataforma de Contratación del Sector Público (PLACSP)

Fuente principal:

https://contrataciondelestado.es

Los datos proceden de los ficheros ATOM publicados por la Plataforma de Contratación del Sector Público, que contienen información oficial sobre:

- Licitaciones
- Adjudicaciones
- Modificaciones
- Actualizaciones de expedientes

La extracción realizada por `data_collector.py` filtra exclusivamente aquellos expedientes relacionados con la Agencia Estatal de Administración Tributaria (AEAT).

---

# Resultado final

El proyecto transforma datos abiertos de contratación pública en una plataforma de análisis compuesta por:

- `data_collector.py`: recopilación y tratamiento de datos
- `data_clean.xlsx`: dataset consolidado
- `data_visualization.html`: cuadro de mando interactivo

Todo ello apoyado en documentación oficial tributaria de la AEAT correspondiente al ejercicio 2025.
