# **🐱🐶 Machine Learning-based Cat & Dog Image Classification**  

![Project Header Image](assets/cover.jpg)

[![Python](https://img.shields.io/badge/Python-3.7+-blue.svg)](https://www.python.org/downloads/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.0+-green.svg)](https://scikit-learn.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

### **📌 Project Overview**  
This project demonstrates my expertise in **machine learning (ML) and Computer Vision** by building a **binary image classifier** to distinguish between cats and dogs. Using traditional ML techniques (not deep learning), I preprocessed image data, trained multiple models, and optimized hyperparameters to achieve the best performance.  

**Key Skills Demonstrated:**  
- **Data Preprocessing** (resizing, normalization, PCA for dimensionality reduction)  
- **Model Training & Evaluation** (10+ ML algorithms compared)  
- **Hyperparameter Tuning** (GridSearchCV, RandomizedSearchCV)  
- **Performance Metrics** (accuracy, precision, recall, F1-score)  
- **Python Libraries** (Scikit-learn, OpenCV, NumPy, Pandas, Matplotlib)  

---

## **🔍 Key Insights & Results**  
### **1. Data Preprocessing Pipeline**  
- **Resized images** to 350x350 pixels for uniformity.  
- **Normalized pixel values** (0–255 → 0–1) to improve model convergence.  
- **Applied PCA** to reduce dimensionality from 122,500 features to 100 principal components.  

```python
# Preprocessing code snippet  
def load_and_preprocess_data(folder):  
    images = []  
    for filename in os.listdir(folder):  
        img = cv2.imread(os.path.join(folder, filename))  
        img = cv2.resize(img, (350, 350)) / 255.0  # Resize & normalize  
        images.append(img.flatten())  # Flatten to 1D vector  
    return np.array(images)  
```  

### **2. Model Training & Evaluation**  
Trained **10 ML models** and evaluated them on a validation set:  

| **Model**               | **Accuracy**|  
|-------------------------|-------------|  
| Support Vector Machine  | **59.7%**   |  
| K-Nearest Neighbors     | **57.2%**   |  
| Gradient Boosting       | **57.2%**   |  
| Logistic Regression     | **52.2%**   |  
| Random Forest           | **52.7%**   |  

**Top Model (SVM) Performance:**  
- **Precision:** 60% (cats), 57% (dogs)  
- **Recall:** 50% (cats), 66% (dogs)  
- **F1-Score:** 55% (cats), 61% (dogs)  

### **3. Hyperparameter Optimization**  
Used **RandomizedSearchCV** to fine-tune SVM:  
```python
best_params = {'C': 0.00103, 'gamma': 0.0033, 'kernel': 'linear'}  
best_svm = SVC(**best_params)  
best_svm.fit(X_train, y_train)  
```  
**Result:** Maintained ~52% accuracy post-tuning (highlighting limitations of traditional ML for image data).  

---

## **🛠️ Technical Approach**  
### **1. Data Loading & Preprocessing**  
- **Dataset:** 1,000 training images (400 cats, 401 dogs) + 100 test images.  
- **Train/Validation Split:** 80/20 stratified split to ensure class balance.  
- **Feature Scaling:** Standardized data using `StandardScaler`.  

### **2. Model Selection**  
Tested diverse algorithms:  
- **Linear Models:** Logistic Regression, SGD Classifier  
- **Ensemble Methods:** Random Forest, Gradient Boosting, AdaBoost  
- **Non-linear Models:** SVM, KNN, Naive Bayes  

### **3. Key Challenges & Solutions**  
- **High-Dimensional Data:** Used PCA to reduce features while preserving 95% variance.  
- **Class Imbalance:** Verified balanced classes (400 vs. 401 samples).  
- **Computational Limits:** Opted for RandomizedSearchCV over GridSearchCV for efficiency.  

---

## **📂 Project Structure**  
```  
cat-dog-classification/  
├── README.md                   # Project overview  
├── assets/                     # Visualizations  
│   ├── test/                   # Test images  
│   └── train/                  # Training images
├── src/                        # Jupyter Notebook & scripts  
│   ├── data_preprocessing.py  
│   ├── model_training.ipynb  
│   └── hyperparameter_tuning.py  
└── report.docx                 # Detailed analysis (docx)  
```  

---

## **🔍 How to Explore Further**  
### **For Employers & Recruiters:**  
This repository provides a **high-level summary** of the project. For full access to:  
✅ **Complete code** (Jupyter Notebook + scripts)  
✅ **Detailed report** with methodology & insights  
✅ **Interactive demo** (contact for Colab link)  

**Email me at:** [olayanjuolawale93@gmail.com](mailto:olayanjuolawale93@gmail.com)
<!-- **Subject:** *"Request: Cat/Dog Classifier Code Access – [Your Company]"*   -->

---

## **🚀 Why This Project Matters**  
- **Real-World ML Skills:** Demonstrates end-to-end ML workflow (preprocessing → tuning → evaluation).  
- **Comparative Analysis:** Highlights strengths/weaknesses of traditional ML vs. deep learning for image tasks.  
- **Scalability Insights:** PCA and efficient search methods (RandomizedSearchCV) optimize resource use.  

**Future Improvements:**  
- Implement **Convolutional Neural Networks (CNNs)** for higher accuracy.  
- Use **data augmentation** to expand the training dataset.  

---

## **📩 Let’s Connect!**  
Interested in discussing ML, computer vision, or potential roles?  
📧 **Email:** [olayanjuolawale93@gmail.com](mailto:olayanjuolawale93@gmail.com)  
🔗 **LinkedIn:** [linkedin.com/in/olayanju-ireoluwa-202488a7/](https://linkedin.com/in/olayanju-ireoluwa-202488a7/)  
💻 **GitHub:** [github.com/highclef93](https://github.com/highclef93) 

---

### **© License & Attribution**  
- **Dataset:** [Dogs vs. Cats | Kaggle](https://www.kaggle.com/c/dogs-vs-cats/data)  
- **Tools:** Scikit-learn, OpenCV, Pandas, NumPy, Colab 
- **Analysis & Code:** © Olayanju Ireoluwa – Shared for portfolio purposes only.  

--- 

✨ **Thanks for reviewing my work!** ✨  
*For full code access or collaboration opportunities, reach out directly.*