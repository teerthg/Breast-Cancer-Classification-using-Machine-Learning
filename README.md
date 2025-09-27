# Breast-Cancer-Classification-using-Machine-Learning
Project Overview This project applies **statistical and machine learning methods** to the **Breast Cancer Wisconsin (Original) Dataset** to classify tumors as **benign** or **malignant**.   The aim is to evaluate multiple models, compare their performance, and interpret feature importance in line with medical knowledge.  
As a **Master’s student in Statistics & Data Science at Uppsala University**, I conducted this project to strengthen my practical skills in:
- Exploratory Data Analysis (EDA)
- Statistical modeling
- Machine Learning algorithms
- Model evaluation & interpretation

---

##  Dataset
- **Source:** Breast Cancer Wisconsin (Original) dataset (UCI ML Repository)  
- **Samples:** 699  
- **Features:** 10 predictors (e.g., Clump Thickness, Cell Size, Bare Nuclei, Mitoses)  
- **Target:** Tumor class (Benign = 0, Malignant = 1)

---

##  Exploratory Data Analysis
- **Class distribution**: more benign cases than malignant.  
- **Feature distributions**: most predictors are right-skewed; higher values are associated with malignancy.  
- **Correlation heatmap**: strong correlation between *Cell Size* and *Cell Shape*.  

---

##  Models Implemented
The dataset was split into **80% training / 20% testing**, with features standardized.  

1. **k-Nearest Neighbors (k=5)** – distance-based, no feature importance.  
2. **Logistic Regression (max_iter=2000)** – interpretable baseline model.  
3. **Random Forest (200 trees)** – robust ensemble with feature importances.  
4. **MLP Classifier (16-8 hidden nodes)** – neural network capturing non-linear patterns.  

---

##  Results

| Model                | Accuracy | F1-Score | ROC AUC |
|-----------------------|----------|----------|---------|
| kNN (k=5)            | 95.6%    | 0.939    | 0.978   |
| Logistic Regression  | 96.3%    | 0.949    | 0.992   |
| Random Forest        | 96.3%    | 0.949    | 0.986   |
| MLP (16-8)           | 96.3%    | 0.949    | 0.993   |

- All models achieved ~96% accuracy.  
- **Random Forest** was selected as the best model → balances performance and interpretability.  
- Key predictive features: **Uniformity of Cell Size, Uniformity of Cell Shape, Bare Nuclei** – consistent with medical literature.  

---

##  Conclusion & Future Work
- Logistic Regression and Random Forest both performed strongly and offered interpretability.  
- MLP achieved the highest ROC AUC but lacks transparency, which is a limitation in medical use.  
- Future directions:
  - Apply cross-validation for more robust evaluation  
  - Tune hyperparameters with GridSearchCV  
  - Explore Explainable AI tools (e.g., SHAP, LIME) for neural networks  
  - Test models on larger, real-world clinical datasets  

---

##  Tech Stack
- **Language:** Python  
- **Libraries:** pandas, numpy, matplotlib, seaborn, scikit-learn  

Name-**Teerth Gupta**  
Master’s Student – Statistics & Data Science  
Uppsala University, Sweden  

