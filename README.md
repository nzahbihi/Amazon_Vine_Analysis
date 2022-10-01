# Amazon_Vine_Analysis
## Overview
The purpose of this analysis is to investigate Amazon's video game data, specifically pertaining to the Vine program. Our goal is to determine if there is any bias towards favorable reviews from Vine members.

## Resources
* Data Source: vine_table.csv, [Amazon Review Data](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt)
* Services: Amazon RDS, Google Colaboratory
* Software: Jupyter Notebook 6.4.8, PostgreSQL 11.16

## Results
We first reviewed how many Vine reviews, and non-Vine reviews there were.

![vine_reviews](https://user-images.githubusercontent.com/106129195/193376398-98d762ec-9338-46da-8189-4140d9e173f0.png)

##### Number of Vine reviews.

![not_vine_reviews](https://user-images.githubusercontent.com/106129195/193376401-8451a216-d0b8-4626-a556-37f9d430f257.png)

##### Number of Non-Vine reviews.

As we can see, there is a drastic difference between the two. There are thousands of reviews that are outside of the Vine program, and less than 100 for the Vine program.

Next, let us investigate how many of the Vine reviews were 5 stars, versus how many non-Vine reviews were 5 stars.

![vine_5_stars](https://user-images.githubusercontent.com/106129195/193376638-b51ddd45-93b3-4bac-b47a-52138d14678b.png)

##### Number of 5 star reviews from the Vine program.

![non_vine_5_stars](https://user-images.githubusercontent.com/106129195/193376642-96e40f05-e3da-40ee-adae-d9994d87b24f.png)

##### Number of 5 star reviews outside the Vine program.

We can see that there are still thousands of reviews for those outside the Vine program, and fewer for the Vine program.

With this data provided, we calculated the percentages of how many Vine reviews were 5 stars, and how many non-Vine reviews were 5 stars.

![percentages](https://user-images.githubusercontent.com/106129195/193376807-2eb0d127-243b-40ac-a054-ba2faaff07a9.png)

##### Percentages of the 5 star reviews.

For the Vine program, 51.1% of reviews were 5 stars. Outside of the Vine program, 38.7% of reviews were 5 stars.

## Summary
Based on the results shown above, over 50% of reviews from the Vine program are 5 stars. In contrast, 38.7% of reviews from outside the Vine program are 5 stars. We can see that there is a difference of 12.4% between the two, which is significant. Therefore, we can deduce that there is a degree of positivity bias with the Vine program reviews within the video game category of Amazon.

To further explore this bias, an additional analysis that could be conducted is including customer ID information and count. If we counted how many unique reviews there are for each customer ID, and compare that information to 5 star ratings and whether that customer is in the Vine program, we could investigate if there are specific customers repeatedly contributing to this bias.
