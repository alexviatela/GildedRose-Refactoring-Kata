# CSDT-2022-1.md :card_index_dividers:	

![N](https://escuelaing.s3.amazonaws.com/staging/images/logo-ecijg.width-380.png)

# Contenido
- [CSDT-2022-1](https://github.com/alexviatela/GildedRose-Refactoring-Kata/blob/main/CSDT-2022-1.md)
  * [Gilded Rose](#gilded-rose)
    + [Prácticas de Testing](#prácticas-de-testing)
    + [Autor](#autor)


### Prácticas de Testing 
------------
Dentro del proyecto se presenta deuda técnica en pruebas y se listan a continuación:

* A pesar de que existe un archivo de pruebas, las pruebas unitarias no son las adecuadas para el proyecto.
* Los estándares de codificación usados para las pruebas no cumplen los requisitos mínimos para la ejecución.
* Faltan escenarios de pruebas.
* El coverage del proyecto es del 5%.

```python
###### Inicio - Fragmento de Código ######
class GildedRoseTest(unittest.TestCase):
    def test_foo(self):
        items = [Item("foo", 0, 0)]
        gilded_rose = GildedRose(items)
        gilded_rose.update_quality()
        self.assertEquals("fixme", items[0].name)

###### End - Fragmento de Código ######
```

#### Reduciendo la deuda de pruebas
Para reducir la deuda técnica en pruebas y mejorar la calidad del código se propone lo siguiente:

* #### Estándares de Nombres para Pruebas Unitarias.
Para mantener el orden en las pruebas unitarias se propone nombrarlas de la siguiente manera:
``` test_(funcionalidad)_(escenario)```
 

* #### Mejoras en Escenarios de Pruebas
Se deben mejorar los escenarios de pruebas unitarias para el proyecto, se proponen los siguientes escenarios:
 * Probar disminución individual de artículos.
```python
###### Inicio - Fragmento de Código ######
 def test_items_decrease_by_one(self):
        self.items.append(Item("Item Test", 10, 20))
        gilded_rose.update_quality(self.items)
        expected = {'sell_in': 9, 'quality': 19}
        item = self.items[0]
        self.assertEqual(item.quality, expected['quality'])
        self.assertEqual(item.sell_in, expected['sell_in'])
###### End - Fragmento de Código ######
```
 * Duplicar la calidad para productos con 10 días o menos restantes.
```python
###### Inicio - Fragmento de Código ######
 def test_quality_by_two_for_products_with_10_days_or_less_left(self):
        self.items.append(Item("Item Test", 10, 34))
        self.items.append(Item("Backstage passes Test", 8, 30))
        gilded_rose.update_quality(self.items)
        expected = [
            {'sell_in': 9, 'quality': 36},
            {'sell_in': 7, 'quality': 32},
        ]

        for index, expectation in enumerate(expected):
            item = self.items[index]
            self.assertEqual(item.quality, expectation['quality'])
            self.assertEqual(item.sell_in, expectation['sell_in'])
###### End - Fragmento de Código ######
```
 * Triplicar la calidad para productos con 5 días o menos restantes.
```python
###### Inicio - Fragmento de Código ######
  def test_quality_by_two_for_products_with_5_days_or_less_left(self):
        self.items.append(Item("Item Test", 4, 11))
        self.items.append(Item("Backstage passes Test", 5, 15))
        gilded_rose.update_quality(self.items)
        expected = [
            {'sell_in': 3, 'quality': 14},
            {'sell_in': 4, 'quality': 18},
        ]

        for index, expectation in enumerate(expected):
            item = self.items[index]
            self.assertEqual(item.quality, expectation['quality'])
            self.assertEqual(item.sell_in, expectation['sell_in'])
###### End - Fragmento de Código ######
```
 * La calidad y la venta disminuyen el doble de rápido después de la venta.
```python
###### Inicio - Fragmento de Código ######
def test_quality_and_sellin_decrease_twice_fast_after_sell_by(self):
        self.items.append(Item("Item Test", 0, 20))
        self.items.append(Item("Item Test", 0, 6))
        gilded_rose.update_quality(self.items)
        expected = [
            {'sell_in': -1, 'quality': 18},
            {'sell_in': -1, 'quality': 4},
        ]

        for index, expectation in enumerate(expected):
            item = self.items[index]
            self.assertEqual(item.quality, expectation['quality'])
            self.assertEqual(item.sell_in, expectation['sell_in'])
###### End - Fragmento de Código ######
```
 * Pasa a calidad cero después de vender productos.
```python
###### Inicio - Fragmento de Código ######
   def test_quality_zero_after_sell_by(self):
        self.items.append(Item("Item Test", 0, 20))
        self.items.append(Item("Backstage passes Item Test", 0, 20))
        gilded_rose.update_quality(self.items)
        expected = [
            {'sell_in': -1, 'quality': 0},
            {'sell_in': -1, 'quality': 0},
        ]

        for index, expectation in enumerate(expected):
            item = self.items[index]
            self.assertEqual(item.quality, expectation['quality'])
            self.assertEqual(item.sell_in, expectation['sell_in'])
###### End - Fragmento de Código ######
```
 * La calidad no aumenta mas de 50.
```python
###### Inicio - Fragmento de Código ######
    def test_quality_does_not_increase_past_50(self):
        self.items.append(Item("Aged Brie", 4, 49))
        gilded_rose.update_quality(self.items)
        expected = {'sell_in': 3, 'quality': 50}
        item = self.items[0]
        self.assertEqual(item.quality, expected['quality'])
        self.assertEqual(item.sell_in, expected['sell_in'])

###### End - Fragmento de Código ######
``` 


* #### Practicas de TDD
Para hacer una ejercicio correcto de pruebas se propone implementar las prácticas de TDD para hacer el refactoring requerido para el proyecto de la mano con el desarrollo de las pruebas necesarias.


### Autor :man_beard:
Wilmer Alexander Viatela Bravo
