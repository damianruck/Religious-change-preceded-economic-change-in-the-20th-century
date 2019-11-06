# Religious-change-preceded-economic-change-in-the-20th-century

## Derive cultural Factors using EFA from raw WEVS data 

Run the script "1construct_variables" to use EFA to learn nine cultural factors from raw World and European Values Survey data. 

## Show that birth decade differences are independent of time period using model comparison

Run "2create_period_generation_matrices" to split the representative samples for each nation by birth decade and time period for the nine cultural factors. Then "3period_corrected_generational_trends" creates birth decade time series by averaging over all time periods and using linear imputation to mitigate missing time period bias. Run "4test_generational_trends_are_period_independent" to use model comparison to test if birth decade differences are indepedent of period effects.

converts all the nation matrices into a dataframe to be used in the model comparison. Then run "kfoldModelComparison.R" which compares hierarchical linear regressions of increasing complexity, testing whether birth decade differences are independent of time period.

## run time-lagged linear regression model

Run the time series analysis and save results using "5multi_level_granger_causality".

