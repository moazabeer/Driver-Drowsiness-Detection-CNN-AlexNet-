# Driver Drowsiness Detection using CNN (AlexNet)

Developed by: **Moaz**

This project implements a computer vision solution to monitor and detect driver drowsiness in real-time. By utilizing the **AlexNet architecture** and deep learning techniques, the system classifies facial features (eyes and mouth) to determine if a driver is alert or showing signs of fatigue, significantly reducing the risk of road accidents.

## 📌 Problem Statement
Driver fatigue is a leading cause of traffic accidents globally. This project aims to design an automated detection system that analyzes facial images to identify drowsiness. By issuing real-time alerts when fatigue is detected, the system provides a critical safety layer for long-distance drivers and daily commuters.

## 📊 Dataset
The model is trained using the **Yawn Eye Dataset** from Kaggle.
*   **Content:** A comprehensive collection of images focusing on open/closed eyes and yawning/non-yawning mouth states.
*   **Categories:** Binary classification (Alert vs. Drowsy).
*   **Source:** (https://www.kaggle.com/datasets/serenaraju/yawn-eye-dataset-new)

## 🛠️ Technical Implementation
*   **Framework:** PyTorch
*   **Architecture:** AlexNet (Convolutional Neural Network)
*   **Preprocessing:** 
    *   Resizing images to $227 \times 227$ pixels (AlexNet standard).
    *   Grayscale conversion for feature emphasis.
    *   Data augmentation to simulate varied lighting conditions.
*   **Training Strategy:** 
    *   Transfer Learning using pre-trained AlexNet weights.
    *   Modified final linear layers for binary drowsiness classification.
    *   **Optimizer:** Adam / SGD.
    *   **Loss Function:** Cross-Entropy Loss.
*   **Data Split:** 80% Training, 20% Testing.

## 🚀 How to Run
1.  **Clone the Repository:**
    ```bash
    git clone https://github.com/your-username/driver-drowsiness-detection.git
    cd driver-drowsiness-detection
    ```
2.  **Dataset Setup:**
    Download the dataset from Kaggle and place it in the `data/` directory, or use the automatic download script provided in the notebook.
3.  **Run the Notebook:**
    Execute `Driver_Drowsiness_Detection_(CNN_+_AlexNet).ipynb` to train the model and evaluate performance.

## 📈 Evaluation Results
The model's performance is evaluated using:
*   **Accuracy Metrics:** Precision and Recall focus on minimizing "False Negatives" (missing a drowsy driver).
*   **Performance Graphs:** Real-time plotting of training accuracy and validation loss.
*   **Webcam Integration:** (Optional) A script is provided to test the model using a live video feed for real-time drowsiness alerts.

## 📦 Requirements
*   `torch`
*   `torchvision`
*   `opencv-python`
*   `numpy`
*   `matplotlib`
*   `scikit-learn`

## 📜 License
This project is open-source and available under the [MIT License](LICENSE).
