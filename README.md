# 1. 📊 Análisis campañas de marketing: Exploratory Data Analysis (EDA)


# 2. 📖 Descripción

Este proyecto realiza un análisis exploratorio de datos con Python de las campañas de marketing directo de una institución bancaria portuguesa. Las campañas de marketing se basaron en llamadas telefónicas. A menudo, se requería más de un contacto con el mismo cliente para determinar si el producto (depósito a plazo bancario) sería suscrito o no. El objetivo es identificar tendencias y patrones basándose en datos históricos para conocer mejor a los clientes y mejorar la segmentación para futuras campañas de marketing.

# 3. 🗂️ Estructura del proyecto

Carpetas y archivos de este proyecto:

🗂️ data/        # Datos crudos y procesados
🗂️ notebooks/   # Notebooks de Jupyter con el análisis
🗂️ src/         # Scripts de procesamiento
🗂️
📃 README.MD

# 4. 🛠️ Instalación y Requisitos

En este proyecto he usado Python 3.13.1 y requiere las siguientes bibliotecas:

    - pandas
    - numpy
    - matplotlib
    - seaborn
    - sys

# 5. 📊 Resultados y Conclusiones







## Cambios a realizar:

### Tipos a cambiar:

    - default: float -> object
    - housing: float -> object
    - loan: -> float -> object
    - cons.price.idx: object -> float
    - cons.conf.idx: object -> float
    - euribor3m: object -> float
    - date: object -> datetime
    
### Columnas con nulos:

    - age
    - job
    - marital
    - education
    - default
    - housing
    - loan
    - cons.price.idx
    - euribor3m
    - date


### Categorías a cambiar

    - job: admin. -> admin
    - marital: está en MAYUS
    - education: separador '.' -> espacio
    - poutcome: está en MAYUS
