# CAI 4104/6108: Machine Learning Engineering
## Project Proposal: Bird Species Classification
### Authors:
  - Jason Ang
    email: jasonang@ufl.edu
  - Sakshi Pandey
    email: sakshi.pandey@ufl.edu
  - Avaneesh Khandekar
    email: akhandekar@ufl.edu
  - Hamsini Sivalenka
    email: hamsinisivalenka@ufl.edu
  - Satyajit Mohanty
    email: satyajit.mohanty@ufl.edu

# Task & Dataset

## Task Description

With over 10,000 species of birds globally, accurate identification and classification are crucial for conservation efforts, ecological studies, and bird watching enthusiasts. Our project aims to develop a model trained on an existing bird species dataset to accurately classify bird species found in the wild. The challenge includes the diversity of bird species which vary in size, shape, color, and habitat, necessitating a robust classification model that can recognize subtle differences between species.

**Type:** Image Classification: Supervised, Multi-Class Classification.

## Dataset

The dataset comprises a diverse collection of images representing 525 distinct bird species.
For training purposes, the dataset includes a substantial 84,635 images. To ensure robust model evaluation, 5
images per species were set aside for testing, resulting in a test set of 2,625 images. Additionally, 2,625 images
were allocated for validation, mirroring the test set’s composition with 5 images per species. This careful
partitioning of data is essential for training, testing, and validating the model’s performance accurately. One
notable characteristic of this dataset is its inherent class imbalance. While the dataset is comprehensive,
containing images for a wide array of species, the number of images per species varies. Each species has a
minimum of 130 training images, but some species may have significantly more images than others. This
imbalance poses a challenge for the model, as it must learn to classify species accurately despite the varying
amounts of training data available for each. The images are gathered from internet searches by species name.
Duplicate or near-duplicate images have been checked for and deleted to prevent any overlap between the
training, test, and validation sets.

- **Size:** 2.11 GB
- **Image instances:** 89,885
- **Features:** 224x224 RGB images
- **Access:** [Dataset on Kaggle](https://www.kaggle.com/datasets/gpiosenka/100-bird-species/data)

# Evaluation

## Methodology

Our approach includes refining and augmenting the dataset with additional images, experimenting with various models like Random Forests and CNNs, and using ensemble methods for robust classification.

**Data Splitting:** Training on provided sets, with additional testing via K-fold validation for enhanced model accuracy.

## Metrics

1. **F1 Score (Macro)**: Ideal for imbalanced datasets, calculates the unweighted mean F1 score across all classes.
   $$\text{Macro F1} = \frac{1}{N} \sum_{i=1}^{N} F1_i$$

2. **AUC-ROC**: Measures the model’s ability to discriminate between classes, represented by the area under the ROC curve.
   $$\text{AUC-ROC is calculated by plotting TPR vs. FPR at various thresholds.}$$

## Baselines

1. **Kaggle Baseline**: Existing model accuracy at 87%.
2. **Scientific Study**: CNN-based bird classification with 95.37% accuracy, described in [1].

# References

[1] Y.-P. Huang and H. Basanta. Bird image retrieval and recognition using a deep learning platform. In IEEE. IEEE, 2019.
