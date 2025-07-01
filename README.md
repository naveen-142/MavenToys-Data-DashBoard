# 🧸 Maven Toys - Business Intelligence Dashboard 📊

This project presents a comprehensive **Power BI dashboard** for **Maven Toys**, a fictional retail toy company. It transforms raw sales, inventory, and product data into interactive visual insights to support data-driven decision-making.


## 🔍 Project Objective

To analyze and visualize:
- **Sales performance** across stores and products
- **Product profitability** based on cost vs selling price
- **Inventory status** across locations
- And provide a combined executive-level overview


## 📁 Dataset Description

The dashboard is built using 4 key datasets:

| Table         | Description |
|---------------|-------------|
| `Sales`       | Records of daily transactions (Store ID, Product ID, Units, Date) |
| `Products`    | Product-level info (Name, Category, Cost, Price) |
| `Stores`      | Store info (City, Location Type, Open Date) |
| `Inventory`   | Stock-on-hand per product at each store |


## 📊 Dashboard Pages

### 1. **Executive Overview**
- Total Revenue, Profit, Units Sold
- Revenue by City & Category
- Sales trend over time

### 2. **Product Dashboard**
- Average Cost, Selling Price, and Profit per Unit
- Visual comparison: Price vs Cost
- Product count by category

### 3. **Sales Insights**
- Top selling products
- Store-wise sales comparison
- Revenue breakdown by product category

### 4. **Inventory Management**
- Stock status by product
- Out of stock / low stock alerts
- Inventory health distribution


## 🧠 Key DAX Measures

```dax
Total Revenue = SUMX(Sales, Sales[Units] * RELATED(Products[Product_Price]))

Total Profit = SUMX(Sales, Sales[Units] * (RELATED(Products[Product_Price]) - RELATED(Products[Product_Cost])))

Profit_Per_Unit = Products[Product_Price] - Products[Product_Cost]

Inventory_Status = 
SWITCH(TRUE(),
    Inventory[Stock_On_Hand] = 0, "Out of Stock",
    Inventory[Stock_On_Hand] < 10, "Low",
    "Sufficient"
)
```

## 🛠️ Tools & Skills Used

- **Power BI**
- **DAX (Data Analysis Expressions)**
- Data Modeling & Relationships
- Interactive Visual Design
- Slicers, Filters, Drillthrough
- Navigation with Bookmarks


## 📌 Key Learnings

- Designed a multi-page professional dashboard with real business KPIs
- Applied DAX to derive meaningful metrics like profit, revenue, and inventory status
- Built dynamic visuals with slicers and interactivity
- Practiced storytelling with data using a clean and intuitive layout


## 🖼️ Dashboard Preview
![Products-Dashbord](https://github.com/user-attachments/assets/293a2c28-6686-40df-b8a5-1112c7214514)

![Sales-Dashbord](https://github.com/user-attachments/assets/14a67b28-c4b6-4cb8-8340-0c8818f74a74)


![Inventory   Store - Dashbord](https://github.com/user-attachments/assets/e9b0dfba-9dbe-4d16-b6f5-b04e94a86aee)


## 📂 How to Use

1. Download the `.pbix` file from this repository
2. Open the file in **Power BI Desktop**
3. Use the page navigation to explore each section:
   - Executive Overview
   - Product Insights
   - Sales Analytics
   - Inventory Management etc.,
4. Interact with slicers to filter data by city, category, or store


## 🙋‍♂️ About Me

Hi! I'm **Naveen Kumar**, a data enthusiast passionate about transforming raw data into business value.  
This project is part of my portfolio to showcase data modeling, DAX, and Power BI storytelling skills.

📧 Email: naveenkv681@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/your-profile)


## ⭐ Support

If you found this project helpful, please **star** this repository and feel free to connect with me on LinkedIn!

