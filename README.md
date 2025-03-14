
# COVID-19 Diagnosis using Chest X-ray Images

## Overview
This project implements a deep learning model for diagnosing COVID-19 using chest X-ray images. The model is built using Convolutional Neural Networks (CNNs) and leverages transfer learning with architectures such as EfficientNet and ResNet to enhance classification performance.

## Features
- **CNN-based Model:** Utilizes deep learning to classify chest X-rays.
- **Transfer Learning:** Incorporates EfficientNet and ResNet for improved accuracy.
- **High Accuracy:** Achieved 93.5% accuracy in 4-class classification.
- **Automated Diagnosis:** Assists medical professionals in detecting COVID-19 from X-ray images.

## Dataset
The dataset consists of labeled chest X-ray images, including:
- COVID-19 positive cases
- Normal (healthy) cases
- Pneumonia cases
- Other respiratory conditions

## Installation
To set up the environment and run the project, follow these steps:

```bash
# Clone the repository
git clone https://github.com/yourusername/covid-19-diagnosis-using-chest-x-ray-images.git
cd covid-19-diagnosis-using-chest-x-ray-images

# Install dependencies
pip install -r requirements.txt
```

## Usage
Run the Jupyter Notebook to train and evaluate the model:
```bash
jupyter notebook covid-19-diagnosis-using-chest-x-ray-images.ipynb
```

## Model Training
The model is trained using TensorFlow/Keras with:
- Adam optimizer
- Categorical cross-entropy loss
- Image augmentation for generalization


This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

