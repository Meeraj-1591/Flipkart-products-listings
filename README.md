# 🛒 Flipkart Products Listings Exploratory Data Analysis (EDA)

## 📝 Project Overview

This project performs an **Exploratory Data Analysis (EDA)** on a publicly available dataset of Flipkart product listings. The primary objective is to extract valuable **business insights** regarding product performance, pricing strategies, discount impact, and customer behavior on one of India's leading e-commerce platforms.

The analysis focuses on historical data to answer critical questions that can help Flipkart optimize its product catalog, refine pricing strategies, and enhance customer satisfaction.

---

## 🎯 Objectives

* **Data Cleaning and Exploration:** Process raw data, handle missing values (using median imputation for prices and mode for others), and ensure data integrity for reliable analysis.
* **Feature Engineering:** Create new, insightful features, including:
    * `discount_pct` (Discount Percentage)
    * `price_range` (Binned prices, e.g., '0-200', '5000+')
    * **Temporal Features** (`month`, `day_of_week`, `time_of_day`, `season`)
* **Exploratory Data Analysis (EDA):** Use statistical methods and data visualization to uncover patterns and answer key business questions related to sales, ratings, and product attributes.

---

## 📊 Key Business Questions and Findings

| Business Question | Key Finding |
| :--- | :--- |
| **Which product categories offer the highest discounts but maintain high ratings?** | Certain niche categories (e.g., specialized **Beauty and Personal Care** accessories, specific **Mobile Accessories**) show exceptionally high discounts (over 90%) while retaining perfect or near-perfect ratings. These could be targeted for high-visibility promotions. |
| **Which product price ranges generate the most products and highest average ratings?** | The majority of products are concentrated in the **low to mid-range price bins** (e.g., ₹201–₹500 and ₹501–₹1000). Products in the **mid-range** (e.g., ₹1001–₹2000) tend to receive the highest average ratings, suggesting a good balance of quality and price. |
| **Does offering higher discounts actually lead to better customer ratings?** | The **correlation analysis** showed that there is almost **no linear relationship** between `discount_pct` and `average_rating` (correlation is close to **0.01**). Customer satisfaction is primarily influenced by inherent **product quality**, not the size of the discount. |
| **How do discount strategies vary among the top 10 brands?** | **Discount distribution varies significantly.** Some top brands show stable pricing (medium discounts), while others rely more heavily on wide promotional spreads (higher median and range of discounts). |
| **How does the average product discount change across different months of the year?** | The data suggests **fluctuations linked to sales periods**. Promotional activity is concentrated in specific months (e.g., higher average discounts in December, peaking in March/April), likely coinciding with major sales or festive seasons. |
| **Is there a relationship between product price and customer ratings?** | The **scatter plot** of `retail_price` vs. `average_rating` confirms a **weak relationship**. High-priced items do not guarantee better ratings, and highly-rated items exist across all price points. |

---

## ✨ Analysis Results (Visualizations)

The following visualizations were used to support the key findings:

### 1. Distribution of Discounts and Ratings
* **`discount_pct` Histogram:** Shows that a significant number of products have substantial discounts (up to 70-80%).
* **`average_rating` Histogram:** Indicates a strong positive skew, with the majority of products clustered around a **4.0 rating**, confirming a generally high level of satisfaction in the dataset.



### 2. Product Count and Rating by Price Range
* **Bar Charts:** Clearly show that the highest volume of products is in the lower price tiers, but the **average rating remains consistently high (near 4.0)** across most price ranges.



### 3. Correlation between Price, Discount, and Rating
* **Correlation Heatmap:** Visual confirmation that the **discount percentage** (`discount_pct`) has a very **weak or negligible correlation** to the `average_rating`.


### 4. Monthly Discount Trend
* **Line Plot:** Highlights the non-linear trend of discounts over time, suggesting **seasonal or promotional peaks** where discounts are significantly higher.


### 5. Discount Distribution by Top Brands
* **Box Plot:** Demonstrates the varying discount strategies, showing differences in the median discount (the line inside the box) and the overall range of discounts (the whiskers) offered by the top 10 brands.


---

## 🛠️ Technologies Used

* **Python:** The core language for data processing and analysis.
* **Pandas:** Used for data loading, cleaning, and manipulation.
* **NumPy:** Essential for numerical operations and array manipulation.
* **Matplotlib & Seaborn:** Used for data visualization and generating insightful plots.

---

## 💾 Dataset

The dataset used for this project is a publicly available **Flipkart E-commerce Dataset** from Kaggle:

* **Source:** [Flipkart E-commerce Dataset on Kaggle](https://www.kaggle.com/datasets/atharvjairath/flipkart-ecommerce-dataset/data)

### Key Columns Analyzed:

* `uniq_id`: Unique identifier for the product listing.
* `product_category_tree`: Hierarchical category of the product.
* `brand`: The brand name of the product.
* `retail_price` / `discounted_price`: Original and sale prices.
* `discount_pct`: *Engineered Feature* - The calculated discount percentage.
* `product_rating` / `overall_rating`: Customer ratings.
* `crawl_timestamp`: Date and time of data collection (*Used for Temporal Features*).

---

## 🔑 How to Run the Project

1.  **Clone the Repository:**
    ```bash
    git clone <Your Repository URL>
    cd <Your Repository Name>
    ```
2.  **Install Dependencies:**
    This project requires common data science libraries.
    ```bash
    pip install pandas numpy matplotlib seaborn
    ```
3.  **Download the Data:**
    Download the `flipkart_com-ecommerce_sample.csv` file from the Kaggle link provided above and place it in your project directory.
4.  **Execute the Notebook/Script:**
    Run the Jupyter Notebook or Python script containing the analysis steps.
    ```bash
    jupyter notebook AI_Assessment.html 
    ```
    ## 👤 Author

**Meeraj Kumar Budike**  
📧 Email: *meerajbudike1501@gmail.com*  
🔗 LinkedIn: *https://www.linkedin.com/in/meeraj-kumar-598712376/*
