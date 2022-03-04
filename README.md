# House-Prices---Advanced-Regression-Techniques
Predict sales prices and practice feature engineering, RFs, and gradient boosting
This competition is very important to me as it helped me to begin my journey on Kaggle few months ago. I've read some great notebooks here. To name a few:

I can't recommend enough every beginner to go carefully through these kernels (and of course through many others great kernels) and get their first insights in data science and kaggle competitions.

After that (and some basic pratices) you should be more confident to go through this great script by Human Analog who did an impressive work on features engeneering.

As the dataset is particularly handy, I decided few days ago to get back in this competition and apply things I learnt so far, especially stacking models. For that purpose, we build two stacking classes ( the simplest approach and a less simple one).

As these classes are written for general purpose, you can easily adapt them and/or extend them for your regression problems. The overall approach is hopefully concise and easy to follow..

The features engeneering is rather parsimonious (at least compared to some others great scripts) . It is pretty much :

Imputing missing values by proceeding sequentially through the data

Transforming some numerical variables that seem really categorical

Label Encoding some categorical variables that may contain information in their ordering set

Box Cox Transformation of skewed features (instead of log-transformation) : This gave me a slightly better result both on leaderboard and cross-validation.

Getting dummy variables for categorical features.

Then we choose many base models (mostly sklearn based models + sklearn API of DMLC's XGBoost and Microsoft's LightGBM), cross-validate them on the data before stacking/ensembling them. The key here is to make the (linear) models robust to outliers. This improved the result both on LB and cross-validation.
