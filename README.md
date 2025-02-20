# 📊 Sales Strategy  

## 🚨 Problem: Incorrect Recommendations  
We are losing revenue by suggesting cheap products to premium customers.  

### Example:  
- **Current:** You bought office supplies → We recommend a $1 pencil  
- **Better:** We recommend a $4 premium pencil  

## 🏆 Identifying Premium Products & Customers  
### **Premium Products**  
- Identified using **Interquartile Range (IQR) Analysis**.  
- A product is premium if its price is significantly higher than similar products in its category.  

### **Premium Customers** (meets at least one):  
- **Bought 3+ premium products**  
- **30%+ of their purchases are premium**  
- **50%+ of total spending is on premium products**  

**Result:** 3% of users (17,138 customers) in April were premium buyers.  

## 🤖 Customer Segmentation with K-Means  
We used **K-Means clustering** to group customers:  

1. **Passing-by Customers 🛍️** – Occasional buyers, low spending.  
2. **Premium Stars 🌟** – Loyal, frequent buyers who prefer premium.  
3. **Discount Hunters 💰** – Buy mainly with discounts, avoid shipping costs.  
4. **Potential Premium 🚀** – High total spending, but not always buying premium.  

## 📈 Business Impact & Revenue Growth  
If just **1 in 5 premium users upgrades one item**, revenue increases significantly.  

### 💰 Revenue Projection:  
1. **Current Revenue:** $172M  
2. **Targeting Key Customers → +200% Revenue Growth**  
3. **New Projected Revenue:** $196M  
4. **Total Additional Revenue:** **+$24.6M**  

**Better premium product recommendations = Huge revenue growth!**  
