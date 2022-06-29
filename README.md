# Amazon Vine Video Game Reviews Analysis

## Overview
---
The purpose of this project is to clean and analyze raw Amazon Reviews data to determine whether reviews written as part of the Amazon Vine program are more likely to be positive.

### What is Amazon Vine?
>Amazon Vine invites the most trusted reviewers on Amazon to post opinions about products to help their fellow customers make informed purchase decisions. Amazon invites customers to become Vine Voices based on the insightful reviews they published on their past purchases and helpfulness of their reviews. Amazon offers Vine members free products that have been submitted to the program by participating selling partners. Vine reviews are the independent opinions of the Vine Voices and the selling partners cannot influence, modify or edit the reviews.

*pulled from https://www.amazon.com/vine/about*

## The Data
---
The raw data used in this project came from an S3 bucket hosted on AWS. The dataset I chose to use for this project was the US video game reviews dataset. 

*The data source*<br>
https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Video_Games_v1_00.tsv.gz

*Data Schematic*
![Data Schematic](images/data_schema.png)

## ETL of the Data
---

### Creating Amazon RDS database and connecting to PgAdmin
1. Created Amazon RDS database to store data
2. Connected PgAdmin to Amazon RDS
3. Created new database in PgAdmin on Amazon RDS server
4. In PgAdmin, created tables according to `challenge_schema.sql` file
    * `customers_table`, `products_table`, `review_id_table`, `vine_table`

### Extract
