# 🛒 Instacart Market Basket Analysis & Product Reorder Prediction  

## 📌 Overview  
This project analyzes **3+ million grocery orders** from **200K+ Instacart users** to uncover **shopping patterns, customer segments, and product affinities**.  

The objectives are to:  
- Enhance **cross-selling & upselling** strategies  
- Improve **store layouts** and **inventory planning**  
- Develop a **machine learning model** to predict products likely to be reordered in a customer’s next purchase  

The workflow includes: **Exploratory Data Analysis (EDA)**, **Customer Segmentation**, **Market Basket Analysis**, and **Predictive Modeling** using **XGBoost** and **Neural Networks**.  

---

## 🎯 Objectives  
- **Data Exploration & Insights** — Analyze anonymized Instacart dataset from [Kaggle](https://www.kaggle.com/c/instacart-market-basket-analysis/data)  
- **Affinity Analysis** — Discover product associations for better cross-selling  
- **Customer Segmentation** — Cluster customers by purchasing patterns for targeted marketing  
- **Reorder Prediction Model** — Predict previously purchased items likely to appear in a user's next order  

---

## 📂 Project Structure  
📦 Instacart-Market-Basket-Analysis
┣ 📂 Plots/ → Visualization outputs
┣ 📜 Data Description and Analysis.ipynb → Initial dataset exploration
┣ 📜 Exploratory Data Analysis.ipynb → Detailed EDA & visual insights
┣ 📜 Customers Segmentation.ipynb → KMeans clustering on customer behavior
┣ 📜 Market Basket Analysis.ipynb → Apriori algorithm for association rules
┣ 📜 Feature Extraction.ipynb → Feature engineering for ML model
┣ 📜 Data Preparation.ipynb → Data cleaning & preprocessing
┣ 📜 ANN Model.ipynb → Neural network implementation
┣ 📜 XGBoost Model.ipynb → XGBoost training & evaluation
┣ 📜 LICENSE → MIT License
┗ 📜 README.md → Project documentation



---

## 📊 Dataset Overview  

**Files:**  
- `aisles.csv` — 134 unique aisles  
- `departments.csv` — 21 product departments  
- `products.csv` — 49,688 products with aisle & department mapping  
- `orders.csv` — 3,421,083 orders from 206,209 users  
- `order_products_prior.csv` — Product details for prior orders  
- `order_products_train.csv` — Product details for training set orders  

**Key Insights:**  
- Most orders are placed on **Saturdays & Sundays** during **daytime hours**  
- Customers typically order **once a week**  
- Popular departments include **produce, dairy, and beverages**  
- **Organic products** have a high reorder percentage despite being fewer in number  

---

## 📈 Exploratory Data Analysis (EDA)  
- Identified **most popular aisles and products**  
- Found **higher reorder rates** for essential food items compared to specialty goods  
- Analyzed **cart order position vs reorder likelihood**  
- Observed that **85% of customers purchase only ~10K products** out of the total 49K+  

---

## 🧩 Customer Segmentation  
- Performed **Principal Component Analysis (PCA)** to reduce dimensions  
- Used **KMeans Clustering** to segment customers into **5 groups** based on purchase patterns  
- Example segments:  
  - Fresh produce lovers  
  - Beverage-focused customers  
  - Mixed-category shoppers  

---

## 🔍 Market Basket Analysis  
Applied **Apriori Algorithm** to find frequent product combinations:  
- Example association: *Limes* & *Large Lemons* (Lift = 3.0)  
- Organic fruits like *Strawberries*, *Raspberries*, and *Blueberries* have strong co-purchase relationships  
- Insights can guide **cross-marketing** and **store layout decisions**  

---

## 🤖 Machine Learning Models  

### **Feature Engineering**  
Created features at:  
- **Product level** (popularity, reorder % etc.)  
- **Aisle/Department level** (average cart position, reorder stats)  
- **User level** (purchase frequency, diversity, reorder patterns)  
- **User-Product level** (historical interactions)  

### **Models Used**  
- **XGBoost Classifier**  
- **Artificial Neural Network (ANN)**  

**Evaluation Metric:** ROC-AUC Score  
- XGBoost slightly outperformed ANN in prediction accuracy  
- Class weights used to handle **imbalanced data**  

---

## 📊 Model Performance  

| Model         | ROC-AUC | Key Strength |
|---------------|--------|--------------|
| XGBoost       | High   | Feature importance & scalability |
| ANN           | High   | Captures complex non-linear patterns |

---

## 🚀 Future Work  
- Integrate **Collaborative Filtering** for personalized recommendations  
- Incorporate **pricing data** to optimize for revenue, not just reorder likelihood  
- Deploy as an **interactive dashboard or API** for retailers  

---

## 📜 License  
This project is licensed under the **MIT License** — you’re free to use, modify, and distribute with attribution.  

---
