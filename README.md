

# **Credit Card Fraud Detection**  

## **Project Overview**  
This project implements a **Credit Card Fraud Detection System** using **Machine Learning models**. The dataset used is highly imbalanced, containing a small percentage of fraudulent transactions. The goal is to build a model that accurately identifies fraudulent transactions while minimizing false positives and false negatives.  

## **Dataset**  
- The dataset consists of anonymized features obtained from credit card transactions.  
- The target variable is **Class**, where:  
  - `0` represents **genuine transactions**  
  - `1` represents **fraudulent transactions**  
- The dataset is highly imbalanced, with fraud cases forming a very small percentage of total transactions.  

## **Technologies and Libraries Used**  
- **Python**  
- **Pandas, NumPy** (Data Preprocessing)  
- **Matplotlib, Seaborn** (Data Visualization)  
- **Scikit-Learn** (Machine Learning Models)  

## **Project Workflow**  

### **1. Data Preprocessing**  
- Checked for missing values and handled them appropriately.  
- Normalized the `Amount` column using `StandardScaler` to improve model performance.  
- Used **stratified train-test split** (70:30 ratio) to maintain the class distribution.  

### **2. Model Training**  
- **Decision Tree Classifier**  
- **Random Forest Classifier**  

### **3. Model Evaluation Metrics**  
- **Accuracy Score**  
- **Precision, Recall, and F1-score**  
- **Confusion Matrix Analysis**  

### **4. Results & Observations**  
| Metric          | Decision Tree | Random Forest |  
|----------------|--------------|--------------|  
| **Accuracy**   | 99.83%  | 99.89%  |  
| **Precision (Fraud Class - 1.0)** | 91%  | 100%  |  
| **Recall (Fraud Class - 1.0)** | 67%  | 73%  |  
| **F1-Score (Fraud Class - 1.0)** | 77%  | 85%  |  

- **Random Forest performed better than Decision Tree**, achieving **higher recall (73%)** and **F1-score (85%)** for fraud detection.  
- Accuracy alone was **not a reliable metric** due to class imbalance.  

## **Confusion Matrix Analysis**  
- **False Negatives (FN) are critical** in fraud detection since missing a fraud case can lead to financial loss.  
- **Random Forest had a lower FN count than Decision Tree**, making it a better choice for fraud detection.  

## **Future Improvements**  
- Implement **SMOTE (Synthetic Minority Oversampling Technique)** to balance the dataset.  
- Use **hyperparameter tuning (GridSearchCV, RandomizedSearchCV)** to improve model performance.  
- Experiment with **Neural Networks (Deep Learning)** for better fraud detection.  

## **How to Run the Project**  

### **1. Clone the Repository**  
```bash
git clone https://github.com/yourusername/credit-card-fraud-detection.git
cd credit-card-fraud-detection
```

### **2. Install Dependencies**  
```bash
pip install -r requirements.txt
```

### **3. Run the Jupyter Notebook**  
Open and execute the notebook step by step:  
```bash
jupyter notebook Credit_Card_Fraud_Detection.ipynb
```

## **Conclusion**  
This project successfully implemented **fraud detection models** using **Decision Tree and Random Forest**. The **Random Forest model outperformed Decision Tree** in recall and F1-score, making it a better fraud detection model. Further improvements, such as **oversampling techniques and deep learning**, can enhance fraud detection performance.  

---
