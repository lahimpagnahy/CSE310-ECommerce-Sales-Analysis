E-Commerce Sales Analysis with Python and Pandas
Overview

This project was created for the CSE 310 Applied Programming course at BYU-Idaho through BYU-Pathway Worldwide.

The purpose of this project is to learn and demonstrate data analysis using Python and the Pandas library. The program analyzes an e-commerce sales dataset and uses data cleaning, filtering, sorting, grouping, aggregation, data conversion, and data visualization.

The project answers three questions about the dataset:

Which product categories generate the most revenue?

Which regions have the highest average order value?

Which products have the highest number of units sold?

Dataset

The dataset used for this project is the Global E-Commerce Sales & Customer Analytics dataset from Kaggle.

The dataset contains e-commerce order information including:

Order ID

Order Date

Customer Name

Customer Segment

Country

Region

Product Category

Product Name

Quantity

Unit Price

The dataset contains sales records covering multiple countries, regions, customer segments, and product categories.

Dataset source:

https://www.kaggle.com/code/muhammadaammartufail/global-e-commerce-sales-customer-analytics/input

Technologies Used

Python 3

Pandas

Matplotlib

CSV

Git

GitHub

Installation

Make sure Python 3 is installed on your computer.

Install the required libraries with:

pip install -r requirements.txt

Project Structure
CSE310-ECommerce-Sales-Analysis/
│
├── data/
│   └── global_ecommerce_sales.csv
│
├── output/
│   └── sales_by_category.png
│
├── main.py
├── README.md
└── requirements.txt

How to Run the Program

Clone or download the repository.

Open a terminal in the project folder.

Install the required libraries:

pip install -r requirements.txt


Run the program:

python main.py


The program will load and clean the dataset, perform the requested analyses, display the results in the terminal, and create a revenue-by-category graph.

Question 1: Which product categories generate the most revenue?

The program groups the dataset by Product_Category.

It calculates:

Total revenue

Total units sold

Number of orders

The program uses the Pandas groupby() and agg() functions to aggregate the data. It then uses sort_values() to sort the categories from the highest revenue to the lowest revenue.

The first category in the resulting sorted data represents the category with the highest total revenue.

Question 2: Which regions have the highest average order value?

The program groups the dataset by Region.

For each region it calculates:

Total revenue

Average order value

Total units

Number of orders

The average order value is calculated using the Pandas mean() aggregation.

The regions are then sorted from the highest average order value to the lowest.

Question 3: Which products have the highest number of units sold?

The program groups the data by Product_Name.

It calculates:

Total units sold

Total revenue

Number of orders

The products are sorted by total units sold, and the top ten products are displayed.

Data Cleaning and Conversion

Before analyzing the data, the program performs several preparation steps.

The Order_Date column is converted from text to a Pandas datetime value.

The Quantity and Unit_Price columns are converted to numeric values.

The program creates a new Revenue column using:

Revenue = Quantity × Unit Price


Duplicate records are removed.

Rows containing missing or invalid values required for analysis are removed.

The program also filters out records with zero or negative quantities and prices.

Filtering

The program demonstrates filtering by identifying orders whose revenue is greater than the average order revenue.

This demonstrates how Pandas can select specific records based on a condition.

Sorting

The project uses sorting in several analyses.

For example, category revenue is sorted from highest to lowest:

.sort_values(
    by="total_revenue",
    ascending=False
)


This makes it possible to identify the categories with the largest revenue.

Aggregation

The project demonstrates several Pandas aggregation operations:

sum()

mean()

count()

These operations are used to calculate revenue, units sold, average order values, and order counts.

Data Conversion

The project converts:

Order dates from strings to datetime values

Quantities to numeric values

Unit prices to numeric values

The converted dates are also used to extract the year and calculate yearly revenue.

Visualization

The program creates a horizontal bar chart showing revenue by product category.

The chart is created using Matplotlib and saved in the output folder.

The output file is:

output/sales_by_category.png

Video Demonstration

The required CSE 310 demonstration video is available here:

www.youtube.com/

The video demonstrates the program running and provides a walkthrough of the source code. My face is visible during the presentation as required by the course.

What I Learned

During this module I learned how to use Python and Pandas to work with a real-world-style dataset.

I learned how to load CSV data into a DataFrame, inspect the data, clean invalid records, convert data types, filter records, group data, calculate statistics, sort results, and create a visualization.

I also learned that data analysis requires careful preparation before calculations are performed. Converting dates and numeric values and handling missing or duplicate data are important because incorrect data types or invalid records can produce misleading results.

Future Improvements

If I continued developing this project, I would add additional visualizations, such as monthly revenue trends and regional revenue charts.

I could also add an interactive interface that allows a user to select a region or product category and view the corresponding analysis.

Author

Student: Andrianasy Jean Rossy Lahimpagnahy

Course: CSE 310 - Applied Programming

Module: Data Analysis

Language: Python
