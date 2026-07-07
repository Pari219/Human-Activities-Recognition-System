# 🏃 Human Activity Recognition System

Classifying human physical activities — **Walking, Running, Sitting, and Jumping** — from raw smartphone accelerometer data using a 1D Convolutional Neural Network.

![Python](https://img.shields.io/badge/Python-3.x-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-CNN-orange)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

---

## 📌 Overview

This project builds a complete, end-to-end Human Activity Recognition (HAR) pipeline — from raw sensor data collection to a trained deep learning classifier — using nothing but a smartphone and open-source tools.

Instead of relying on a public benchmark dataset, the sensor data was **self-collected** using the [phyphox](https://phyphox.org/) app, which turns a smartphone's built-in accelerometer into a scientific data logger. This makes the project a full-stack demonstration of practical ML skills: sensor data acquisition, signal preprocessing, model design, training, and evaluation.

## 🎯 Motivation

Wearable and mobile sensor-based activity recognition powers real-world applications like fitness tracking, fall detection, and health monitoring. This project explores how far a lightweight 1D CNN can go in classifying everyday human activities using only raw triaxial accelerometer signals — no handcrafted features required.

## 🗂️ Activities Classified

| Class | Description |
|---|---|
| 🚶 Walking | Normal walking pace |
| 🏃 Running | Fast-paced running |
| 🪑 Sitting | Stationary, seated position |
| 🤸 Jumping | Repeated vertical jumps |

## 📊 Dataset

- **Source:** Self-collected using the phyphox app's accelerometer sensor
- **Device:** Smartphone (carried/held during activity)
- **Format:** Raw `.csv` files, one per recording session
- **Classes:** 4 (Walking, Running, Sitting, Jumping)
- **Structure:**

```
assets/
└── sensorData/
    ├── Walking/
    │   └── *.csv
    ├── Running/
    │   └── *.csv
    ├── Sitting/
    │   └── *.csv
    └── Jumping/
        └── *.csv
```

Each CSV contains time-series accelerometer readings (X, Y, Z axes) recorded during a single activity session.

## 🧠 Methodology

1. **Data Collection** — Accelerometer signals recorded via phyphox for each of the 4 activities across multiple sessions.
2. **Preprocessing** — Raw CSV signals cleaned, segmented into fixed-length windows, and normalized for model input.
3. **Model Architecture** — A 1D Convolutional Neural Network (1D CNN) designed to learn temporal patterns directly from raw accelerometer sequences.
4. **Training & Evaluation** — Model trained and validated in Google Colab, with accuracy and loss tracked across epochs.
5. **Deployment-Ready Conversion** — Trained model converted to **TensorFlow Lite (TFLite)** format for lightweight, on-device inference — a key step toward real-world mobile/edge deployment.

## 📈 Results

- **Test Accuracy:** ~99.8%
- The model reliably distinguishes between dynamic activities (Walking, Running, Jumping) and static activity (Sitting), demonstrating strong generalization from a compact, self-collected dataset.

## 🛠️ Tech Stack

- **Data Collection:** phyphox (smartphone sensor app)
- **Language:** Python
- **Environment:** Google Colab
- **Deep Learning:** TensorFlow / Keras (1D CNN)
- **Deployment Format:** TensorFlow Lite (TFLite)

## 📁 Repository Structure

```
Human-Activities-Recognition-System/
├── assets/
│   └── sensorData/
│       ├── Walking/
│       ├── Running/
│       ├── Sitting/
│       └── Jumping/
├── HumanActivityRecognition.ipynb
└── README.md
```

## 🚀 Getting Started

1. Clone the repository
   ```bash
   git clone https://github.com/Pari219/Human-Activities-Recognition-System.git
   ```
2. Open `HumanActivityRecognition.ipynb` in Google Colab or Jupyter Notebook
3. Run all cells to preprocess the data, train the 1D CNN, and view evaluation results

## 🔮 Future Improvements

- Expand dataset with more subjects and sessions per activity for better generalization
- Add gyroscope data alongside accelerometer for richer motion signals
- Deploy the TFLite model in a real Android app for live activity recognition
- Experiment with LSTM/GRU or hybrid CNN-RNN architectures for comparison

## 👩‍💻 Author

**Karishma Rajput (Pari)**
B.Tech, Computer Science & Engineering (Data Science), NSUT Delhi
[GitHub: @Pari219](https://github.com/Pari219)

---

⭐ If you find this project interesting, consider giving it a star!
