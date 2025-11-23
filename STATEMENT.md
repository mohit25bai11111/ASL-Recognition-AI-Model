# 📄 Project Statement

## **ASL-RECOGNITION AI MODEL**
**Real-Time American Sign Language (ASL) Recognition and Sentence Construction System**

---

## **1. The Problem Statement**
Communication is a fundamental human need. However, for the millions of people in the Deaf and Hard-of-Hearing (DHH) community, communicating with the hearing majority is a daily challenge. 

* **The Barrier:** Most non-signers do not understand American Sign Language (ASL).
* **Current Solutions:** Human interpreters are expensive and not always available. Existing automated apps often lack real-time capabilities or require expensive hardware (like sensory gloves).
* **The Technical Gap:** Many computer vision models suffer from "Ghosting" (detecting gestures when no hand is present) or struggle to distinguish between similar static signs (e.g., 'M', 'N', and 'S').

There is a critical need for a **low-cost, real-time, and highly accurate** translation tool that works on standard consumer laptops.

---

## **2. Proposed Solution**
We propose an AI-powered desktop application that translates ASL alphabets into text in real-time using a standard webcam. 

Unlike basic classification models, our system will implement **Transfer Learning** using the **MobileNetV2** architecture. This ensures the model is lightweight enough to run without a dedicated GPU while maintaining professional-grade accuracy (>95%).

### **Key Innovations:**
1.  **Transfer Learning Backbone:** Leveraging MobileNetV2 (pre-trained on ImageNet) to extract complex visual features (edges, textures, shapes) efficiently.
2.  **Intelligent Sentence Builder:** A logic layer that allows users to construct full sentences by holding a sign for a specific duration (1.5 seconds), rather than just flashing random letters.
3.  **False Positive Rejection:** Implementation of a high-confidence threshold (95%) to prevent the system from predicting random letters on empty backgrounds.

---

## **3. Methodology & Tech Stack**

### **3.1 Dataset**
* **Source:** Kaggle ASL Alphabet Dataset.
* **Volume:** 87,000 images across 29 classes (A-Z, Space, Delete, Nothing).
* **Preprocessing:** Image augmentation (rotation, zoom) and normalization to `[-1, 1]` range.

### **3.2 Architecture**
* **Input Layer:** 224x224 RGB Images.
* **Feature Extractor:** MobileNetV2 (Frozen weights).
* **Classifier Head:** Global Average Pooling -> Dense (128) -> Dropout (0.2) -> Softmax (29 classes).

### **3.3 Tools**
* **Programming Language:** Python 3.x
* **Deep Learning Framework:** TensorFlow / Keras
* **Computer Vision:** OpenCV (cv2)
* **Data Processing:** NumPy, Pandas

---

## **4. Expected Outcomes**
1.  A functional **Python application** that opens the webcam and detects hand signs with low latency.
2.  Classification **accuracy of 90% or higher** on validation data.
3.  A robust user interface that displays the **live prediction**, **confidence score**, and **constructed sentence**.
4.  Ability to handle special command gestures like **'Space'** (to separate words) and **'Del'** (to correct mistakes).

---

## **5. Social Impact**
This project aims to democratize access to communication technology. By utilizing standard webcams and open-source software, this tool can be deployed in:
* **Educational Institutions:** To help students learn ASL interactively.
* **Public Service Desks:** To assist staff in understanding basic requests from deaf individuals.
* **Personal Use:** As a translation assistant for daily interactions.

---

**Submitted By:** [MOHIT PILLAI]  
[**25BAI11111**]
