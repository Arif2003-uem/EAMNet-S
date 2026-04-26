# 🔍 EAMNet-S: Lightweight Deepfake Liveness Detection

EAMNet-S is a lightweight and efficient deepfake detection framework designed for real-time liveness verification. The model integrates **MobileNetV3Small** with the **CBAM (Convolutional Block Attention Module)** to enhance feature extraction while maintaining high accuracy and low computational cost.

---

## 🚀 Key Features

- ⚡ Lightweight architecture for real-time detection  
- 🧠 Attention-based feature enhancement using CBAM  
- 🎯 High accuracy (~95.3%)  
- 📷 Webcam-based live deepfake detection  
- 🔥 Grad-CAM visualization for interpretability  
- 🌐 Flask-based web application for deployment  

---

## 🏗️ Model Architecture

The proposed **EAMNet-S** model consists of:

- MobileNetV3Small (Backbone Network)  
- CBAM Attention Module (Channel + Spatial Attention)  
- Global Average Pooling  
- Fully Connected Layers  
- Sigmoid Output (Binary Classification: Real / Fake)  

---

## 📊 Dataset

- Total Images: ~108,000  
- Real Images: 52,000  
- Fake Images: 56,000  
- Resolution: 256×256 (resized to 192×192 for training)  
- Source: Kaggle + publicly available datasets  

---

## ⚙️ Training Details

- Optimizer: Adam  
- Learning Rate: 1e-3 (initial), 1e-5 (fine-tuning)  
- Batch Size: 32  
- Epochs: 10 + 7 (fine-tuning phase)  
- Loss Function: Binary Cross-Entropy  
- Hardware: RTX 3050 GPU, 16GB RAM  

---

## 📈 Performance Metrics

| Metric     | Value   |
|------------|--------|
| Accuracy   | 95.3%  |
| Precision  | 95.1%  |
| Recall     | 94.8%  |
| F1-score   | 94.9%  |
| AUC        | 0.96   |

---

## 🧪 Real-Time Testing

The system supports live detection using webcam input:

- Face detection using OpenCV  
- Prediction with confidence score  
- Grad-CAM heatmap visualization  
- Temporal smoothing for stable results  

---

## 🛠️ Tech Stack

- Python  
- TensorFlow / Keras  
- OpenCV  
- Flask  
- NumPy, PIL  

---

## 📂 Project Structure
EAMNet-S/
│── model/ # Trained model (.h5)
│── static/ # CSS, JS files
│── templates/ # HTML frontend
│── app.py # Flask backend
│── requirements.txt # Dependencies
│── README.md # Project documentation
