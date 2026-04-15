# 🛒 Customer Segmentation using Clustering

## 📌 Overview

This project performs customer segmentation using clustering techniques on retail data. It helps identify different groups of customers based on their behavior, spending patterns, and demographics.

---

## 📊 Dataset

* Total records: 2240
* Features: 22 (raw) → 18 (after preprocessing)

### Key Attributes:

* Income, Age, Recency
* Purchase behavior (web, store, catalog)
* Spending on products
* Education & Living status

---

## ⚙️ Tech Stack

* Python
* Pandas, NumPy
* Matplotlib, Seaborn
* Scikit-learn

---

## 🔄 Workflow

### 1. Data Preprocessing

* Filled missing values (Income → median)
* Converted date column to datetime
* Removed irrelevant columns

### 2. Feature Engineering

* Created:

  * `Age`
  * `Customer_Tenure_Days`
  * `Total_Spending`
  * `Total_Children`
* Simplified categories:

  * Education → Undergraduate / Graduate / Postgraduate
  * Marital Status → Alone / Partner

### 3. Outlier Removal

* Removed extreme values in:

  * Age (> 90)
  * Income (> 600,000)

### 4. Encoding & Scaling

* One-Hot Encoding for categorical variables
* StandardScaler for normalization

---

## 📉 Dimensionality Reduction

* Applied PCA (3 components)
* Explained variance:

  * PC1: ~23%
  * PC2: ~11%
  * PC3: ~10%

---

## 📊 Finding Optimal Clusters

* Elbow Method → **Optimal K = 4**
* Silhouette Score used for validation

---

## 🤖 Clustering Models

* K-Means Clustering
* Agglomerative Clustering

---

## 📈 Results

### 🔹 Total Clusters: 4

### 🔹 Cluster Insights:

* **Cluster 0**

  * Medium income
  * Moderate spending
  * Mostly living with partner

* **Cluster 1**

  * High income
  * High spending
  * Active buyers

* **Cluster 2**

  * Low income
  * Low spending
  * Mostly living alone

* **Cluster 3**

  * High income
  * High response rate
  * Premium customers

---

## 📊 Key Insights

* Income strongly influences spending behavior
* Customers with higher income tend to spend more
* Living status affects purchasing patterns
* High-value customers can be targeted for marketing

---

## ▶️ How to Run

```bash
git clone <repo-link>
cd customer-segmentation
pip install -r requirements.txt
python main.py
```

---

## 📌 Future Improvements

* Use advanced clustering (DBSCAN, Hierarchical tuning)
* Deploy dashboard (Streamlit / Power BI)
* Add real-time customer segmentation

---

## 👤 Author

Gurbachan Singh
