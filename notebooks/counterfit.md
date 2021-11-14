# Counterfit

* Counterfit (https://github.com/Azure/counterfit) es una CLI escrita en Python y desarrollada por Microsoft.
* Desarrollada para auditorías de seguridad sobre modelos de ML.
* Implementa algoritmos de evasión de caja negra.
* Se basa en ART y TextAttack.

## Instalación

1. Clonar repositorio

  ```bash
  git clone https://github.com/Azure/counterfit
  ```

2. Instalar dependencias

  > Puede tardar bastante tiempo.

  ```bash
  cd counterfit
  pip install -r requirements.txt
  ```

## Comandos básicos

* `list targets`: lista modelos disponibles
* `list frameworks`: lista frameworks de ataque disponibles
* `load <framework>`: carga el framework especificado
* `list attacks`: lista ataques del framework seleccionado
* `interact <target>`: selecciona el modelo objetivo
* `predict -i <ind>`: predicción sobre la entrada `ind`
* `use <attack>`: selecciona ataque
* `run`: ejecuta ataque
* `scan`: ejecuta ataque
* `show options`: muestra opciones del ataque
* `set <param>=<value>`: cambia el valor de param a value
* `save`: guarda los resultados en json

## Demo

1. Ejecutar `counterfit`.

  > Ejecutar desde el directorio `counterfit`.

  ```bash
  python counterfit.py
  ```

2. Ejecutar los siguientes comandos en la CLI de `counterfit`.

  ```
  list targets
  interact tutorial
  predict
  predict -i 100
  list frameworks
  load art
  list attacks
  use hop_skip_jump
  show options
  set max_iter=100
  run
  scan --iterations 10 --attack hop_skip_jump
  save
  ```
