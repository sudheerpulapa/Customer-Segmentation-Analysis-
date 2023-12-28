# Data Analytics Customer Segmentation

## Goal of the Project

The aim of this project is to perform a Customer Segmentation Analysis for an Automobile bike Company using an RFM Model. RFM (Recency, Frequency, Monetary) analysis is a behavior-based approach that groups customers into segments based on their previous purchase transactions. The project involves dividing the customer segment into 11 groups to determine which segments should be targeted to enhance sales revenue. A **Sales Dashboard for Customer Segmentation** has been developed using **Tableau**, and data quality assessment and analysis are conducted using **Python**.

## Tableau Dashboard

The Sales Dashboard for Customer Segmentation can be found [here](https://public.tableau.com/profile/abhishek.chowdhury#!/vizhome/CustomerSegmentationDashboard_16175595616510/RFMDashboard).  
![Sales Dashboard](data%20visualization/Sales%20Dashboard.gif)

**Note**: In case of difficulty loading Jupyter Notebooks on GitHub, you can view the notebooks on nbviewer by clicking on the respective hyperlinks.

- [RFM Analysis.ipynb](https://nbviewer.jupyter.org/github/AbhishekGit-hash/Data-Analytics-Customer-Segmentation/blob/master/RFM%20Analysis.ipynb)
- [DQA and Data Cleaning CustomerDemographic.ipynb](https://nbviewer.jupyter.org/github/AbhishekGit-hash/Data-Analytics-Customer-Segmentation/blob/master/DQA%20and%20Data%20Cleaning%20CustomerDemographic.ipynb)
- [DQA and Data Cleaning NewCustomerList.ipynb](https://nbviewer.jupyter.org/github/AbhishekGit-hash/Data-Analytics-Customer-Segmentation/blob/master/DQA%20and%20Data%20Cleaning%20NewCustomerList.ipynb)
- [DQA and Data Cleaning Transactions.ipynb](https://nbviewer.jupyter.org/github/AbhishekGit-hash/Data-Analytics-Customer-Segmentation/blob/master/DQA%20and%20Data%20Cleaning%20Transactions.ipynb)
- [DQA and Data Cleaning Customer Address.ipynb](https://nbviewer.jupyter.org/github/AbhishekGit-hash/Data-Analytics-Customer-Segmentation/blob/master/DQA%20and%20Data%20Cleaning%20Customer%20Address.ipynb)

## Analysis Approach

### 1. Data Quality Assessment and Data Cleaning

The initial step involves data preparation, quality assessment, and cleaning. Key observations and processes for each dataset are as follows:

- **CustomerDemographics.xlsx:**
  - Irrelevant column dropped.
  - Handling missing values (dropped or imputed).
  - Standardized gender data.
  - Transformed Date of Birth to create 'Age' and 'Age Group' features.
  - Removed outlier in the age distribution.
  - Checked for duplicate records (none found).

- **NewCustomerList.xlsx:**
  - Dropped irrelevant columns.
  - Addressed missing values (dropped or imputed).
  - Transformed Date of Birth to create 'Age' and 'Age Group'.
  - Checked for duplicate records (none found).

- **Transaction_data.xlsx:**
  - Converted 'product_first_sold_date' to datetime format.
  - Handled missing values (dropped or imputed).
  - Created a 'Profit' feature.
  - Checked for duplicate records (none found).

- **CustomerAddress.xlsx:**
  - Standardized 'states' data.
  - Addressed discrepancies in customer IDs between tables.

### 2. Exploratory Data Analysis on Customer Segments

After data cleaning, exploratory analysis was conducted, leading to the following insights:

- **New vs Old Customers Age Distribution:**
  - Most customers (both new and old) are aged between 40-49.
  - Steep drop in customers in the 30-39 age group among new customers.

- **Bike Purchases Over the Last 3 Years by Gender:**
  - Female customers made more bike purchases (51%) compared to male customers (49%).

- **New vs Old Customers Job Industry Distribution:**
  - New customers are primarily from the Manufacturing and Financial Services sectors.

- **Wealth Segmentation by Age Category:**
  - 'Mass Customer' segment dominates across all age categories.
  - 'Affluent' segment outperforms 'High Net Worth' in the 40-49 age group.

- **Cars Owned by States:**
  - New South Wales has the highest number of people who do not own a car.

### 3. RFM Analysis and Customer Segmentation

Customer segmentation was performed using an RFM Model, resulting in 11 groups:

- Platinum Customers
- Very Loyal Customers
- Recent Customers
- Potential Customers
- Lost Customers
- Losing Customers
- Late Bloomer
- High-Risk Customers
- Evasive Customers
- Becoming Loyal
- Almost Lost Customers

The current distribution of customer segments is displayed below:

![Customer Segment Distribution](data%20visualization/Customer%20Segment%20Distribution.PNG)

### 4. RFM Analysis: Scatter Plots

#### Recency vs Monetary:

Recent customers have purchased more products and generated more revenue compared to customers who visited a while ago.

![Recency vs Monetary](data%20visualization/Recency%20vs%20Monetary.PNG)

#### Frequency vs Monetary:

Customers in Platinum, Very Loyal, and Becoming Loyal segments have higher frequency and generate more monetary value.

![Frequency vs Monetary](data%20visualization/Frequency%20vs%20Monetary.PNG)

## Datasets Used

The datasets used in this project include:

- **Raw_data.xlsx:** This excel file contains the following sheets of data:
  - **Transactions_data.xlsx:** Transactions data of customers across different states in Australia.
  - **NewCustomerList.xlsx:** Data of new customers who visited the automobile bike company recently.
  - **CustomerDemographic.xlsx:** Details of Customer Demographics.
  - **CustomerAddress.xlsx:** Customer addresses.

## Tools and Technologies Used

The tools used in this project include:

- **Python 3.11.4:** Used for Data Quality Assessment and Data Cleaning processes, leveraging libraries such as pandas, matplotlib, and seaborn.
- **Tableau:** A Business Intelligence tool employed to explore data and create charts, graphs, and visualizations, resulting in a Sales Dashboard for Customer Segmentation for the automobile bike company.

## Authors

- Pulapa Sudheer Chowdary - [GitHub Profile](https://github.com/dashboard)
