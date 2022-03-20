# CSDT-2022-1.md :card_index_dividers:	

![N](https://escuelaing.s3.amazonaws.com/staging/images/logo-ecijg.width-380.png)

# Contenido
- [CSDT-2022-1](https://github.com/alexviatela/GildedRose-Refactoring-Kata/blob/main/CSDT-2022-1.md)
  * [Gilded Rose](#gilded-rose)
    + [Análisis Preliminar](#análisis-preliminar)
		+ [Herramienta de Análisis Utilizada](#herramienta-de-análisis-utilizada)
		+ [Resultados Satisfactorios](#resultados-satisfactorios)
		+ [Resultados Insatisfactorios](#resultados-insatisfactorios)
    + [Autor](#autor)


### Análisis Preliminar
Se ha realizado un análisis preliminar al código del proyecto haciendo uso de dos herramientas de análisis estático de código, esto nos permitirá identificar oportunamente las falencias en nuestri código para así corregirlas fácilmente.


### Herramienta de Análisis Utilizada

#### Better Code Hub
Better Code Hub es un servicio de análisis de código fuente,gratuito para código abierto, basado en la web que verifica el cumplimiento de una base de código con las diez pautas presentadas en Creación de software mantenible. 

#### Análisis Realizado
Se realizó el análisis del código del proyecto, una vez realizado este análisis se evidencia que se cumplen 5 de los 10 principios evaluados, a continuación se detallan los resultados de este análisis.

[![BCH compliance](https://bettercodehub.com/edge/badge/alexviatela/GildedRose-Refactoring-Kata?branch=main)](https://bettercodehub.com/)

#### Resultados Satisfactorios


##### Write Code Once
En relación al análisis realizado por la herramienta, nos muestra que el código no presenta duplicidad.
Este análisis de complementa con el análisis previo realizado en la revisión de Code Smells, donde se comentaba que el código no presentaba duplicidad.
![](https://raw.githubusercontent.com/alexviatela/GildedRose-Refactoring-Kata/main/images/bettercodehub_ok_1.png)

##### Keep Unit Interfaces Small
En relación al análisis realizado por la herramienta, se muestra que se cumple el principio de mantenerlo sencillo y simple, esto permite que el código sea entendible, para un futuro refactoring no sería dificil analizar el funcionamiento correcto del código.
![](https://raw.githubusercontent.com/alexviatela/GildedRose-Refactoring-Kata/main/images/bettercodehub_ok_2.png)
![](https://raw.githubusercontent.com/alexviatela/GildedRose-Refactoring-Kata/main/images/bettercodehub_ok_2_1.png)

##### Couple Architecture Components Loosely
En relación al análisis realizado por la herramienta, se evidencia que hay bajo acoplamiento entre los componentes del código esto facilita el mantenimiento de los componentes de forma aislada.
En comparación con el análisis previo, se había informado que este principio no se cumplia porque se implementaba el código en un solo método.
![](https://raw.githubusercontent.com/alexviatela/GildedRose-Refactoring-Kata/main/images/bettercodehub_ok_3.png)


##### Keep Your Codebase Small
![](https://raw.githubusercontent.com/alexviatela/GildedRose-Refactoring-Kata/main/images/bettercodehub_ok_4.png)
![](https://raw.githubusercontent.com/alexviatela/GildedRose-Refactoring-Kata/main/images/bettercodehub_ok_4_1.png)


##### Write Clean Code
En relación al análisis realizado por la herramienta, nos dice la mayoria del codigo no cuenta con codel smells.
Sin embargo nosotros encontramos varios code smells en la primera revisión.
![](https://raw.githubusercontent.com/alexviatela/GildedRose-Refactoring-Kata/main/images/bettercodehub_ok_5.png)


#### Resultados Insatisfactorios


##### Write Short Units of Code
En relación al análisis realizado por la herramienta, se evidencia que el código no está estructurado en pequeños fragmentos.
Este análisis se complementa con el estudio previo realizado en Clean Code.
![](https://raw.githubusercontent.com/alexviatela/GildedRose-Refactoring-Kata/main/images/bettercodehub_fail_1.png)
![](https://raw.githubusercontent.com/alexviatela/GildedRose-Refactoring-Kata/main/images/bettercodehub_fail_1_1.png)

##### Write Simple Units of Code
En relación al análisis realizado por la herramienta, se muestra que el código tiene múltiples puntos de bifurcación (if, for, while, etc.) lo cuál afecta la complejidad para la modificación y prueba de los distintos métodos en el programa.
![](https://raw.githubusercontent.com/alexviatela/GildedRose-Refactoring-Kata/main/images/bettercodehub_fail_2.png)
![](https://raw.githubusercontent.com/alexviatela/GildedRose-Refactoring-Kata/main/images/bettercodehub_fail_2_1.png)

##### Automate Tests
El análisis realizado con la herramienta se complementa con el estudio previo realizado, ya que nos muestra que a pesar de que el programa cuenta con pruebas unitarias, estas tienen un bajo porcentaje de cobertura, por esta razón se necesita complementarlas para mejorar la calidad del código del programa.
![](https://raw.githubusercontent.com/alexviatela/GildedRose-Refactoring-Kata/main/images/bettercodehub_fail_5.png)
![](https://raw.githubusercontent.com/alexviatela/GildedRose-Refactoring-Kata/main/images/bettercodehub_fail_5_1.png)

##### Separate Concerns in Modules
![](https://raw.githubusercontent.com/alexviatela/GildedRose-Refactoring-Kata/main/images/bettercodehub_fail_3.png)
![](https://raw.githubusercontent.com/alexviatela/GildedRose-Refactoring-Kata/main/images/bettercodehub_fail_3_1.png)

##### Keep Architecture Components Balanced

![](https://raw.githubusercontent.com/alexviatela/GildedRose-Refactoring-Kata/main/images/bettercodehub_fail_4.png)
![](https://raw.githubusercontent.com/alexviatela/GildedRose-Refactoring-Kata/main/images/bettercodehub_fail_4_1.png)



### Autor :man_beard:
Wilmer Alexander Viatela Bravo
