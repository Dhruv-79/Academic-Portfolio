# 🤖 ProctorAI: Intelligent Exam Surveillance System

## 📌 Project Overview

**ProctorAI** is an AI-powered examination surveillance system designed to monitor online examinations in real time and identify potentially suspicious behaviour.

The system uses computer vision and behavioural analysis to detect events such as **looking away, mobile phone usage, presence of multiple people, and unusual movement**. It provides real-time alerts, evidence screenshots, session logging, and post-examination review capabilities.

The platform is designed for local deployment, reducing dependence on external cloud services while supporting privacy-conscious examination monitoring.

## 🎯 Objectives

- To automate real-time examination surveillance using AI.
- To detect suspicious candidate behaviour.
- To identify mobile phone usage and multiple-person presence.
- To analyse candidate head pose and gaze direction.
- To generate real-time examination integrity alerts.
- To maintain structured evidence and audit records.
- To provide administrators with a real-time monitoring dashboard.
- To support privacy-preserving and locally deployable examination monitoring.

## ⚙️ Key Features

- 👁️ Look-away and gaze deviation detection
- 📱 Mobile phone detection
- 👥 Multiple-person detection
- 🏃 Movement analysis
- 🚨 Real-time behavioural alerts
- 📸 Evidence screenshot capture
- 📊 Monitoring dashboard
- 📝 Examination event logging
- 🔍 Post-session incident review
- 📄 PDF report generation
- 📊 CSV data export
- 🔐 JWT-based authentication
- 🌐 WebSocket-based real-time communication
- 🔒 Local processing and privacy-focused architecture

## 🧠 AI & Computer Vision

The system combines multiple computer vision techniques:

- **YOLOv8 Nano** for object detection, including mobile phones and people.
- **MediaPipe Face Mesh** for facial landmark detection and gaze/head-pose analysis.
- **OpenCV** for video processing and head-pose estimation.
- Temporal filtering and multi-frame confirmation are used to reduce false-positive alerts.

YOLOv8 Nano achieved a reported phone-detection accuracy of **89.7%**, while multi-person detection achieved **93.8% accuracy**. Look-away detection achieved **91.3% accuracy**. :contentReference[oaicite:0]{index=0}

## 🏗️ System Architecture

```text
              Candidate Webcam
                     │
                     ▼
              Video Acquisition
                     │
                     ▼
              AI Inference Layer
              ┌──────┴──────┐
              ▼             ▼
          YOLOv8n      MediaPipe Face Mesh
              │             │
              └──────┬──────┘
                     ▼
             Behaviour Analysis
                     │
                     ▼
              Alert & Logging
              ┌──────┴──────┐
              ▼             ▼
           SQLite       WebSocket
              │             │
              ▼             ▼
        Evidence &      Live Dashboard
        Audit Records
