# Real-Time Deepfake Detection with Grad-CAM++

This project implements a **real-time deepfake detection system** using a **CNN-LSTM model** and integrates **Grad-CAM++** for visualizing the regions influencing the model's predictions. The system is capable of processing video streams (webcam or file-based) to classify frames as either "Real" or "Deepfake" with explainable AI insights.

---

## Table of Contents
1. [Features](#features)
2. [Installation](#installation)
3. [Usage](#usage)
4. [Project Details](#project-details)
5. [Dependencies](#dependencies)
6. [Results](#results)
7. [Future Work](#future-work)
8. [License](#license)

--
Research
## Research Paper
This project is supported by the following research paper:
- [Read the paper on arXiv](https://arxiv.org/abs/your-paper-link)
- [Download the PDF](docs/deepfake_detection_research_paper.pdf)

---

## Features
- **Real-Time Detection**: Processes live webcam feeds or video files.
- **Explainable AI**: Generates Grad-CAM++ heatmaps to visualize areas influencing predictions.
- **Flexibility**: Supports both real-time and offline video processing.
- **Accurate Predictions**: Uses a pre-trained CNN-LSTM model for sequential frame classification.

---

## Installation

### Prerequisites
- Python 3.7 or higher
- OpenCV for video capture and frame processing
- TensorFlow/Keras for model inference
- Matplotlib for visualization (optional)

### Steps
1. Clone this repository:
    ```bash
    git clone https://github.com/your-username/deepfake-detection.git
    cd deepfake-detection
    ```
2. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```
3. Download the pre-trained model `cnn_lstm_final_model.keras` and place it in the project directory.

---

## Usage

### Running the Script
1. To process a **webcam feed**:
    ```bash
    python real_time_detection.py
    ```
2. To process a **video file**:
    Replace `cap = cv2.VideoCapture(0)` with your video file path:
    ```python
    cap = cv2.VideoCapture('/path/to/video.mp4')
    ```

### Grad-CAM++ Heatmap Visualization
- If a sequence is classified as "Deepfake," the Grad-CAM++ heatmap is displayed in a separate window, highlighting areas of importance in the frame.

### Key Bindings
- Press **`q`** to quit the real-time detection.

---

## Project Details

### Workflow
1. **Frame Capture**: Video frames are captured and resized to `224x224`.
2. **Buffering**: A sequence of 16 frames is maintained for sequential processing.
3. **Prediction**: The CNN-LSTM model classifies the sequence as "Real" or "Deepfake."
4. **Explainability**: Grad-CAM++ generates a heatmap for deepfake classifications.

### Model Architecture
- **CNN Backbone**: EfficientNetB0 for feature extraction.
- **LSTM**: Processes sequential data for temporal dependencies.
- **Output Layer**: Binary classification (Real/Deepfake).

---

## Dependencies
- **Python**: 3.7+
- **TensorFlow/Keras**: 2.0+
- **OpenCV**: 4.5+
- **NumPy**
- **Matplotlib**

Install dependencies using:
```bash
pip install -r requirements.txt
```
##Results
Test Accuracy: 99.5%
Validation Accuracy: 95.0%
Explainability: Grad-CAM++ highlights the facial regions used for decision-making.

##Future Work
Performance Optimization: Improve real-time processing speed with frame skipping and optimized models.
Multimodal Inputs: Incorporate audio analysis for better deepfake detection.
Mobile Deployment: Port the model to mobile devices for on-the-go detection.

##License
This project is licensed under the MIT License. See the LICENSE file for details.

##Acknowledgements
The CNN-LSTM model is inspired by state-of-the-art research in deepfake detection.
Grad-CAM++ implementation adapted for interpretability in sequential video analysis.
Dataset sourced from Deepfake Detection Challenge and additional synthetic datasets.
