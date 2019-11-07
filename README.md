# Religious change preceded economic change in the 20th century
Data code and instructions to reproduce the findings for the paper "Religious change preceded economic change in the 20th century". Each of the numbered scripts in the root directory run a series of R and Python scripts that runs a chunk of the analysis in the paper.

Please cite: Ruck  D.J., Bentley  R.A. and Lawson  D.J. (2018). Religious change preceded economic change in the 20th century. Science Advances, 4(7).

**python code is python2**

**raw WEVS data too large to upload to this repository**

## Directories
data - data files required for analysis

R - all R scripts

python - all Python scripts

## Get raw data
European Values Survey https://www.gesis.org/en/services/data-analysis/international-survey-programs/european-values-study/

World Values Survey http://www.worldvaluessurvey.org/WVSContents.jsp

Maddison historic GDP data  https://www.rug.nl/ggdc/historicaldevelopment/maddison/releases/maddison-project-database-2018

## Derive cultural Factors using EFA from raw WEVS data 

Run the script "1construct_variables" to use EFA to learn nine cultural factors from raw World and European Values Survey data. This also constructs decade time series for GDP from raw Maddison historical GDP data. 

## Show that birth decade differences are independent of time period using model comparison

Run "2create_period_generation_matrices" to split the representative samples for each nation by birth decade and time period for the nine cultural factors. Then "3period_corrected_generational_trends" creates birth decade time series by averaging over all time periods and using linear imputation to mitigate missing time period bias. 

Run "4test_generational_trends_are_period_independent" to use model comparison to test if birth decade differences are independent of period effects.

## Run time-lagged linear regression model

Run the time series analysis and save results using "5multi_level_granger_causality".

