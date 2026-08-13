# 🏥 AI-Driven Healthcare Decision Support System

## 📌 Project Overview

The **AI-Driven Healthcare Decision Support System** is an intelligent healthcare assistance platform designed to provide preliminary, context-aware healthcare guidance through a conversational interface.

Rather than functioning as a simple chatbot, the system combines **Natural Language Processing (NLP), Retrieval-Augmented Generation (RAG), a structured medical knowledge base, risk classification, confidence evaluation, medication safety controls, and human-in-the-loop escalation**.

The project focuses on developing a responsible AI-based healthcare system where intelligent assistance is supported by safety mechanisms and professional intervention.

---

## 🎯 Objectives

The major objectives of the project are:

- To develop an AI-based healthcare decision support platform.
- To analyse user symptoms through a structured conversational workflow.
- To integrate a verified medical knowledge base.
- To implement Retrieval-Augmented Generation for evidence-grounded responses.
- To classify cases according to risk severity.
- To evaluate confidence in system outputs.
- To restrict unsafe medication recommendations.
- To provide doctor escalation for high-risk or uncertain cases.
- To develop an accessible conversational user interface.
- To evaluate the system through functional, safety, performance, and usability testing.

---

## 🧠 Intelligent Components

The system integrates several AI and decision-support components:

### Natural Language Processing

Processes user-provided symptom descriptions and conversational input.

### Retrieval-Augmented Generation

Retrieves relevant information from the medical knowledge base before generating responses, helping ground the system's outputs in structured medical information.

### Risk Classification

Classifies cases into categories such as:

- Mild
- Moderate
- Severe

### Confidence Scoring

Evaluates the confidence associated with the system's analysis.

Low-confidence cases can trigger professional consultation rather than direct recommendations.

### Medication Safety Engine

The system restricts recommendations to permitted over-the-counter medications and blocks prescription or potentially harmful medication recommendations.

### Doctor Escalation

High-risk or uncertain cases are directed toward qualified healthcare professionals.

---

## ⚙️ Key Features

- 💬 Conversational symptom assessment
- 🧠 AI-assisted healthcare guidance
- 🔎 RAG-based medical information retrieval
- 📚 Structured medical knowledge base
- 🛡️ Medication safety controls
- 📊 Risk classification
- 📈 Confidence evaluation
- 👨‍⚕️ Doctor escalation
- 📅 Appointment booking support
- 🔐 Local LLM deployment
- 🌐 Interactive Streamlit interface
- 🧪 Multi-layer testing and validation

---

## 🏗️ System Architecture

The system follows a modular architecture consisting of:

```text
User
  │
  ▼
Streamlit Interface
  │
  ▼
FastAPI Backend
  │
  ├── Symptom Processing
  ├── Risk Classification
  ├── Confidence Evaluation
  ├── Medication Safety Engine
  │
  ▼
AI Layer
  │
  ├── Local LLM
  ├── RAG
  └── FAISS
  │
  ▼
Medical Knowledge Base
  │
  ▼
Safe Guidance / Doctor Escalation
