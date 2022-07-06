# Intro_AA

Repositorio de respuestas de la materia: Introducción al Aprendizaje Automático (2022), en el marco de la Diplomatura en Ciencia de Datos - Universidad Nacional de Córdoba.

# **DIPLOMATURA 2022**

# Introducción al Aprendizaje Automático

## GRUPO Nº24

## INTEGRANTES:
   - [x] Nico Rosales 
   - [x] Daniel Rubio
   - [x] Diana Fonnegra
   - [x] Clarisa Manzone

----   
En este repositorio se encuentran las entregas con resultados correspondientes a la asignatura de _Introducción al Aprendizaje Automático_.

## **Requerimientos - Librerías necesarias**:
   - [x] matplotlib.pyplot
   - [x] pandas
   - [x] seaborn
   - [x] numpy
   - [x] 
   - [x] sklearn
----

# Documentación:
## Laboratorio 1: Regresión en Boston

   - [x] En este laboratorio se realizaron experimentos con el método de regresión sobre el conjunto de datos "Boston house prices dataset".
   - [x] Se estudio el conjunto de datos, así como se generaron visualizaciones y seleccionaron atributos relevantes.
   - [x] Luego, se entreno y evaluó diferentes tipos de regresiones, buscando las configuraciones que mejores resultados presenten.

La elaboración del punto 1 se trabajo con el conjunto de datos Boston siguiendo el siguiente flujo:

### Características del conjunto:
Se trata de un conjunto de datos que representa el costo de las viviendas de Boston dado un número de habitaciones. Presenta caracteristicas como: 506 registros, 13 variables entre numéricas/categóricas y un valor de Mediana (atributo 14 - denominado: target). A su vez este conjunto de datos no presenta valores faltantes.

1. CRIM: tasa per cápita de crimen para la ciudad.
2. ZN: proporción de terrenos residenciales con zonificación para lotes de más de 25.000 pies cuadrados.
3. INDUS: proporción de acres comerciales no minoristas por ciudad.
4. CHAS: Charles River dummy variable (= 1 si el tramo linda con el río; 0 en caso contrario).
5. NOX: concentración de óxidos nítricos (partes por 10 millones).
6. RM: número medio de habitaciones por vivienda.
7. AGE: proporción de unidades ocupadas por sus propietarios construidas antes de 1940.
8. DIS: distancias ponderadas a cinco centros de empleo de Boston.
9. RAD: índice de accesibilidad a las autopistas radiales.
10. TAX: tasa de impuesto sobre la propiedad de valor total por 10.000 dólares.
11. PTRATIO: tasa alumno-profesor por ciudad.
12. B -> 1000(Bk - 0.63)^2: donde Bk es la proporción de población negra por ciudad.
13. LSTAT: porcentaje de población de menor estatus.
14. MEDV: valor medio de las viviendas ocupadas por sus propietarios en miles de dólares. -> Variable Objetivo/Target.

Nota 1: En la [documentación](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_boston.html), se presenta una advertencia que indica:
   - El conjunto de datos sobre los precios de la vivienda en Boston tiene un problema ético: los autores de este conjunto de datos diseñaron una variable "B", la cual supone que la autosegregación racial tenía un impacto positivo en los precios de la vivienda.
    A su vez argumentan que: *el objetivo de la investigación que condujo a la creación de este conjunto de datos era estudiar el impacto de la calidad del aire, pero no se demostró adecuadamente la validez de esta suposición*.
   - Por lo tanto, desaconsejan el uso de este conjunto de datos a menos que el propósito del código sea estudiar y educar sobre cuestiones éticas en la ciencia de datos y el aprendizaje automático.

----

### Visualización de los Datos - Variables independientes vs Target:
![image](https://user-images.githubusercontent.com/103326439/177621596-0c10a6dd-4b73-4645-bc11-0738bfcd1a73.png)

### Regresión Lineal Simple:
![image](https://user-images.githubusercontent.com/103326439/177621854-c607b739-8653-4c9f-af10-e085ffbfa946.png)

Datos del Modelo:
--- --- --- --- --- --- --- --- --- --- --- ---
Valor de la pendiente o coeficiente "a":  [9.37638431]
Valor de la intersección o coeficiente "b":  -36.476189627647315
--- --- --- --- --- --- --- --- --- --- --- --- 
Precisión del modelo entrenamiento (Train):
0.497
--- --- --- --- --- --- --- --- --- --- --- --- 
Precisión del modelo prueba (Test):
0.424
--- --- --- --- --- --- --- --- --- --- --- --- 
Root-Mean-Squared-Error (RMSE):
Train error: 42.820
Test error: 46.907

