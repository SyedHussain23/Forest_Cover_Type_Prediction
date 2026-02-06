# 🌲 Forest Cover Type Prediction

This project focuses on predicting the **forest cover type** using cartographic and environmental features.
It demonstrates a complete **machine learning workflow**, including data loading, exploratory data analysis (EDA), preprocessing, model training, evaluation, and prediction.

The goal is to classify forest land into one of **7 cover types** based on geographic and soil characteristics.

---

## 📌 Project Overview

- **Problem Type:** Multi-class classification  
- **Domain:** Environmental / Geospatial Data Science  
- **Target Variable:** `Cover_Type` (7 classes)  
- **Model Used:** Logistic Regression (baseline)  
- **Framework:** Scikit-learn  

---

## 📊 Dataset

- **Source:** Forest Cover Type Dataset  
- **File Used:** `train.csv`  
- **Total Records:** 15,120  
- **Total Features:** 54  
- **Target Classes:** 7 (perfectly balanced)

### Feature Categories
- **Numerical:** Elevation, Aspect, Slope, Horizontal/Vertical Distances, Hillshade features  
- **Binary (One-Hot Encoded):**
  - Wilderness Area (4 types)
  - Soil Type (40 types)

✔ No missing values  
✔ All features are integer-based  

---

## 🔍 Exploratory Data Analysis (EDA)

- Checked dataset shape and data types
- Verified absence of missing values
- Analyzed descriptive statistics
- Examined class distribution of `Cover_Type`
- Confirmed **balanced target classes** (2,160 samples per class)

---

## 🔧 Data Preprocessing

- Dropped non-informative column: `Id`
- Separated features (`X`) and target (`y`)
- Categorical features were **already one-hot encoded**
- Dataset split into:
  - **Training:** 80%
  - **Testing:** 20%

---

## 🧠 Modeling Approach

### Model Used: Logistic Regression

- Chosen as a **baseline multi-class classifier**
- Easy to interpret and suitable for beginners
- Trained using scikit-learn’s `LogisticRegression`

⚠️ A **ConvergenceWarning** was observed, indicating that feature scaling or higher iterations could further improve performance.

---

## 📈 Model Evaluation

### Training Performance
- **Accuracy:** ~47.9%
- **Precision:** ~46.2%
- **Recall:** ~47.9%
- **F1-score:** ~46.7%

### Test Performance
- **Accuracy:** ~60.98%
- **Precision:** ~60.07%
- **Recall:** ~60.98%
- **F1-score:** ~60.15%

### Metrics Used
- Accuracy
- Precision (weighted)
- Recall (weighted)
- F1-score (weighted)

---

## 🔮 Insights & Observations

- Logistic Regression provides **moderate performance** on this dataset
- Model did not fully converge due to:
  - Lack of feature scaling
  - Limited number of iterations
- Performance suggests that **non-linear models** may be better suited for this task

---

## 🚀 How to Run

1. Clone the repository:
```bash
git clone https://github.com/SyedHussain23/Forest_Cover_Type_Prediction.git
cd Forest_Cover_Type_Prediction
pip install pandas numpy scikit-learn
jupyter notebook Forest_Cover_Type_Prediction.ipynb
```

---

## 🔮 Future Improvements
Apply feature scaling using StandardScaler
Increase max_iter to resolve convergence warnings
Try tree-based models (Random Forest, XGBoost)
Perform hyperparameter tuning
Analyze feature importance
Add confusion matrix visualization

---

👨‍💻 Author

Syed Hussain Abdul Hakeem

LinkedIn: https://www.linkedin.com/in/syed-hussain-abdul-hakeem
GitHub: https://github.com/SyedHussain23

---

📄 License

This project is open source and available under the MIT License.

---

⭐ Show Your Support

If you found this project useful, consider giving it a ⭐.
