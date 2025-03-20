# Predicting Heart Attack Risk: Machine Learning Analysis

## ** Data Source**
https://www.kaggle.com/datasets/iamsouravbanerjee/heart-attack-prediction-dataset/data

## **Background**
Heart attack prediction is a critical component of preventative healthcare, as cardiovascular diseases remain a leading cause of mortality worldwide. This analysis leverages a dataset with known heart attack risk values, using both unsupervised and supervised machine learning methods to identify patterns and predict risks effectively.

### **Methods Used**
- **Unsupervised Learning**:
  - K-Means Clustering
  - Principal Component Analysis (PCA)
- **Supervised Learning**:
  - Logistic Regression
  - Random Forest

---

## **Goals**
1. Build a predictive framework to assess heart attack risk using machine learning.
2. Compare and contrast unsupervised and supervised learning methods.
3. Identify key lifestyle, biological, and environmental factors that contribute to heart attack risk.
4. Optimize models for balanced accuracy, precision, and recall.

---

## **Key Findings**

### **K-Means (Clustering)**
- Unsupervised learning (K-Means) is ineffective for heart attack risk assessment because clusters do not align with actual risk levels.
- Clustering is not suitable for predictive insights; classification models are more appropriate.
- **Future Work**: Explore advanced techniques like Neural Networks or XGBoost for improved accuracy.

---

### **Principal Component Analysis (PCA)**
- Around 20 principal components are needed to retain 95% of the variance in the data.
- Using only 2-3 components leads to significant information loss.
- **PC1 (First Component)**:
  - Highly influenced by lifestyle factors such as smoking, age, and sex.
  - Cholesterol has little impact on PC1 but contributes significantly to other components.
- Adding a third component improves data separation but still shows some overlap between high-risk (🔴) and low-risk (🟣) individuals.
- Outliers reveal extreme-risk cases that warrant further investigation.

---

### **Logistic Regression**
- Risk factors were graphically represented, splitting participants into those with and without specific risk factors.
- The model showed limited ability to understand the dataset, with variability observed across multiple iterations.
- Logistic Regression struggles to effectively capture complex relationships between features and heart attack risk.

---

### **Random Forest**
- **Target Class Imbalance**: The "No Risk" class heavily outweighs the "At Risk" class.
- **Initial Performance**:
  - Accuracy: ~64%, primarily predicted the majority class (no risk).
- **After SMOTE (Balancing the Dataset)**:
  - Accuracy dropped to ~55%, but minority class recall improved.
  - Lower thresholds (e.g., 0.10) achieved perfect recall but had low precision, leading to many false positives.
  - Higher thresholds improved precision but drastically reduced recall.
- **Optimal Threshold**:
  - F1-Score was highest at lower thresholds, favoring a recall-focused approach to ensure high-risk cases are not missed.

---

## **Purpose**
1. Provide actionable insights to aid in heart attack risk prediction.
2. Compare machine learning approaches to identify the most effective methods.
3. Highlight key predictors of risk to improve early detection and preventative measures.

---

## **Future Work**
- Explore additional supervised methods like Neural Networks or XGBoost for improved performance.
- Further refine thresholds to balance precision and recall effectively.
- Investigate the role of outliers and extreme-risk cases in greater depth.
- Use feature importance analysis to better understand high-impact predictors like lifestyle and blood pressure.

---

This analysis highlights the challenges and opportunities in predicting heart attack risk, emphasizing the importance of selecting suitable methods and addressing imbalances in the dataset.
