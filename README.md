 🩺 BreastScan — AI-Powered Mobile App for Breast Cancer Prediction

<div align="center">

![BreastScan Banner](https://img.shields.io/badge/BreastScan-AI%20Health%20App-e91e8c?style=for-the-badge&logo=android)
![Platform](https://img.shields.io/badge/Platform-Android-3DDC84?style=for-the-badge&logo=android)
![ML](https://img.shields.io/badge/ML-TensorFlow%20Lite-FF6F00?style=for-the-badge&logo=tensorflow)
![OCR](https://img.shields.io/badge/OCR-Google%20ML%20Kit-4285F4?style=for-the-badge&logo=google)
![Grade](https://img.shields.io/badge/Grade-S%20(Highest)-gold?style=for-the-badge)
![VIT](https://img.shields.io/badge/VIT%20Bhopal-EPICS%20Project-blue?style=for-the-badge)

> **EPICS Phase II Project | VIT Bhopal University | March 2026**  
> Awarded **S Grade** (Highest) by project supervisor Dr. Praveen Lalwani

</div>

---

## Table of Contents
- [About](#about)
- [Features](#features)
- [System Architecture](#system-architecture)
- [Tech Stack](#tech-stack)
- [Dataset](#dataset)
- [Model Performance](#model-performance)
- [Screenshots](#screenshots)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [Team](#team)
- [Acknowledgements](#acknowledgements)

---

##  About

**BreastScan** is an intelligent Android mobile application built to assist in early breast cancer detection. It combines machine learning, optical character recognition (OCR), and image-based deep learning — all running **on-device** without requiring internet access.

The app targets individuals in resource-limited areas where clinical testing facilities are unavailable or inaccessible. By putting AI-driven screening directly into a smartphone, BreastScan makes early detection accessible to everyone.

>  **Disclaimer:** BreastScan is a supportive screening tool and does not replace professional medical diagnosis. Always consult a certified medical professional for clinical advice.

---

 Features

| Feature | Description |
|--------|-------------|
| Form-Based Prediction** | Enter clinical parameters manually — get instant ML prediction results |
| OCR Report Upload** | Photograph a medical report — AI extracts data automatically |
| Image-Based Prediction** | Upload medical scans for CNN-based visual analysis |
|  Quick Self-Check** | Step-by-step guided self-examination tool |
| Educational Content** | Learn about symptoms, causes, risk factors, and prevention |
  On-Device Processing** | All predictions run locally — no data leaves your device |
| User Profile Management** | Secure login with personal health data management |
| Offline Support** | Works without internet — powered by TensorFlow Lite |

---

System Architecture

```
User Input (Form / Report Image / Medical Scan)
              ↓
    ┌─────────────────────┐
    │   Presentation Layer │  ← XML Layouts + Java Activities
    │   (Android UI)       │
    └─────────┬───────────┘
              ↓
    ┌─────────────────────┐
    │   Processing Layer   │  ← Data Validation + Preprocessing
    │   (Business Logic)   │     + Feature Normalization
    └─────────┬───────────┘
              ↓
    ┌─────────────────────┐
    │     Data Layer       │  ← TFLite Model + OCR Engine
    │  (ML + OCR Engine)   │     + Local Storage
    └─────────┬───────────┘
              ↓
    Prediction Output: Benign / Malignant + Confidence Score
```

---

## 🛠️ Tech Stack

Development
| Tool | Purpose |
|------|---------|
| Android Studio | Primary IDE |
| Java | Backend logic and module development |
| XML | UI layout design |
| Gradle | Build and dependency management |

Machine Learning & AI
| Library | Purpose |
|---------|---------|
| TensorFlow Lite | On-device ML model inference |
| Scikit-learn | Model training (SVM, Random Forest, Logistic Regression) |
| Google ML Kit | OCR — text extraction from medical reports |
| Android Bitmap API | Image preprocessing for CNN model |

Security & Storage
| Tool | Purpose |
|------|---------|
| Firebase Authentication | Secure user login and registration |
| Local On-Device Storage | Private data — never sent to cloud |

---

Dataset

| Dataset | Size | Purpose |
|---------|------|---------|
| **Wisconsin Breast Cancer Dataset (WBCD)** | ~570 samples, 30 features | Form-based ML prediction training |
| **Breast Histopathology Images (BreakHis)** | ~7,909 images | Image-based CNN model training |
| **Custom OCR Test Reports** | 50+ sample reports | OCR pipeline validation |

Key Features Used for Prediction:**
- Radius Mean, Texture Mean, Perimeter Mean
- Area Mean, Smoothness Mean, Compactness Mean
- Concavity Mean, Concave Points Mean
- Symmetry Mean, Fractal Dimension Mean

---

Model Performance

| Metric | Value |
|--------|-------|
| **Form-Based Prediction Accuracy** | ≥ 90% (on clean input data) |
| **Image Classification Accuracy** | ~87% (CNN on preprocessed scans) |
| **OCR Extraction Accuracy** | ~92% (printed text, good lighting) |
| **Prediction Response Time** | 2–3 seconds on-device |
| **Supported Android Version** | Android 6.0 (API 23) and above |
| **Offline Operation** | ✅Full functionality without internet |

---

Screenshots

| Splash Screen | Login Page | Home Screen |
|:---:|:---:|:---:|
| ![Splash](<img width="339" height="300" alt="form bs" src="https://github.com/user-attachments/assets/a43024d6-b7b7-48bb-b98c-8749052df11c" />
) | ![hospitals nearmapping <img width="339" height="300" alt="hospitals near m,e bs" src="https://github.com/user-attachments/assets/2ec9476d-7f1a-4b67-8e9e-9ffe99f938cd" />
) | ![ocr](<img width="339" height="300" alt="hospitals near m,e bs" src="https://github.com/user-attachments/assets/d435d75f-bc1a-40a2-8b08-876a61bbfbf5" />
) |

| Form Prediction | Image Prediction | Profile Page |
|:---:|:---:|:---:|
| ![Form](<img width="262" height="188" alt="Screenshot 2026-06-13 at 5 19 56 PM" src="https://github.com/user-attachments/assets/9163aec2-dfa6-40ee-972a-185a15b03e87" />
) | ![Image](<img width="382" height="300" alt="prediction" src="https://github.com/user-attachments/assets/9805c64f-88a2-4ed2-b681-dbb0c18b5498" />
) | ![Profile](<img width="370" height="306" alt="welcome bs" src="https://github.com/user-attachments/assets/d517c59b-1a67-4fb7-9f93-046cdd424d20" />
) |

> 📁 Add your screenshots to the `/screenshots` folder

---

Installation

Prerequisites
- Android Studio (Hedgehog or later)
- Android SDK (API 23+)
- Java 11+
- Gradle 8.0+

Steps

Clone the repository**
```bash
git clone https://github.com/YOUR_USERNAME/BreastScan.git
cd BreastScan
```

 Open in Android Studio**
```
File → Open → Select the BreastScan folder
```

 Add the ML Model**
```
Place your .tflite model file in:
app/src/main/assets/breast_cancer_model.tflite
```
 Configure Firebase**
```
Add your google-services.json to:
app/google-services.json
```

 Build and Run**
```
Click Run ▶ in Android Studio
Or: ./gradlew assembleDebug
```

---

 Project Structure

```
BreastScan/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/breastscan/
│   │   │   │   ├── activities/
│   │   │   │   │   ├── MainActivity.java
│   │   │   │   │   ├── LoginActivity.java
│   │   │   │   │   ├── FormPredictionActivity.java
│   │   │   │   │   ├── ImagePredictionActivity.java
│   │   │   │   │   └── SelfCheckActivity.java
│   │   │   │   ├── ml/
│   │   │   │   │   ├── ModelHelper.java
│   │   │   │   │   └── DataPreprocessor.java
│   │   │   │   ├── ocr/
│   │   │   │   │   └── OCRManager.java
│   │   │   │   └── utils/
│   │   │   │       ├── ValidationUtils.java
│   │   │   │       └── ImageUtils.java
│   │   │   ├── assets/
│   │   │   │   └── breast_cancer_model.tflite
│   │   │   └── res/
│   │   │       ├── layout/
│   │   │       ├── drawable/
│   │   │       └── values/
│   └── build.gradle
├── ml_model/
│   ├── train_model.py
│   ├── convert_to_tflite.py
│   └── breast_cancer_model.pkl
├── screenshots/
├── docs/
│   └── EPICS_Phase2_Report.pdf
├── .gitignore
├── README.md
└── LICENSE
```

---



**Project Guide:** Dr. Praveen Lalwani, Assistant Professor, VIT Bhopal University

---

 Recognition

> This project was submitted as part of the **EPICS (Engineering Projects in Community Service) Phase II** at VIT Bhopal University and was awarded the **S Grade — the highest distinction** by the project supervisor and reviewers.

**Reviewers:**
- Dr. Buvaneswari P. R. — School of Electrical and Electronics Engineering
- Dr. Ankit Pal — School of Applied Science and Language

---

References

1. K. R. Shravya and V. Sreenivas, "Breast cancer prediction using machine learning techniques," *Journal of Applied Science and Engineering*, 2020.
2. A. T. Assegie, "CNNs for breast cancer classification from histopathology images," *International Journal of Computer Applications*, 2021.
3. I. Cioffi, "TensorFlow Lite optimization strategies for edge deployment," *Future Generation Computer Systems*, 2023.
4. R. Kumar and S. Mehta, "Random forest-based classification for medical diagnosis," *International Journal of Data Science*, 2021.

---

 Acknowledgements

Special thanks to **Dr. E. Nirmala** (Program Chair, CSE-Core) and **Dr. Praveen Lalwani** (Project Guide) for their continuous support and guidance throughout this project.

---

 License

```
MIT License — Free to use with attribution.
See LICENSE file for details.
```

---

<div align="center">

Made with ❤️ by Team BreastScan | VIT Bhopal University | 2026

</div>
