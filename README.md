# ⚽ FIFA20  
## FIFA 20 Player Performance Analysis & Prediction  
**by:**  
- Abisha C  

---

## 📌 Project Overview
This project presents an end-to-end data analysis and machine learning solution built on the **FIFA 20 Career Mode dataset**. The objective is to explore football player characteristics, analyze performance trends, cluster players based on skill attributes, and build predictive models to classify player performance levels.

The project combines **exploratory data analysis, unsupervised learning, supervised machine learning, and model explainability** to deliver actionable insights for football analytics.

---

## 🎯 Problem Statement
The main goals of this project are:

1. Prepare a comprehensive data analysis report on FIFA 20 player data  
2. Cluster football players based on their skill attributes  
3. Answer key analytical questions:
   - Which countries produce the most professional football players?
   - At what age does a football player stop improving?
   - Which offensive position earns the highest salary: Striker, Right Winger, or Left Winger?
4. Build and compare machine learning models to classify player performance  
5. Select the best-performing model for production use  

---

## 📂 Dataset Description
- **Dataset Name:** `players_20.csv`
- **Source:** FIFA 20 Career Mode (EA Sports)
- **Total Records:** 18,278 players
- **Total Features:** 61 attributes

### Key Attribute Categories:
- **Demographics:** Age, nationality, height, weight  
- **Skill Ratings:** Pace, shooting, passing, dribbling, defending, physicality  
- **Mental Attributes:** Reactions, vision, composure, positioning  
- **Positional Skills:** ST, RW, LW, CM, CB, etc.  
- **Financial Data:** Wages, player value (used only for analysis)  

---

## 🔍 Key Analysis Performed

### 📊 Exploratory Data Analysis (EDA)
- Age, height, weight distributions
- Overall vs potential rating trends
- Skill vs performance relationships
- Positional and nationality-based analysis

### 🌍 Country-wise Player Analysis
- Ranked top 10 countries producing the most players
- Identified football powerhouses like England, Germany, Spain, France, and Brazil

### 💰 Salary Analysis
- Compared wages of Strikers (ST), Right Wingers (RW), and Left Wingers (LW)
- Found that **strikers generally earn the highest wages**

---

## 🔀 Player Clustering (Unsupervised Learning)
- Used **KMeans clustering**
- Features: pace, shooting, passing, dribbling, defending, physicality
- Optimal clusters identified using the **Elbow Method**
- Players grouped into **4 distinct skill-based archetypes**
- Clustering is independent of performance labels (valid and intentional)

---

## 🧠 Machine Learning Pipeline

### 🎯 Target Variable
Player performance was categorized based on overall rating:

| Encoded Label | Performance Level |
|--------------|------------------|
| 0 | Low |
| 1 | Medium |
| 2 | High |

---

### ⚙️ Preprocessing Techniques
- Missing value imputation (median / most frequent)
- Outlier handling using IQR method
- Feature scaling (for Logistic Regression only)
- Class imbalance correction using **SMOTE**
- Multicollinearity analysis using VIF

---

### 🤖 Models Trained & Compared
- Logistic Regression  
- Random Forest  
- XGBoost  
- LightGBM  

### 🏆 Best Model Selected
**LightGBM** was chosen as the final production model due to:
- Highest weighted F1-score
- Robustness to class imbalance
- Ability to handle multicollinearity
- Faster training time

---

## 📈 Model Performance
- **Accuracy:** ~95.3%  
- **Weighted F1-score:** ~0.95  
- **ROC–AUC:** ~0.99 (macro & weighted)

Advanced evaluation included:
- Confusion Matrix
- Multiclass ROC–AUC curves
- Threshold tuning
- Probability calibration curves

---

## 🔎 Model Explainability
To ensure transparency and trust:
- **Permutation Feature Importance**
- **SHAP (SHapley Additive Explanations)**

Key influential features identified:
- Defending
- Reactions
- Ball Control
- Shooting
- Physical attributes

---

## ⚠️ Challenges Faced
- Severe class imbalance (High-performance players ~3%)
- High multicollinearity among skill attributes
- Large number of missing values in goalkeeping features
- Presence of outliers in ratings and age
- Need for explainability in complex models

Each challenge was addressed using appropriate statistical and machine learning techniques.

---

## ✅ Final Conclusion
This project successfully delivers a robust football analytics solution by integrating exploratory analysis, clustering, predictive modeling, and explainability. The selected LightGBM model achieves high accuracy and reliability while maintaining transparency through SHAP-based explanations.

The solution is **practically applicable** for:
- Player scouting
- Performance benchmarking
- Salary analysis
- Strategic squad planning
- Sports analytics research

---


