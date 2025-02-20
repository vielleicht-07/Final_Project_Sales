# 📊 Sales Strategy

## Dataset Overview
- **2 Dataset:** 1.3M Orders | 603K Users
- **Timeframe:** April 2022
- **Analysis:** Customer purchases and behaviors within a one-month period

## 🚨 Missed Opportunities in Recommendations
We are losing revenue by recommending the wrong products to potential premium customers. 

### The Problem
1. Identifying premium users.
2. Recommending the right products to them.

Currently, we suggest the cheapest products to maximize engagement, but this ignores users willing to pay for quality.

## 🔍 What Customers See vs. What They Should See
Imagine you're shopping online. You just bought office supplies…
- **Current Recommendation:** Cheap $1 pencil 
- **Better Recommendation:** Premium $4 pencil

## 🏆 Defining Premium Products
Key questions:
- Do a few products generate most revenue?
- Are premium products spread across all categories?
- Are high-revenue products always premium?

To identify premium products, we used **Interquartile Range (IQR) Analysis**:
- A product is **premium** if its price is significantly higher than similar products in its **Product Group**.

### Grouping Products:
- **5+ products** → Group by **Product Group**
- **<5 products** → Group by **Subcategory** for better accuracy.

## 👥 Defining a Premium Customer
We classify a user as **premium** if they meet at least one of these:
- **Bought 3+ premium products**
- **30%+ of their purchases are premium**
- **50%+ of total spending is on premium products**

### Why These Rules?
- **3+ Premium Purchases:** Avoids one-time expensive buyers.
- **30% of Purchases are Premium:** Indicates a preference for high-value items.
- **50% of Spending on Premium:** Shows they invest in premium products.

By applying these rules, **3% of active users (17,138 customers)** in April were identified as potential premium buyers.


## 🤖 Customer Segmentation with K-Means
Since "premium" is hard to define, we used **K-Means clustering** to group customers based on behaviors.

### Features Used:
- `total_variable_gross_profit_3yr`
- `total_variable_gross_profit_6mo`
- `lifecycle_segment_name`
- `registered`
- `count_lifecycle`
- `discount_percentage`
- `total_qty_bought_apr`
- `total_bookings_april`
- `avg_ship_cost_apr`

### 4 Customer Clusters:
1. **Passing-by Customers 🛍️** – Occasional buyers, low spending.
2. **Premium Stars 🌟** – Loyal, frequent buyers who prefer premium.
3. **Discount Hunters 💰** – Buy mainly with discounts, avoid shipping costs.
4. **Potential Premium 🚀** – High total spending, but not always buying premium.

## 📈 Business Impact Simulation
**What if we recommend premium products more effectively?**

### Example Price Differences:
- **Business cards:** €0.012 → €0.025 per card
- **T-shirts:** €1.30 → €15 per piece

If just **1 in 5 premium users upgrades one item**, revenue would increase drastically.

### 💰 Revenue Projection with Increased Spending
By targeting **Clusters 1 & 3** with better recommendations, we simulate a **200% revenue growth**:
- Low-value users upgrading to premium can significantly boost total sales.

## 🐍 How We Modeled It in Python
### 📈 Current Revenue vs. Projected Revenue & Additional Gains

We analyzed the impact of **better product recommendations** for premium customers. By suggesting premium products instead of cheaper alternatives, we projected a significant revenue increase.

### 💰 Revenue Simulation:
1. **Current Total Revenue:** $172M  
2. **Applying a 200% Increase for Targeted Customers**  
3. **New Projected Revenue:** $196M  
4. **Total Additional Revenue:** **+$24.6M**

---
 **Better recommendations for premium customers = Huge revenue growth!**
