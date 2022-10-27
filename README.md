# Deliverable 1
## Linear Regression to Predict MPG
![Linear Regression Stats](../Desktop/Lin Reg Stats.png)
1. Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?

### A 95% confidence level is the standard for R, which means that the p-value should be greater than or equal to the alpha (0.05) to be statistically significant. The most significant (non-random) variables in this dataset which show a non-random effect on the MPG of the MechaCar are the __Vehicle Length__ and the __Ground Clearance__. A linear regression model run on this dataset found that both vehicle length and ground clearance both have significant p-values (less than 0.05). On the other hand, vehicle weight, spoiler angle, and All Wheel Drive (AWD) have insignificant p-values, which indicates a random amount of variance within the dataset.

### Coefficient P-values:
### vehicle_length (p≈0.000) < α (0.05)
### vehicle_weight (p=0.08) > α (0.05)
### spoiler_angle (p=0.31) > α (0.05)
### ground_clearance (p≈0.000) < α (0.05)
### AWD (p=0.19) > α (0.05)
###

2. Is the slope of the linear model considered to be zero? Why or why not?

### The p-value for this model (p=0.0000000000535) is much smaller than the minimum requirement for significance (0.05), so the null hypothesis can be rejected. The slope of the linear model cannot be considered zero because the model was as follows: _MPG = -0.01 (intercept) + 6.26 (vehicle length) + 0.001 (vehicle weight) + 0.069 (spolier angle) + 3.546 (ground clearance) + -3.41 (AWD)_

3. Does this linear model predict MPG of MechaCar prototypes effectively? Why or why not? 

### The model's R-squared is 0.7149, which means that just over 70% of the observed varation can be explained by this model, so this model does predict the MPG of MechaCar prototypes better than it does not predict them.

# Deliverable 2
## Summart Statistics on Suspension Coils 

1. The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch (PSI). Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

### The variance of the full lot coils is 62.29 PSI, which does not exceed the design specifications of 100 PSI. The individual lots (1 and 2) have PSI variances below the design specificaitons (0.97 and 7.46, respectively); however, lot 3 has a PSI variance well above the design specifications (170.28). Since lot 3 has a much higher variance than lots 1 and 2, it is dramatically increasing the full lot variance. If lot 3 were excluded, the full lot coil variance would be well below the design specifications.

# Deliverable 3
## T-Tests on Suspension Coils (All Manufacturing Lots and Individual Lots)

## T-Test for All Manufacturing Lots 
### A t-test was conducted to determine the effect of all manufacturing lots on MPG. The true mean of the sample is 1498.78 and has a p-value of 1.00. At a 95% confidence, there was not a statistically significant difference between the mean of all three manufacturing lots and the presumed population mean of 1500.00, so we __fail to reject the null hypothesis__.

### All Manufacturing Lots: p-value = 1.00, alpha = 0.05
### p > α, 1.00 > 0.05 


## T-Test for Lot 1

### A t-test was conducted to determine the effect of the first manufacturing lot on MPG. The true mean of the sample is 1500.00 and has a p-value of 0.00000000001568 (p < α). At a 95% confidence, there was  a statistically significant difference between the mean of the first manufacturing lot and the presumed population mean of 1500.00, so we __reject the null hypothesis__.

### Manufacturing Lot 1: p-value = 0.00000000001568, alpha = 0.05
### p < α, 0.00000000001568 < 0.05 

## T-Test for Lot 2
### A t-test was conducted to determine the effect of the second manufacturing lot on MPG. The true mean of the sample is 1500.20 and has a p-value of 0.0005911 (p < α). At a 95% confidence, there was  a statistically significant difference between the mean of the first manufacturing lot and the presumed population mean of 1500.00, so we __reject the null hypothesis__.

### Manufacturing Lot 2: p-value = 0.0005911, alpha = 0.05
### p < α, 0.0005911 < 0.05 

### T-Test for Lot 3
### A t-test was conducted to determine the effect of the third manufacturing lot on MPG. The true mean of the sample is 1496.14 and has a p-value of 0.1589.At a 95% confidence, there was not a statistically significant difference between the mean of all three manufacturing lots and the presumed population mean of 1500.00, so we __fail to reject the null hypothesis__.

### Manufacturing Lot 3: p-value = 0.1589, alpha = 0.05
### p > α, 0.1589 > 0.05 

# Deliverable 4
## Study Design: MechaCar vs Competition

