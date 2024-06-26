# KingCounty_HousingData 
This repository contains data analysis on Housing Sales in King County,USA on python jupyter notebook with the help of statistical tools and machine learning algorithms.
# Introduction
This is an open source project available at Kaggle.

The main aim of this project is to interpret how the prices are varying based on various aspects and how effectively and accurately can we predict those prices for an unknown data.

This aims to help buyers/sellers or real estate agents to make informed decisions. 

# Dataset
This dataset is free and opensource , available at Kaggle website.

Dataset -> https://www.kaggle.com/datasets/harlfoxem/housesalesprediction

The data consists of around 21,000 pieces of observation of residential homes at KC,USA based on past buy/sell history and these were based on 21 peculiarities.

# Data Exploration and Visualization
EDA(Exploratory Data Analysis) revealed that prices are heavily affected by its aesthetics , area of living and geographical location.

True model of the data was found to be a bit deviated with the Linear model and it was easier to interpret through visualisation techniques of non-linear models.

Below link will redirect you to depository where various graphs are plotted which would help you visualize how prices predictions varied from actual data from both the asssumptions of linear and non-linear models, and to understand what mattered most while deciding the price of a house at King County.

Visual directory--> https://github.com/As00-00/KingCounty_HousingData/tree/main/Visuals

These were the basic plots if you wanted to visualize at a broader scale, further illustrations , test data examples are compiled in the code snippet

# Feature Engineering
There were 21 predictors or features which were originally given, out of which only 15 were useful, so filtered them out.

Out of those 15 features, some were showing very high multicollinearlity which was further handled by regularisation techniques which was incorporated with the statistical model.

Other techniques like dimensional reduction is not used because of few number of predictor variables in the dataset (relative to how much is required for PCA)

Transformation of variables was not required.

# Modeling
Firstly, Outliers from the data set were removed which were first visualised by plotting the box plots and Kernal density plots.

Multicollinearity was seen through correlation Matrices and Variance Infation Factor(VIF).

Then the data was normalised(standardized) and statistical model swere applied.

Statistical models which were used in the process of analysing the data were-->

1)Gradient Descent Algorithm (Linear Regression)

2)Weighted Gadient Decent Algorithm

3)Polynomial Regression

4)Partial Least Squares

5)Generalized Additive Models(GAM's)

6)Decision Tress(Random Forests)

Further regularisation Techniques like Ridge and Lasso regression were used to further optimize the model by tackling overfitting and multicollinearity.

# Model Evaluation
The above mentioned model were evaluated based on how accurate they were on testing data set.

Testing data set was generated through K-Fold Cross Validation(CV) and evaluated based on R2 scores, mean sqaured error and graphical visualisation.

It was seen that Linear model was able to explain 67% of variance in the data and polynomial regression of degree 2 was able to explain 80% of the variance on test data generated through CV.

Random forests obviously came out by explaining 86% of variance in the data, infact they predicted the test data with sharp accuracy.

But ofcourse data was more visually interpretable through linear models.

# Results and Discussion

It was seen that prices were highly positively related with the grade and sqft_living of the house.

There was high multicollinearity between (#bathrooms and sqft_living) , (sqft_living,sqft_above) which seems obvious as well.

While the model performs well in polynomial regression for training data when higher degree poly. is used, it tend to overfit the data, hence huge error in test data were observed.Therefore, when almost similar test parameter were given, it was fine, but when data was given which seemed an outlier, these models performed poorly. Although decision trees gave significantly better results by accurately interpreting the complexity of the data.


Overall,Linear model was able to explain descent amount of variance, as data was a bit complex when price responses were at extreme ends.

# Conclusion

The project was able to successfully explain and predict the housing prices with high accuracy based on various peculiarities given in the dataset.

Any real estate agent or stakeholder can have valuable insights by this project.

# Future work
Although the project is complete , the code snippet provided can further be used in websites and other ML models with a bit of changes so that outside users can also access and predict prices with there own testing data.

In future, other predictors can be included in the dataset according to the economic growth of the location,etc.








