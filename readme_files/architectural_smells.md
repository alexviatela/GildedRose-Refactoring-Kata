# CSDT-2022-1.md :card_index_dividers:	

![N](https://escuelaing.s3.amazonaws.com/staging/images/logo-ecijg.width-380.png)

# Contenido
- [CSDT-2022-1](https://github.com/alexviatela/GildedRose-Refactoring-Kata/blob/main/CSDT-2022-1.md)
  * [Gilded Rose](#gilded-rose)
    + [Architectural Smells](#Architectural-Smells)
		+ [¿Qué son los Architectural Smells?](#¿Qué-son-los-Architectural-Smells?)
		+ [Architectural Smells en el Proyecto](#Architectural-Smells-en-el-Proyecto)
    + [Autor](#autor)


## Architectural Smells


### ¿Qué son los Architectural Smells?
Los Architectural Smells son combinaciones de construcciones de arquitectura que reducen la mantenibilidad del sistema.

Algunos puntos a tener en cuenta son:
* Estos no son errores, el código puede funcionar correctamente aún si estos Smells se presentan.
* Pueden ralentizar la velocidad de desarrollo de software y los procesos de refactorización que se puedan realizar.
* Estos pueden aumentar el riesgo de errores a futuro


### Architectural Smells en el Proyecto

A continuación se detallan algunos de los *architectural smells* que se han encontrado en el proyecto a trabajar:


* #### No Layers
No existen capas en el código del proyecto, este es altamente acoplado lo que genera varias afectaciones que deben ser refactorizadas.

* #### The Grand Old Duke of York
No se percibe una buena abstracción en la arquitectura implementada en el proyecto. Los procesos no son lo bastante claros para que un equipo de desarrollo pueda trabajar cómodamente entendiendo todo el proceso.

* #### Feature Concentration
Todas las funcionalidades están concentradas en una única y enorme clase, esto hace que la los componentes se acoplen demasiado y deben preocuparse del funcionamiento completo del código al momento de ejecutarse.

* #### Packages Not Clearly Named
Las clases y componentes creados en el proyecto no están nombrados claramente, esto puede generar reprocesos y confusiones al momento de refactorizar el código del proyecto.




### Autor :man_beard:
Wilmer Alexander Viatela Bravo
