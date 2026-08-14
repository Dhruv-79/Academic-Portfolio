# 🫁 Multimodal COPD Prediction System

## 📌 Project Overview

The **Multimodal COPD Prediction System** is an AI-based healthcare application designed to support COPD screening by combining **chest X-ray imaging** with **clinical spirometry information**.

The system uses a **Convolutional Neural Network (CNN)** for image-based prediction and an **Artificial Neural Network (ANN)** for clinical-data prediction. Their outputs are combined using a **50:50 weighted fusion approach** to generate an integrated prediction.

The application also incorporates clinical indicators including **FEV1/FVC ratio, BMI, smoking status, and GOLD-based risk assessment**, while presenting separate CNN, ANN, and fusion probabilities for greater transparency. :contentReference[oaicite:0]{index=0}

## 🎯 Objectives

- To develop a multimodal AI system for COPD prediction.
- To analyse chest X-ray images using a CNN.
- To process clinical and spirometry data using an ANN.
- To combine imaging and clinical predictions using weighted fusion.
- To incorporate the GOLD criterion of FEV1/FVC < 0.70.
- To calculate relevant clinical indicators automatically.
- To provide separate prediction probabilities.
- To develop a user-friendly Streamlit application for real-time prediction. :contentReference[oaicite:1]{index=1}

## ⚙️ Key Features

- 🩻 Chest X-ray analysis
- 🧠 CNN-based prediction
- 📊 ANN-based clinical prediction
- 🔗 50:50 multimodal fusion
- 📐 BMI calculation
- 🫁 FEV1/FVC analysis
- 🚬 Smoking-status assessment
- 📋 GOLD-based risk interpretation
- 📈 Separate CNN, ANN, and fusion probabilities
- 🌐 Streamlit web interface
- ⚡ Lightweight CPU-based inference
- ✅ Input validation

## 🏗️ System Architecture

```text
              Patient Information
                     │
          ┌──────────┴──────────┐
          │                     │
          ▼                     ▼
    Chest X-Ray            Clinical Data
          │                     │
          ▼                     ▼
         CNN                   ANN
          │                     │
          └──────────┬──────────┘
                     ▼
               50:50 Fusion
                     │
                     ▼
              COPD Prediction
                     │
                     ▼
          Clinical Interpretation
                     │
                     ▼
             Streamlit Output
