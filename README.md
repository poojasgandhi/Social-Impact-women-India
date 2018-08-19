# Social_Impact_women_India
This repository encompasses my submission for the WIDS (Women In Data Science) Challenge for 2018, held in Jan-Mar'18. It was an invite only competition based on InterMedia Survey Institute, a grant recipient of the Bill &amp; Melinda Gates foundation in their Financial Services for the Poor program.  

Participants were required to predict gender based on demographic and behavioral information of survey respondents from India and their usage of traditional financial and mobile financial services. 

By predicting gender, idea was to explore the key differences in behavior patterns of men and women, and how that may impact their use of new financial services. Ideally, these findings would influence plans to reach women in developing economies and encourage them to adopt new financial tools that would help to lift them and their families out of poverty. 

# Approach
My objective that I inetnded to achieve through this competition was especially to learn model parmeters tuning in Python. I approach this challenge through two different training data

1. Using only the columns present in Data Dictionary
All the column names in the data were coded and not representative on the data. So, my first assumption was probably the organizers didnt want participants to use the variables not present in data dictionary. Accordingly, I started with a subset of the original dataset - only the columns present in dictionary

I decided to start with the Gradient Boosting Model since it is suppossed to be a winning solution for lot of Kaggle challenges
Starting with the base model (with default parameters), I used Grid Search to  methodically tune the parameters of the model as below
- Fixing learning rate and optimizing # trees
Tuning parameters of tree
- Optimize max depth and split size sample
- Optimize the nim # samples in a leaf node
- Optimize maximum # features in a tree
Tuning the boosting parameters
- Optimize the sub sample proportion
- Optimize the learning rate

2. Using all the columns

GBM
For this I just use the base model with default parameter values and model with the same parameters as finalized in the first approach

I also try the default XGB (Extreme Gradient Boosting) and Random Forest models

Instead of tuning these models further, I figured there was a higher gain in building ensembles of the models built so far.

# Final submission and result
Final submission was an ensemble of the GBM with all variables (parameters tuned based on approach 1) and tuned GBM with variables from data dictioanry only. 

Our team's leaderboard standing was as were as below:
Private leaderboard score - 0.97233
Public leaderboard score - 0.97314
Rank - 39 (Top 17 %ile)




