# 🛒 Amazon Product Analytics Dashboard

### 📊 Product Performance | Pricing | Discounts | Customer Ratings

A Power BI dashboard developed to analyze Amazon product data and uncover insights related to product categories, pricing, discounts, customer ratings, and customer engagement.

---

## 📌 Project Overview

This project analyzes Amazon product-level data using **Microsoft Power BI** to understand product performance, pricing patterns, discount strategies, and customer ratings.

The dashboard transforms raw product data into an interactive and easy-to-understand analytical report designed to support data-driven decision making.

The project focuses on answering questions such as:

- Which product categories contain the most products?
- Which categories offer the highest average discounts?
- What is the overall customer rating distribution?
- How do actual prices compare with discounted prices?
- Which products have the highest customer engagement based on rating counts?
- What are the overall pricing and discount trends across the dataset?

---

## 🎯 Business Objective

The primary objective of this project is to convert raw Amazon product data into meaningful business insights.

The dashboard can help stakeholders understand:

- 📦 Product distribution across categories
- 💰 Pricing and discount patterns
- ⭐ Customer satisfaction through ratings
- 👥 Customer engagement through rating counts
- 🏷️ Product-level performance
- 📈 Differences between actual and discounted prices

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| **Microsoft Power BI** | Data visualization & dashboard development |
| **Power Query** | Data cleaning and transformation |
| **DAX** | Measures and KPI calculations |
| **Microsoft Excel / CSV** | Data source and initial inspection |

---

## 🧹 Data Preparation

Before building the dashboard, the raw dataset was cleaned and transformed using **Power Query**.

The data preparation process included:

- Removing duplicate records
- Handling data type inconsistencies
- Cleaning product categories
- Extracting the main product category
- Converting price columns into numeric values
- Converting discount percentages into percentage format
- Handling rating-related errors
- Creating appropriate data types for numerical columns
- Renaming columns for easier analysis

### Key fields used

- `product_id`
- `product_name`
- `category`
- `Main Category`
- `actual_price`
- `discounted_price`
- `discount_percentage`
- `rating`
- `rating_count`
- `product_link`

---

# 📊 Dashboard Features

## 1. KPI Cards

The dashboard contains five key performance indicators:

### Total Listings

Represents the total number of product records available in the dataset.

### Unique Products

Represents the number of distinct products based on `product_id`.

### Average Rating

Shows the overall average customer rating across products.

### Average Discount

Shows the average discount percentage offered across the dataset.

### Average Selling Price

Shows the average discounted price of products.

These KPIs provide a quick overview of the marketplace before diving into detailed visualizations.

---

## 2. 📦 Products by Main Category

### Visual: Horizontal Bar Chart

This visualization shows the number of products available within each main category.

It helps identify categories with the largest product presence and provides an overview of the composition of the dataset.

---

## 3. 🏷️ Average Discount by Main Category

### Visual: Horizontal Bar Chart

This chart compares the average discount percentage across different product categories.

It helps identify categories where products are generally offered with higher discounts.

---

## 4. ⭐ Rating Distribution

### Visual: Column Chart

This visualization displays the distribution of product ratings.

It helps understand the overall customer rating pattern and identify the rating ranges where most products are concentrated.

---

## 5. 💰 Actual Price vs Discounted Price

### Visual: Clustered Column Chart

This visualization compares the average actual price with the average discounted price across product categories.

It provides a clear view of the difference between the original listed price and the price offered after discounts.

---

## 6. 🏆 Top 10 Products by Discounted Price

### Visual: Matrix / Table

The dashboard includes a product-level table showing the top products based on discounted price.

The table contains:

- Product Name
- Category
- Actual Price
- Discounted Price
- Discount Percentage
- Rating
- Rating Count
- Product Link

This allows users to move from high-level analysis to individual product details.

---

# 📐 Key DAX Measures

The dashboard uses DAX measures to create dynamic KPIs.

### Total Product Listings

```DAX
Total Product Listings =
COUNTROWS(amazon)
