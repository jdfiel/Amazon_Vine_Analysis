# Amazon_Vine_Analysis

## Overview

The purpose of this analysis is to determine if paid Vine reviews in Amazon feature a positivity bias. This will be done by analyzing one of ~50 datasets and comparing the Vine reviews to normal reviews.

For this analysis we will be looking at video game reviews.

## Results

To conduct the analysis, we filtered our reviews into multiple stages. First, we filtered out potentially useless or misleading reviews based on vote count. Any vote with less than 20 votes was filtered out. To further ensure that the reviews we would receive we actually useful, reviews that were voted to be useful by less than 50% of their total votes were filtered out.

The results were as follows:

![results]()

* In total there were 37,921 reviews
* 44 Vine reviews were 5 stars
* 14,704 non-Vine reviews were 5 stars
* 48.89% of Vine reviews were 5 stars
* 38.87% of non-Vine reviews were 5 stars

Below, are the steps taken to filter the raw Vines data.

![results](https://github.com/jdfiel/Amazon_Vine_Analysis/blob/main/Resources/results.png)

![raw_df](https://github.com/jdfiel/Amazon_Vine_Analysis/blob/main/Resources/raw_df.png)

![filtered](https://github.com/jdfiel/Amazon_Vine_Analysis/blob/main/Resources/filtered.png)

![helpful](https://github.com/jdfiel/Amazon_Vine_Analysis/blob/main/Resources/helpful.png)

![paid](https://github.com/jdfiel/Amazon_Vine_Analysis/blob/main/Resources/paid.png)

![unpaid](https://github.com/jdfiel/Amazon_Vine_Analysis/blob/main/Resources/unpaid.png)



## Summary 

Based on the results of the analysis, it is _possible_ that a positivity bias exists as the number of 5 star Vine reviews does exceed the non-Vine reviews by just over 10% -- a significant number.

However, looking at the sample size of the total number of Vine reviews, it is very likely that the sample is simply too small. given a larger data set to properly compare it to, it may be that there is no positivity bias.

To test his, we could look at the mean and medians of our dataset. Performing a linear regression may help to better establish whether or not there is a positivity bias. It may be that Vine reviewers are simply more polarized and that 51.11% of Vine reviewers all left a 1 star review. Our analysis wouldn’t capture that type of, admittedly, extreme behaviour.