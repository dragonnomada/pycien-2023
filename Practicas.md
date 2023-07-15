# Prácticas del Curso de Python Científico

## P101. Escribir un reporte de texto con las métricas del Titanic

Genera un reporte de texto con cabeceras decoradas a partir del conjunto de datos del titanic que contenga los siguientes estadísticos.

* Total de supervivientes
* Total de supervivientes mujeres
* Total de supervivientes hombres
* Total de supervivientes mayores a 18 años
* Total de supervivientes menores a 18 años
* Total de supervivientes mayores a 50 años
* Total de muertos
* Total de muertos mujeres
* Total de muertos hombres
* Tasa de supervivencia de la clase 1
* Tasa de supervivencia de la clase 2
* Tasa de supervivencia de la clase 3
* Tasa de supervivencia de la clase 1 siendo mujer
* Tasa de supervivencia de la clase 2 siendo mujer
* Tasa de supervivencia de la clase 3 siendo mujer
* Probabilidad de sobrevivir dado que se es mujer (usar regla de Bayes)
* Probabilidad de sobrevivir dado que se es hombre (usar regla de Bayes)
* Probabilidad de sobrevivir dado que se es mujer y está en la clase 1 (usar regla de Bayes compuesta)

## P102. Extraer datos de una hoja y rangos de celdas específicas de un archivo de Excel

Genera un archivo de Excel que contenga una hoja llamada `Datos` con una tabla de datos que inicie en la columna `D` y en la fila `8`. La tabla debe contener al menos 6 columnas y 20 registros. Extrae los datos usando pandas y genera los siguientes puntos:

* Quita las últimas dos columnas del DataFrame
* Intercambia las primeras dos columnas del DataFrame
* Ordena los datos por la tercer columna
* Genera una nueva columna con la suma de las primeras dos columnas numéricas
* Calcula el promedio de la primer columna numérica
* Guarda los datos del DataFrame en una hoja de excel partiendo de la columna `C` y la fila `4`

## P103. Insertar el reporte del Titanic con imágenes en un archivo de Excel

Genera un archivo de Excel que una hoja con los datos del Titanic y coloca una gráfica generada a partir de los datos del Titanic en una celda específica que no se encime con los datos.

* Carga los datos del Titanic desde el CSV y retenlos en un DataFrame
* Genera una gráfica de pastel o barras con datos relevantes como la tasa supervivencia por edad
* Guarda los datos del DataFrame en una hoja de un archivo de Excel
* Guarda la gráfica generada en una celda de la misma hoja del archivo de Excel

## P104. Unir dos DataFrames de productos y ventas relacionados mediante un JOIN

Construye dos DataFrames de productos, ventas, donde el primer DataFrame tendrá las columnas necesarias para guardar cada producto y el segundo para guardar cada venta como se muestra en las siguientes tablas:

> DataFrame de Productos

| PRODUCTO_ID | NOMBRE          | PRECIO |
| :---------: | --------------- | :----: |
| 1           | Coca Cola       | 17.5   |
| 2           | Galletas Marías | 18.9   |
| 3           | Gansito         | 21.3   |
| 4           | Pepsi           | 16.0   |
| 5           | Chetos          | 11.5   |

> DataFrame de Ventas

| VENTA_ID | PRODUCTO_ID | FECHA               |
| :------: | :---------: | ------------------- |
| 101      | 1           | 2023-07-05 11:55:00 |
| 101      | 3           | 2023-07-05 11:55:00 |
| 101      | 1           | 2023-07-05 11:55:00 |
| 102      | 2           | 2023-07-05 11:57:00 |
| 102      | 2           | 2023-07-05 11:57:00 |
| 102      | 3           | 2023-07-05 11:57:00 |
| 103      | 5           | 2023-07-05 12:31:00 |
| 103      | 4           | 2023-07-05 12:31:00 |

Cumple los siguientes puntos:

* Crea un DataFrame que extienda el DataFrame de Ventas con los productos usando el operado JOIN
* Agrupa el DataFrame extendido para calcular el monto total por venta (suma la columna precio)
* Agrupa el DataFrame extendido para calcular el monto total por producto (suma la columna precio)
* Reporta los valores de los montos obtenidos en la impresión estándar

## P105. Construir un DataFrame a partir de datos de personas en formato JSON

Genera un archivo JSON con datos de más de `100` personas que contengan al menos los siguientes campos: `Nombre`, `Edad`, `Estatura`, `Peso`, `Trabaja`, `Casado`, `Número de Hijos`, etc.

El JSON debe ser un arreglo de objetos. Extrae dicho JSON en python y conviértelo en un DataFrame llamado `personas`.

Resuelve los siguientes puntos, y genera un archivo JSON de salida con los resultados.

