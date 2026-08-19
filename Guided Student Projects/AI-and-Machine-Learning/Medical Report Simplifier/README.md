# 🔎 Medical Report Simplifier for Patients

## 📌 Project Overview

The **Medical Report Simplifier for Patients** is an AI-powered healthcare communication platform designed to process complex clinical reports and convert them into simple, accessible, patient-friendly language.

Unlike conventional health reference tools that require users to look up individual medical terms manually, this system leverages **Natural Language Processing (NLP), Machine Learning (ML), and rule-based dictionary mappings** to transform entire medical reports—such as discharge summaries, lab results, and diagnostic notes—into easy-to-understand summaries without losing original clinical meaning or context.

## 🎯 Objectives

- Process user-provided medical reports in multiple formats, including raw text and PDF uploads.
- Automate text preprocessing using standardized NLP techniques such as tokenization, stopword removal, and lemmatization.
- Simplify complex clinical terminology using a validated, rule-based medical mapping dictionary.
- Generate context-aware, structured report summaries using machine learning algorithms.
- Deliver a responsive and accessible user interface for patients and non-technical users through Streamlit.
- Secure patient data and report history using session authentication and a relational MySQL database.

## ⚙️ Key Features

- 📄 **Multi-Format Input:** Direct text entry and digital PDF file parsing.
- 🧹 **NLP Preprocessing:** Automated text cleaning, stopword removal, tokenization, and lemmatization.
- 📖 **Medical Dictionary Mapping:** Rule-based translation of dense medical jargon, such as converting *Hypertension* to *High Blood Pressure*.
- 🧠 **Hybrid Simplification Engine:** Combines rule-based logic and machine learning models to improve clinical fidelity and preserve context.
- 📊 **Multi-Model Evaluation:** Performance-tested using Logistic Regression, Naive Bayes, KNN, Random Forest, and Support Vector Machine (SVM) algorithms.
- 🔐 **User Authentication:** Encrypted login and signup system for private, isolated user sessions.
- 🗄️ **Report History Vault:** Persistent storage of original and simplified reports in a MySQL database.
- 📥 **Export Functionality:** Capability to export simplified summaries into PDF or image formats for offline clinical use.

## 🧠 System Architecture & Workflow

```text
User Input (Raw Text / PDF Upload)
       │
       ▼
Text Extraction & Cleanup
       │
       ▼
NLP Preprocessing (Tokenization, Stopwords, Lemmatization)
       │
       ▼
TF-IDF Feature Vectorization
       │
       ├───────────────────────────────┐
       ▼                               ▼
Rule-Based Module               ML Model Layer
(Dictionary Mapping)            (Trained SVM Model)
       │                               │
       └───────────────┬───────────────┘
                       │
                       ▼
            Hybrid Output Combination
                       │
                       ▼
            Context-Rich Summary Output
                       │
        ┌──────────────┴──────────────┐
        ▼                             ▼
Streamlit Display UI        MySQL History Database
