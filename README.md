# 🔍 EAMNet-S: Lightweight Deepfake Liveness Detection

EAMNet-S is a lightweight and efficient deepfake detection framework designed for real-time liveness verification and fake face detection. The model combines the power of **MobileNetV3Small** with the **CBAM (Convolutional Block Attention Module)** to improve feature extraction, attention learning, and classification performance while maintaining low computational complexity.

The framework is optimized for deployment in real-world applications such as biometric authentication, online examination systems, identity verification, social media content validation, and deepfake prevention systems.

---

## 🌐 Live Demo

🚀 **Try the deployed application here:**

🔗 https://deepsight-deepfake-detector-production.up.railway.app/

The web application allows users to upload face images and perform real-time deepfake detection with confidence scores and visual analysis.

---

## 🚀 Key Features

* ⚡ Lightweight architecture suitable for real-time deployment
* 🧠 CBAM-based attention mechanism for enhanced feature learning
* 🎯 High classification accuracy (~95.3%)
* 📷 Webcam-based live deepfake detection
* 🔥 Grad-CAM visualization for model interpretability
* 🌐 Flask-powered web application deployment
* 📊 Confidence score prediction for real/fake classification
* 🚀 Optimized inference speed with MobileNetV3Small backbone

---

## 🏗️ Model Architecture

The proposed EAMNet-S framework consists of the following components:

### 1. MobileNetV3Small Backbone

* Lightweight CNN architecture
* Efficient feature extraction
* Reduced parameter count
* Suitable for edge devices and low-resource systems

### 2. CBAM Attention Module

The Convolutional Block Attention Module improves feature representation through:

#### Channel Attention

* Learns important feature channels
* Enhances discriminative information

#### Spatial Attention

* Focuses on important image regions
* Improves localization of manipulation artifacts

### 3. Classification Head

* Global Average Pooling Layer
* Fully Connected Dense Layers
* Dropout Regularization
* Sigmoid Output Layer

### Output Classes

* Real Face (0)
* Fake Face / Deepfake (1)

---

## 📊 Dataset

The model was trained using a combination of publicly available deepfake datasets.

| Dataset Information | Value                    |
| ------------------- | ------------------------ |
| Total Images        | ~108,000                 |
| Real Images         | ~52,000                  |
| Fake Images         | ~56,000                  |
| Original Resolution | 256×256                  |
| Training Resolution | 192×192                  |
| Dataset Sources     | Kaggle + Public Datasets |

### Data Preprocessing

* Image resizing
* Normalization
* Data augmentation
* Face extraction and alignment
* Train-validation-test split

---

## ⚙️ Training Configuration

### Hyperparameters

| Parameter                 | Value                |
| ------------------------- | -------------------- |
| Optimizer                 | Adam                 |
| Initial Learning Rate     | 1e-3                 |
| Fine-Tuning Learning Rate | 1e-5                 |
| Batch Size                | 32                   |
| Initial Training Epochs   | 10                   |
| Fine-Tuning Epochs        | 7                    |
| Loss Function             | Binary Cross-Entropy |
| Input Size                | 192×192×3            |

### Hardware Used

* NVIDIA RTX 3050 GPU
* 16GB RAM
* TensorFlow/Keras Framework

---

## 📈 Performance Metrics

The proposed EAMNet-S model achieved strong performance on the test dataset.

| Metric    | Score |
| --------- | ----- |
| Accuracy  | 95.3% |
| Precision | 95.1% |
| Recall    | 94.8% |
| F1-Score  | 94.9% |
| AUC Score | 0.96  |

### Advantages

* High accuracy with fewer parameters
* Faster inference compared to larger CNN architectures
* Improved explainability using Grad-CAM
* Suitable for deployment on resource-constrained systems

---

## 🧪 Real-Time Detection Pipeline

The system supports live deepfake detection using webcam input.

### Workflow

1. Capture video frame
2. Detect face using OpenCV
3. Preprocess image
4. Extract features using MobileNetV3Small
5. Apply CBAM attention mechanism
6. Predict Real/Fake probability
7. Generate confidence score
8. Display Grad-CAM heatmap
9. Apply temporal smoothing for stable predictions

---

## 🔥 Grad-CAM Visualization

To improve model transparency and interpretability, Grad-CAM visualization is integrated into the framework.

Benefits:

* Highlights manipulated regions
* Explains model decisions
* Improves trustworthiness
* Assists in debugging and performance analysis

---

## 🌍 Applications

EAMNet-S can be used in:

* Face Authentication Systems
* Digital Identity Verification
* Online Examination Monitoring
* Deepfake Detection Platforms
* Cybersecurity Systems
* Social Media Content Verification
* Video Conferencing Security
* Financial KYC Verification

---

## 🛠️ Technology Stack

### Backend

* Python
* Flask

### Deep Learning

* TensorFlow
* Keras

### Computer Vision

* OpenCV
* PIL

### Data Processing

* NumPy
* Pandas

### Visualization

* Matplotlib
* Grad-CAM

### Deployment

* Railway

---

## 📂 Project Structure

```bash
EAMNet-S/
│
├── model/                 # Trained model (.h5)
├── static/                # CSS, JavaScript files
├── templates/             # HTML frontend templates
├── app.py                 # Flask backend application
├── requirements.txt       # Project dependencies
├── README.md              # Project documentation
└── dataset/               # Dataset directory
```

---

## 🚀 Installation

### Clone Repository

```bash
git clone https://github.com/your-username/EAMNet-S.git
cd EAMNet-S
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Run Application

```bash
python app.py
```

Open:

```bash
http://127.0.0.1:5000
```

---

## 📌 Future Improvements

* Video-level deepfake detection
* Multi-face detection support
* Mobile deployment using TensorFlow Lite
* ONNX optimization
* Transformer-based attention modules
* Edge AI deployment
* Explainable AI dashboard

---

## 👨‍💻 Authors

**Arif Mondal** 

B.Tech CSE (AI & ML)
Institute of Engineering & Management (IEM), Kolkata

Research Interests:

* Deep Learning
* Computer Vision
* Explainable AI
* Deepfake Detection
* Edge AI Systems

---

## 📜 License

This project is intended for academic, research, and educational purposes.

---

## ⭐ Support

If you found this project useful, please consider giving it a ⭐ on GitHub and sharing it with others.
