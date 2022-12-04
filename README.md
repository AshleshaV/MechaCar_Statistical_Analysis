

# MechaCar_Statistical_Analysis

## Linear Regression to Predict MPG
The image shows the results of producing a linear regression model to predict MPG from the MechaCar_mpg dataset. Of these variables, vehicle length and ground clearance provided a non-random amount of variance to the mpg values in the dataset shown by their low p-values. 

 This model predicts the mpg of MechaCar protoypes effectively because the Adjusted R-squared reflects that ~68.25% of the variation within mpg is explained by the coefficients.

### Linear Regression to Predict MPG
![linear_regression_summary](https://github.com/AshleshaV/MechaCar_Statistical_Analysis/blob/main/linear_regression_summary.PNG?raw=true)


Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
A 95% level of confidence was predetermined, meaning the p-value should be compared to alpha = .05 level of significance to verify if statistically significant.
Coefficients:
mpg: 0 < .05, statistically significant, non-random amount of variance
vehicle length: 0 < .05, statistically significant, non-random amount of variance
vehicle weight: .08 > .05 not statistically significant, random amount of variance
spoiler angle: .31 > .05 not statistically significant, random amount of variance
ground clearance: 0 > .05 statistically significant, non-random amount of variance
AWD: .19>=.05 not statistically significant, random amount of variance

In summary, vehicle length and ground clearance variables represent non-random amounts of variance as applied to the mpg values.

Is the slope of the linear model considered to be zero? Why or why not?
Converting from scientific notation, all of the slopes of the variables are shown to be non-zero even though some are close to zero:
Coefficients:
vehicle length: 6.267
vehicle weight: .001
spoiler angle: .069
ground clearance: 3.546
AWD: -3.411

The multiple linear regression formula for mpg = -.01 + 6.267(vehicle length)+.001(vehicle weight)+.069(spoiler angle)+3.546(ground clearance)-3.411(AWD), which results in a non-zero slope.

Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
R-squared is .7149, which is a strong correlation for the dataset and shows the dataset is an effective dataset. However, r-squared is not the only consideration for effectiveness. There may be other variables not included in the dataset contributing to the variation in the mpg.

## Summary Statistics on Suspension Coils
Summary statistics of the mean, median, variance, and standard deviation of the PSI for the suspension coils overall and for the manufacturing lots. The design specifications for the MechaCar suspension coils shows that the variance of the suspension coils must not exceed 100 pounds per square inch (PSI). 

However, the lot summary shows that while manufacturing Lots 1 and 2 meet the design specifications and have variances under 100 PSI, Lot 3 does not meet the design specifications as its variance is much over the 100 PSI limit.

### Total Summary
![suspension_coils_total_summary](https://github.com/AshleshaV/MechaCar_Statistical_Analysis/blob/main/suspension_coils_total_summary.png?raw=true)

### Lot Summary
![suspension_coils_lot_summary](https://github.com/AshleshaV/MechaCar_Statistical_Analysis/blob/main/suspension_coils_lot_summary.png?raw=true)



The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?
The variance for the total manufacturing lot is 62 < 100, which is within the expected design specifications of staying under 100 PSI. However, when reviewing the data by Lot number, Lot 3 is a large contributing factor to the variance being high. Lot 3 shows a variance of 170 > 100 and does not meet the design specifications. Lot 1 and Lot 2 have significantly lower variance, 1 and 7 respectively.



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

Lot 1: p-value = 1, alpha = .05
1 > .05, which means Lot 1 is not statistically significant from the normal distribution and normality can be assumed. The mean falls within the 95% confidence interval.

### Lot2 Suspension Coil T-Test:
![lot2_t_test](https://github.com/AshleshaV/MechaCar_Statistical_Analysis/blob/main/lot2_t_test.PNG?raw=true)

-Lot 2: p-value = .6072, alpha = .05

.60 > .05, which means Lot 2 is not statistically significant from the normal distribution and normality can be assumed. The mean falls within the 95% confidence interval.

### Lot3 Suspension Coil T-Test:
![lot3_t_test](https://github.com/AshleshaV/MechaCar_Statistical_Analysis/blob/main/lot3_t_test.PNG?raw=true)

Lot 3: p-value = .04168, alpha = .05
.04 < .05, which means it is statistically significant from the normal distribution and normality cannot be assumed. However, the mean falls within the 95% confidence interval.

The overall manufacturing, Lot 1, and Lot 2 show a normal distribution. Therefore, there is not sufficient evidence to reject the null hypothesis, which shows the two means are statistically similar.




## Study Design: MechaCar vs Competition
-To summarize, 
When comparing MechaCar to its competitor’s other metrics that could be of interest to a consumer could include car color, fuel efficiency, horsepower, maintenance cost, or safety rating.

What metric or metrics are you going to test?
The next metrics to test should be the safety rating, horsepower, and fuel efficiency, which address some safety concerns of consumers.

What is the null hypothesis or alternative hypothesis?
The null hypothesis is that the mean of the safety rating is zero. 
The alternative hypothesis is that the mean of the safety rating is not zero.

What statistical test would you use to test the hypothesis? And why?
Using a multiple linear regression statistical summary would show how the variables impact the safety ratings for MechaCar and their competitors.

What data is needed to run the statistical test?
 A random sample greater than 30 need to be collected including the safety ratings, fuel efficiency, and horsepower and  then analysing the datain RStudio.
