# **Retinopathy Classification using Deep Learning**

---

## **Project Overview**

This project focuses on building a deep learning-based system for the **classification of diabetic retinopathy** from retinal fundus images. The objective is to assist in early detection and grading of retinopathy severity using automated image analysis.

The system evaluates multiple deep learning architectures, including both **custom Convolutional Neural Networks (CNNs)** and **transfer learning models**, to identify the most effective approach for this medical imaging task.

---

## **Problem Statement**

Diabetic retinopathy is a leading cause of vision impairment. Early detection is critical for effective treatment. Manual diagnosis is time-consuming and requires expert knowledge.

This project aims to:

* Develop an automated classification system for retinal images
* Compare different deep learning architectures
* Identify the most suitable model for medical image classification
* Improve performance through systematic optimization and pipeline refinement

---

## **Dataset Description**

The dataset consists of labeled retinal fundus images categorized into three classes representing severity levels.

### **Class Distribution**

| Class | Samples |
| ----- | ------- |
| 1     | 649     |
| 2     | 455     |
| 3     | 307     |

### **Dataset Characteristics**

* Moderate class imbalance (~2:1 ratio)
* High intra-class similarity
* Subtle differences between severity levels
* Medical imaging complexity requiring fine feature extraction

---

## **Project Workflow**

The project follows a structured deep learning pipeline:

```
1. Data Loading and Preprocessing
2. Exploratory Data Analysis (EDA)
3. Data Augmentation
4. Model Development
5. Training and Validation
6. Model Comparison
7. Performance Evaluation
```

---

## **Key Features**

* Multiple deep learning models implemented
* Separate preprocessing pipelines for each model type
* Extensive data augmentation techniques
* Early stopping and learning rate scheduling
* Model performance comparison using multiple metrics
* Confusion matrix and classification report analysis

---

## **Technologies Used**

* Python
* TensorFlow / Keras
* NumPy, Pandas
* Matplotlib, Seaborn
* Scikit-learn

---

## **Model Architectures**

### **Custom Deep Learning Models**

* Light CNN
* CNN
* CNN Deep
* Mini ResNet
* Attention CNN

### **Transfer Learning Models**

* VGG16
* ResNet50
* MobileNetV2
* EfficientNetB0

---

## **Model Performance Summary**
```

| Model         | Best Validation Accuracy | Best Validation Loss |
| ------------- | ------------------------ | -------------------- |
| EfficientNet  | **0.8526**               | 0.0238               |
| VGG16         | 0.7365                   | 0.0637               |
| CNN           | 0.7252                   | 0.0592               |
| Light CNN     | 0.7082                   | 0.0644               |
| ResNet50      | 0.5297                   | 0.0664               |
| Attention CNN | 0.6260                   | 0.1024               |
| MobileNet     | 0.4975                   | 0.3627               |
| CNN Deep      | 0.3314                   | 0.1231               |
| Mini ResNet   | 0.3229                   | 0.1304               |
```

---

## **Results and Observations**

### **Top Performing Model: EfficientNet**

* Achieved highest validation accuracy (85.26%)
* Demonstrated strong generalization capability
* Effectively captured fine-grained retinal features

### **Strong Baseline Models**

* CNN and Light CNN showed stable and reliable performance
* VGG16 performed well due to balanced architecture and pretrained features

---

## **Key Insights**

### **What Worked Well**

* Proper preprocessing alignment significantly improved transfer learning performance
* Simpler CNN architectures performed competitively due to dataset size
* EfficientNet demonstrated superior feature extraction capability
* Data augmentation improved generalization

---

### **Challenges and Limitations**

* Moderate class imbalance affected minority class detection
* Some deep models (ResNet, CNN Deep) were not suitable for the dataset size
* MobileNet showed overfitting due to model capacity
* Class 3 detection remained relatively weaker due to fewer samples and complexity

---

## **Engineering Improvements**

The project underwent multiple refinements to achieve optimal performance:

* Corrected preprocessing mismatch across models
* Implemented separate data pipelines for each architecture
* Fine-tuned transfer learning models
* Optimized training strategies (learning rate, early stopping)
* Removed underperforming models
* Stabilized training and evaluation workflow

---

## **Evaluation Metrics**

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

---

## **How to Run**

### **1. Clone the Repository**

```
git clone <repository-link>
cd <project-folder>
```

---

### **2. Install Dependencies**

```
pip install -r requirements.txt
```

---

### **3. Run the Notebook**

Open the Jupyter/Colab notebook and execute all cells:

```
notebooks/training_notebook.ipynb
```

---

## **Future Enhancements**

* Increase dataset size for better generalization
* Apply class balancing techniques (focal loss, weighted training)
* Implement ensemble models
* Add Grad-CAM for explainability
* Deploy as a web-based diagnostic tool

---

## **Conclusion**

This project demonstrates that **well-optimized deep learning pipelines can achieve strong performance in medical image classification tasks**, even with moderately sized datasets.

EfficientNet proved to be the most effective model, while simpler CNN architectures provided reliable baselines. The results highlight the importance of **correct preprocessing, model selection, and iterative optimization**.

The system provides a solid foundation for further development toward real-world clinical applications.

---

## **Dataset**


```
Dataset Link: https://d3ilbtxij3aepc.cloudfront.net/projects/AI-Client-Projects/AIPRCL-003-Retinopathy/ratinopathy.zip
```

---

## **Author**

Thomas Mathew

---
