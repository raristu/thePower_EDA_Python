# **1. 📊 Análisis campañas de marketing: Exploratory Data Analysis (EDA)**


# **2. 📖 Descripción**

Este proyecto realiza un análisis exploratorio de datos con Python de las campañas de marketing directo de una institución bancaria portuguesa. Las campañas de marketing se basaron en llamadas telefónicas. A menudo, se requería más de un contacto con el mismo cliente para determinar si el producto (depósito a plazo bancario) sería suscrito o no. El objetivo es identificar tendencias y patrones basándose en datos históricos para conocer mejor a los clientes y mejorar la segmentación para futuras campañas de marketing.

# **3. 🗂️ Estructura del proyecto**

Carpetas y archivos de este proyecto:

    🗂️ data/        # Datos crudos y procesados
    🗂️ notebooks/   # Notebooks de Jupyter con el análisis
    🗂️ src/         # Scripts de procesamiento
    📃 README.MD

# **4. 🛠️ Instalación y Requisitos**

En este proyecto he usado Python 3.13.1 y requiere las siguientes bibliotecas:

    - pandas
    - numpy
    - matplotlib
    - seaborn
    - datetime

# **5. 📊 Resultados y Conclusiones**

## **5.1 📊 Resultados**

### 🔠 **Análisis de las variables categóricas:**

- **Job**:  las categorías más destadadas son **admin** (25.29%), **blue-collar** (22.45%) y **technician** (16.34%).
- **Marital**: la categoría **married** es la más destacada con un 60.66%.
- **Education**: las categorías más destacadas son **basic** (30.35%), **university_degree** (29.59%), **high_school** (23.08%) y **professional_course** (12.74%).
- **Default**: la categoría más destacada es **no** con un 79.11%.
- **Housing**: las categorías más destacadas son **yes** (52.32%) y **no** (45.29%).
- **Loan**: las categorías más destacadas son **no** (82.81%) y **yes** (15.19%).
- **Contact**: las categorías más destacadas son **cellular** (63.71%) y **telephone** (36.29%).
- **Y**: las categorías más destacadas son **no** (88.73%) y **yes** (11.27%).

### 🔢 **Análisis de las variables numéricas:**

- Se detectaron outliers en varias columnas pero se decidió no hacer nada con ellos porque pueden servir para futuros análisis.
- **Age**: las edades más comunes son entre 30 y 35 años, y la mediana se encuentra en 38 años. Tenemos outliers por arriba pero tienen sentido ya que corresponden con edades de clientes superiores a 65 años aproximadamente.
- **Duration**: y **Campaign**: formas muy parecidas. La distribución se centra en los valores bajos y hay bastantes outliers por arriba. 
    -  **Duration**: Tiene una correlación del 0.4 con **Y**, es decir, parece que la duración (en segundos) del último contacto con cliente y si contratan o no un producto o servicio están relacionados. Los valores más comunes se encuentran en el rango entre 70 y 110 segundos aproximadamente.
    - **Campaign**: los número de contacto más comunes son entre 1 y 3 veces.
- **Pdays**: el valor 999 con una aparición del 96.31% de las veces,nos sugiere que nunca antes se había contactado con cliente. Tiene una correlación con **Y** de -0.3.
- **Previous**: confirma el punto anterior. Antes de esta campaña, en el 86,29 % de las ocasiones nunca se había contactado anteriormente con cliente. Tiene una correlación con **Y** de 0.23.
- **Emp_Var_Rate** y **Euribor3M**: ambas tienen una forma muy parecida. Mirando la matriz de correlación, comprobamos que ambas están muy correlacionadas (0.97). Cuando el Euribor a tres meses sube, la tasa de variación de empleo sube, y viceversa. Además, ambas tienen una correlación de -0.3 y -0.31 respectivamente con **Y** por lo que cuando ambas suben, los clientes suscriben menos productos y viceversa, cuando ambas bajan, los clientes suscriben más productos.
- **Cons_Price_Idx**: tiene una alta correlación con **Euribor3M** (0.68).

## **5.2 💡 Conclusiones**

- **🎯 Segmentación de las estrategias de marketing**: sería conveniente personalizar/adaptar estas estrategias para clientes con las siguientes características (ya que conforman el grueso de la muestra):
    - 🛠️ Trabajan en puestos como: oficina, mano de obra y técnicos.
    - 💍 Estado civil: más de la mitad están casados.
    - 🎓 Educación: tienen educación básica, universitaria o bachillerato.

- **📱 Forma de contacto**: casi 2/3 de las comunicaciones con cliente fueron a teléfonos móviles. Sería interesante analizar cuántos de esos contactos a móvil resultaron en la contratación de productos. En caso afirmativo, sería conveniente centrar las campañas en esa forma de contacto o explorar otras como Redes Sociales, etc.

- **⌛ Duración de las llamadas**: al haber una correlación entre la duración de las llamadas y la respuesta del cliente, sería interesante realizar un estudio de estas duraciones para ajustar el guión de las llamadas.

- **📈Paro y Euribor**: parece ser que cuando las tasas de paro y el euribor son más altos, los clientes no contratan este tipo de productos. Sería interesante realizar estas campañas en periodos de bajo paro y euribor.

# **6. 🔄 Próximos pasos**

Sería interesante realizar análisis más en detalle para comprobar, de los clientes que contrataron el depósito a plazo bancario, aspectos como:
    - Duración de las llamadas
    - Forma de contacto
    - Puesto de trabajo
    - Estado civil
    - Educación

# **7. 🤝 Contribuciones**

**¡Las contribuciones son bienvenidas!**

# **8. 👏 Autores y agradecimientos** 

**Agradecimientos:** gracias a los profesores de thePower, en especial a Silvia Alsina Ruíz y Jaime Rollón Castro, ¡¡unos auténticos cracks!!

**Autor:**
  - Raúl Aristu
  - @raristu (https://github.com/raristu)