__Variables__: Cost, City Fuel Efficiency (MPG), Highway Fuel Efficiency (MPG), Horse Power, Maintenance Cost, and Safety Rating 
__Research Questions__: 
    a. How does MechaCar and its competitor differ in cost?
    b. How does MechaCar and its competitor differ in city fuel efficiency?
    c. How does MechaCar and its competitor differ in highway fuel efficiency?
    d. How does MechaCar and its competitor differ in horse power?
    e. How does MechaCar and its competitor differ in maintenance cost?
    f. How does MechaCar and its competitor differ in safety rating?

1. What metric or metrics are you going to test?
    a. Cost
    b. City Fuel Efficiency
    c. Highway Fuel Efficiency
    d. Horse Power
    e. Maintenance Cost
    f. Safety Rating
2. What is the null hypothesis or alternative hypothesis?
    a.  __Cost:__ Null Hypothesis (H₀: μ1 = μ2): MechaCar's cost is not different from its competitor.
        Research Hypothesis (H₁: μ1 ≠ μ2 (non-directional)): MechaCar's cost is statistically different from its competitor.
        Research Hypothesis (H₁: μ1 < μ2 (directional)): MechaCar's cost is statistically lower than its competitor.
        Research Hypothesis (H₁: μ1 > μ2 (directional)): MechaCar's cost is statistically higher than its competitor.
    b.  __City Fuel Efficiency:__ Null Hypothesis (H₀): MechaCar's city fuel efficiency (MPG) is not different from its competitor.
        Research Hypothesis (H₁: μ1 ≠ μ2 (non-directional)): MechaCar's city fuel efficiency (MPG) is statistically different from its competitor.
        Research Hypothesis (H₁: μ1 < μ2 (directional)): MechaCar's city fuel efficiency (MPG) is statistically lower than its competitor.
        Research Hypothesis (H₁: μ1 > μ2 (directional)): MechaCar's city fuel efficiency (MPG) is statistically higher than its competitor.
    c.  __Highway Fuel Efficiency:__ Null Hypothesis (H₀): MechaCar's highway fuel efficiency (MPG) is not different from its competitor.
        Research Hypothesis (H₁: μ1 ≠ μ2 (non-directional)): MechaCar's highway fuel efficiency (MPG) is statistically different from its competitor.
        Research Hypothesis (H₁: μ1 < μ2 (directional)): MechaCar's highway fuel efficiency (MPG) is statistically lower than its competitor.
        Research Hypothesis (H₁: μ1 > μ2 (directional)): MechaCar's highway fuel efficiency (MPG) is statistically higher than its competitor.
    d.  __Horse Power:__ Null Hypothesis (H₀): MechaCar's horse power is not different from its competitor.
        Research Hypothesis (H₁: μ1 ≠ μ2 (non-directional)): MechaCar's horse power is statistically different from its competitor.
        Research Hypothesis (H₁: μ1 < μ2 (directional)): MechaCar's horse power is statistically lower than its competitor.
        Research Hypothesis (H₁: μ1 > μ2 (directional)): MechaCar's horse power is statistically higher than its competitor.
    e.  __Maintenance Cost:__ Null Hypothesis (H₀): MechaCar's maintenance cost is not different from its competitor.
        Research Hypothesis (H₁: μ1 ≠ μ2 (non-directional)): MechaCar's maintenance cost is statistically different from its competitor.
        Research Hypothesis (H₁: μ1 < μ2 (directional)): MechaCar's maintenance cost is statistically lower than its competitor.
        Research Hypothesis (H₁: μ1 > μ2 (directional)): MechaCar's maintenance cost is statistically higher than its competitor.
    f.  __Safety Rating:__ Null Hypothesis (H₀): MechaCar's safety rating is not different from its competitor.
        Research Hypothesis (H₁: μ1 ≠ μ2 (non-directional)): MechaCar's safety rating is statistically different from its competitor.
        Research Hypothesis (H₁: μ1 < μ2 (directional)): MechaCar's safety rating is statistically lower than its competitor.
        Research Hypothesis (H₁: μ1 > μ2 (directional)): MechaCar's safety rating is statistically higher than its competitor.
3. What statistical test would you use to test the hypothesis? And why?
    I would use t-tests for all of these hypotheses to compare the means of the two groups (MechaCar and its competitor). 
4. What data is needed to run the statistical test?
    Data on MechaCar's competitor's cost, city and highway fuel efficiency, horse power, maintenance cost, and safety rating is needed. It would be better if MechaCar can get data on more than one of its competitors. 

