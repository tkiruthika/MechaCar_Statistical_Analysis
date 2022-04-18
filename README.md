# MechaCar_Statistical_Analysis

## Overview

The overview of this module is understanding of statistics and hypothesis testing to analyze a series of datasets from the automotive industry. Your analysis will include visualizations, statistical tests, and interpretation of the results. All of your statistical analysis and visualizations will be written in the R programming language.

## Purpose

Throughout the module, you'll extract, transform, and load (ETL) data; visualize the data; and analyze the data using R. Additionally, you'll learn a variety of statistical tests, their real-world application in data science, and their implementation in R. The goal is for you to apply these statistical concepts beyond this module, to any dataset, using any programming language—including Python.

## Deliverable 1

## Linear Regression to Predict MPG

Linear regression is performed using the lm() function. In the lm() function, all six variables(i.e., columns) are passed and the dataframe we created from our dataset is added as the data parameter.

![R1](https://user-images.githubusercontent.com/95719819/163742779-2852db85-c34c-4f34-aabe-995df40ad91d.png)

  - **Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?**
   
   The vehicle_length and ground_clearance variables greatly affects the significance over the vehicle_weight and spoiler_angle variables which provides a non random amount of variance to the mpg values within our dataset.
  
  - **Is the slope of the linear model considered to be zero? Why or why not?**
  
  The slope of the linear model is not considered to be zero, because the p-Value 5.35e-11, is much smaller than the assumed significance level of 0.05%. This indicates there is sufficient evidence to reject our null hypothesis.
  
  - **Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?**
  
  This linear model does predict mpg of MechaCar prototypes effectively, because this linear model has the r-squared value of 0.7149, which means that approximately 71% of all mpg predictions will be determined by this model.

## Deliverable 2

An RScript is written to create a total summary dataframe that has the mean, median, variance, and standard deviation of the PSI for all manufacturing lots.

![R2](https://user-images.githubusercontent.com/95719819/163744037-d3af33fe-6c8f-47f7-a0c0-68f146d4014d.png)

An RScript is written to create a lot summary dataframe that has the mean, median, variance, and standard deviation for each manufacturing lot 

![R3](https://user-images.githubusercontent.com/95719819/163744092-5b23d0e9-5427-48a7-a0a3-278384cab880.png)

## Summary Statistics on Suspension Coils

**The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?**

The current manufacturing data meet the design specification for all manufacturing lots in total, because the variance across all three lots is 62.29 PSI, which did not exceed the 100 PSI.

However, when examining the PSI of the suspension coils in the three lots seperately, the variance between Lot 1 & Lot 2 does meet the requirement of the suspension coil under 100 pounds per square inch whereas Lot 3 showed a variance above 100 pounds per square inch. The Lot 3 data showed a variance of 170.29 which does not meet the MechaCar specifications per the PSI.

## Deliverable 3

## T-Tests on Suspension Coils

  - **RScript is written using the t.test() function to determine if the PSI across all manufacturing lots is statistically different from the population mean of 1,500 pounds per square inch.**

![R4](https://user-images.githubusercontent.com/95719819/163745174-1d317d3a-6006-4ea7-a82f-73bd7c885e36.png)

#### Summary

The One Sample t-test of all the suspension coils in the manufacturing lots returns a p-value 0.06 which is higher than the common significance level of 0.05. Therefore, there is no enough evidence to reject the null hypothesis.

  - **Three more RScripts are written using the t.test() function and its subset() argument to determine if the PSI for each manufacturing lot is statistically different from the population mean of 1,500 pounds per square inch.**

![R5](https://user-images.githubusercontent.com/95719819/163745187-7c6c1f0d-8554-4f30-838b-8058b1e485e8.png)

#### Summary

  - The t-test for Lot 1 returned a p-value of 1, which is above the significance level of 0.05. Therefore, there is no enough evidence to reject the null hypothesis.
  - The t-test for Lot 2 returned a p-value of 0.60, which is also above the significance level of 0.05. Therefore, there is no enough evidence to reject the null hypothesis.
  - The t-test for Lot 3 returned a p-value of 0.04, which is below the significance level of 0.05. Therefore, there is enough evidence to reject the null hypothesis.

## Delieverable 4

## Study Design: MechaCar vs Competition

The study is to design the MechaCar vehicle to perform better than the general marketplace vehicles. To accomplish this goal we need to determine fuel efficiency, as well as fuel efficiency over time. The dataset must include general marketplace competitor's data for comparison.

  - **What metric or metrics are you going to test?**
 
  The metrics to test would be the fuel efficiency and engine compared to the competitors.
  
  - **What is the null hypothesis or alternative hypothesis?**
  
  The Null Hypothesis would be that MechaCars have same values for fuel efficiency compared to other competitors. The Alternative Hypothesis is that MechaCars have different values for fuel efficiency compared to other competitors.
  
  - **What statistical test would you use to test the hypothesis? And why?**

  In order to test our hypothesis, we could use analysis of variance (ANOVA) test, because it is most straightforward to compare the means of a continuous numerical variable across a number of groups (or factors in R).

  - **What data is needed to run the statistical test?**
  
  To run this statistical test we will need the MechaCars fuel efficiency data as well as the mean data from competitors.
