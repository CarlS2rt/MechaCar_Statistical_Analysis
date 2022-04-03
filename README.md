# MechaCar Statistical Analysis

## Linear Regression to Predict MPG

![](C:\Users\carla\OneDrive\Documents\GitHub\MechaCar_Statistical_Analysis\image-20220403123528447.png)

### Non-random Variance Coefficients

The coefficients that provided a non-random amount of variance to the mpg linear model are vehicle length and ground clearance (as well as intercept). The intercept term explains a significant amount of variability in the dependent variable when all independent variables are equal to zero. The significant intercept in the model could indicate that the significant features, length and ground clearance, may need scaling to help improve the model. Alternately, the significant intercept could suggest that other coefficients outside the model could explain the variability of miles per gallon.

### Slope of the Linear Model

The slope of the linear model is considered non-zero because some of the independent variables show significant effect on the dependent variable. If none of the independent variables had shown significant effect on the dependent variable, the slope of the model would be considered zero, which would affirm the null hypothesis. 

### Linear Model Predictive Power

The linear model effectively predicts the miles per gallon of MechaCar prototypes because the R-squared value is sufficiently close to 1. The closer the R-squared value is to 1, the higher the model's predictive power. In this case, the R-squared value is 0.715, which explains a large portion of the variance in the outcome variable. Additionally, the adjusted R-squared value of 0.683 still explains a large portion of variance even when accounting for the number of independent variables. 

## Summary Statistics on Suspension Coils

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch (psi). The summary data for suspension coil performance shows that the current manufacturing data does meet design specifications. 

<img src="C:\Users\carla\OneDrive\Documents\GitHub\MechaCar_Statistical_Analysis\image-20220403134654421.png" style="zoom:200%;" />

Additionally, the manufacturing data shows that Lots 1 and 2 are meeting the design specifications, but Lot 3 is not meeting them. The variance in Lot 3 is 170.29 whereas the variance in Lots 1 and 2 are 0.98 and 7.47 respectively.  

<img src="C:\Users\carla\OneDrive\Documents\GitHub\MechaCar_Statistical_Analysis\image-20220403135114952.png" style="zoom:150%;" />

## T-Tests on Suspension Coils

Using T-Tests, we can determine if the mean of the total and lot datasets is statistically different from the population mean of 1500. The PSI across all manufacturing lots is not statistically different from the population mean because the p-value of 0.06028 is not significant, so the null hypothesis cannot be rejected. 

<img src="C:\Users\carla\OneDrive\Documents\GitHub\MechaCar_Statistical_Analysis\image-20220403141844146.png" style="zoom:150%;" />

The PSI of manufacturing Lot 1 is not statistically different from the population mean because the p-value of 1 is not significant, so the null hypothesis cannot be rejected. 

<img src="C:\Users\carla\OneDrive\Documents\GitHub\MechaCar_Statistical_Analysis\image-20220403142100833.png" style="zoom:150%;" />

The PSI of manufacturing Lot 2 is not statistically different from the population mean because the p-value of 0.6072 is not significant, so the null hypothesis cannot be rejected. 

<img src="C:\Users\carla\OneDrive\Documents\GitHub\MechaCar_Statistical_Analysis\image-20220403142210123.png" style="zoom:150%;" />

The PSI of manufacturing Lot 3 is statistically different from the population mean because the p-value of 0.04168 is below our significance level of 0.05, so there is sufficient evidence to reject the null hypothesis. 

<img src="C:\Users\carla\OneDrive\Documents\GitHub\MechaCar_Statistical_Analysis\image-20220403142504697.png" style="zoom:150%;" />

## Study Design: MechaCar vs Competition

A statistical study that could quantify how MechaCar performs against competing manufacturers should be designed to determine how interested consumers would be in MechaCar. The study should focus on metrics that influence consumer car purchases, such as cost and city & highway fuel efficiency. 

For the metrics listed, the null hypotheses and alternative hypotheses are as follows:

- Cost: The null hypothesis is there is no difference in cost between MechaCar and competitor cars of the same class. The alternative hypothesis is there is a difference in cost.
- City Fuel Efficiency: The null hypothesis is there is no difference in city fuel efficiency between MechaCar and competitor cars of the same class. The alternative hypothesis is there is a difference in city fuel efficiency.
- Highway Fuel Efficiency: The null hypothesis is there is no difference in highway fuel efficiency between MechaCar and competitor cars of the same class. The alternative hypothesis is there is a difference in highway fuel efficiency.

The study should use an ANOVA analysis to determine if there is a statistical difference between the distribution means from the sample of MechaCar and competitor cars in the same class. The analysis should be done for each measure to determine if there is any statistical difference present. To help visualize the data findings, ggplot2 should be employed to show boxplots of the representative data. To complete this analysis, datasets should be created containing the cost values (MSRP, mean selling price, resale value) and city and highway fuel efficiency ratings for each competitor car in the same class as MechaCar. 