

# MechaCar_Statistical_Analysis

## Linear Regression to Predict MPG
The image shows the results of producing a linear regression model to predict MPG from the MechaCar_mpg dataset. Of these variables, vehicle length and ground clearance provided a non-random amount of variance to the mpg values in the dataset shown by their low p-values. 

 This model predicts the mpg of MechaCar protoypes effectively because the Adjusted R-squared reflects that ~68.25% of the variation within mpg is explained by the coefficients.

### Linear Regression to Predict MPG
![linear_regression_summary](https://github.com/AshleshaV/MechaCar_Statistical_Analysis/blob/main/linear_regression_summary.PNG?raw=true)

## Summary Statistics on Suspension Coils
Summary statistics of the mean, median, variance, and standard deviation of the PSI for the suspension coils overall and for the manufacturing lots. The design specifications for the MechaCar suspension coils shows that the variance of the suspension coils must not exceed 100 pounds per square inch (PSI). 

However, the lot summary shows that while manufacturing Lots 1 and 2 meet the design specifications and have variances under 100 PSI, Lot 3 does not meet the design specifications as its variance is much over the 100 PSI limit.

### Total Summary
![suspension_coils_total_summary](https://github.com/AshleshaV/MechaCar_Statistical_Analysis/blob/main/suspension_coils_total_summary.png?raw=true)

### Lot Summary
![suspension_coils_lot_summary](https://github.com/AshleshaV/MechaCar_Statistical_Analysis/blob/main/suspension_coils_lot_summary.png?raw=true)



## T-Tests on Suspension Coils
T-tests were run on the suspension coil data to determine if all manufacturing lots, and each lot individually, are statistically different from the population mean of 1,500 pounds per square inch (PSI). The results of the t-tests across all lots and each individual lot shown in the images.

### Overall Suspension Coil T-Test:
![suspension_coil_t_test](https://github.com/AshleshaV/MechaCar_Statistical_Analysis/blob/main/suspension_coil_t_test.PNG?raw=true)

-The results of the t-test to test if the PSI across all manufacturing lots is statistically different from the population mean of 1,500 pounds per square inch show that, at a 95% confidence level, the two means are not statistically different,
-p-value of 0.06028 is higher than the critical value of 0.05,
-There is no difference between the means of the PSI for the population and overall manufacturing lot sample accepting the null hypothesis, 
-The means within the 95% confidence range are between 1497.5 and 1500 PSI.

### Lot1 Suspension Coil T-Test:
![lot1_t_test](https://github.com/AshleshaV/MechaCar_Statistical_Analysis/blob/main/lot1_t_test.PNG?raw=true)

The results of the t-test to test if the PSI mean for Lot1 show that, the two means are not statistically different. 
The p-value of 1 shows that the mean for Lot1 is exactly the same as the population mean of 1500 PSI.

### Lot2 Suspension Coil T-Test:
![lot2_t_test](https://github.com/AshleshaV/MechaCar_Statistical_Analysis/blob/main/lot2_t_test.PNG?raw=true)

-The results of the t-test to test if the PSI mean for Lot2 show that, the two means are not statistically different. 
with the p-value of 0.6072 is higher than the critical value of 0.05. 
-The null hypothesis can be accepted in that there is no difference between the means of the PSI for the population and Lot2.
-The means within the 95% confidence range are between 1499.423 and 1500.977 PSI.

### Lot3 Suspension Coil T-Test:
![lot3_t_test](https://github.com/AshleshaV/MechaCar_Statistical_Analysis/blob/main/lot3_t_test.PNG?raw=true)

-The results of the t-test to test if the PSI mean for Lot3 show that, the two means are statistically different with the p-value of 0.04168 is lower than the critical value of 0.05,
-The null hypothesis should be rejected in that there is a difference between the means of the PSI for the population and Lot3 and the true mean is not equal to 1500. -The means within the 95% confidence range are between 1492.431 and 1499.849 PSI.


## Study Design: MechaCar vs Competition
-To summarize, an independent t-test could be used to compare the safety ratings of MechaCar against the competition.
-An independent t-test could be used to compare the means of the MechaCar and the competition, to determine whether the population means are significantly different. --To run this statistical test, ordinal data on the safety ratings for each group would be more beneficial.
-Further analysis could  be done using the results from the t-test, the alternative hypothesis would be useful to find the difference in the safety ratings between those two groups.
