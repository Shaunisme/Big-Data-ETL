# Big-Data-ETL
Module 22

## Background
In this assignment, you will put your ETL skills to the test. Many of Amazon's shoppers depend on product reviews to make a purchase. Amazon makes these datasets publicly available. They are quite large and can exceed the capacity of local machines. One dataset alone contains over 1.5 million rows; with over 40 datasets, data analysis can be very demanding on the average local computer. Your first goal will be to perform the ETL process completely in the cloud and upload a DataFrame to an RDS instance. The second goal will be to use PySpark or SQL to perform a statistical analysis of selected data.

This Challenge contains two parts. Part 1 is required. Part 2 is optional but highly recommended.

* Part 1: Extract two Amazon customer review datasets, transform each dataset into four DataFrames, and load the DataFrames into an RDS instance.
* Part 2: Extract two Amazon customer review datasets and use either SQL or PySpark to analyse whether reviews from Amazon's Vine program are trustworthy.

## Instructions

### Part 1
1. Upload the part_one_starter_code.ipynb into Google Colab and create a duplicate of this file.

2. Explore the Amazon Reviews Links to an external site.datasets and pick two datasets to perform ETL.

3. Rename each part_one_starter_code.ipynb file according to the dataset you are using. For example, if you are going to use the Video Game reviews Links to an external site.file, rename file, part_one_video_games.ipynb. Repeat the process for the duplicate file you created in Step 2.

#### Extract the Data

1. Read in each dataset using the correct header and sep parameters.

2. Get the number of rows in each dataset.

#### Transform the Data

For each dataset use the schema.sql file located in the Resources folder of the Starter_Code.zip file to create the four DataFrames as follows:

1. Create the "review_id_df" DataFrame with the appropriate columns and data types.

2. Create the "products_df" DataFrame that drops the duplicates in the "product_id" and "product_title columns.

3. Create the "customers_df" DataFrame that groups the data on the "customer_id" by the number of times a customer reviewed a product.

4. Create the "vine_df" DataFrame that has the "review_id", "star_rating", "helpful_votes", "total_votes", and "vine" columns.

#### Load the Data into an RDS Instance

Export each DataFrame into the RDS instance to create four tables for each dataset.
![screen shot of load](image/Snipaste_2023-01-08_03-14-12.png "load")

