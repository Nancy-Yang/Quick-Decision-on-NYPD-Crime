This is the ReadMe file for “Quick Decision” Machine Learning final project created by Prasanth Bathae Kumaresh, Nancy Yang and Hao Zheng.

This model uses crime data provided by NYPD to adjudicate the risk from an incoming 911 call. The input file is downloaded from “https://catalog.data.gov/dataset/nypd-shooting-incident-data-historic”

The accompanying ‘.ipynb’ file has the following attributes:

- Exploratory data analysis
- feature pre-processing
- feature selection
- model selection through pipelining and GridSearchCV
- final model selection
- exploring different scenarios for the final model 
- training and validation error rates for each scenario
- test_error rate for the final model on the selected scenario
- Feature importance list for both ‘Black’ and ‘Rest’ (non-black) model
- assigning different threshold levels
- Sample scenario (to test our model)


This model uses the following features to predict probability of murder:
- Gender
- Race
- Age
- Location
- Time of day

The probabilities are then bucketed into different groups based on the threshold set by the police department. We have built two models - one for 'Black' assailants and one for 'rest' due to the high percentage of 'Black' people in the original crime data. This is to overcome the inherent bias in the criminal justice system against African Americans.

In our model, we selected the following cut-offs to send officers:
<=60% = Send 2 officers
60-85% = Send 4 officers
85-95% = Send 8 officers
>95% = Send SWAT team

These threshold levels can be changed as needed. 
