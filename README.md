# COVID-19 Diagnosis Using Chest X-Ray Images

![Medical AI](https://img.shields.io/badge/Field-Medical_AI-blue) ![Deep Learning](https://img.shields.io/badge/Technique-Deep_Learning-orange) ![Python](https://img.shields.io/badge/Language-Python-green)

An automated system for COVID-19 diagnosis using chest X-ray images with deep learning (CNN models). Achieved **93.5% accuracy** in 4-class classification (COVID-19/Normal/Viral Pneumonia/Lung Opacity).

## Table of Contents
- [Problem Statement](#problem-statement)
- [Dataset](#dataset)
- [Technical Approach](#technical-approach)
- [Results](#results)
- [Future Work](#future-work)
- [References](#references)

## Problem Statement
Manual diagnosis of COVID-19 from chest X-rays is:
- Time-consuming for radiologists
- Prone to human error  
- Challenging in resource-limited settings

**Solution:** Develop an AI system to assist medical professionals with rapid, automated diagnosis.

## Dataset
Used a curated dataset of chest X-rays with 4 classes:
- COVID-19
- Normal
- Viral Pneumonia  
- Lung Opacity



## Technical Approach

### Pre-processing Pipeline
1. **Image Enhancement**
   - Histogram Equalization (HE)
   - CLAHE (Contrast Limited Adaptive HE)
   - Image Complement

2. **Lung Segmentation**  
   - U-Net model for mask generation
   - ROI extraction by masking

3. **Standardization**  
   - Resized to 224×224 pixels

### Model Architecture
- **Transfer Learning** with:
  - EfficientNetB0
  - VGG19
- Custom CNN layers for fine-tuning
- Trained with Adam optimizer

## Results
| Model          | Accuracy | Precision | Recall | F1-Score | AUC-ROC |
|----------------|----------|-----------|--------|----------|---------|
| EfficientNetB0 | 77.9%    | 77.4%     | 77.9%  |  76.0%   |  94.0%  |
| VGG19          | 81.4%    | 82.0%     | 94.7%  |  81.5%   |  94.8%  |



## How to Use
```bash
git clone https://github.com/yourusername/covid-19-diagnosis.git
cd covid-19-diagnosis
pip install -r requirements.txt
python predict.py --image_path="samples/covid_case.png"
