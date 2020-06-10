[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/InPhyT/PlantDiseaseDetection/master)
[![Kaggle](https://kaggle.com/static/images/open-in-kaggle.svg)]()
[![nbviewer](https://github.com/jupyter/design/blob/master/logos/Badges/nbviewer_badge.svg)](https://nbviewer.jupyter.org/github/InPhyT/PlantDiseaseDetection/)

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
In this project we train N convolutional neural networks (*add specific models*)

1. Class balancing with [SMOTE](https://imbalanced-learn.readthedocs.io/en/stable/generated/imblearn.over_sampling.SMOTE.html)
1. Data augmentation with [Keras ImageDataGenerator](https://keras.io/api/preprocessing/image/)
1. Learning rate schedule
1. Optimal dropout
1. Epoch grid search
1. Filters and feature maps visualization of the layers.

Auxiliary elements of the pipeline (e.g. SMOTE) have been manually fine tuned,

#### Results 

* ROC = 0.956 applying the Keras pre-trained model [DenseNet121](https://keras.io/api/applications/densenet/#densenet121-function);
* ROC = 0.915 applying a relatively shallow CNN defined and trained from scratch. 

#### References

1. Kaggle [Plant Pathology 2020 - FGVC7](https://www.kaggle.com/c/plant-pathology-2020-fgvc7/overview) 
1. Ranjita Thapa et al., 2020 [The Plant Pathology 2020 Challenge Dataset to Classify Foliar Disease of Apples](https://arxiv.org/abs/2004.11958), *arXiv*.

## Methods 

## Results 

## Discussion / Conclusion 

<br><br>

**Copyright 2020 InPhyT**

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
