# CSDT-2022-1.md :card_index_dividers:	

![N](https://escuelaing.s3.amazonaws.com/staging/images/logo-ecijg.width-380.png)

# Contenido
- [CSDT-2022-1](https://github.com/alexviatela/GildedRose-Refactoring-Kata/blob/main/CSDT-2022-1.md)
  * [Gilded Rose](#gilded-rose)
    + [Integración Continua](#Integración-Continua)
    + [Autor](#autor)


## Integración Continua
Se han establecido dos workflow de github para la implementación de integración continua y un análisis de seguridad para el proyecto.


### Proceso de Integración Continua
Para el proceso de integración continua se realiza la configuración del workflow Python Package, este nos permite ejecutar el proceso de integración en distintas versiones de python, las versiones utilizadas para este proceso son 3.8, 3.9, 3.10.

#### Configuración YML para proceso.
Se realiza la configuración inicial para la ejecución del workflow.
```
# This workflow will install Python dependencies, run tests and lint with a variety of Python versions
# For more information see: https://help.github.com/actions/language-and-framework-guides/using-python-with-github-actions

name: Python package

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  build:

    runs-on: ubuntu-latest
    strategy:
      fail-fast: false
      matrix:
        python-version: ["3.8", "3.9", "3.10"]

    steps:
    - uses: actions/checkout@v2
    - name: Set up Python ${{ matrix.python-version }}
      uses: actions/setup-python@v2
      with:
        python-version: ${{ matrix.python-version }}
    - name: Install dependencies
      run: |
        python -m pip install --upgrade pip
        python -m pip install flake8 pytest
        if [ -f requirements.txt ]; then pip install -r requirements.txt; fi
    - name: Lint with flake8
      run: |
        # stop the build if there are Python syntax errors or undefined names
        flake8 . --count --select=E9,F63,F7,F82 --show-source --statistics
        # exit-zero treats all errors as warnings. The GitHub editor is 127 chars wide
        flake8 . --count --exit-zero --max-complexity=10 --max-line-length=127 --statistics
    - name: Test with pytest
      run: |
        pytest
```

#### Ejecución Inicial del proceso.
Se realiza el commit inicial para la ejecuión del workflow, el cual nos muestra una novedad durante el proceso de pruebas unitarias
![](https://raw.githubusercontent.com/alexviatela/GildedRose-Refactoring-Kata/main/images/continuous_integration_2.png)

Se realiza la corrección de la prueba unitaria correspondiente, posteriormente el flujo vuelve a enviarse y genera resultados satisfactorios.
![](https://raw.githubusercontent.com/alexviatela/GildedRose-Refactoring-Kata/main/images/continuous_integration_3.png)

### Análisis de Seguridad
Para el Análisis de Seguridad del proyecto



### Autor :man_beard:
Wilmer Alexander Viatela Bravo
