# Proyecto 3 - Tópicos especiales en telemática
Spark sobre COVID-19 
## Estudiantes
- Alejandro Cano Múnera
- Luis Javier Palacio Mesa
### Universidad EAFIT

## Fuentes de datos
https://data.humdata.org/dataset/novel-coronavirus-2019-ncov-cases </br>
https://data.humdata.org/dataset/positive-cases-of-covid-19-in-colombia </br>

## Notebook
[Notebook](https://github.com/alejocano22/TETproject3/blob/master/notebooks/colab/covid.ipynb)
![EMR](https://github.com/alejocano22/TETproject3/blob/master/images/NotebookEMR.PNG)

## Ingesta y Almacenamiento de datos en S3
### Datasets
Colombia: s3://tet-covid-datasets/colombia </br>
Mundial: s3://tet-covid-datasets/mundial </br>
![Datasets](https://github.com/alejocano22/TETproject3/blob/master/images/S3.PNG)

### Ingesta de datos en S3
Se realizó la ingesta de datos en S3:
![Ingesta](https://github.com/alejocano22/TETproject3/blob/master/images/IngestaDatosS3.PNG)

### Datos guardados en S3
Posterior a su análisis, los datasets fueron nuevamente guardados en S3:
![Guardados](https://github.com/alejocano22/TETproject3/blob/master/images/GuardarDatosS3.PNG)

### Outputs 
Outputs: s3://tet-covid-datasets/outputs </br>

## Análisis descriptivo exploratorio
Se usó pyspark, además se realizó la limpieza de algunos datos que presentaban inconsistencias, se eliminaron y añadieron columnas.
A continuación se presentarán algunas de las agrupaciones y filtrados realizados en los datasets </br>
Filtro 1: Personas menores de 18 años en estado Grave o Fallecido
![filtro1](https://github.com/alejocano22/TETproject3/blob/master/images/filtro1.PNG)

Grupo 1: Contador de personas agrupadas por país de procedencia del COVID
![grupo1](https://github.com/alejocano22/TETproject3/blob/master/images/grupo1.PNG)

Grupo 2: Contador de personas agrupadas por Departamento o Distrito
![grupo2](https://github.com/alejocano22/TETproject3/blob/master/images/grupo2.PNG)

Grupo 3: Contador de personas Fallecidas agrupadas por Departamento o Distrito
![grupo3](https://github.com/alejocano22/TETproject3/blob/master/images/grupo3.PNG)

Grupo 4: Casos confirmados, muertes y tasa de fatalidad agrupados por código ISO y por región
![grupo4](https://github.com/alejocano22/TETproject3/blob/master/images/grupo4.PNG)

Grupo 5: Número de muertes agrupados por código ISO y región
![grupo5](https://github.com/alejocano22/TETproject3/blob/master/images/grupo5.PNG)

Grupo 6: Número de recuperados agrupados por código ISO y región
![grupo6](https://github.com/alejocano22/TETproject3/blob/master/images/grupo6.PNG)

## Gráficas
Se realizaron visualizaciones de datos de Colombia, el mundo y Colombia vs el mundo. </br>
Gráficas realizadas usando plotly

### Número de casos por departamento o distrito
En esta gráfica se evidencia claramente que Bogotá D.C. tiene un número de casos muy elevados, lo siguen lugares como el Valle del Cauca, Cartagena y el Meta. Los lugares con menor número de casos son Arauca, Putumayo y Sucre.
![Image1](https://github.com/alejocano22/TETproject3/blob/master/images/newplot.png)

### Casos positivos en Colombia por edad
En este punto evidenciamos que la mayoria de casos se encuentran entre personas  con edades entre 25-40 años con un 34.6% y personas entre 40-65 años con un 34.1%
![Image2](https://github.com/alejocano22/TETproject3/blob/master/images/newplot%20(1).png)

### Países con tasa de letalidad más alta y Colombia
La tasa de letalidad se define como el número de muertes por cien, dividido el número total de casos. </br>
Se puede evidenciar que los paises con mayor tasa de letalidad son Nicaragua, Belgica y Francia, sin embargo, Nicaragua y Bélgica son países con pocos casos confirmados, mientras que países como Francia, Italia y España tienen un número muy alto de casos confirmados y por su alta tasa de letalidad, entonces se tiene mayor número de muertes.
![Image3](https://github.com/alejocano22/TETproject3/blob/master/images/newplot%20(2).png)

### Países latinos con tasa de letalidad más alta y Colombia
En latinoamerica los países con tasas de letalidad más alta son Mexico, Ecuador y Argentina. Se puede observar que Peru tiene un número de casos confirmados muy alto, sin embargo su tasa de mortalidad ronda el 2.81%. Colombia tienen una tasa de letalidad del 3.86%
![Image4](https://github.com/alejocano22/TETproject3/blob/master/images/newplot%20(3).png)

### Casos confirmados por tiempo en los 10 países con más casos y Colombia
En esta gráfica se muestra la curva de crecimiento de los 10 países con mayor número de casos confirmados y Colombia. Es claro que Estados unidos tiene una curva muy elevada a comparación de los demás países.
![Image5](https://github.com/alejocano22/TETproject3/blob/master/images/newplot%20(4).png)

### Casos confirmados por tiempo en los 10 países con más casos sin USA y con Colombia
Eliminando la curva de Estados Unidos, se observa de una manera más clara el comportamiento de los demás paises, podemos evidenciar como algunas curvas siguen en crecimiento y como otras intentan aplanarce con el paso del tiempo.
![Image6](https://github.com/alejocano22/TETproject3/blob/master/images/newplot%20(5).png)

### Casos confirmados por tiempo en algunos países de latinoamérica
En latinoamérica el país con mayor número de casos y que presenta una curva en crecimiento exponencial es Perú. Países como México y Chile también presentan curvas en crecimiento. En este punto se puede evidenciar que Colombia se encuentra en un estado intermedio respecto a las curvas de crecimiento de paises vecinos
![Image7](https://github.com/alejocano22/TETproject3/blob/master/images/newplot%20(6).png)

### Casos confirmados de coronavirus en el mundo por fecha
En este gráfico podemos evidenciar el crecimiento de la pandemia geográficamente, se pueden observar los países con mayor número de muertes con la barra de color, Estados Unidos y Europa presentan cifras altas de muertes.
![Image8](https://github.com/alejocano22/TETproject3/blob/master/images/newplot%20(7)2.png)
![Image8](https://github.com/alejocano22/TETproject3/blob/master/images/newplot%20(7)3.png)

### Casos confirmados de coronavirus en el mundo (División política)
En esta gráfica se hace una diferenciación de la división politica de una manera más clara y se evidencia como al pasar el tiempo países como China controlan el número de casos confirmados, mientras que países como Estados Unidos aumentan significativamente el número de casos. También se observa crecimiento de número de casos en regiones como Europa y Sur America.
![Image9](https://github.com/alejocano22/TETproject3/blob/master/images/newplot%20(8)2.png)
![Image9](https://github.com/alejocano22/TETproject3/blob/master/images/newplot%20(8)3.png)
