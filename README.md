# MRI Breast Cancer Classification via DCE-MRI 🧬



[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white)](https://pytorch.org/get-started/locally/)

Repositorio académico correspondiente al desarrollo experimental de la clasificación binaria de lesiones mamarias benignas y malignas. Para esto se utilizaron técnicas de aprendizaje profundo aplicadas sobre imágenes de resonancia magnética dinámica con contraste (DCE-MRI).

# 📄 **Clasificación de lesiones mamarias utilizando aprendizaje profundo en imágenes de resonancia magnética.**


## 👩‍💻 Autora

**Erika Alexandra García Barrios**
Ingeniería de Software — Institución Universitaria Pascual Bravo

## 👨‍🏫 Asesores

**Rubén Darío Fonnegra Tarazona**
Ph.D. en Ingeniería

**Mateo Rico García**
M.Sc. en Automatización y Control Industrial


## 🚀 Descripción del proyecto

El proyecto implementa múltiples experimentos basados en arquitecturas CNN e híbridas CNN-Transformer. En estos se utilizaron estrategias de transferencia de aprendizaje, representaciones multicanal DCE-MRI y evaluación clínica mediante métricas diagnósticas.

## 🎯 Objetivo general

Implementar y evaluar arquitecturas de aprendizaje profundo para la clasificación binaria de lesiones mamarias benignas y malignas en imágenes de resonancia magnética dinámica con contraste (DCE-MRI), mediante estrategias de entrenamiento y evaluación experimental aplicadas al análisis de imágenes médicas.

## 📌 Objetivos específicos

* Diseñar un proceso de preprocesamiento, normalización y representación multicanal para las imágenes de resonancia magnética dinámica con contraste, orientada a la preparación de datos para modelos de aprendizaje profundo aplicados a la clasificación binaria de lesiones mamarias.
* Implementar y comparar diferentes arquitecturas de aprendizaje profundo, incluyendo modelos basados en redes neuronales convolucionales y arquitecturas híbridas basadas en mecanismos de atención para la clasificación binaria de lesiones mamarias en categorías benignas o malignas.
* Evaluar el desempeño de las arquitecturas implementadas mediante métricas clínicas como sensibilidad (*recall*), especificidad, *F1-score* y área bajo la curva ROC, utilizando conjuntos independientes de entrenamiento, validación y prueba.

## 🧠 Arquitecturas implementadas

* ResNet50
* EfficientNet-B3
* MobileViT-S

## 📁 Estructura del repositorio

* `configs/`: configuraciones experimentales utilizadas durante el entrenamiento y la evaluación.
* `data/processed/`: archivos CSV procesados con rutas, etiquetas y particiones.
* `experimentos/`: contiene los cinco experimentos desarrollados durante el proyecto.
* `GeneracionTablas.ipynb`: notebook para la consolidación de métricas, tablas y figuras finales.

## 🛠️ Instalación

El proyecto fue desarrollado utilizando Python 3.10+ y PyTorch.

### 1. Requisitos del sistema

* Python 3.10+
* Git
* GPU NVIDIA con CUDA 11.8+

### 2. Clonar repositorio
 git clone https://github.com/PandoraRiot/MRI_BreastCancer_Classification.git

cd MRI_BreastCancer_Classification

 ### 3. Instalar dependencias
 pip install -r requirements.txt
## 💻 Ejecución de experimentos

Cada experimento posee su notebook principal ubicado en:

`experimentos/experimentoX/cuadernos/ExperimentoOficial.ipynb`

Los notebooks experimentales fueron desarrollados para ejecutarse principalmente en el entorno de Jupyter Notebook.

## 📊 Generación de tablas 

El notebook `GeneracionTablas.ipynb` fue desarrollado para ejecutarse en Google Colab y permite:

* Consolidar métricas experimentales.
* Generar tablas finales para la tesis.
* Construir figuras comparativas.
* Exportar resultados utilizados dentro de la tesis.

## 🗂️ Dataset

El proyecto utiliza imágenes DCE-MRI provenientes del dataset público BreastDM, especializado en la clasificación y segmentación de lesiones mamarias.

## 📈 Mejores resultados correspondientes a Experimento 4. 

| Model | Best Epoch | Best Phase | Train AUC | Val AUC Patient | Val Threshold | TEST AUC (cal) | TEST AUC CI95 | TEST Recall | TEST Specificity | TEST F1 | TEST PPV | TEST NPV | TEST FNR | TEST Brier | TP / TN / FP / FN | Exec Time (min) |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| resnet50 | 12 | finetune | 0.9996 | 0.9615 | 0.590 | 0.9406 | [0.827 - 1.000] | 0.8636 | 0.8462 | 0.8837 | 0.9048 | 0.7857 | 0.1364 | 0.0939 | 19 / 11 / 2 / 3 | 1.66 |
| efficientnet_b3 | 23 | finetune | 0.9221 | 0.9510 | 0.480 | 0.8304 | [0.680 - 0.962] | 0.9091 | 0.3846 | 0.8000 | 0.7143 | 0.7143 | 0.0909 | 0.1839 | 20 / 5 / 8 / 2 | 2.64 |
| mobilevit_s | 14 | finetune | 0.9065 | 0.9161 | 0.515 | 0.7797 | [0.576 - 0.946] | 0.8182 | 0.6923 | 0.8182 | 0.8182 | 0.6923 | 0.1818 | 0.1678 | 18 / 9 / 4 / 4 | 1.35 |

Los resultados experimentales además incluyen:

* Curvas ROC.
* Matrices de confusión.
* Curvas *train loss* vs. *validation loss*.
* Métricas clínicas de clasificación.
* Análisis de generalización y estabilidad.
* Interpretabilidad visual mediante Grad-CAM.


## 🔗 Repositorio oficial

* **Enlace:** [https://github.com/PandoraRiot/MRI_BreastCancer_Classification](https://github.com/PandoraRiot/MRI_BreastCancer_Classification)
* **GitHub:** PandoraRiot
