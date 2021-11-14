# Introducción al Adversarial Machine Learning

Taller de Adversarial Machine Learning para las [XV Jornadas STIC CCN-CERT](https://www.ccn-cert.cni.es/xvjornadas).

  <p align="center">
    <img alt="XV Jornadas STIC CCN-CERT" src="./docs/xv-jornadas-ccn-cert.png" data-canonical-src="./docs/xv-jornadas-ccn-cert.png" width="100%" />
  </p>

## ¿Qué es el Adversarial Machine Learning?

Rama del machine learning que trata de averiguar los ataques que puede sufrir un modelo en la presencia de un adversario malicioso y cómo protegerse de ellos.

### Taxonomía de ataques

El Adversarial Machine Learning establece que existen 4 tipos de ataque que pueden sufrir los modelos de ML.

* Extracción (o robo) de modelo: permiten a un adversario robar los parámetros de un modelo de machine learning.
* Inversión: tienen como objetivo invertir el flujo de información de un modelo de machine learning. Permiten a un adversario tener un conocimiento del modelo que no pretendía ser compartido de forma explícita.
* Envenenamiento: buscan corromper el conjunto de entrenamiento haciendo que un modelo de machine learning reduzca su precisión. Pueden añadir puertas traseras en el modelo.
* Evasión: un adversario inserta una pequeña perturbación (en forma de ruido) en la entrada de un modelo de machine learning para que clasifique de forma incorrecta (ejemplo adversario).

## Herramientas empleadas

* [Adversarial Robustness Toolkit (ART)](https://adversarial-robustness-toolbox.readthedocs.io/en/latest): es una librería opensource de Adversarial Machine Learning que permite comprobar la robustez de los modelos de machine learning. Está desarrollada en Python e implementa ataques y defensas de extracción, inversión, envenenamiento y evasión. ART soporta los frameworks más populares: Tensorflow, Keras, PyTorch, MxNet, ScikitLearn, entre muchos otros). Además, no está limitada al uso de modelos que emplean imágenes como entrada, sino que soporta otros tipos de datos como audio, vídeo, datos tabulares, etc.

  <p align="center">
    <img alt="Logo de ART" src="./docs/art_logo.png" data-canonical-src="./docs/art_logo.png" width="30%" />
  </p>

## Notebooks

> Todos los notebooks se pueden ejecutar más rápidamente empleando una GPU. 
> Se recomienda el uso de [Colab](https://colab.research.google.com), que permite emplear GPUs de forma gratuita y no tener que instalar nada en el equipo.

La carpeta `notebooks` contiene 5 notebooks que cubren ataques de extracción, inversión, envenenamiento y evasión.

* `art_install.ipynb`: contiene la instalación de ART y verificar que todo funciona correctamente.
* `evasion.ipynb`: contiene cómo realizar ejemplos adversarios (no dirigidos y no dirigidos) y cómo proteger los modelos frente a ellos.
* `inversion.ipynb`: contiene un ataque de inversión, que permite inferir datos de entrenamiento.
* `poisoning.ipynb`: contiene cómo generar una puerta trasera en un modelo y cómo defenderse de ella.
* `extraction.ipynb`: contiene cómo robar un modelo y aplicar defensas para minimizar el robo.

El orden en el que se ejecuten los notebooks es irrelevante, pero es recomendable comenzar por Hola ART y evasión para familiarizarse con la librería.

## Importar notebooks en Colab

1. Entrar en [Google Colab](https://colab.research.google.com), iniciando sesión con una cuenta de `Google`.

2. Importar todos los notebooks de este repositorio usando la pestaña `GitHub`, copiando la url de este repositorio.
  <p align="center">
    <img alt="Importar notebooks" src="./docs/importar-repos.png" data-canonical-src="./docs/importar-repos.png" width="75%" />
  </p>

3. Cambiar el entorno de ejecución a `GPU`. Se realiza desde el menú `Entorno de ejecución` > `Cambiar entorno de ejecución`. Esto acelera la ejecución de los notebooks.
  <p align="center">
    <img alt="Cambiar entorno de ejecución a GPU" src="./docs/cambiar-entorno-ejecucion.png" data-canonical-src="./docs/cambiar-entorno-ejecucion.png" width="40%" />
  </p>

## Crédito

Los notebooks de inversión y envenenamiento se basan en los [ejemplos y notebooks proporcionados]() por ART. 
