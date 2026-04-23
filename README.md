# Proyecto-Shark-Attacks

## 🦈 SharkSpotter: Optimización de Avistamientos para Turismo de Buceo.
Objetivo del proyecto:
Maximizar la probabilidad de éxito en expediciones de buceo mediante un modelo de recomendación basado en datos históricos, reduciendo la incertidumbre logística y económica asociada al avistamiento de especies específicas de tiburones.

Dataset
* Fuente: Global Shark Attack File (GSAF).
* Naturaleza: Datos reales históricos de interacciones y avistamientos.
* Variables Principales:
    * Date / Month: Temporalidad del avistamiento.
    * Country / Location: Geolocalización precisa.
    * Species: Identificación del espécimen (Filtrado para especies de interés turístico como el Gran Blanco, Toro, Tigre, etc.).

Proceso de análisis
Para transformar datos brutos en una herramienta de planificación, se siguió este flujo:
1. Data Wrangling: Limpieza profunda de la columna Species mediante regex para unificar nombres, y estandarización de fechas para extraer estacionalidad.
2. EDA (Análisis Exploratorio de Datos): Identificación de "Hotspots" globales y patrones de migración.
3. Filtrado MVP: Selección de los países con mayor densidad de registros y las especies más demandadas por el turismo subacuático.
4. Métricas Clave:
    * Índice de Densidad Histórica: Registros por rango temporal/localización.
    * Probabilidad Mensual de Avistamiento: Ratio de presencia histórica por mes en zonas específicas.

Resultados / Insights (Ejemplos basados en tendencias comunes del dataset)
* Estacionalidad Crítica: El análisis revela que viajar a destinos sin considerar el mes exacto reduce la probabilidad de avistamiento.
* Especialización por Zona: Identificación de áreas donde la presencia de una especie (ej. Tiburón Tigre) es constante durante todo el año versus zonas migratorias.
* Optimización de Costes: La app permite al usuario descartar destinos con registros históricos pobres, asegurando que la inversión en logística de buceo sea eficiente.

Próximos pasos
* Integración de API de Clima/Corrientes: Para ajustar la probabilidad según condiciones oceanográficas en tiempo real.
* Módulo de Reservas: Enlaces de afiliados a resorts de buceo y centros certificados (PADI/SSI) en los "hotspots" identificados.
* Alertas de Usuario: Sistema de notificaciones cuando la "temporada alta" de una especie específica esté por comenzar en un destino favorito.
* Escalabilidad: Ampliar el dataset a nivel global e incluir especies de macro-vida o mantas.

Cómo replicar el proyecto
1. Clonar el repositorio: git clone [tu-enlace-aquí]
2. Instalar dependencias: pip install pandas, xlrd
3. Ejecutar el Notebook: Abre shark_analysis_eda.ipynb para ver el proceso de limpieza y los gráficos resultantes.