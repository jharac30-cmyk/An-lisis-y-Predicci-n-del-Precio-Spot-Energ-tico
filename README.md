# Analisis-y-Prediccion-del-Precio-Spot-Energetico

# Descripción

Este proyecto analiza la evolución y comparación de los precios spot de energía eléctrica en Colombia y otros países (Argentina y Chile). Utiliza datos diarios (reales o simulados) convertidos a USD, aplicando visualizaciones gráficas y ajustes económicos para facilitar la comparación entre mercados energéticos.
Además, permite realizar comparaciones entre países, observar tendencias, volatilidad y aplicar ajustes polinomiales para mejorar la interpretación de los datos.

Dentro del notebook también se incluye un texto explicando cómo ejecutar el código, junto con algunas conclusiones y limitaciones.

# Estructura del repositorio

# JHARA_CM__Proyecto_3_.ipynb → Notebook principal (Google Colab).
# README.md → Este archivo.

- /DATOS - PAÍSES/ → Carpeta principal que contiene los archivos y fuentes de datos necesarios para ejecutar el código.

- /DATOS - PAÍSES/COMPARACION - PRECIOS/ → Contiene los archivos CSV con los precios reales o históricos.

- /DATOS - PAÍSES/MODELO DE PREDICCION/ → Incluye archivos con datos simulados o proyectados, usados para pruebas de predicción o modelos de ajuste.

- /DATOS - PAÍSES/FUENTES DE LOS DATOS/ → Documento con las referencias y fuentes originales de los datos utilizados.

Cada subcarpeta contiene archivos como Colombia.csv, Chile.csv, Argentina.csv, que deben ser seleccionados al ejecutar el código según el tipo de análisis que se desee realizar (comparación o predicción).

# Requisitos del proyecto

El proyecto está diseñado para ejecutarse principalmente en Google Colab, aunque también puede abrirse en un entorno local.

Dependencias necesarias (si se ejecuta localmente):

- Python 3.8 o superior

- Librerías: pandas, numpy, matplotlib, seaborn, scikit-learn, statsmodels

# Ejecución del código en Google Colab 

1. Abre el archivo JHARA_CM__Proyecto_3_.ipynb en Google Colab.

2. Conéctate al entorno de ejecución (botón Conectar arriba a la derecha).

3. Ejecuta las celdas en orden, una por una (o usa Runtime → Ejecutar todo).

4. Cuando el notebook solicite subir archivos, selecciona los CSV desde la carpeta DATOS - PAÍSES.

- Para trabajar con precios históricos: usa los archivos dentro de COMPARACION - PRECIOS.

- Para probar modelos predictivos: usa los archivos de MODELO DE PREDICCION.

- Los archivos deben contener al menos las columnas Fecha y Valor.

5. Si no subes ningún archivo, el código generará datos simulados automáticamente.

6. Al finalizar la ejecución, se mostrarán gráficas comparativas de precios, volatilidad semanal y relaciones entre variables energéticas.
Además, el notebook genera tablas representativas que resumen los datos mostrados en los gráficos, facilitando su interpretación.

También se incluyen gráficas de comparación entre países, permitiendo analizar de manera visual las diferencias entre los mercados eléctricos internacionales.

El proyecto incorpora módulos de análisis y modelado con scikit-learn, donde el modelo toma como variables de entrada —por ejemplo— precios históricos, niveles de embalses, precipitaciones y factores temporales (como la hora o el día del año).
Estas variables permiten construir relaciones más completas y explorar patrones en la evolución del precio de la energía.

 # Formato esperado de los datos

Cada archivo CSV debe contener:

- Fecha: en formato YYYY-MM-DD

- Valor: precio en moneda local o USD

  # NOTA:
 El proyecto tiene la opcion de convertir los precios locales a USD utilizando tasas de cambio definidas en el diccionario TASAS_USD,  con el fin de que los factores puedan  simular precios de mercado libre y permitir una comparación más realista entre países..

El código también puede reconocer nombres alternativos como “Precio”, “precio”, “Price”, “Date” o “date”.
Durante la ejecución, se normalizan los nombres de las columnas para garantizar compatibilidad con el modelo.

# Guardar resultados y gráficos

Si deseas guardar las gráficas generadas, puedes agregar esta línea después de cada figura:
plt.savefig("/content/resultados/grafico_nombre.png", dpi=150, bbox_inches="tight")

Antes, crea la carpeta de salida con:
!mkdir -p /content/resultados

# Conclusiones y limitaciones

El análisis permite visualizar de manera comparativa e internacional la evolución de los precios de energía, su volatilidad y las relaciones con variables energéticas clave.
El modelo facilita la interpretación mediante ajustes polinomiales y la estandarización a una moneda común (USD), lo que posibilita comparaciones más precisas entre distintos mercados energéticos.

Entre las principales limitaciones se encuentra la disponibilidad y consistencia de los datos, así como el uso de simulaciones para ciertos escenarios.
El enfoque puede ampliarse incluyendo más variables o fuentes de información para mejorar la precisión de los resultados.
