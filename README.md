# CartWise: Instacart Market Basket Optimization
---

## 📊 Data Summary  
Dataset: [Kaggle - Instacart Market Basket Analysis](https://www.kaggle.com/c/instacart-market-basket-analysis/data)  

- **134 aisles** across **21 departments**  
- **49,688 products**  
- **3,421,083 orders** from **206,209 users**  
- Includes prior, train, and test sets for predictive modeling  

---

## 📈 Key Insights & Visualizations  

### 🗓 Orders by Day of Week  
Most orders are placed on **weekends**, with peaks on **Saturday & Sunday**.  
![Orders by Day of Week](https://github.com/parthgawande/CartWise_Instacart-Market-Basket-Optimization-/blob/main/Plots/dow.png?raw=true)

---

### ⏰ Orders by Day & Hour  
Prime order times are **Saturday afternoons** and **Sunday mornings**.  
![Order Heatmap](https://github.com/parthgawande/CartWise_Instacart-Market-Basket-Optimization-/blob/main/Plots/heatmap.png?raw=true)

---

### 📦 Cart Size & Prior Orders  
Most carts contain **1–15 items**; repeat purchases dominate.  
![Prior Orders](https://github.com/parthgawande/CartWise_Instacart-Market-Basket-Optimization-/blob/main/Plots/prior.png?raw=true)

---

### 🛍 Top Aisles & Departments  
Produce aisles dominate sales, followed by dairy and beverages.  
![Popular Aisles](https://github.com/parthgawande/CartWise_Instacart-Market-Basket-Optimization-/blob/main/Plots/popular-aisles.png?raw=true)  
![Popular Departments](https://github.com/parthgawande/CartWise_Instacart-Market-Basket-Optimization-/blob/main/Plots/popular-departments.png?raw=true)

---

### 🌱 Organic vs Inorganic  
Organic items, though fewer, have a **higher reorder percentage**.  
![Organic vs Inorganic](https://github.com/parthgawande/CartWise_Instacart-Market-Basket-Optimization-/blob/main/Plots/Total-organic-inorganic-products.png?raw=true)  
![Reorder Organic vs Inorganic](https://github.com/parthgawande/CartWise_Instacart-Market-Basket-Optimization-/blob/main/Plots/Reorder-organic-inorganic-products.png?raw=true)

---

### 🔄 Reorder Trends  
Items added earlier in the cart are more likely to be reordered.  
![Add-to-Cart vs Reorder](https://github.com/parthgawande/CartWise_Instacart-Market-Basket-Optimization-/blob/main/Plots/Add-to-cart-VS-reorder.png?raw=true)

---

## 🧩 Customer Segmentation  
Applied **PCA** for dimensionality reduction and **KMeans** clustering. Optimal clusters = **5** (Elbow Method).  

**Elbow Method:**  
![Elbow Method](https://github.com/parthgawande/CartWise_Instacart-Market-Basket-Optimization-/blob/main/Plots/elbow.png?raw=true)  

**Cluster Visualization:**  
![Customer Clusters](https://github.com/parthgawande/CartWise_Instacart-Market-Basket-Optimization-/blob/main/Plots/cluster.png?raw=true)  

---

## 🔍 Market Basket Analysis  
Used **Apriori Algorithm** to find frequent product pairs:  

**Example:**  
- *Limes* & *Large Lemons* (Lift = 3.0)  
- *Organic Strawberries* & *Organic Raspberries* (Lift = 2.21)  

These insights can guide **cross-marketing** & **store layouts**.

---

## 🤖 Machine Learning Model  

### Features Engineered:  
- **Product-level** (popularity, reorder %)  
- **Aisle/Dept-level** (order stats, reorder ratios)  
- **User-level** (purchase frequency, diversity)  
- **User-Product-level** (historical interaction patterns)  

---

### Model Performance  

**XGBoost Feature Importance:**  
![XGBoost Feature Importance](https://github.com/parthgawande/CartWise_Instacart-Market-Basket-Optimization-/blob/main/Plots/XGBoost%20Feature%20Importance%20Plot.png?raw=true)  

**Neural Network Architecture:**  
![NN Architecture](https://github.com/parthgawande/CartWise_Instacart-Market-Basket-Optimization-/blob/main/Plots/NN%20Architecture.png?raw=true)  

---

## 🚀 Future Work  
- Implement **Collaborative Filtering** for personalized recommendations  
- Use **price data** to optimize for revenue as well as reorder likelihood  
- Build a **real-time recommendation dashboard**  

---

## 📜 License  
Licensed under the **MIT License** – free to use with attribution.  
