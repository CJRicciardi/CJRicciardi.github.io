---
layout: Post
title: Kenosha, WI Real Estate Valuation Models
---

For my second build week I decided to call on my former career, Real Estate for inspiration, and see if we can predict home sale prices.  The data set used includes single-family home sales from April 2011 – February 2020 in Sommers, Pleasant Prairie and Kenosha, WI.  These are the three municipalities that lie predominantly east of I-95 in Kenosha County; they are so intermingled geographically that most do not make much distinction between the three.  
The target for the data set was painfully obvious, Sold Price, the sale price of the property.  Since this is a financial model, if deployed, the error in the model does not need to be penalized any more than the actual dollar amount that is incorrect by, thus mean absolute error (MAE) is the metric by which we will judge the models.  The average sale price for the data set is $169,975 which will be the base line prediction for the model.  The MAE when predicting the baseline for all sales is $108,608.  
The data set included a few columns that contained leakage, the original list price, list price, and taxes.  The original list price was the price the home was originally listed for sale at, and the list price is the price the home was listed at when it sold.  Both numbers reflect primarily a realtor’s best estimate of the sale price, although overzealous homeowners do from time to time insist on inflated pricing.  The third column that presented leakage was taxes.  Taxes are calculated from the properties assessed value multiplied by the tax rate.  
Models like these if valuable could be deployed to help realtors price homes, inform consumers, lenders or investors of a homes value.  In any of those cases relying on estimates of the home’s value would influence the model and negate its usefulness.  Assessors are known to be off by as much as 20% in a homes value.  Realtors and home sellers even with the best intentions can get overzealous in their pricing. I hope to one day use this model to determine flip and investment opportunities, which would require the model to find errors in these factors rather than be influenced by them.  
Three educational, but undeployable models were developed for this project.  The three models were a linear regression, random forest regression, and gradient boosted regression.  The three models had very similar MAE:
| Model | Validation MAE | Test MAE |
|:---|:---:|:---:|
| Linear Regression | $34,940 | $38,611 |
| Random Forest Regression | $35,440 | $44,109 |
| Gradient Boosted Regression |	$32,794 | $41,806 |
Models that miss home pricing by between 22.72% - 25.95% are undeployable.  
Following are a few visuals to help understand what the model used in its predictions.



