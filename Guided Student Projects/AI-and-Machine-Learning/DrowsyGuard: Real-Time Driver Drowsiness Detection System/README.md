# 🚗 DrowsyGuard: Real-Time Driver Drowsiness Detection System

## 📌 Project Overview

**DrowsyGuard** is an AI-powered real-time driver drowsiness detection system designed to monitor driver alertness using a standard webcam and consumer-grade hardware.

The system combines **Eye Aspect Ratio (EAR)** analysis using MediaPipe Face Mesh with a custom **Convolutional Neural Network (CNN)** for eye-state classification. The hybrid approach combines geometric and deep-learning-based detection to improve robustness while maintaining real-time performance.

Additional capabilities include low-light enhancement using CLAHE, blink-rate and head-pitch monitoring, a browser-based monitoring dashboard, and two-tier audio and email alerts.

## 🎯 Objectives

- To develop a real-time driver drowsiness detection system.
- To detect prolonged eye closure using EAR analysis.
- To classify eye states using a custom CNN.
- To combine EAR and CNN predictions through hybrid fusion.
- To improve detection under varying illumination.
- To provide real-time audio and email alerts.
- To provide a browser-based monitoring dashboard.
- To develop a low-cost solution using consumer hardware.

## ⚙️ Key Features

- 👁️ Real-time eye-state detection
- 🧠 CNN-based eye classification
- 📐 Eye Aspect Ratio analysis
- 🔗 Hybrid EAR + CNN fusion
- 🌙 CLAHE-based low-light enhancement
- 📊 Blink-rate monitoring
- 📈 Head-pitch monitoring
- 🔊 Audio alerts
- 📧 Email alerts
- 🌐 Flask-based web dashboard
- 📹 Real-time MJPEG video streaming
- 💻 Consumer CPU deployment
- 🔒 Local video processing

## 🧠 Detection Approach

```text
              Webcam Feed
                   │
                   ▼
            Face Detection
                   │
          ┌────────┴────────┐
          ▼                 ▼
   MediaPipe Face Mesh     Eye ROI
          │                 │
          ▼                 ▼
        EAR              CNN Model
          │                 │
          └────────┬────────┘
                   ▼
             Hybrid Fusion
                   │
                   ▼
        Drowsiness Assessment
                   │
          ┌────────┴────────┐
          ▼                 ▼
     Audio Alert        Email Alert
