# Predicting Aerobic Fitness from Wearable Sensor Data

Final year project (B.Sc. Computer Science) — Rahman Rufai-Alao, Crescent University, Abeokuta.

## Overview

This project predicts aerobic fitness (VO2max, categorized as Low/High) from wearable heart-rate
and accelerometer sensor data collected during submaximal treadmill running. Three classifiers —
Logistic Regression, Random Forest, and SVM — are trained and compared using cross-validation.
The best-performing model (Random Forest) is deployed in a simple Gradio app that lets anyone
estimate their aerobic fitness from age, body mass, and heart rate readings.

## Dataset

De Brabandere et al. (2018), *PLOS ONE* — 41 treadmill running trials with heart-rate and
body-worn accelerometer signals, plus lab-measured VO2max for each subject.

## Methods

- Feature selection: `SelectKBest` (ANOVA F-test)
- Models compared: Logistic Regression, Random Forest, SVM
- Validation: Stratified K-Fold cross-validation
- Metrics: F1-score, confusion matrix, ROC-AUC

## Results

Random Forest performed best:
- Accuracy: ~76%
- ROC-AUC: ~0.80

## Fitness Checker App

Built with [Gradio](https://gradio.app). Takes age, body mass, warm-up heart rate, and running
heart rate as input and returns a Low/High fitness verdict with a confidence score.

## Run it

Click the badge to open and run the notebook directly in Google Colab — no local setup needed.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Rahmmeycodes/aerobic-fitness-ml-prediction/blob/main/aerobic_fitness_prediction.ipynb)

Run all cells top to bottom; the last cell launches the Gradio app with a live URL you can open and test.

Prefer to run it locally instead?

```bash
pip install -r requirements.txt
jupyter notebook aerobic_fitness_prediction.ipynb
```

## Supervisor

Mrs Bakare, Z.M. — Department of Computer Science, College of ICT (CICOT), Crescent University, Abeokuta.
