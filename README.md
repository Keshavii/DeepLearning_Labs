# Image-Based AQI Classification using CNN and Transfer Learning

**Course:** IT549 – Deep Learning

**Assignment:** Lab 3 – Image-Based AQI Classification

**Name:** Hiya Modi

**Student ID:** 202301011

---

## Project Overview

This project implements an image classification system to predict **Air Quality Index (AQI) classes** from outdoor images using deep learning. The objective is to compare the performance of:

1. A **Convolutional Neural Network (CNN) built from scratch**
2. A **Pretrained CNN model (ResNet18) using transfer learning**

The models are trained on a dataset containing images of various locations along with their corresponding AQI class labels.

---

## Dataset

The dataset consists of two main components:

* **data.csv** – Contains image filenames and AQI class labels.
* **sampled_images/** – Folder containing the corresponding images.

Only the following columns were used from the dataset:

* `Filename` → image input
* `AQI_Class` → target class label

Images were resized to **224 × 224 pixels** and normalized before training.

---

## Methodology

### 1. Data Preparation

* Loaded dataset using `pandas`
* Encoded AQI class labels into numeric format
* Split the dataset into:

  * **Training set:** 70%
  * **Validation set:** 15%
  * **Test set:** 15%
* Applied image transformations using `torchvision.transforms`

---

### 2. CNN Model (From Scratch)

A simple Convolutional Neural Network was implemented using PyTorch with:

* 3 Convolutional layers
* ReLU activation
* Max pooling layers
* Fully connected classifier

The CNN model was trained using the **Adam optimizer** and **CrossEntropyLoss**.

---

### 3. Transfer Learning (ResNet18)

A pretrained **ResNet18** model was used for transfer learning.

Steps:

* Loaded pretrained ResNet18 model
* Froze convolutional layers
* Replaced the final fully connected layer to match the number of AQI classes
* Trained only the final layer on the dataset

---

## Model Evaluation

Both models were evaluated on the **test dataset** using:

* **Accuracy**
* **Precision**
* **Recall**
* **F1-score**
* **Confusion Matrix**

Training curves were plotted to analyze model performance over epochs.

---

## Results

The pretrained **ResNet18 model outperformed the CNN built from scratch**. This is expected because pretrained models learn useful visual features from large datasets such as ImageNet, which helps improve performance even on smaller datasets.

---

## Key Observations

* The CNN trained from scratch achieved good training accuracy but showed some overfitting.
* The ResNet model generalized better on the validation and test sets.
* Transfer learning significantly improved classification performance.

---

## Files in Repository

* `AQI_Image_Classification.ipynb` – Google Colab notebook containing the full implementation
* `data.csv` – Dataset file containing image labels
* `README.md` – Project description and methodology

---

## Results Summary

The performance of the models was evaluated on the **test dataset** using classification metrics such as **Accuracy, Precision, Recall, and F1-score**.

| Model                        | Test Accuracy |
| ---------------------------- | ------------- |
| CNN (from scratch)           | 84.44%           |
| ResNet18 (Transfer Learning) | 71.33%           |

### Observations

* The **CNN model trained from scratch achieved higher test accuracy compared to the pretrained ResNet18 model** in this experiment.
* Although pretrained models often perform better due to transfer learning, this result may occur when the dataset size is relatively small or when the pretrained features are not perfectly aligned with the specific characteristics of the dataset.
* The CNN model was able to learn dataset-specific features effectively, which may have helped it perform better on the test set.

### Conclusion

In this experiment, the **custom CNN model slightly outperformed the pretrained ResNet18 model on the test dataset**. While transfer learning is generally beneficial, its effectiveness depends on factors such as dataset size, data distribution, and training configuration.
