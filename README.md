# 🛩️ Aerial Object Detection using YOLOv8

An AI-powered **aerial object detection system** built using **YOLOv8** to identify and localize objects such as **birds and drones** from aerial images. The project uses a custom dataset prepared with **Roboflow** and trains a deep-learning object detection model using Python.

## 📌 Project Overview

Aerial imagery can contain objects that are small, distant, or difficult to identify manually. This project applies **computer vision and deep learning** to automatically detect objects in aerial images.

The system:

* Detects **Birds and Drones** in aerial images
* Uses **YOLOv8** for real-time object detection
* Uses a custom dataset prepared and annotated using **Roboflow**
* Performs model training and validation
* Generates bounding boxes around detected objects
* Can be used for aerial surveillance and monitoring applications

## 🎯 Objectives

* Develop an automated aerial object detection system.
* Detect multiple object classes from aerial imagery.
* Apply YOLOv8 for accurate and efficient object detection.
* Train a custom model using an annotated aerial dataset.
* Visualize predictions using bounding boxes and confidence scores.

## 🗂️ Dataset

The dataset was prepared and annotated using **Roboflow**.

**Dataset size:** 6,812 images

**Classes:**

* 🐦 Bird
* 🚁 Drone

The dataset was divided into training, validation, and testing sets before training the YOLOv8 model.

## 🧠 Model

The project uses **YOLOv8 (You Only Look Once)**, a deep-learning based object detection architecture designed for efficient object localization and classification.

YOLOv8 predicts:

* **Class label**
* **Bounding box coordinates**
* **Confidence score**

For example:

```text
Input Image
     ↓
YOLOv8 Model
     ↓
Feature Extraction
     ↓
Object Detection
     ↓
Bounding Boxes + Class + Confidence
```

## 🛠️ Technologies Used

| Technology       | Purpose                          |
| ---------------- | -------------------------------- |
| Python           | Programming language             |
| YOLOv8           | Object detection model           |
| Ultralytics      | YOLOv8 implementation            |
| Roboflow         | Dataset preparation & annotation |
| OpenCV           | Image processing                 |
| Google Colab     | Model training                   |
| Jupyter Notebook | Development & experimentation    |

## ⚙️ Project Workflow

1. Collect aerial images.
2. Annotate images using Roboflow.
3. Prepare the dataset for YOLOv8.
4. Split the dataset into training, validation, and testing sets.
5. Configure the YOLOv8 model.
6. Train the model on the aerial dataset.
7. Validate the trained model.
8. Test the model on unseen images.
9. Generate bounding boxes and confidence scores.
10. Visualize the detection results.

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/shreya3090/Aerial-Object-Detection.git
cd Aerial-Object-Detection
```

### 2. Install Dependencies

```bash
pip install ultralytics
pip install opencv-python
```

If you are using Google Colab, dependencies can be installed directly inside the notebook.

### 3. Run the Notebook

Open:

```text
Aerial Object Detection (1).ipynb
```

The notebook contains the model training and object detection workflow.

## 🔍 Detection Example

After training, the model can be used to detect objects in an image:

```python
from ultralytics import YOLO

model = YOLO("best.pt")

results = model("test_image.jpg")

for result in results:
    result.show()
```

The output contains detected objects with their corresponding **bounding boxes, class labels, and confidence scores**.

## 📊 Results

The trained YOLOv8 model is capable of identifying the target aerial objects and localizing them using bounding boxes.

### Detected Classes

* **Bird**
* **Drone**

The trained model weights can be saved as:

```text
best.pt
```

## 💡 Applications

This project can be extended to applications such as:

* 🛡️ Aerial surveillance
* 🚨 Drone detection
* 🐦 Wildlife monitoring
* ✈️ Airport security
* 🌳 Environmental monitoring
* 🔎 Search and reconnaissance
* 📹 Real-time aerial video analysis

## 🔮 Future Scope

The project can be further improved by:

* Supporting additional aerial object classes
* Training on larger and more diverse datasets
* Improving detection of small and distant objects
* Implementing real-time video detection
* Deploying the model as a web application
* Optimizing the model for edge devices
* Adding object tracking using **DeepSORT/ByteTrack**
* Integrating the system with live drone or CCTV feeds

## 📁 Repository Structure

```text
Aerial-Object-Detection/
│
├── Aerial Object Detection (1).ipynb
└── README.md
```

## 👩‍💻 Author

**Shreya Sachan**

B.Tech CSE – Cyber Security

GitHub: [shreya3090](https://github.com/shreya3090)

---

⭐ If you found this project useful, consider giving the repository a star!
