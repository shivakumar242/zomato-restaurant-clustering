# 🍽️ Zomato Restaurant Clustering

## 📌 Project Overview

Ratings alone do not fully represent restaurant performance. Two restaurants with the same rating can differ significantly in customer sentiment, pricing strategy, and review behavior.

This project applies **unsupervised machine learning (clustering)** combined with **NLP-based sentiment analysis** to segment Zomato restaurants into meaningful groups based on customer experience and pricing characteristics.

---

## 🎯 Problem Statement

* Are ratings sufficient to evaluate restaurant performance?
* Does higher cost guarantee better customer satisfaction?
* Can restaurants be grouped based on sentiment, reviews, and pricing?

Since no target variable exists, this problem is approached using **unsupervised learning**.

---

## 🗂️ Datasets Used

### 1️⃣ Restaurant Metadata

* Restaurant name
* Cost
* Cuisine information

### 2️⃣ Customer Reviews

* Review text
* Ratings

---

## 🔍 Exploratory Data Analysis (EDA)

Key analyses performed:

* Rating and cost distributions
* Review length patterns
* Rating variability across restaurants
* Cost vs rating relationship

**Key Insight:** Pricing alone does not explain customer satisfaction.

---

## 🧹 Data Cleaning & Feature Engineering

* Removed duplicate reviews
* Handled missing values using median imputation
* Cleaned review text for NLP
* Extracted sentiment using **VADER**
* Engineered features:

  * Average sentiment score
  * Negative sentiment ratio
  * Review count
  * Average review length
  * Cuisine count
  * Log-transformed cost

All features were aggregated at the **restaurant level**.

---

## 📊 Hypothesis Testing

* **Cost vs Cuisine Count** → Pearson Correlation (Significant)
* **Low-cost vs High-cost Ratings** → Welch’s t-test (No significant improvement)
* **Cost Category vs Rating Category** → Chi-square test (Significant association)

**Conclusion:** Cost and ratings are related, but pricing alone does not drive satisfaction.

---

## 🤖 Models Implemented

* **K-Means Clustering** ✅ (Final Model)
* Hierarchical Clustering
* DBSCAN (Rejected due to noise)

### Model Evaluation

* Elbow Method
* Silhouette Score
* Dendrogram analysis

K-Means was selected for its stability and business interpretability.

---

## 🧠 Cluster Insights

The model groups restaurants into segments such as:

* High sentiment & high engagement restaurants
* Budget restaurants with mixed sentiment
* Premium restaurants with inconsistent experience
* Underperforming restaurants needing improvement

---

## 💼 Business Impact

* Helps customers choose better restaurants
* Supports recommendation systems
* Enables restaurant owners to:

  * Identify weaknesses
  * Improve service quality
  * Optimize pricing strategies

---

## ⚠️ Limitations

* Static historical data
* City-level effects not fully modeled
* No real-time review updates

---

## 🚀 Future Enhancements

* Add location-based features
* Integrate operational metrics
* Real-time sentiment dashboards
* Deploy clustering using web apps

---

## 🛠️ Tech Stack

* Python
* Pandas, NumPy
* NLTK (VADER)
* Scikit-learn
* Matplotlib, Seaborn
* SciPy

---

## 👤 Author

**Shivakumar L R**
Aspiring Data Scientist | Machine Learning & NLP Enthusiast
