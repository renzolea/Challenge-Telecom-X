# Alura Cursos - Challenge 2: Data Science LATAM

## Telecom X - Análisis de Evasión de Clientes (Churn)

Bienvenido al repositorio del **Challenge 2: Data Science LATAM** de Alura Cursos. Este desafío está diseñado para desarrollar y fortalecer tus habilidades en el proceso de **ETL (Extract, Transform, Load)** utilizando Python, con un enfoque en el análisis de datos para abordar el problema de la evasión de clientes en **Telecom X**.

---

## Descripción del Proyecto

**Telecom X** enfrenta una alta tasa de cancelaciones de clientes (churn) y necesita identificar los factores que contribuyen a esta pérdida. Como asistente de análisis de datos, tu misión es recopilar, procesar y analizar datos de clientes para extraer información valiosa que permita al equipo de Data Science desarrollar estrategias para reducir la evasión.

### Objetivos del Desafío
- **Extraer** datos desde una API en formato JSON.
- **Transformar** los datos mediante limpieza, estandarización y creación de nuevas columnas relevantes.
- **Cargar y analizar** los datos para generar insights estratégicos.
- Crear un informe claro y estructurado con visualizaciones que resuman los hallazgos y ofrezcan recomendaciones.

### ¿Qué vas a practicar?
- ✅ Importar y manipular datos desde una API de manera eficiente.
- ✅ Aplicar los conceptos de ETL (Extracción, Transformación y Carga).
- ✅ Crear visualizaciones estratégicas para identificar patrones y tendencias.
- ✅ Realizar un Análisis Exploratorio de Datos (EDA) y generar un informe con insights relevantes.
- ✅ (Opcional) Explorar correlaciones entre variables para identificar factores clave relacionados con la evasión.

---

## Estructura del Repositorio

- **TelecomX_Data.json**: Archivo JSON con los datos de clientes de Telecom X, incluyendo información demográfica, servicios contratados y estado de evasión.
- **TelecomX_LATAM.ipynb**: Cuaderno base opcional que sugiere un flujo de trabajo organizado para el proceso de ETL y análisis.
- **README.md**: Este archivo, con una descripción general del desafío y las instrucciones.

---

## Proceso de ETL

### 1. Extracción (Extract)
- **Objetivo**: Obtener los datos de la API de Telecom X.
- **Pasos**:
  - Cargar los datos desde el archivo JSON: [TelecomX_Data.json](https://github.com/ingridcristh/challenge2-data-science-LATAM/blob/main/TelecomX_Data.json).
  - Convertir los datos a un **DataFrame de Pandas** para facilitar su manipulación.
- **Recursos**:
  - Enlace a la API: [TelecomX_Data.json](https://github.com/ingridcristh/challenge2-data-science-LATAM/blob/main/TelecomX_Data.json).
  - Documentación útil: [Pandas DataFrame](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.html).

### 2. Transformación (Transform)
- **Conocer el dataset**:
  - Explorar las columnas y sus tipos de datos utilizando `DataFrame.info()` y `DataFrame.dtypes`.
  - Consultar el diccionario de datos para entender el significado de las variables.
  - Identificar columnas relevantes para el análisis de churn.
  - Recursos: [DataFrame.info()](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.info.html), [DataFrame.dtypes](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.dtypes.html).
- **Manejo de inconsistencias**:
  - Corregir valores faltantes, duplicados o inconsistentes.
  - Aplicar técnicas de manipulación de strings (e.g., `lower`, `replace`, `startswith`, `contains`).
  - Recursos: [Manipulación de strings en Pandas](https://www.aluracursos.com/).
- **Creación de la columna "Cuentas_Diarias"**:
  - Calcular el valor diario a partir de la facturación mensual para un análisis más granular.
- **Estandarización (opcional)**:
  - Convertir valores textuales (e.g., "Sí"/"No") a binarios (1/0).
  - Renombrar columnas para mayor claridad y accesibilidad.

### 3. Carga y Análisis (Load & Analysis)
- **Análisis Descriptivo**:
  - Calcular métricas como media, mediana, desviación estándar, etc., usando `DataFrame.describe()`.
  - Recursos: [DataFrame.describe()](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.describe.html).
- **Distribución de Evasión**:
  - Visualizar la proporción de clientes que permanecieron versus los que cancelaron (churn) mediante gráficos.
- **Evasión por Variables Categóricas**:
  - Analizar la distribución de churn según variables como género, tipo de contrato, método de pago, etc.
- **Evasión por Variables Numéricas**:
  - Explorar cómo variables como "total gastado" o "tiempo de contrato" se relacionan con la evasión.
- **Análisis de Correlación (Opcional)**:
  - Usar `DataFrame.corr()` para identificar relaciones entre variables (e.g., cuenta diaria y churn).
  - Visualizar resultados con gráficos de dispersión o matrices de correlación.

---

## Informe Final
El informe debe incluir las siguientes secciones, elaboradas dentro del notebook:

1. **Introducción**: Explicar el objetivo del análisis y el problema de evasión de clientes.
2. **Limpieza y Tratamiento de Datos**: Detallar los pasos realizados para importar, limpiar y procesar los datos.
3. **Análisis Exploratorio de Datos (EDA)**: Presentar los análisis realizados, incluyendo gráficos y visualizaciones.
4. **Conclusiones e Insights**: Resumir los principales hallazgos y su relevancia para reducir la evasión.
5. **Recomendaciones**: Proponer estrategias basadas en el análisis para retener clientes.

Asegúrate de que el informe sea claro, bien estructurado y respaldado por visualizaciones que refuercen los insights.

---

## Recursos Adicionales
- **Cuaderno Base (Opcional)**: [TelecomX_LATAM.ipynb](https://github.com/alura-cursos/challenge2-data-science-LATAM/blob/main/TelecomX_LATAM.ipynb).
- **Diccionario de Datos**: Incluido en el repositorio para comprender las columnas del dataset.
- **Documentación de Pandas**:
  - [DataFrame.info()](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.info.html)
  - [DataFrame.dtypes](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.dtypes.html)
  - [DataFrame.describe()](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.describe.html)
- **Manipulación de strings**: [Guía de Alura](https://www.aluracursos.com/).

---

## Instrucciones para Contribuir
1. Clona este repositorio.
2. Carga los datos desde el archivo JSON proporcionado.
3. Sigue el flujo de trabajo ETL descrito.
4. Usa el cuaderno base (opcional) o crea tu propio notebook.
5. Genera visualizaciones y un informe final con tus hallazgos.
6. Sube tu solución al repositorio y comparte tus resultados.

---

## ¡A por el desafío! 🚀
Transforma los datos en información estratégica y ayuda a **Telecom X** a reducir la evasión de clientes. ¡Usa tus habilidades en Python, Pandas y visualización para generar impacto!

**Autor**: Alura Cursos  
**Repositorio**: [challenge2-data-science-LATAM](https://github.com/ingridcristh/challenge2-data-science-LATAM)  
**Licencia**: MIT

## 🛡️ Insignia

La realización y entrega de este proyecto otorgó una exclusiva insignia:

![Badge Challenge TelecomX Analisis Evasión Clientes - Alura](https://cdn1.gnarususercontent.com.br/6/409126/007f0f58-5970-4133-94b8-9af2551f2ab2.png)
