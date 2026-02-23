# Amazon Sales Data Wrangling & Preparation

## Overview

This project focuses on cleaning, reducing, and preparing Amazon product sales data for structured analysis.

The original dataset contained **42,676 rows and 17 columns** of product-level sales information sourced from Kaggle. The objective was to transform the raw dataset into a manageable, consistent, and analysis-ready format suitable for SQL querying and business decision-making.

Completed as part of **BUS 211A – Foundations of Data Analytics (Brandeis University, Fall 2025).**

---

## Business Context

Retail sales data often arrives in large and unstructured formats, making direct analysis inefficient and error-prone.

The goal of this project was to:

- Improve data usability  
- Remove irrelevant or non-analytical fields  
- Reduce dataset size while preserving representativeness  
- Ensure consistency and data integrity  
- Prepare the dataset for database and analytical tools  

---

## Dataset Information

- **Source:** Kaggle – *Amazon Product Sales for a Month*  
- **Original Size:** 42,676 rows × 17 columns  
- **Final Size:** 5,000 rows × 13 columns  
- **Data Type:** Product listings and sales performance metrics  

### Retained Variables (13)

- `product_title`  
- `product_rating`  
- `total_reviews`  
- `purchased_last_month`  
- `discounted_price`  
- `original_price`  
- `discount_percentage`  
- `product_category`  
- `is_best_seller`  
- `is_sponsored`  
- `has_coupon`  
- `buy_box_availability`  
- `sustainability_tags`  

Removed columns included image URLs, page URLs, and metadata fields not relevant for analytical use.

---

## Data Reduction Strategy

The dataset was reduced from 42,676 rows to 5,000 rows using **stratified sampling**.

### Why Stratified Sampling?

- Preserves proportional representation across product categories  
- Prevents smaller categories from being excluded  
- Maintains dataset diversity  
- Enables faster querying and analysis  

Alternative approaches considered:

- Category filtering  
- Sales-volume filtering  
- Random sampling  

Stratified sampling was selected as the most balanced and representative method.

---

## Data Cleaning Process

### 1. Column Reduction
Irrelevant and non-essential fields were removed to streamline analysis.

### 2. Missing Value Handling
- Missing numeric values were imputed using category-level averages  
- Fewer than 2% of records contained missing data  

### 3. Standardization
- Converted price fields from text to numeric format  
- Cleaned rating values into consistent numeric scales  
- Standardized categorical labels  

### 4. Duplicate & Error Removal
- Removed duplicate rows  
- Corrected pricing inconsistencies  
- Eliminated logically invalid records  

### 5. Feature Engineering
Created grouped analytical variables:

- **Price Buckets:** Low / Medium / High  
- **Rating Categories:** Poor / Average / Excellent  
- **Discount Tiers:** None / Moderate / High  

These transformations simplify comparative analysis and aggregation.

---

## Tools Used

- Microsoft Excel  
- Pivot Tables  
- Data validation tools  
- Sampling logic  
- Basic statistical checks  

---

## Business Impact

The cleaned dataset:

- Is fully analysis-ready  
- Contains no missing or duplicate records  
- Maintains representative category distribution  
- Supports SQL queries and structured analytics workflows  

This project demonstrates practical data preparation and data quality management skills essential for business analytics roles.

---

## Repository Structure

```
amazon-sales-data-wrangling/
│
├── README.md
├── Report.pdf
```

---
