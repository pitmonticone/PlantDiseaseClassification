## Documents

| Report  | Code |
| ---- | ---- |
| [PDF](https://pitmonticone.github.io/PlantDiseaseClassification/Report/report.pdf)  | [Jupyter Notebook](https://nbviewer.jupyter.org/github/pitmonticone/PlantDiseaseClassification/blob/master/Notebooks/notebook.ipynb) |
| [HTML](https://pitmonticone.github.io/PlantDiseaseClassification/Report/report.html) | [Kaggle Notebook](https://www.kaggle.com/inphyt2020/neuralnetworksproject) |


## Extended Abstract

### Problem 

Misdiagnosis of the many diseases impacting agricultural crops can lead to misuse of chemicals leading to the emergence of resistant pathogen strains, increased input costs, and more outbreaks with significant economic loss and environmental impacts. Current disease diagnosis based on human scouting is time-consuming and expensive, and although computer-vision based models have the promise to increase efficiency, the great variance in symptoms due to age of infected tissues, genetic variations, and light conditions within trees decreases the accuracy of detection.

### Objectives

The [Plant Pathology Challenge](https://www.kaggle.com/c/plant-pathology-2020-fgvc7/overview) we have attended consists in training a model using images of the [training dataset](https://arxiv.org/abs/2004.11958) to
* accurately classify a given image from testing dataset into different diseased category or a healthy leaf; 
* accurately distinguish between many diseases, sometimes more than one on a single leaf;
* deal with rare classes and novel symptoms;
* address depth perception—angle, light, shade, physiological age of the leaf; 
* Incorporate expert knowledge in identification, annotation, quantification, and guiding computer vision to search for relevant features during learning.

Submissions are evaluated on [mean column-wise ROC AUC](https://www.kaggle.com/c/plant-pathology-2020-fgvc7/overview/evaluation).

### Data 

Both the training and the testing [datasets](https://www.kaggle.com/c/plant-pathology-2020-fgvc7/data) are composed of 1821 high-quality, real-life symptom images of multiple apple foliar diseases to be classified into four categories: `healthy`, `multiple_diseases`, `rust`, `scab`. 

### Methods

1. Class balancing with [`SMOTE`](https://imbalanced-learn.readthedocs.io/en/stable/generated/imblearn.over_sampling.SMOTE.html)
1. Data augmentation with [Keras `ImageDataGenerator`](https://keras.io/api/preprocessing/image/)
1. Learning rate schedule
1. Optimal dropout
1. Epoch grid search
1. Visualization of convolutional filters and activation maps of the layers.

### Results 

| Model  | ROC AUC |
| ---- | ---- |
| Keras `DenseNet121` | 0.972 |
| InPhyT `EKM` | 0.937 |

### References 

1. [Plant Pathology 2020 - FGVC7: Identify the category of foliar diseases in apple trees](https://www.kaggle.com/c/plant-pathology-2020-fgvc7), *Kaggle* (2020). 
1. Ranjita Thapa et al. [The Plant Pathology 2020 challenge dataset to classify foliar disease of apples](https://arxiv.org/abs/2004.11958), *arXiv pre-print* (2020). 
