# 🚀 Face Mask Detection with CNN & OpenCV

This repository provides a **complete working solution** for real-time **Face Mask Detection** using Convolutional Neural Networks (CNN) and OpenCV. It is designed to work **flawlessly in Google Colab or locally** (e.g., VS Code), with **no broken links** and a **ready-to-run dataset from Kaggle**.

---

## ✅ Features

- ✔️ 98% Accuracy  
- 📸 Real-Time Webcam Detection  
- 💻 Runs in Google Colab & VS Code  
- 📦 Uses Kaggle Dataset (no 404 errors)  
- 🧠 Simple CNN Architecture  

---

## 🔧 Installation & Setup

Install all required dependencies:

```bash
pip install tensorflow opencv-python matplotlib numpy scikit-learn kaggle
```

---

## 📂 Dataset Download (Kaggle)

1. Create and download your `kaggle.json` API key from your [Kaggle account](https://www.kaggle.com/account).
2. Upload `kaggle.json` to your working directory (Colab/local).
3. Run the following to set up:

```python
from google.colab import files
files.upload()  # Upload kaggle.json

!mkdir ~/.kaggle
!cp kaggle.json ~/.kaggle/
!chmod 600 ~/.kaggle/kaggle.json
```

Then, download and unzip the dataset:

```bash
kaggle datasets download -d omkargurav/face-mask-dataset
unzip face-mask-dataset.zip
```

---

## 🧼 Data Loading & Preprocessing

- Reads images from `with_mask` and `without_mask` folders
- Resizes them to 128x128
- Normalizes pixel values
- Splits into training and testing sets

---

## 🧠 Model Architecture (CNN)

A simple CNN model with:

- Conv2D → MaxPooling → Conv2D → MaxPooling → Conv2D → MaxPooling  
- Flatten → Dense → Dropout → Dense (Output)

Loss: `sparse_categorical_crossentropy`  
Optimizer: `Adam`  
Metrics: `Accuracy`

---

## 🏋️‍♂️ Model Training

Train the model with 10 epochs and plot accuracy trends.

```python
model.fit(X_train, y_train, epochs=10, validation_data=(X_test, y_test))
```

---

## 🎥 Real-Time Detection

Real-time webcam detection using OpenCV and Haar cascades:

- Captures video feed
- Detects face
- Classifies as Mask or No Mask using trained model
- Displays result with bounding box

Works in Google Colab using JavaScript webcam integration.

---

## 📈 Results & Performance

- Achieves over **98% accuracy** on validation data.
- Handles real-time inference efficiently on webcam streams.

---

## 🎯 Why Use This Project?

- ✅ End-to-end pipeline — no additional setup needed
- 🔗 Uses working Kaggle dataset — no broken URLs
- 🚀 Ready to deploy or extend for mobile/web
- 🧪 Ideal for learning CNNs and image classification

---

## 📌 License 
Feel free to fork, clone, and modify!

