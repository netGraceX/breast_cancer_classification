# breast_cancer_classification

## Table of contents
- Description
- Technologies
- Tasks performed
- Results

## Description

The goal of this project is to classify malignant and benign tumors using ML techniques.

Dataset source: https://scholar.cu.edu.eg/?q=afahmy/pages/dataset - Al-Dhabyani W, Gomaa M, Khaled H, Fahmy A. Dataset of breast ultrasound images. Data in Brief.

## Technologies

   - Python (Jupyter Notebook)
   - pandas
   - matplotlib
   - numpy 
   - sklearn

## Tasks performed
   - Data cleaning
   - Data exploration 
   - Testing of different classification algorithms (Logistic Regression, SVM, Decision Tree, Neural Networks)

## Results

 Model                | Training score  | Test Score   | ValidationScore
----------------------| --------------  | ------------ |----------------
LogisticRegression    |   0.6           |0.6           |   0.5
LinearSVC             |   0.6           |0.6           |   0.5
DecisionTreeClassifier|   0.8           |0.6           |   0.8
OneVsRestClassifier   |   0.8           |0.7           |   0.8

Logistic regression and SVM with linear kernel were the first algorithms selected because they are simple and work similarly for problems with a similar number of features and training data as the problem under consideration. Given the obvious problem of overfitting, after using various techniques, we proceeded by testing other models such as Decision Trees and Neural Networks without obtaining better results, however, in fact the results worsen significantly by increasing even slightly the number of hidden layers or trying to work on the regularization parameter. In general, the various models used fail to make satisfactory predictions, all of them suffering from overfitting. Various techniques were applied to improve the models: using the training set division, validation set, test set, increasing the regularization parameter or decreasing the C parameter, and using fewer features. It was precisely the latter that turned out to be the problem, in fact after the application of the PCA technique to reduce the number of features per pixel, Decision Trees and Neural Networks turned out to be the best models with excellent accuracy as can be seen from the table above. The model that allows us to obtain the absolute best results is the one obtained from Neural Networks that with two hidden layers of 5 nodes each allows us to reach an accuracy ranging between 70% and 80%.