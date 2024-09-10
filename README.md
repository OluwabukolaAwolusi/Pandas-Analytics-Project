NB: This is a template to make documentation process easy. You can remove the `To-Do` notes in your final commit

# XYZ SUPERMARKET DATA ANALYSIS

This analysis combines customer shopping habits and sales data from three supermarket branches (Abuja, Lagos, and Port Harcourt) into a single dataset. The combined data reveals insights into sales patterns, customer behavior, and product performance across different branches and demographics.

# Project Steps

Step 1: Import Libraries and Set Working Directory

- Import necessary libraries: os, glob, pandas (as pd), datetime (as dt), time, numpy (as np), matplotlib.pyplot (as plt), seaborn (as sns)
- Set the working directory to the location where the data files are stored: os.chdir(r"C:\Users\DELL\Downloads")

Step 2: Combine Datasets

- Load the three datasets (Abuja, Lagos, and PortHarcourt) into separate DataFrames (PH, Lagos, Abuja)
- Combine the datasets using pd.concat: xyz = pd.concat([PH, Lagos, Abuja], axis=0, ignore_index=True)

Step 3: Save Combined Dataset to CSV

- Save the combined dataset to a new CSV file named 'xyz.csv' (or 'pandasproject.csv'): xyz.to_csv('xyz.csv')

Step 4: Load Combined Dataset

- Load the combined dataset from the CSV file into a new DataFrame using pd.read_csv: cxyz = pd.read_csv('xyz.csv', index_col='Unnamed: 0').squeeze()

Step 5: Check for Missing Values

- Check for missing values in the dataset using cxyz.isnull().sum()

Step 6: Data Manipulation and Cleaning

- Check the number of rows and columns using dfs.shape
- Check the number of dimensions using dfs.ndim
- Get the names of the columns using cxyz.columns
- Get information about the dataset using cxyz.info()
- Get a statistical summary of the data using cxyz.describe()

Step 7: Convert Date to Datetime Feature

- Convert the 'Date' and 'Time' columns to datetime format using pd.to_datetime

Step 8: Add New Rows for Day, Month, Year, and Hour

- Add new rows for day, month, year, and hour using the dt accessor

Step 9: Aggregation and Grouping

- Group the data by 'City' using cxyz.groupby('City')
- Aggregate the data using citys.agg()

Step 10: Visualization

- Generate visualizations using seaborn (sns) for proper understanding of the data


# Insights

1. Product Category Sales

- Highest sales recorded in:
    - Home and Lifestyle
    - Fashion Accessories
    - Electronics (primarily among female customers)
- Highest sales among male customers:
    - Food and Beverages
    - Sports
    - Travel

2. Gender-Based Purchasing Habits

- Female customers:
    - Purchase more Fashion Accessories
    - Record high total purchases of Home and Lifestyle products
- Male customers:
    - Have a higher habit of purchasing Sports and Leisure
    - Health and Beauty products

3. Product Quantity and Unit Price

- High quantity of Food and Beverages sold
- Slight difference in quantity of Electronic Accessories between male and female customers
- Fashion Accessories have the highest unit price
- Health and Beauty have the lowest unit price

4. Payment Channels

- Payment channels vary across branches
- Epay, Cash are the most common methods, and Card are the least common methods

5. Gross Income and Tax

- Higher gross income leads to higher tax

Key Insights

- Female customers drive sales in Fashion Accessories and Home and Lifestyle products
- Male customers dominate sales in Food and Beverages, Sports, and Travel
- Fashion Accessories command the highest unit price, while Health and Beauty products are the most affordable
- Payment channels differ across branches, with a preference for non-cash methods
- Gross income and tax have a direct correlation, indicating a potential opportunity for upselling and cross-selling

# Future Work

1. Segmentation Analysis: Perform customer segmentation based on demographics, behavior, and preferences to identify target audiences.

2. Predictive Modeling: Develop predictive models to forecast sales, customer churn, and response to marketing campaigns.

3. Product Recommendation: Implement a product recommendation system to suggest relevant products to customers based on their purchase history and preferences.
   
# Standout Section

I ensured that dates are properly extracted using the dt.day function, also used a line grap to identify the reason for an increase in tax rate By properly extracting dates using the dt.day function,i ensured accurate analysis of temporal trends. And, by using a line graph to investigate the increase in tax rate,i effectively visualized the data to identify potential causes.[Executive Summary pandas.docx](https://github.com/user-attachments/files/16947879/Executive.Summary.pandas.docx)



# Executive Summary.

To-Do - Include your Executive Summary document in your repository.
