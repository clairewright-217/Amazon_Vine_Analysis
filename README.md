# Amazon_Vine_Analysis

## Overview of Vine Program

The purpose of this exercise was to evaluate the paid versus unpaid customer reviews of a product line sold on Amazon. A dataset of reviews for [Toys products](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt) sold on Amazon was used. 

Before conducting the analysis, the data was extracted, transformed, and loaded into tables in pgAdmin from an AWS RDS database created for this. The following screenshots show that the tables created in pgAdmin were successfully populated with transformed data from the Amazon S3 bucket via the AWS RDS database. 

![customers_table](/Resources/customers_table.png)

![products_table](/Resources/products_table.png)

![review_id_table](/Resources/review_id_table.png)

![vine_table](/Resources/vine_table.png)

## Results of Reviews Analysis

**Vine Reviews of Toys Sold on Amazon, Results**
![Paid Reviews Analysis](/Resources/Paid_Reviews.png)

**Non-Vine Reviews of Toys Sold on Amazon, Results**
![Unpaid Reviews Analysis](/Resources/Unpaid_Reviews.png)

- How many Vine reviews and non-Vine reviews were there?
There were 1266 Vine reviews and 61849 non-Vine reviews, so almost 50x more unpaid versus paid for product reviews of Toys sold on Amazon.

- How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
There were 432 five-star Vine reviews and 29950 five-star non-Vine reviews.

- What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
The percentage of five-star Vine reviews out of the total number of Vine reviews is 34%, compared to 48% of total non-Vine reviews are five-stars. 

## Summary

From the results, it does not appear that the Vine program, which paid people who purhcased Toys on Amazon to leave a review, caused a positivity bias in the reviews. The non-Vine reviews, that is reviews that users were not paid to give, had 14% more five-star reviews than the Vine reviews. 

Another analysis I would conduct next to evaluate if there is any positivity bias in the reviews of the Vine program is to make a histogram of total number of reviews per each star rating, one for Vine reviews and the other for non-Vine reviews. This would show the number of reviews that left 1 star, 2 stars, 3 stars, 4 stars, or 5 stars among the two reviewer groups. I would want to see similar distributions of star ratings between the two groups, or at least not a huge difference in the frequency of negative and positive reviews between Vine and non-Vine reviews. For example, even if the percentage of five-star reviews is higher among the non-Vine group, if the number of one-star reviews is also much higher in this group, that could still indicate that there is a positivity bias among paid reviews. 