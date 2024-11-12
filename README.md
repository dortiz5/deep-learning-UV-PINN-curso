# Applications of Physics-Informed Neural Networks (PINNs)

Este repositorio contiene material para el **taller** sobre redes neuronales informadas por la física (PINNs).

## Introduction

En los últimos años, las redes neuronales profundas se han convertido en herramientas fundamentales para la modelación y el análisis de datos complejos en espacios de alta dimensionalidad. No obstante, estas técnicas suelen requerir grandes volúmenes de datos para ajustar sus numerosos parámetros, lo cual no siempre es viable en situaciones donde la disponibilidad de datos es limitada. Para abordar este desafío, se han desarrollado métodos innovadores como las Redes Neuronales Informadas por Física (PINNs), que combinan el aprendizaje profundo con información física del problema a resolver. Basadas en el teorema de aproximación universal, estas redes son capaces de aproximar funciones no lineales complejas bajo ciertas arquitecturas [(Hornik, 1991)](https://www.sciencedirect.com/science/article/pii/089360809190009T?via%3Dihub), [(Barron, 1993)](https://ieeexplore.ieee.org/document/256500), [(Villota, 2019)](https://investigacion.unirioja.es/documentos/5fbf7e47299952682503c2fa/). Adicionalmente, el uso de diferenciación automática [(Baydin *et al.*, 2018)](https://arxiv.org/abs/1502.05767) permite que las PINNs resuelvan modelos físicos complejos sin la necesidad de grandes cantidades de datos. Esta integración de información adicional facilita la optimización del modelo, permitiendo un mayor nivel de precisión y robustez en aplicaciones donde los datos disponibles son escasos [(Raissi *et al.*, 2019)](https://www.sciencedirect.com/science/article/pii/S0021999118307125), [(Karniadakis *et al.*, 2021)](https://www.nature.com/articles/s42254-021-00314-5).



## Instalación y configuración
Hay dos opciones para participar en este taller, con las instrucciones que figuran a continuación:

 - via a [Instalación local](#Instalación-local) (recomendada)
 - on [Google Colab](#google-colab)

### Instalación local
Recomendamos usar ``conda`` para instalar los paquetes necesarios para
este tutorial.

#### (opcional) Instalación `Miniconda`
Instalar conda es fácil y funciona en *Windows, macOS y Linux*. Solo tienes que seguir las [instrucciones](https://docs.anaconda.com/free/miniconda/miniconda-install/) en el sitio web. **¡Asegúrate de probar tu instalación!**


#### 1. Crear el ambiente utilizando `conda`
**Asegúrate de tener conda instalado**. Este proyecto incluye un archivo [`pinns-tutorial.yml`](pinns-tutorial.yml) para crear e instalar el entorno `python3`.

Desde el directorio raíz `deep-learning-UV-PINNs-curso/`, abre el *Anaconda Prompt* en _Windows_, o en la *terminal* en macOS y Linux, y ejecuta el siguiente código:

```console
conda env create -f pinns-tutorial.yml
```

Esto creará un entorno `conda` llamado `pinn-ihealth-tutorial`. Para activarlo sólo tienes que ejecutar

```console
conda activate pinns-tutorial
```

#### 2. Ejecuta el notebook

Desde el directorio actual, inicia el servidor de jupyter notebook:
```
jupyter lab
```

Este comando debería llevarte a la ubicación correcta dentro de tu navegador para usar el notebook, típicamente [http://localhost:8888/](http://localhost:8888/).

El siguiente paso a veces es útil si tienes problemas con tu jupyter notebook al encontrar el entorno. Querrás hacer esto antes de iniciar el jupyter notebook.

```
python -m ipykernel install --user --name=pinn-ihealth-tutorial
```

### Google Colab
To launch the notebooks in Google Colab click the following links for each of the exercises:

* [Activity 1](https://colab.research.google.com/github/dortiz5/ihealth-pinns-workshop/blob/main/notebooks/activity-1.ipynb) 
* [Activity 2](https://colab.research.google.com/github/dortiz5/ihealth-pinns-workshop/blob/main/notebooks/activity-2.ipynb) 
* [Activity 3](https://colab.research.google.com/github/dortiz5/ihealth-pinns-workshop/blob/main/notebooks/activity-3.ipynb) 

_Notes:_
* _Running in Google Colab requires you to have a Google account._
* _If you leave a Colab session your work will be lost, so be careful to save any work
  you want to keep._
<!--### Binder

If a local installation is not feasible, you can launch the repository on [Binder](https://mybinder.org/v2/gh/dortiz5/ihealth-pinns-workshop/HEAD).

_Notes:_
* _If you exit a Binder session, your work will be lost, so make sure to save any work you want to keep._-->


## Material relacionado y algunas referencias:

- Workshop realizado por [Prof. Ph.D. Francisco Sahli](https://fsahli.github.io/), en abril del 2024: [Workshop](https://fsahli.github.io/PINN-notes/)

- Redes Neuronales Artificiales: [Interesante serie de vídeos de 3Blue1Brown sobre redes neuronales y aprendizaje automático](https://www.3blue1brown.com/topics/neural-networks)

- Diferenciación automática. Aquí encontrará 3 enlaces sobre la diferenciación automática y los números duales: [link 1](https://thenumb.at/Autodiff/), [link 2](https://blog.demofox.org/2014/12/30/dual-numbers-automatic-differentiation/), [link 3](https://en.wikipedia.org/wiki/Dual_number). Also, here you can find a  [tutorial](https://pytorch.org/tutorials/beginner/blitz/autograd_tutorial.html#a-gentle-introduction-to-torch-autograd) in 
PyTorch

- [Redes neuronales basadas en la física para visión por ordenador e imágenes médicas [1].](https://collab.dvb.bayern/display/TUMdlma/Physics+Informed+Neural+Network+for+Computer+Vision+and+Medical+Imaging)

- Ben Moseley [personal blog](https://benmoseley.blog/)


Existen muchos artículos científicos relacionados con PINNs. A continuación,
compartimos 4 que pueden servir como punto de partida para el tópico.

- Raissi, Maziar, Paris Perdikaris, and George E. Karniadakis.
  ["Physics-informed neural networks: A deep learning framework for solving
  forward and inverse problems involving nonlinear partial differential
  equations."](https://www.sciencedirect.com/science/article/pii/S0021999118307125)
  Journal of Computational physics 378 (2019): 686-707.

- Karniadakis, George Em, et al.
  ["Physics-informed machine learning."](https://doi.org/10.1038/s42254-021-00314-5)
  Nature Reviews Physics 3.6 (2021): 422-440.

- Chuang, Pi-Yueh, and Lorena A. Barba.
  ["Predictive limitations of physics-informed neural networks in vortex shedding."]
  (https://arxiv.org/abs/2306.00230) arXiv preprint arXiv:2306.00230 (2023).

- Krishnapriyan, Aditi, et al. ["Characterizing possible failure modes
  in physics-informed neural networks."](https://arxiv.org/abs/2109.01050)
  Advances in Neural Information Processing Systems 34 (2021): 26548-26560.


## Acknowledgements