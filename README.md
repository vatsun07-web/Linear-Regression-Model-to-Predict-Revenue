# 📈 Ecommerce Revenue Optimization: Strategic Predictive Modeling

## 📝 Project Overview
This project tackles a real-world ecommerce resource allocation question:

> **Should the company invest more in improving the Website or the Mobile App?**

Using a dataset of **500 unique customer profiles**, I built and evaluated regression models to identify the strongest revenue drivers and deliver **data-backed product strategy recommendations for 2026**.

---

## 🎯 Business Objectives
- **Identify Revenue Drivers**  
  Determine which customer behaviors most influence `Yearly Amount Spent`

- **Guide Resource Allocation**  
  Decide whether engineering effort should prioritize the Website or the Mobile App

- **Quantify Business Impact**  
  Translate customer engagement and loyalty into **clear dollar values**

---

## 🛠️ Technical Stack & Methodology

### Tools & Libraries
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn

### Approach
- **Exploratory Data Analysis (EDA)**  
  Analyzed feature relationships, correlations, and linear trends to understand revenue behavior

- **Feature Engineering Pipeline**  
  Built a `scikit-learn Pipeline` with:
  - `StandardScaler`
  - `PolynomialFeatures`  
  to ensure consistent preprocessing and prevent data leakage

- **Model Selection & Optimization**  
  Conducted a **model tournament** using `GridSearchCV` with 5-fold cross-validation to compare:
  - Ordinary Least Squares (Linear Regression)
  - Ridge Regression (L2 regularization)
  - Lasso Regression (L1 regularization)

---

## 📊 Model Performance & Results

### Model Comparison
| Model | R² Score | RMSE | Decision |
|------|---------|------|---------|
| **Linear Regression** | **0.8604** | **27.55** | ✅ Selected |
| Ridge Regression (L2) | 0.8510 | 28.46 | ❌ Rejected |
| Lasso Regression (L1) | 0.8494 | 28.61 | ❌ Rejected |

**Key takeaway:**  
Regularization did not improve generalization — the simpler linear model performed best.

---

## 🔍 Key Business Insights

### 📱 Mobile App vs Website
- **Mobile App:** ≈ **$38.59 revenue per minute**
- **Website:** ≈ **$0.79 revenue per minute**

➡️ The Mobile App is **~50× more effective** at driving customer spend.

---

### 🔁 Customer Loyalty Matters Most
- **Length of Membership** is the strongest predictor of revenue
- Each additional year of membership adds approximately **$62.56** in annual spending

➡️ Retention outperforms short-term engagement tactics.

---

## 🧪 Bias–Variance Tradeoff & Overfitting Analysis
Polynomial regression models with degrees **1 through 10** were evaluated:

- Low-degree models (linear to degree 4) generalize well
- Higher-degree models show **overfitting**:
  - Training error decreases
  - Test error increases sharply

**Conclusion:**  
More complexity ≠ better performance.

---

## 📈 Strategic Recommendations
- **Adopt a Mobile-First Strategy**  
  Shift development resources from Website optimization to Mobile App enhancements

- **Invest in Retention Programs**  
  Increase `Length of Membership` through loyalty incentives and personalized experiences

- **Next Step: Churn Prediction**  
  Build a **classification model** to identify high-risk, high-value customers before they churn

---

## 👤 Author
**Seiha Vat**

## 📅 Date
**February 9, 2026**
