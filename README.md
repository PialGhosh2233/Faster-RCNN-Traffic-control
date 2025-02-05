# 🚗 Traffic Object Detection using Faster R-CNN  

## 📌 Objective  

This report demonstrates an **object detection model** that has been trained using the **dataset I had made**. **Faster R-CNN** was used as an object detection model. It was trained on an **annotated traffic dataset** with objects such as:  

- **Car**  
- **Motorcycle**  
- **Leguna**  
- **Pedestrian**  
- **Bus**  
- **Truck**  
- **CNG**  
- **Rickshaw**  

The goal is to train an **object detection model** to detect the mentioned objects. This model is highly suitable for building **traffic monitoring systems** and **autonomous driving systems**.  

## 🏗 Model  

**Faster R-CNN** is an object detection model. It is a **state-of-the-art object detection architecture** of the **R-CNN family**. Faster R-CNN consists of two main components:  

### 1️⃣ **Region Proposal Network (RPN)**  

RPN is responsible for **generating possible regions of interest** in images that may contain objects. It uses an **attention mechanism** to instruct the subsequent **Fast R-CNN detector** where to look for objects in the image.  

Key components of **RPN**:  

- **Anchor Boxes**: Used to generate region proposals in the Faster R-CNN model.  
- **Sliding Window Approach**: RPN operates as a **sliding window** over the feature map using a **3×3 convolutional layer**.  
- **Objectness Score**: Represents the probability that a given anchor box contains an object rather than background.  
- **IoU (Intersection over Union)**: Measures the **degree of overlap** between two bounding boxes.  
- **Non-Maximum Suppression (NMS)**: Removes redundant region proposals and keeps the most accurate ones.  

### 2️⃣ **Fast R-CNN Detector**  

- **Region of Interest (RoI) Pooling**: Converts **variable-sized** region proposals into **fixed-size** feature maps.  
- **Feature Extraction**: Extracts meaningful features using the CNN backbone.  
- **Fully Connected Layers**: Performs object classification and bounding box regression.  
- **Object Classification**: Predicts the class probabilities for each region proposal.  
- **Bounding Box Regression**: Adjusts bounding box positions to align with actual object boundaries.  
- **Softmax Layer**: Predicts object categories (N classes + background).  
- **Bounding Box Regression Layer**: Refines the bounding box locations.  

## 🛠 Methodology  

### **📂 Dataset Preparation**  

- Extracted object **bounding boxes** with labels.  
- Divided the dataset into:  
  - **Training (80%)**  
  - **Validation (10%)**  
  - **Testing (10%)**  

### **⚙️ Hyperparameters**  

- **Optimizer**: AdamW  
- **Learning Rate**: 0.0001  
- **Batch Size**: 4  
- **Epochs**: 30  

## 📊 Evaluation Metrics & Results  

### **📌 Metrics**  

- **mAP (Mean Average Precision)**: Measures the accuracy of the model in detecting and classifying objects. It combines **precision** and **recall** for a comprehensive evaluation.  

### **📈 Results**  

- The model achieved **66.08% mAP**, which is **good for object detection in traffic images**.  
- **Training Loss**: **0.0783**  

---

This repository provides a **detailed implementation** of Faster R-CNN for traffic object detection. 🚀 Feel free to explore and contribute!  
