# CSDT-2022-1.md :card_index_dividers:	

![N](https://escuelaing.s3.amazonaws.com/staging/images/logo-ecijg.width-380.png)

### Clean Code
------------
Para el proyecto se ha encontrado algunas implementaciones de caracteriaticas de Clean Code.

![](https://github.com/alexviatela/GildedRose-Refactoring-Kata/blob/develop_code_refactoring/images/CleanCodeOK.png?raw=true)

![](https://github.com/alexviatela/GildedRose-Refactoring-Kata/blob/develop_code_refactoring/images/CleanCodeFail.png?raw=true)

### Principios de Programación
------------
Algunos de los principios de programación que no se están cumpliendo para el proyecto son:

* #### Yagni - You Aren´t Gonna Need It
El código implementado en el proyecto está agregando cálculos adicionales innecesarios que podrían resumirse y producen un exceso de líneas de código.

* #### KISS - Keep it Simple, Stupid:
El código implementado puede simplificarse y mejorar la eficiencia y comprensión al momento de ejecutarlo.

```python
###### Inicio - Fragmento de Código ######
if item.quality < 50:
                    item.quality = item.quality + 1
                    if item.name == "Backstage passes to a TAFKAL80ETC concert":
                        if item.sell_in < 11:
                            if item.quality < 50:
                                item.quality = item.quality + 1
                        if item.sell_in < 6:
                            if item.quality < 50:
                                item.quality = item.quality + 1
###### End - Fragmento de Código ######
```
### Prácticas XP
------------
Para mejorar la calidad del código del proyecto se podráin implementar varias prácticas de XP, entre ellas están:

* #### Test Driven Development
Se pueden escribir las pruebas unitarias antes de realizar la refactorización del código y de esta manera se mejora la calidad del código.
* #### Planning Game
Se aprueban y revisan inicialmente las características requeridas para el desarrollo del proyecto para definir el correcto alcance de las funcionalidades.
* #### Small Realeses
Generando una primera versión preliminar y realizando el desarrollo incrementalmente para dar solución completa e integral al código implementado.
* #### Refactoring
Eliminar redundancia y código innecesario, mejorar la coherencia del código y realizar el desacoplamiento de los métodos.
* #### Continuous Integration
Se debe mantener el código completamente integrado, se debe revisar que parte de los códigos pueden ser reutilizados en el proyecto, para saber así que es necesario refactorizar.
* #### Simple Design
Realizar la funcionalidad con el menos número de líneas de código posible, simplificando los métodos lo más que se pueda.
* #### Coding Standard
Se mantienen buenas practicas de codificación  utilizando los mismos formatos y estilos para la redacción. Esto facilita la comprensión y refactorización en el proyecto.



### Autor :man_beard:
Wilmer Alexander Viatela Bravo
