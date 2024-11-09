# Defective vs. Non-Defective Image Classification Model
This project implements an image classification model to detect **defective** and **non-defective** items in images. Using **InceptionV3** as a feature extractor, 
the model leverages data preprocessing and augmentation for enhanced interpretability and accuracy.

## Dataset
[Data](https://drive.google.com/drive/folders/1_27gGkLNHTyYa6xfjpso3K8jXGAZ-dL9?usp=drive_link)

The dataset is organized into directories representing each class:
- `Data/good` for **non-defective** images
- `Data/manipulated_front`, `Data/scratch_head`, `Data/thread_side`, `Data/thread_top` for **defective** images with various defect types

## Preprocessing and Augmentation
Images are resized to `(256, 256)`, normalized, and converted to grayscale. To address class imbalance, images from the minority class (defective) are augmented using **ImageDataGenerator** with techniques like rotation and horizontal flipping.

### Inception Architecture

The Inception model, specifically InceptionV3, is a deep convolutional neural network developed by Google as part of the Inception series. It introduces "Inception modules" that allow the model to capture features at multiple scales by using a 
combination of convolutional filters of different sizes in parallel within each layer
![image](https://github.com/user-attachments/assets/8305ff87-5d38-4adc-a8a6-f527b8f42b87)

## Model Architecture
The model uses InceptionV3 as a feature extractor, followed by additional layers for binary classification to distinguish between defective and non-defective items.

![image](https://github.com/user-attachments/assets/ec05583d-05d2-4cfa-be27-175a2814f5c4)

## Training and Evaluation
The model is compiled with binary cross-entropy loss and the Adam optimizer.

![image](https://github.com/user-attachments/assets/2d751bf2-fd5c-4900-9c9f-ddcbc082cccf)

## Performance Metrics
Accuracy: Measure of correct classifications
Loss: Evaluation of model's error
Confusion Matrix: Detailed breakdown of true positives, false positives, etc

![image](https://github.com/user-attachments/assets/9a215ed8-a4a2-4c10-a76c-6254e589b8ad)


## Installation and Setup
Clone the repository:
```sh
git clone https://github.com/username/repo-name.git
```

Install the required dependencies:
```sh
pip install -r requirements.txt
```

