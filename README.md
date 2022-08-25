# MechaCar Statistical Analysis

### Overview

In this analysis we identify the production problems with Mechacar by performing multiple linear regression analysis on different variables in the dataset to predict the mpg of MechaCar prototypes. Summary statistics on the PSI of suspension coils are collected and T-tests are run to determine if manufacturing lots are different from the mean population. A statistical study is also designed to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers.

### Resources

  - MechaCar MPG dataset
  - Suspension Coil dataset

### Tools Used

  - R and RStudio
  - dplyr library

### Deliverable - 1: Linear Regression to Predict MPG

  _Linear Regression Results_
  
  ![Linear_Regression_Model](https://user-images.githubusercontent.com/106279653/186502580-6459484d-650f-46e1-b180-9ee43bae1606.JPG)


   _Statistical Summary_
   
   ![Summary_Statistics](https://user-images.githubusercontent.com/106279653/186505605-70a1414b-b709-4c10-b077-5164e42728df.JPG)

  _Summary_
  
   - Vehicle length and ground clearance (as well as intercept) are statistically unlikely to provide random amounts of variance to the linear model.
   - As the p-value is 5.35e-11, which is much smaller than the assumed significance level of 0.05%, we can reject our null hypothesis, indicating the slope of the linear model is not zero.
   - The R-squared value of the model is 0.714, which means that roughly 71% of the variability of MPG is explained using this linear model. Implying this model effectively predicts the mpg of MechaCar prototypes.


### Deliverable - 2: Summary Statistics on Suspension Coils

  _Total summary for all manufacturing lots_
  
  ![Total_Summary](https://user-images.githubusercontent.com/106279653/186514256-d0f65ddf-7131-42c8-adb5-d0cbd62fa85f.JPG)
  
  
  _Lot summary for each manufacturing lot_

  ![Lot_Summary](https://user-images.githubusercontent.com/106279653/186514440-6a47c292-e895-4348-9bd3-563c8be0c697.JPG)
  
  
  - In total for all manufacturing lots the variance is 62.29 which meets the design specification of variance not exceeding 100 PSI
  - Lot wise - Lots 1 & 2 meet the design specification of variance under 100 PSI but for Lot 3 the variance is 170.3, which is significantly higher than the limit of 100 PSI.


### Deliverable - 3: T-Tests on Suspension Coils

  _T-Test comparing all manufacturing lots against mean PSI._
  
  ![T-Test_all_Lots](https://user-images.githubusercontent.com/106279653/186517588-70b1ddac-9cee-4cb1-90fa-dad962dbe337.JPG)


  _T-Test for lot wise comparison against mean PSI._
  
   *_Lot-1_*
   
  ![T-Test_Lot_1](https://user-images.githubusercontent.com/106279653/186517823-af33cc80-9527-4176-b696-81b9da6f5d69.JPG)

  *_Lot-2_*
  
  ![T-Test_Lot_2](https://user-images.githubusercontent.com/106279653/186517978-8d6cf959-1568-4738-8181-2b944dbaa2b5.JPG)

  *_Lot-3_*
  
  ![T-Test_Lot_3](https://user-images.githubusercontent.com/106279653/186518023-b9491ac0-35c1-4c70-9cbb-7e07d712db2d.JPG)


  - For all lots our p-value is slightly above the significance level, therefore we cannot reject the null hypothesis, implying the two means are statistically similar.
  - For lot-1 only, p-value is higher than the significance level of 0.05, therefore the two means are statistically similar.
  - For lot-2 only, p-value is higher than the significance level of 0.05, therefore the two means are statistically similar.
  - For lot-3 only, p-value is lower than the significance level of 0.05, therefore the two means are not statistically similar indicating the PSI values in this lot vary significantly indicating possible manufacturing problems.


### Deliverable - 4: Study Design: MechaCar vs Competition

#### Metrics to be tested:
   - Fuel efficiency based on fuel type and horse power of MechaCar and the Competition
    
#### Hypothesis:

   - Null Hypothesis: The means of all groups are equal.
   - Alternate Hypothesis: At least one of the means is different from all other groups. 
  
#### Type of test:

  A two way ANOVA test will be required to test the means of a single dependent variable (Fuel efficiency) across two independent variables (fuel type & horse power) within multiple groups.
  
#### Data Required:

  - Fuel efficiency sample data
  - Fuel type data
  - Horse power data
  

