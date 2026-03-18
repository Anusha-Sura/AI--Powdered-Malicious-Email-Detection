🛡️ AI-Powered Real-Time Phishing Detection for Thunderbird

A real-time phishing detection system designed to enhance email security by integrating a custom Mozilla Thunderbird extension with machine learning models. The system identifies malicious emails instantly using deep learning and traditional ML techniques.

🚀 Overview

Phishing attacks are becoming increasingly sophisticated, making them difficult for traditional spam filters to detect. This project introduces a hybrid ML-powered detection system that analyzes both URLs and email metadata to classify phishing attempts in real time.

The solution combines:

A Thunderbird extension for email monitoring

A Flask-based backend API

LSTM and Random Forest models for classification

🔍 Key Features

🔗 URL-Based Phishing Detection using LSTM deep learning model

📧 Sender & Metadata Analysis with Random Forest

⚡ Real-Time Email Scanning inside Thunderbird

🔁 Seamless Backend Communication via Flask APIs + Ngrok

🧠 Trained on Real-World Datasets (Kaggle & Zenodo)

🚨 Visual Alerts for suspicious emails in inbox

🧠 Machine Learning Models
🔹 LSTM Model (URL Classification)

Character-level embedding

2-layer LSTM (hidden size: 32)

Detects malicious URL patterns

Accuracy: ~84.2%

🔹 Random Forest (Email Metadata)

Features:

Digit count

Domain length

Special characters

100 estimators

F1 Score: 0.80

🏗️ System Architecture
Thunderbird Extension → Flask API → ML Models → Prediction → UI Alert

Email is opened in Thunderbird

Extension extracts sender + URLs

Data sent to Flask backend

Models perform classification

Result returned and displayed in UI

🛠️ Tech Stack

Backend:

Python

Flask

PyTorch

Scikit-learn

Frontend:

JavaScript

CSS

JSON (Thunderbird Extension APIs)

Deployment:

Google Colab

Ngrok

Other Tools:

Kaggle datasets

Zenodo datasets

⚙️ Setup & Installation
📦 1. Backend Setup (Google Colab)
Step 1: Upload Required Files

Upload the following files to your Colab environment:

LSTM.py

Embedding_and_positional_encoding.py

Preprocessing.py

Training_and_evaluating.py

Final_rf_model.pkl

Lstm_url_classifier.pth

Step 2: Install Dependencies
pip install flask torch pyngrok
Step 3: Configure Ngrok

Create account at https://ngrok.com

Copy your auth token

ngrok authtoken YOUR_AUTH_TOKEN
Step 4: Run Flask Server

Start the Flask app

Copy generated Ngrok public URL

🧩 2. Thunderbird Extension Setup
Step 1: Update Backend URL

Open background.js

Replace API endpoint with Ngrok URL

Step 2: Load Extension

Open Thunderbird

Go to: Tools → Developer Tools → Debug Add-ons

Click Load Temporary Add-on

Select manifest.json

📬 Usage

Open any email in Thunderbird

Extension automatically extracts:

Sender details

Embedded URLs

Data is sent to backend

Email is classified as:

✅ Safe

🚨 Phishing

Visual Indicators:

Red highlight → Suspicious

Label → Spam / Safe

⚠️ Important Note

The extension is temporary and must be reloaded after restarting Thunderbird

Ngrok session URLs change unless using a paid plan

📊 Future Enhancements

Deploy backend on AWS / GCP for scalability

Replace LSTM with Transformer-based models (BERT, etc.)

Add multilingual phishing detection

Build interactive dashboard for monitoring

Enable continuous learning with user feedback

🎯 Use Case

This system helps:

Detect phishing attacks in real time

Improve email security systems

Support cybersecurity research

Demonstrate practical ML + full-stack integration

👩‍💻 Author

Anusha Sura

MS in Information Systems (Business Data Analytics)

Skills: Python, Machine Learning, SQL, Tableau, Full Stack Development
