# Deepfake Detection for Online Misinformation

This project focuses on developing a real-time deepfake detection system to combat the spread of misinformation using cutting-edge machine learning models and explainable AI techniques. The solution is built with Python, TensorFlow, OpenCV, and Matplotlib and was primarily developed and tested in Google Colab.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Results and Visualization](#results-and-visualization)
- [Future Work](#future-work)
- [License](#license)

## Overview
With the rise of misinformation through manipulated media, real-time deepfake detection is crucial for maintaining online content integrity. This project leverages 3D Convolutional Neural Networks (CNNs) and sequential models like LSTM/GRU to enhance deepfake detection accuracy, achieving a performance improvement of 45% over traditional methods. The project also integrates explainable AI techniques such as Grad-CAM++ and Layer-wise Relevance Propagation (LRP) to offer users insights into the model's decision-making process.

## Features
- **Real-time Deepfake Detection:** Processes live video feeds to detect manipulated content.
- **Explainable AI:** Utilizes Grad-CAM++ and Layer-wise Relevance Propagation (LRP) to highlight regions in each frame contributing to the prediction.
- **Webcam Demo:** Live demo setup for real-time video analysis and heatmap visualization, emphasizing model interpretability.

## Project Structure

## Installation
To set up the environment, clone the repository and install the required packages.


git clone https://github.com/yourusername/deepfake-detection.git
cd deepfake-detection
pip install -r requirements.txt
python scripts/train.py --dataset_path data/DFDC --epochs 50 --batch_size 8
python scripts/explainable_ai.py --video_path path_to_video.mp4
