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

## S3
### Datasets
Colombia: s3://tet-covid-datasets/colombia </br>
Mundial: s3://tet-covid-datasets/mundial </br>

### Outputs 
Outputs: s3://tet-covid-datasets/outputs </br>

## Análisis de datos
Gráficas realizadas usando plotly
### Número de casos por departamento o distrito
En esta gráfica se evidencia claramente que Bogotá D.C. tiene un número de casos muy elevados, lo siguen lugares como el Valle del Cauca, Cartagena y el Meta. Los lugares con menor número de casos son Arauca, Putumayo y Sucre.
![Image1](https://github.com/alejocano22/TETproject3/blob/master/images/newplot.png)
### Casos positivos en Colombia por edad
En este punto evidenciamos que la mayoria de casos se encuentran entre personas  con edades entre 25-40 años con un 34.6% y personas entre 40-65 años con un 34.1%
![Image2](https://github.com/alejocano22/TETproject3/blob/master/images/newplot%20(1).png)
### Países con tasa de letalidad más alta y Colombia
La tasa de letalidad se define como el número de muertes por cien, dividido el número total de casos. </br>
Se puede evidenciar que los paises con mayor tasa de letalidad son Nicaragua, Belgica y Francia, sin embargo, Nicaragua y Belgica son países con pocos casos confirmados, mientras que paises como Francia, Italia y España tienen un número muy alto de casos confirmados y por su alta tasa de letalidad, entonces se tiene mayor número de muertes.
![Image3](https://github.com/alejocano22/TETproject3/blob/master/images/newplot%20(2).png)
### Países latinos con tasa de letalidad más alta y Colombia
En latinoamerica los paises con tasas de letalidad más alta son Mexico, Ecuador y Argentina. Se puede observar que Peru tiene un número de casos confirmados muy alto, sin embargo su tasa de mortalidad ronda el 2.81%. Colombia tienen una tasa de letalidad del 3.86%
![Image4](https://github.com/alejocano22/TETproject3/blob/master/images/newplot%20(3).png)
### Casos confirmados por tiempo en los 10 países con más casos y Colombia
En esta gráfica se muestra la curva de crecimiento de los 10 paises con mayor número de casos confirmados y Colombia. Es claro que Estados unidos tiene una curva muy elevada a comparación de los demás paises.
![Image5](https://github.com/alejocano22/TETproject3/blob/master/images/newplot%20(4).png)
### Casos confirmados por tiempo en los 10 países con más casos sin USA y con Colombia
Eliminando la curva de Estados Unidos, se observa de una manera más clara el comportamiento de los demás paises, podemos evidenciar como algunas curvas siguen en crecimiento y como otras intentan aplanarce con el paso del tiempo.
![Image6](https://github.com/alejocano22/TETproject3/blob/master/images/newplot%20(5).png)
### Casos confirmados por tiempo en algunos países de latinoamerica
En latinoamerica el país con mayor número de casos y que presenta una curva en crecimiento exponencial es Peru. Paises como Mexico y Chile también presentan curvas en crecimiento. En este punto se puede evidenciar que Colombia se encuentra en un estado intermedio respecto a las curvas de crecimiento de paises vecinos
![Image7](https://github.com/alejocano22/TETproject3/blob/master/images/newplot%20(6).png)
### Casos confirmados de coronavirus en el mundo por fecha
En este gráfico podemos evidenciar el crecimiento de la pandemia geográficamente, se pueden evidenciar los paises con mayor número de muertes con la barra de color, Estados Unidos y Europa presentan cifras altas de muertes.
![Image8](https://github.com/alejocano22/TETproject3/blob/master/images/newplot%20(7).png)
![Image8](https://github.com/alejocano22/TETproject3/blob/master/images/newplot%20(7)2.png)
![Image8](https://github.com/alejocano22/TETproject3/blob/master/images/newplot%20(7)3.png)
### Casos confirmados de coronavirus en el mundo (División política)
En esta gráfica se hace una diferenciación de la división politica de una manera más clara y se evidencia como al pasar el tiempo paises como China controlan el número de casos confirmados, mientras que paises como Estados Unidos aumentan significativamente el número de casos. También se observa crecimiento de número de casos en regiones como Europa y Sur America.
![Image9](https://github.com/alejocano22/TETproject3/blob/master/images/newplot%20(8).png)
![Image9](https://github.com/alejocano22/TETproject3/blob/master/images/newplot%20(8)2.png)
![Image9](https://github.com/alejocano22/TETproject3/blob/master/images/newplot%20(8)3.png)
