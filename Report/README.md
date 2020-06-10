# Convolutional Neural Network for Plant Disease Classification 


## Abstract

#### Problem 
Misdiagnosis of the many diseases impacting agricultural crops can lead to misuse of chemicals leading to the emergence of resistant pathogen strains, increased input costs, and more outbreaks with significant economic loss and environmental impacts. Current disease diagnosis based on human scouting is time-consuming and expensive, and although computer-vision based models have the promise to increase efficiency, the great variance in symptoms due to age of infected tissues, genetic variations, and light conditions within trees decreases the accuracy of detection.

#### Objectives
The [Plant Pathology Challenge](https://www.kaggle.com/c/plant-pathology-2020-fgvc7/overview) we have attended consists in training a model using images of the [training dataset](https://arxiv.org/abs/2004.11958) to

* accurately classify a given image from testing dataset into different diseased category or a healthy leaf; 
* accurately distinguish between many diseases, sometimes more than one on a single leaf;
* deal with rare classes and novel symptoms;
* address depth perception—angle, light, shade, physiological age of the leaf; 
* Incorporate expert knowledge in identification, annotation, quantification, and guiding computer vision to search for relevant features during learning.

Submissions are evaluated on [mean column-wise ROC AUC](https://www.kaggle.com/c/plant-pathology-2020-fgvc7/overview/evaluation).

#### Data 

Both the training and the test [datasets](https://www.kaggle.com/c/plant-pathology-2020-fgvc7/data) are composed of 1821 high-quality, real-life symptom images of multiple apple foliar diseases, with variable illumination, angles, surfaces, and noise have been manually captured, expert-annotated to create a pilot dataset for apple scab, cedar apple rust, and healthy leaves. 

We found no indication that "multiple_diseases" refers to both "rust" and "scab", it just seems to indicate the presence of other different kinds of illnesses.


#### Solution 
In this project we train a convolutional neural network and apply the following methods

1. class balancing with [SMOTE](https://imbalanced-learn.readthedocs.io/en/stable/generated/imblearn.over_sampling.SMOTE.html)
1. data augmentation with [Keras ImageDataGenerator](https://keras.io/api/preprocessing/image/)
1. learning rate schedule
1. optimal dropout
1. epoch grid search
1. filters and feature maps visualization of the layers.

Auxiliary elements of the pipeline (e.g. SMOTE) have been manually fine tuned.

#### Results 

* **ROC = 0.956** applying the Keras pre-trained model [DenseNet121](https://keras.io/api/applications/densenet/#densenet121-function);
* **ROC = 0.915** applying a CNN which has been defined and trained from scratch. 
