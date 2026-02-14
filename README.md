# 🧠 RetailX Customer Segmentation – KMeans Clustering

## 📌 Project Overview
This project applies **unsupervised machine learning (K-Means clustering)** to segment customers based on behavioral features.

The goal is to identify natural customer groups and translate data-driven insights into actionable marketing strategies.

Developed as part of the **MSc Data Science – Marketing Analytics** module.

---

## 🎯 Objective
To identify distinct customer segments using behavioral data and design targeted marketing strategies that enhance:

- Customer engagement  
- Retention  
- Revenue growth  

---

## 📊 Dataset Features Used for Clustering

Behavioral variables only (standardized before clustering):

- `avg_order_size`
- `avg_order_freq`
- `crossbuy`
- `multichannel`
- `per_sale`
- `tenure`
- `return_rate`
- `loyalty_card`
- `avg_mktg_cnt`

Demographic features were excluded to ensure segmentation was behavior-driven.

---

## ⚙️ Methodology

### 1️⃣ Data Preprocessing
- Missing value handling
- Feature scaling using `StandardScaler`
- Exploratory Data Analysis (EDA)

### 2️⃣ Clustering
- Algorithm: `KMeans`
- Tested values: k = 2, 3, 4
- Evaluation techniques:
  - Elbow Method
  - Silhouette Score
  - Calinski–Harabasz Index
  - PCA visualization

### 3️⃣ Optimal Model Selection
**k = 3** was selected because it provided:
- Strong statistical separation
- Behavioral diversity
- Strategic interpretability

---

## 📈 Model Validation

To validate cluster separability, supervised models were trained to predict segment labels.

| Model | Accuracy | Macro F1 |
|--------|----------|----------|
| Logistic Regression | 98.7% | 98.5% |
| Decision Tree | 93.5% | 91.8% |
| Random Forest | 95.0% | 93.2% |

High accuracy confirms well-defined clusters.

---

## 👥 Segment Profiles

### 🔹 Segment 0 – Loyalty-Driven Explorers
- High `crossbuy`
- Active `loyalty_card`
- Moderate `order_freq`
- Lower `order_size`

**Strategy:** Gamified rewards, loyalty incentives, personalized bundles.

---

### 🔹 Segment 1 – Multichannel Deal Seekers
- High `multichannel`
- High `per_sale`
- Long `tenure`
- Low `return_rate`

**Strategy:** Flash sales, cross-channel promotions, exclusive offers.

---

### 🔹 Segment 2 – High-Spend Occasionalists
- High `order_size`
- High `return_rate`
- Low `tenure`
- Lower `order_freq`

**Strategy:** Retention campaigns, satisfaction guarantees, post-purchase engagement.

---

## 🔍 Feature Importance (Random Forest)

Top drivers of segmentation:

1. `per_sale`
2. `tenure`
3. `crossbuy`
4. `avg_order_freq`
5. `multichannel`

Behavioral features dominate cluster formation.

---

## 🧪 Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- PCA
- KMeans
- Random Forest
- Logistic Regression

---

## 📁 Repository Structure

RetailX-Customer-Segmentation/
│
├── data/
├── notebooks/
│ └── segmentation_analysis.ipynb
├── report/
│ └── RetailX_Report.pdf
├── README.md
└── requirements.txt


---

## 🚀 Business Impact

This segmentation framework enables:

- Personalized marketing campaigns
- Optimized promotional strategies
- Improved customer retention
- Increased revenue per customer

---

## 👤 Author

**Khaled Walid**  
MSc Data Science  
University of Europe for Applied Sciences
