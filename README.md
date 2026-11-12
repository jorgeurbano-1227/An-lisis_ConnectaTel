# An-lisis_ConnectaTel
# Análisis de una empresa de telecomunicaciones (ConnectaTel)

Objetivo del proyecto
Evaluar el comportamiento de los clientes de la empresa de telecomunicaciones ConnectaTel en Latinoamérica (con información registrada hasta el año 2024), con el fin de construir un perfil estadístico, detectar comportamientos atípicos, identificar patrones de consumo, diseñar estrategias de retención y sugerir mejoras en los planes ofrecidos.

Datasets utilizados
El proyecto utiliza tres fuentes de datos principales:
- **`plans.csv`**: Información de los planes actuales (precio, minutos incluidos, GB incluidos y costos por excedentes).
- **`users_latam.csv`**: Información demográfica y de estado de los clientes (edad, ciudad, fecha de registro, plan contratado y fecha de baja/churn).
- **`usage.csv`**: Detalle del uso real de los servicios por parte de los usuarios (tipo de evento: llamadas o mensajes, fecha, duración y longitud).

Etapas del análisis realizadas
1. **Carga y exploración:** Importación de librerías, verificación de dimensiones (`.shape`) y revisión de tipos de datos y nulos (`.info()`).
2. **Calidad de datos:** Detección de valores nulos, proporciones y análisis de valores inválidos o *sentinels* (como edades con `-999` y ciudades con `?`).
3. **Limpieza de datos:** Tratamiento de sentinels, corrección de fechas inválidas y validación de tipos de valores ausentes (como análisis MAR en las columnas de uso).
4. **Uso por usuario:** Agregación de métricas de llamadas y mensajes por cada cliente mediante *named aggregations* y combinación con uniones (`merge`).
5. **Distribuciones y outliers:** Análisis estadístico, visualizaciones gráficas y detección de valores atípicos mediante el rango intercuartílico (IQR).
6. **Segmentación:** Creación de funciones y gráficos para agrupar a los clientes según su nivel de consumo.
7. **Insight ejecutivo:** Cuantificación de problemas de negocio y conclusiones finales sobre el rendimiento de los planes.
8. **Publicación:** Versionado y entrega del proyecto en un repositorio público de GitHub.

Cómo ejecutar el notebook
Puedes abrir y ejecutar este proyecto de forma interactiva utilizando Google Colab:
1. Haz clic en el botón de Google Colab (o sube el archivo `.ipynb` a tu entorno de Colab).
2. Asegúrate de contar con la estructura de carpetas y datasets requerida en el directorio `/datasets/` o actualiza las rutas de lectura según corresponda en la primera celda.

Guía de reproducción
1. Clona este repositorio o descarga los archivos.
2. Abre el archivo principal del notebook en JupyterLab o Google Colab.
3. Ejecuta las celdas de forma secuencial (desde la carga de librerías en el Paso 1 hasta el análisis final) para reproducir la limpieza, los gráficos y las conclusiones del estudio.
