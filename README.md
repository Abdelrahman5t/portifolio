DEPI – Final Project Proposal
Project Title: Image Classification and Object Detection System

---

Team Members and Responsibilities

1. Basel Mohamed Mostafa – Object Detection Model Implementation and Evaluation
2. Zeyad Ahmed Samir – Data Collection, Preprocessing and Exploratory Analysis
3. Zeyad Gamal Mohamed – Team Leader, Model Development and Azure Deployment
4. Abdutrahman Kamal Saeed – Image Classification Model and Transfer Learning
5. Mohamed Hamada Farghali – MLOps, Monitoring and Retraining Strategy
6. Omar Yasser Sayed – Web Interface Development and API Integration

---

Project Overview

Our project aims to create an intelligent system that can both classify images and detect objects within them. We will develop this system using advanced deep learning models and deploy it on Microsoft Azure cloud platform. The final product will include a web-based interface that allows users to upload images and receive instant analysis. This system has practical applications in areas such as security surveillance, retail analytics, and automated quality control in manufacturing.

---

Project Milestones Detailed Breakdown

Milestone 1: Data Collection and Preparation
Lead: Zeyad Ahmed Samir
This initial phase focuses on building our dataset foundation. The team will gather images from multiple reliable sources and public datasets. We will clean the data by removing corrupt or low-quality images and standardize all images to consistent dimensions. Each image will be carefully labeled for both classification categories and object boundaries. Finally, we will perform exploratory data analysis to understand the distribution across different categories and ensure we have a balanced dataset for training.

Milestone 2: Model Development
Lead: Basel Mohamed Mostafa and Abdutrahman Kamal Saeed
During this core development phase, we will build and train our machine learning models. For image classification, we will implement and train a model based on ResNet50 architecture. Simultaneously, for object detection, we will develop a YOLOv8-based model to identify and locate multiple objects within images. We will establish performance baselines for both models and conduct initial evaluations to identify strengths and areas needing improvement.

Milestone 3: Model Optimization and Cloud Deployment
Lead: Zeyad Gamal Mohamed
This phase enhances our models and makes them accessible. We will apply transfer learning techniques to adapt pre-trained models to our specific use cases, significantly improving accuracy. The optimized models will be deployed to Microsoft Azure cloud platform, where we will set up container instances and create a secure REST API that can receive image data and return predictions.

Milestone 4: System Integration and Monitoring
Lead: Omar Yasser Sayed and Mohamed Hamada Farghali
Here we bring all components together into a complete system. We will develop a responsive web interface that allows users to upload images and view results. The frontend will connect to our backend API for processing. We will implement MLOps pipelines for continuous monitoring of model performance and data quality. The system will include automated alerting for performance degradation and establish procedures for model retraining.

Milestone 5: Final Testing and Documentation
Lead: Entire Team
In our final phase, we will conduct comprehensive system testing under various conditions and workloads. We will optimize the complete user experience from image upload to result display. The team will prepare detailed technical documentation covering system architecture and API specifications. Finally, we will create demonstration materials showcasing system capabilities and performance metrics.

---

Complete System Workflow: From Start to Finish

Stage 1: User Input
The process begins when a user accesses our web application through any modern browser.The interface presents a clean, intuitive upload area where the user can either drag and drop an image file or select one from their local storage. The system accepts common image formats including JPG, PNG, and BMP.

Stage 2: Frontend Processing
Once the image is selected,the frontend interface immediately performs initial validation checks. It verifies that the file is a valid image format and checks the file size to ensure it falls within acceptable limits. The image is then temporarily stored in a browser cache and a preview is displayed to the user with a loading indicator.

Stage 3: Backend Reception and Preparation
When the user clicks the process button,the frontend sends the image data to our backend API hosted on Azure. The API receives the image and begins preprocessing. This includes converting the image to the appropriate color format, resizing it to the dimensions required by our models while maintaining aspect ratio, and normalizing pixel values to a standard range.

Stage 4: Model Processing
The preprocessed image is sent to two parallel model pipelines.The classification model analyzes the entire image to determine the overall scene category, such as "urban street," "office interior," or "natural landscape." Simultaneously, the object detection model scans the image to identify and localize specific objects, drawing bounding boxes around each detected item and assigning appropriate labels.

Stage 5: Results Generation
Both models complete their analysis within milliseconds.The classification model returns a primary label along with confidence scores for alternative categories. The detection model returns coordinates for each bounding box, object labels, and individual confidence levels. The backend combines these results into a unified JSON structure that includes both the scene classification and all detected objects with their positions.

Stage 6: Results Delivery and Display
The backend sends the structured results back to the frontend application.The web interface then presents the results in an easily understandable format. The original image is displayed with semi-transparent bounding boxes overlaid on detected objects, each with a label showing the object name and confidence percentage. The overall scene classification appears prominently above the image, and additional details are available in an expandable sidebar.

Stage 7: Continuous Monitoring and Improvement
Behind the scenes,our MLOps system continuously monitors model performance. Each prediction is logged for quality assessment, and performance metrics are tracked in real-time. If model accuracy drops below our defined thresholds, the system alerts the team and can trigger automated retraining processes using new data collected through the application.

---

Performance Targets

Data Quality Standards

· Complete handling of missing values: 100%
· Data accuracy after preprocessing: 98%
· Dataset diversity and balance: 90% or higher

Model Performance Metrics

· Classification accuracy: 92% or higher
· Object detection accuracy (mAP@0.5): 85% or higher
· Prediction response time: 300 milliseconds or less
· Model error rate: 5% or less

System Reliability

· API availability: 99% or higher
· Total response time per request: 500 milliseconds or less
· Real-time processing capability: 10 frames per second or higher

Practical Impact

· Reduction in manual effort: 70%
· Cost savings compared to manual analysis: 40%
· Target user satisfaction rating: 4.5 out of 5

---

Technical Architecture

Our system employs a modular architecture with clear separation between components. The frontend web application communicates with backend services through RESTful APIs. The backend utilizes containerized models deployed on Azure Kubernetes Service, allowing for automatic scaling based on demand. We implement message queues for handling multiple simultaneous requests and ensure data persistence through Azure Blob Storage for uploaded images and results.

---

Conclusion

This project represents a comprehensive approach to building a practical AI system for image analysis. The detailed workflow ensures a seamless user experience while maintaining robust performance and reliability. Each team member has clearly defined responsibilities across the project milestones, ensuring efficient progress toward our goals. The system architecture supports scalability and continuous improvement through integrated monitoring and retraining capabilities.
