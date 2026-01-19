# Human Action Recognition from Videos using Pose-Based Time Series

## Project Objective
The objective of this project is to classify human actions from video sequences by using pose-based time-series data instead of raw pixel information. Body joint keypoints are extracted from each video frame to focus on motion patterns and reduce computational complexity.

The actions classified in this project are:
- Boxing
- Handclapping
- Handwaving
- Jogging
- Running
- Walking

## Methods and Techniques
- **Pose Extraction:**  
  - OpenPose (BODY-25 model) used to extract 25 body joint keypoints per frame  
  - Videos converted into normalized time-series data and saved as `.npz` files  

- **Classification Approaches:**
  - **Global Alignment Kernel (GAK) + SVM** for time-series similarity-based classification  
  - **Shapelet Transform + MLP** to learn discriminative subsequences and classify them using a neural network  
  - **LSTM (PyTorch)** to directly model temporal dependencies in pose sequences  
  - **XGBoost (Extra Method)** using statistical features such as mean, standard deviation, and velocity  

- **Evaluation:**
  - Accuracy used as the main performance metric  
  - Hyperparameter experiments and ablation studies conducted for all methods  

> The dataset is not included in this repository you can download dataset in this link : https://drive.google.com/file/d/1lbBzVOeASQ0z44-I4cRFBwCvMQ7cO46u/view?usp=sharing 
