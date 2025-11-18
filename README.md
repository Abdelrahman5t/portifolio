 Image Classification & Object Detection System

(Final Project – DEPI)

 Overview

This project is an end-to-end AI system capable of performing Image Classification and Object Detection using state-of-the-art deep learning models.
The system uses ResNet50 for classification and YOLOv8 for detection, with deployment on Microsoft Azure and a complete MLOps pipeline for monitoring, retraining, and experiment tracking.

The final product includes a web interface for real-time predictions, cloud APIs, and scalable infrastructure suitable for realistic applications such as surveillance, retail analytics, and automated quality inspection.


---

 Team Members & Roles

Member	Role

Basel Mohamed Mostafa	Object Detection Model Implementation & Evaluation
Zeyad Ahmed Samir	Data Collection, Preprocessing & EDA
Zeyad Gamal Mohamed	Team Leader, Model Development & Azure Deployment
Abdulrahman Kamal Saeed	Image Classification Model & Transfer Learning
Mohamed Hamada Farghali	MLOps, Monitoring & Retraining Strategy
Omar Yasser Sayed	Web Interface (Frontend & API Integration)



---

 Objectives

Collect and preprocess high-quality datasets.

Build classification and detection models using ResNet50 and YOLOv8.

Apply transfer learning and fine-tuning to improve model accuracy.

Deploy the models on Azure Cloud using containerized services and REST APIs.

Implement MLOps (MLflow + Azure ML Pipelines).

Develop a simple and user-friendly web interface.

Ensure scalability, high uptime, and performance metrics.



---

 Technologies Used

🔹 Deep Learning

TensorFlow, Keras

OpenCV

YOLOv8 (Ultralytics)

ResNet50


🔹 Cloud & MLOps

Azure Machine Learning

Azure Container Instances

MLflow

Prometheus / Grafana

Application Insights


🔹 Web Development

FastAPI / Flask

HTML, CSS, JavaScript

Streamlit (optional)


🔹 Data Tools

NumPy, Pandas

Matplotlib, Seaborn

Albumentations



---

 System Architecture

┌────────────────────────┐
                         │     Web Interface       │
                         │ (Image Upload + Results)│
                         └─────────────┬──────────┘
                                       │
                  ┌────────────────────┼───────────────────┐
                  │                    │                   │
        ┌─────────▼────────┐   ┌──────▼────────┐   ┌──────▼────────┐
        │ Classification API │   │ Detection API │   │ MLOps Tracking │
        │ (FastAPI + TF)     │   │ (YOLO + ACI)  │  │    (MLflow)     │
        └─────────┬─────────┘   └──────┬────────┘   └──────┬────────┘
                  │                    │                   │
                  └──────────┬─────────┴─────────┬─────────┘
                             │                   │
                      ┌──────▼──────┐     ┌──────▼────────┐
                      │ Azure ML     │     │ Azure Storage │
                      │ (Training)   │     │ (Models/Data) │
                      └──────────────┘     └───────────────┘


---

 Methodology

1. Data Collection & Preprocessing

Collected datasets for classification & detection.

Cleaning, normalization, augmentation (rotate, flip, brightness).

Ensured dataset balance and valid image-label mappings.

Performed EDA to analyze:

Class distribution

Bounding box verification

Data diversity



2. Model Development

Classification (ResNet50)

Pre-trained on ImageNet.

Custom top layers added.

Fine-tuned for domain-specific tasks.

Output metrics: Accuracy, F1-score.


Object Detection (YOLOv8)

Custom dataset labeled.

YOLOv8 training & validation.

Evaluation using mAP@0.5 and precision/recall.


3. Deployment

Models containerized with Docker.

Azure Container Instances used for hosting APIs.

REST APIs built using FastAPI for inference requests.


4. MLOps Pipeline

MLflow for experiment tracking and model versioning.

Monitoring includes latency, error rates, throughput.

Retraining pipeline triggered based on data drift or performance drop.


5. Web Interface

Simple UI allowing:

Image uploads

Display of predictions

Bounding boxes drawn for detected objects


---

📈 KPIs

Data Quality

Missing values handled: 100%

Data accuracy: 98%

Dataset diversity: ≥ 90%


Model Performance

Classification accuracy: ≥ 92%

Object detection mAP@0.5: ≥ 85%

Prediction latency: ≤ 300 ms

Error rate: ≤ 5%


Deployment & Scalability

API uptime: ≥ 99%

API response time: ≤ 500 ms

Real-time detection fps: ≥ 10 FPS


Business Impact

Manual effort reduction: 70%

Cost savings: 40%

User satisfaction: ≥ 4.5/5



---

 Deliverables

Trained ResNet50 Classification Model

Trained YOLOv8 Detection Model

Azure Cloud Deployment (APIs + Containers)

Web Interface (HTML/JS or Streamlit)

MLflow tracking system

Monitoring dashboard

Final documentation

Presentation & demo video



---

🏁 Conclusion

This project provides a scalable and powerful end-to-end image analysis system combining deep learning, cloud deployment, and MLOps.
It delivers high accuracy, real-time predictions, and a production-ready solution for real-world use cases.
