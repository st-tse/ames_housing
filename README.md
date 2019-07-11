# Project 2 - Ames Housing Data and Kaggle Challenge

Regularizied Linear Regression for predicting housing prices on Ames Housing Data set

File Description:

cleaning_train.ipynb -  
cleaning for training data, most missing values filled in with proper terms where they represented features absent formthe house. The remainder were estimated using the other features of the house

cleaning_test.ipynb -  
same as above but for th testing data

BoxPlots.ipynb -  
EDA for the discrete and categorical features of the houses  
Only contains the plots themselves which were a basis of whether or not to include the feature in the model. Can seet he effects of certain varaibles on sale price

ContinuousPlots.ipynb -  
EDA for continuous and some discrete features.  
For continuous has fucntions used to plot distribution and transformed versions of data agaisnt sale price.
Also included funcitons for checking interations and some plots seeing how well those interations fit sale price
    
    plots(): creates a histogram, and regplots for first-third degree and log vs sale price
    get_interations(): prints interactions where the correlation of the interation with sale price is stronger than individual interations

ModelTester.ipynb - 
Included functions for streamlining model testing process.
Functions for creating new features, trandformations, and interactions, as well as an easy way to determine which variables whould be used in the model and how. Supports Linear Regression, Lasso, Ridge, and ElasticNet, with the option to save predictions to a labelled csv file. Allows for evaluation of the model with cross validation score, root mean square error using a train test split, and plotting actual vs predicted values

    reformat(): includes all features to be added based on existing features
    format_split: uses both training and testing data to create dummy variables for both ensuing that columns are the same in each
    build_model: creates a model of your choice and scores it
    fot_model: builds and model and hass the optiion of rebuilding on the whole training set and saving predictions
    
    features_num: continuous varaibles that the model will use, this is where interactions and transformed variables go
    conintuous: list of features to be transformed, creates log, quadratic, and cubic for each
    features_nonpoly: list of features to have outliers removed at 4 std from the mean
    features_dis: discrete variables that are to be converted to strings and treated as categrical
    features_cate: list of categorical features
    
    