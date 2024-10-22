# House Value Predictor 🏠

The full report can be found [here](https://htdanganh.github.io/house-value-predictor/).

## Developers

Anh Dang, Arjun Birthi, Ayush Gundawar, Daniel Oh, and Jatong Su

## Introduction

The accurate valuation of residential properties is a critical component in the real estate and mortgage lending industries, as it is influenced by both the physical attributes of the property and the characteristics of the surrounding neighborhood. Extensive research has been conducted to evaluate various machine learning techniques for predicting housing prices. A study titled "An Optimal House Price Prediction Algorithm: XGBoost" compared the performance of algorithms such as XGBoost, Support Vector Regressor, Random Forest Regressor, Multilayer Perceptron, and Multiple Linear Regression using the Ames City housing dataset.

The study identified XGBoost as the most effective model, offering interpretability, simplicity, and accuracy [3]. The dataset utilized in this analysis consists of property listings scraped from realtor.com, focusing on houses sold within the past decade in the area located around Duluth, Johns Creek, and Suwanee. The dataset includes features such as sale price, property location, year of construction, number of bedrooms, number of bathrooms, and other amenities that are crucial for determining property value. The inclusion of location details will facilitate future regional analysis [1].

## Problem Definition

Accurate house pricing in Georgia's dynamic real estate market poses a complex challenge. Traditional valuation methods, such as comparative market analysis, frequently overlook essential details and lack critical contextual information [2], resulting in frequent mispricing and discrepancies from true market value. Furthermore, obtaining more precise valuations can be time-consuming and costly. This project aims to address these limitations by leveraging machine learning models, which can analyze vast amounts of data to provide more precise and reliable property valuations.

## Methods

### Preprocessing

Initially, the data was cleansed by eliminating duplicate entries and imputing missing values. In the preprocessing phase, a selection was made to include only those features amenable to numerical representation for the training process. The original dataset comprised 29 columns, from which 12 pertinent features were retained after excluding irrelevant ones such as `mls_id`, `property_url`, and `primary_photo`.


### Models

This project explored the outputs of using linear regression, ridge regression, random forest, and XGBoost. 


## Comparison and Next Steps

Among the four models analyzed, XGBoost distinguished itself with its balanced performance across both training and testing datasets. The comparative analysis of the models highlights specific trade-offs and strengths. Linear Regression and Ridge Regression, while providing interpretability and resistance to multicollinearity, respectively, were less effective in capturing non-linear relationships, resulting in higher RMSE values. Conversely, Random Forest achieved a lower RMSE during training but exhibited signs of overfitting as evidenced by the disparity between its training and testing outcomes, underscoring the necessity of meticulous hyperparameter tuning. Nevertheless, its ability to address non-linear relationships and offer insights into feature importance remains valuable.

XGBoost, however, demonstrated superior overall performance with low RMSE and high R-squared values across both datasets, indicating better generalization capabilities compared to Random Forest. Its proficiency in managing complex data, missing values, and categorical features further enhanced its utility.

Despite their respective strengths, each model encountered challenges in accurately predicting housing prices within the complexities of the real estate market.

Future initiatives will focus on refining hyperparameters for the Random Forest and XGBoost models, advancing feature engineering techniques to derive more significant data insights, exploring ensemble methods such as stacking and blending to augment accuracy and incorporating external factors like market trends and economic indicators into our analysis.

# References
[1] F. Bergadano, R. Bertilone, D. Paolotti, and G. Ruffo, “Developing real estate automated valuation models by learning from  heterogeneous data sources,” International Journal of Real Estate Studies, vol. 15, no. 1, pp. 72–85, Jun. 2021. doi:10.11113/intrest.v15n1.10

[2] G. Kamtziridis, D. Vrakas, and G. Tsoumakas, “Does noise affect housing prices? A case study in the urban area of Thessaloniki,” EPJ Data Science, vol. 12, no. 1, Oct. 2023. doi:10.1140/epjds/s13688-023-00424-3

[3] H. Sharma, H. Harsora, and B. Ogunleye, “An optimal house price prediction algorithm: Xgboost,” Journal of Analytics, vol. 3, no. 1, pp. 30–45, Jan. 2024. doi:10.3390/analytics3010003
