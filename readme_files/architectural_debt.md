# CSDT-2022-1.md :card_index_dividers:	

![N](https://escuelaing.s3.amazonaws.com/staging/images/logo-ecijg.width-380.png)

# Contenido
- [CSDT-2022-1](https://github.com/alexviatela/GildedRose-Refactoring-Kata/blob/main/CSDT-2022-1.md)
  * [Gilded Rose](#gilded-rose)
    + [Architectural Debt](#Architectural-Debt)
		+ [¿Qué es ATAM y cuál es su objetivo?](#¿Qué-es-ATAM-y-cuál-es-su-objetivo?)
		+ [¿Qué es QAW?](#¿Qué-es-QAW?)
    + [Autor](#autor)


## Architectural Debt


### ¿Qué es ATAM y cuál es su objetivo?
ATAM(Architecture Trade-Off Analysis Method) es un método de evaluación de arquitecturas. 

* El propósito de ATAM es evaluar las decisiones arquitectónicas en relación a los atributos de calidad y las metas de negocio.
* Ayuda a predecir como un atributo de interés puede ser afectado por decisiones arquitectónicas.
* Los atributos de calidad de interés son aclarados mediante el análisis de los escenarios que son definidos por los stakeholders

### ¿Qué es QAW?
QAW(Quality Attribute Workshops) es un taller donde se integran los diferentes stakeholders para identificar los atributos de calidad que serán drivers del diseño de arquitectura del producto.

QAW facilita la resolución temprana de conflictos, obtiene consensos entre los stakeholders y ayuda a mejorar los requerimientos a todos los niveles.


### Aplicación de ATAM en el Proyecto


#### Presentación de la arquitectura
A continuación se presenta una arquitectura preliminar para el despliegue de la aplicación:

![](https://raw.githubusercontent.com/alexviatela/GildedRose-Refactoring-Kata/main/images/ModeloArquitectura.png)

#### Escenarios QAW's
Se han planteado los siguientes escenarios para QAW's:

* Actualización masiva de inventario:
![](https://raw.githubusercontent.com/alexviatela/GildedRose-Refactoring-Kata/main/images/Scenario_1_QAW.png)


* Actualización en reglas de calidad y caducidad de productos:
![](https://raw.githubusercontent.com/alexviatela/GildedRose-Refactoring-Kata/main/images/Scenario_2_QAW.png)




### Autor :man_beard:
Wilmer Alexander Viatela Bravo