* Filtra los datos por segmento de edad (de 0-5, 5-10, 10-20, 20-30, ...)
* Filtra los datos por segmento de estatura (0-20, 20-40, ..., 100-120, 120-140, ...)
* Filtra los datos por segmento de peso (de 0-10, 10-20, 20-30, 30-40, ...)
* Filtra los datos por si trabaja o no
* Filtra los datos por si está o no casado
* Filtra los datos por segmento de hijos (0, 1, 2, 3, 4, 5+)

## P106. Generar una gráfica de Mapa con Puntos coloreados por categoría (Mapa político)

Genera un DataFrame que tenga al menos los siguientes campos: `latitud`, `longitud`, `persona_id`, `partido_preferido`, `partido_rechazado`. General al menos 100 datos con ubicaciones reales de méxico, usa siglas de partidos políticos que no existan, por ejemplo (RAP, MAP, PRO, MOT, etc). Llena el DataFrame como en el ejemplo:

> Ejemplo de la tabla de preferencias políticas por persona y ubicación

| latitud    | longitud     | persona_id | partido_preferido | partido_rechazado |
| :--------: | :----------: | :--------: | :---------------: | :---------------: |
| 19.3204968 | -99.1526134  | 1          | MOT               | RAP               |
| 18.8928205 | -98.6017383  | 2          | RAP               | MOT               |
| 20.643614  | -103.423788  | 3          | MAP               | MOT               |
| 19.914386  | -101.5954695 | 4          | PRO               | RAP               |

Resuelve los siguientes puntos:

* Crea un mapa de la republica con Matplolib
* Ubica cada coordenada y dibuja un punto de color en el mapa
* El color será diferente para cada partido
* Usa un color similar pero más oscuro para los rechazados

## P107. Generar una gráfica de Red para personas relacionadas por preferencias psicológicas

Genera un DataFrame con al menos 50 muestras de personas y preferencias psicológicas, usa al menos las siguientes columnas: `persona_id`, `fuma`, `bebe`, `deportista`, `ciclista`, `montañista`, `anarquista`, `izquierda`, `casado`, `hijos`, etc.

Genera las siguientes gráficas de red usando la librería `Networkx`. En cada nodo se pondrá como etiqueta el `persona_id`.

* Una gráfica que muestre la relación entre personas que fuman.
* Una gráfica que muestre la relación entre personas que beben.
* Una gráfica que muestre la relación entre personas que son deportistas
* Una gráfica que muestre la relación entre personas que son anarquistas
* Una gráfica que muestre la relación entre personas que son de izquierda
* Una gráfica que muestre la relación entre personas que fuman y beben y son anarquistas
* Una gráfica que muestre la relación entre personas que fuman y tienen en un segundo nivel de relación a alguien que es deportista

## P108. Extraer los productos de la página de Sanborns usando Selenium

Crea un programa de Python capaz de abrir un navegador automatizado de Chrome para extraer los productos de la página principal de Sanborns [https://www.sanborns.com.mx/](https://www.sanborns.com.mx/).

Cumple los siguientes puntos:

* Abre el navegador usando Selenium
* Visita la página de Sanborns
* Busca los nodos donde está la información de cada producto (imagen, título y precio)
* Recolecta la información de esos nodos
* Guarda la información en un DataFrame
* Guarda el DataFrame en un archivo CSV
* Cierra el navegador de Selenium (el Chrome)

## P109. Extraer las frutas y sus ventas e insertar los reportes de venta en otra tabla en MySQL

Conecta una base de datos MySQL que tenga una tabla de frutas con al menos los siguientes campos: `fruta_id`, `nombre`, `precio`, `existencias` y una tabla de ventas con al menos los siguientes campos `venta_id`, `fruta_id`, `fecha`.

Recupera los datos de ambas tablas en dos DataFrames de `frutas` y `ventas`. Cumple los siguientes puntos:

* Filtra las frutas con precio menor a `20` y guardalos en la base de datos en la tabla `frutas_20`.
* Filtra las ventas del dia de actual y guardalos en la base de datos en la tabla `ventas_dia`.

## P110. Crear un clasificador SVC o MLP capaz de predecir los dígitos escritos a mano

Recupera el dataset de 60,000 imágenes de entrenamiento y 1,000 imágenes de prueba de dígitos escritos a mano en Sklearn. Y recupera las imágenes en forma de matriz, crea un modelo de clasificación SVC o MLP y convierte las matrices de imágenes en vectores.

Cumple los siguientes pasos:

* Entrena el clasificador con los vectores y objetivos usando las muestras de entrenamiento.
* Calcula la precisión del clasificador con las muestras de prueba.
* Predice el dígito de una matriz escrita a mano en código (una matriz de 28x28 de 1's y 0's).