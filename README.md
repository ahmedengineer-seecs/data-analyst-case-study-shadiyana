# Shadiyana.pk - Data-Driven Growth Strategy for a Wedding Services Platform

## Introduction

This repository contains a data analytics case study for Shadiyana.pk, a prominent wedding services platform. The project leverages historical customer query and vendor data to uncover actionable insights. The primary goal is to provide data-driven recommendations that inform marketing, product development, and sales strategies, ultimately driving business growth and enhancing market position.

## Problem Statement

Shadiyana.pk aimed to gain a deeper understanding of its customer preferences and vendor dynamics to make more informed business decisions. The central business objective was to identify untapped market opportunities by answering the following key questions:

* What are the characteristics of our primary customer personas?
* What is the seasonal demand for wedding services throughout the year?
* Are there popular geographic areas or venue types that are currently underserved by our vendor network?
* How can we optimize our sales and marketing efforts to capitalize on these market opportunities?

This analysis addresses these questions by identifying a critical mismatch between high customer demand for premium venues in specific areas and a low supply of vendors in those same locations.

## Data

The analysis is based on two primary datasets:

* **Customer Information:** Contains details of 2,042 customer queries, including event dates, number of guests, and the specific venues they are interested in.
* **Vendor Information:** Includes details for 80 vendors, such as their budget category (Premium, Mid-range, Budget) and their operational sub-area.

***Note: For the purpose of this public repository, the data has been anonymized to protect privacy and confidentiality.***

## Methodology

The data analysis was conducted using Python with the `pandas`, `matplotlib`, and `seaborn` libraries. The methodology followed these key steps:

1.  **Data Cleaning and Preparation:**
    * Loaded the customer and vendor data from Excel files.
    * Cleaned column names to remove leading/trailing spaces.
    * Handled missing values in the 'Number of Guests' column by filling them with the mean (187).
    * Converted the 'Event Date' column to a datetime format to enable time-series analysis.
    * Merged the customer and vendor dataframes to create a unified dataset for comprehensive analysis.

2.  **Exploratory Data Analysis (EDA):**
    * **Seasonal Demand Analysis:** Analyzed the number of customer queries per month to identify peak wedding seasons.
    * **Customer Persona Analysis:** Segmented customers based on the number of guests to understand the most common event sizes.

3.  **Geographic Market Gap Analysis:**
    * Calculated the demand (number of queries) and supply (number of vendors) for each sub-area.
    * Determined a "demand ratio" (queries per vendor) to pinpoint the most underserved markets.

## Key Recommendations and Proof

The analysis yielded several high-impact, actionable recommendations supported by the following data visualizations:

### 1. Targeted Vendor Acquisition in Underserved Markets

* **Insight:** There is a severe mismatch between high customer demand and low vendor supply in specific geographic areas. **Bahria Town** is the most underserved market, with a demand-to-supply ratio of nearly 24 queries for every listed vendor.
* **Proof:**

    ![Market Gap Analysis](<img width="1400" height="800" alt="8_market_gap_ratio" src="https://github.com/user-attachments/assets/f76cb581-3165-4f88-a764-bbfa677c30aa" />
)
* **Action (Sales Team):** Immediately launch a targeted vendor acquisition campaign in Bahria Town and Lahore Cantt., with the goal of tripling the number of Premium and Mid-range venues listed within the next quarter.

### 2. Align Marketing with Peak Season and Customer Personas

* **Insight:** The peak wedding season runs from **October to April**. The primary customer persona is planning a wedding for **200-400 guests**.
* **Proof:**

    ![Monthly Demand Trend](<img width="1200" height="600" alt="1_seasonal_demand" src="https://github.com/user-attachments/assets/e589412b-b346-45a5-96e5-4c32253f5a20" />
)
    ![Guest Count Distribution](<img width="1200" height="600" alt="2_guest_count_distribution" src="https://github.com/user-attachments/assets/0feca830-8700-4e09-a2fd-bc233bf8f7bd" />
)
* **Action (Marketing Team):** Reallocate marketing spend to the August-November period to capture customers planning for the peak winter wedding season. Create targeted digital ad campaigns with messaging like, "Find the Perfect Venue for Your 300-Guest Wedding."

### 3. Enhance Product Features to Improve User Experience

* **Insight:** A large segment of users is searching for venues that can accommodate a specific range of guests (200-400). Making it easier for them to find suitable options will improve the user experience and increase conversion rates.
* **Proof:** The guest count distribution chart above clearly shows the concentration of customers in this segment.
* **Action (Product Team):** Enhance the website's search functionality by adding a "Guest Count" filter with pre-set popular ranges (e.g., 200-250, 250-350). Create a "Premium Collection" or "Luxury Venues" section on the homepage.

## How to Run the Code

1.  **Prerequisites:**
    * Python 3.x
    * Jupyter Notebook or JupyterLab
    * The following Python libraries: `pandas`, `matplotlib`, `seaborn`.

2.  **Installation:**
    You can install the required libraries using pip:
    ```bash
    pip install pandas matplotlib seaborn
    ```

3.  **Running the Notebook:**
    * Clone this repository to your local machine.
    * Place the `Customer information.xlsx` and `vendor information.xlsx` files in the same directory as the notebook.
    * Open and run the Jupyter Notebook (`Untitled11 (2).ipynb`) to reproduce the analysis and generate the visualizations.
    * Place the anonymized `customer_information.csv` and `vendor_information.csv` files in a `data` directory.
    * Open the `shadiyana_analysis.ipynb` notebook in Jupyter Notebook or JupyterLab.
    * Run the cells in the notebook sequentially to reproduce the analysis.
