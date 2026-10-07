# Amazon India Product Price Analysis

## Project Overview

This project performs an end-to-end analysis of Amazon India product pricing across three major categories:

- Laptops
- Mobiles
- Washing Machines

The dataset was collected from Amazon product listings and processed using Python, Pandas, NumPy, Matplotlib, and Seaborn.

The analysis focuses on product pricing, discounts, MRP, ratings, brands, product segments, and relationships between key product attributes.

After data cleaning, product-relevance filtering, deduplication, and data-quality validation, the final analytical dataset contains **1,382 products** with **0 duplicate ASINs**.

> Note: Review-count data was identified as unreliable during validation and is therefore excluded from the final business analysis.

---

## Project Objectives

- Collect product-level pricing data from Amazon India
- Analyze pricing differences across product categories
- Compare selling prices and MRP
- Analyze advertised discounts
- Study customer rating patterns
- Compare brands across product categories
- Identify budget, mid-range, and premium price segments
- Explore relationships between price and product ratings
- Perform correlation analysis
- Generate business-oriented insights from product pricing data
- Apply data-quality checks before drawing conclusions

---

## Dataset

The final validated dataset contains:

| Category | Products |
|----------|---------:|
| Mobiles | 473 |
| Laptops | 465 |
| Washing Machines | 444 |
| **Total** | **1,382** |

### Key Fields

- `ASIN`
- `Category`
- `Brand`
- `Product_Title`
- `Price_Numeric`
- `MRP_Numeric`
- `Discount_Pct_Final`
- `Rating_Numeric`
- `RAM_GB`
- `Storage_GB`
- `Storage_Type`
- `Capacity_KG`

---

## Data Quality & Validation

Several validation steps were performed before the final analysis.

### Duplicate Validation

- Total products: **1,382**
- Unique ASINs: **1,382**
- Duplicate ASINs: **0**

### Price Validation

Selling prices were checked for missing and unrealistic values.

### MRP Validation

MRP values were independently checked against selling prices.

A small number of corrupted MRP values were identified and corrected before calculating final discounts.

After correction:

- Products with valid Price + MRP: **1,301**
- Products with MRP below selling price: **0**
- Maximum calculated discount: **83.39%**

### Rating Validation

- Products with ratings: **1,199**
- Missing ratings: **183**
- Invalid ratings: **0**
- Valid rating range: **1.0–5.0**

### Review Data Validation

Review-count extraction was found to contain systematic parsing errors. Therefore, review-based metrics were excluded from the final business analysis rather than presenting unreliable results.

This validation step helps ensure that the final insights are based on reliable fields.

---

## Analysis Performed

### 1. Product Category Analysis

- Product count by category
- Category distribution
- Category-level pricing comparison

### 2. Price Analysis

- Price distribution
- Average price
- Median price
- Price range
- Category-wise price comparison
- Price distribution by category

### 3. Discount Analysis

- Discount distribution
- Average discount by category
- Advertised discount vs selling price
- Price savings analysis
- MRP vs selling price comparison

### 4. Rating Analysis

- Rating distribution
- Average rating by category
- Price vs rating relationship
- Price-rating correlation

### 5. Brand Analysis

- Top brands by product count
- Average price by brand
- Average rating by brand

### 6. Price Segmentation

Products were grouped into three analytical segments:

- **Budget:** Below ₹15,000
- **Mid-Range:** ₹15,000–₹49,999
- **Premium:** ₹50,000 and above

Category-level comparisons were performed across these segments.

### 7. Correlation Analysis

Correlation analysis was performed across available numerical product attributes including:

- Selling price
- MRP
- Discount
- Rating
- RAM
- Storage
- Washing-machine capacity

---

## Key Findings

The analysis shows substantial differences in pricing across the three categories.

### Category Pricing

Laptops have the highest typical selling prices, while mobiles and washing machines occupy lower price ranges.

Because laptop prices are strongly right-skewed by premium gaming and professional models, both mean and median prices were considered.

### Discounts

The corrected dataset shows a median calculated discount of approximately **27.27%** among products with valid MRP and selling price.

### Ratings

Washing machines have the highest average rating among the three categories:

- Washing Machines: **4.05**
- Mobiles: **3.93**
- Laptops: **3.92**

These averages are calculated only from products with available ratings.

### Price Segmentation

The dataset contains products across budget, mid-range, and premium price segments, allowing category-level comparison of product positioning.

---

## Visualizations

The project includes portfolio-quality visualizations covering:

- Category distribution
- Price distribution
- Average price by category
- Median price by category
- Discount distribution
- Average discount by category
- Rating distribution
- Average rating by category
- Price vs rating
- Price-rating correlation
- Mean vs median price
- MRP vs selling price
- Average price savings
- Selling price vs advertised discount
- Top brands by product count
- Top brands by average rating
- Top brands by average price
- Product price segmentation
- Category-wise price segments
- Correlation heatmap

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook
- Selenium
- BeautifulSoup
- Microsoft Edge WebDriver

---

## Project Workflow

```text
Amazon Product Listings
        ↓
Data Collection
        ↓
Product Deduplication
        ↓
Data Cleaning
        ↓
Numeric Feature Extraction
        ↓
Product Relevance Filtering
        ↓
Data Quality Validation
        ↓
Price / MRP / Discount Validation
        ↓
Rating Validation
        ↓
Exploratory Data Analysis
        ↓
Data Visualization
        ↓
Business Insights
