# Advanced E-Commerce Data Analysis using SQL & Python

This project performs an in-depth analysis of an e-commerce dataset. It leverages the power of SQL for data querying and Python for advanced analytics, data visualization, and database automation. The core of the project is implemented within two Jupyter Notebooks, providing a comprehensive workflow from data ingestion to actionable insights.

---

### 🧠 Project Overview

This repository explores and analyzes a rich e-commerce dataset through two primary Jupyter notebooks:

1.  **`E-Commerce_Analysis.ipynb`**:
    * Performs advanced analytics by executing SQL queries directly within a Python environment using a MySQL connector.
    * Visualizes key business metrics, including:
        * 🛍️ **Fastest Sellers:** Identifies sellers with the quickest delivery times.
        * 📈 **Price Trends:** Tracks monthly variations in product prices.
        * 🌆 **High-Value Cities:** Determines cities with the highest average order payments.
        * 💳 **Payment Behavior:** Analyzes the usage of installment payments across different product categories.
        * 📅 **Order Volume:** Monitors the number of orders placed per month throughout 2018.
        * 🧮 **Order Composition:** Calculates the average number of products per order for each city.
        * 🔍 **Price vs. Demand:** Investigates the correlation between product price and order frequency.
    * Presents findings through a combination of bar charts, line plots, and interactive visualizations powered by Plotly.

2.  **`PythonSQLConnector.ipynb`**:
    * Automates the process of loading raw CSV data into a structured MySQL database.
    * It reads each CSV file using Pandas, dynamically infers data types (e.g., `INT`, `FLOAT`, `DATETIME`), creates the corresponding tables in MySQL, and efficiently inserts the data row-by-row, with robust handling of null values.

---

### 📁 Repository Structure

```
E‑Commerce‑Analysis‑SQL‑Python/
├── datasets/
│   ├── customers.csv
│   ├── geolocation.csv
│   ├── order_items.csv
│   ├── orders.csv
│   ├── payments.csv
│   ├── products.csv
│   └── sellers.csv
├── E‑Commerce Analysis Summary.pdf
├── E‑Commerce_Analysis.ipynb
└── PythonSQLConnector.ipynb
```

---

### 📄 Analysis Summary

For a concise summary of the key findings and strategic recommendations derived from the analysis, please refer to the **[E-Commerce Analysis Summary.pdf](E-Commerce%20Analysis%20Summary.pdf)**. This document covers:

* Fast-delivery and high-efficiency sellers.
* Pricing trends and product seasonality.
* Payment method preferences and installment behavior.
* Actionable insights with strategic recommendations for the business.

---

### ✅ Prerequisites

To run the notebooks and reproduce the analysis, you will need the following:

* **Python 3.8+**
* **Python Libraries**:
    ```bash
    pip install pandas matplotlib seaborn plotly mysql-connector-python
    ```
* **MySQL Server**:
    * A running MySQL instance.
    * A database named `ecommerce`.
    * Access credentials configured as follows:
        ```ini
        host=localhost
        user=root
        password=admin123
        ```

---

### 🚀 Getting Started

Follow these steps to set up the project environment and run the analysis.

**1. Set up the Database**
* Launch your MySQL server.
* Create the `ecommerce` database using the following SQL command:
    ```sql
    CREATE DATABASE ecommerce;
    ```
* Ensure your MySQL server is running and accessible with the credentials listed in the prerequisites.

**2. Load Data from CSVs**
* Open and run the **`PythonSQLConnector.ipynb`** notebook.
* This script will automatically create the necessary tables based on the CSV file structures and populate them with the provided data.

**3. Run the Analysis**
* Once the data is loaded into the database, open the **`E-Commerce_Analysis.ipynb`** notebook.
* Execute the cells sequentially to perform the data analysis and generate the interactive charts and insights.

---

### 🎯 Key Insights & Recommendations

The analysis yields several actionable insights that can inform strategic decisions:

* **Top-Performing Sellers**: Focus logistics training and offer incentives to the top 10 fastest sellers to set a standard for others.
* **City-Level Payment Trends**: Consider implementing localised pricing strategies or promotional offers in cities with high average order values.
* **Installment-Driven Categories**: Actively promote installment payment options for the top 10 product categories where this payment method is most popular.
* **Price-Order Correlation**: The analysis reveals a weak negative correlation (~ -0.11) between product price and order count, suggesting that pricing is not a strong driver of order frequency.
* **Operational Decisions**: Apply dynamic pricing strategies, streamline seller performance based on delivery metrics, and emphasize popular payment channels to enhance customer experience.

---

### 🛠 Customization

This project can be easily customised to fit different datasets or analytical needs:

* **Database Connection**: Change the database connection configurations in both `PythonSQLConnector.ipynb` and `E-Commerce_Analysis.ipynb` if your MySQL setup is different.
* **Datasets**: Point the `datasets/` path to new CSV files. The importer script will adapt as long as the format is consistent.
* **Analytics**: Modify the SQL queries and plotting functions in `E-Commerce_Analysis.ipynb` to explore new Key Performance Indicators (KPIs), dimensions, or business questions (e.g., seasonal breakdowns, new geographies).
