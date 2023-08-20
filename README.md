# Disaster Relief Project

Note: See Project Part 2 files (Rmd for code, or html/pdf for summary) for the full final report.

This project uses a number of classification methods to tackle a
real-world problem. The goal was to use pixel data from satellite
imagery to identify the locations of people displaced by the 2010
earthquake in Haiti. One of the most challenging issues plagueing
disaster relief services is locating displaced people in a timely and
efficient manner. If it were possible to speed up and make more
efficient the process of locating displaced Haitians, this would allow
search and rescue workers to provide relief to those in need before they
run out of food, water, and medicine.

A team from the Rochester Institute of Technology gathered
geo-referenced imagery which was converted to pixel data. This pixel
data is then used to train a number of classification models in this
project to identify blue tarps, which were used as temporary shelters by
Haitians displaced by the earthquake. Later, holdout data is used to 
evaluate the performance of the models.

The first part of this project focuses on exploratory data analysis and
data visualization, exploring the relationships between the RGB values
of each pixel, the classes of each pixel, and interesting insights
uncovered.

This project then applies logistic regression, linear discriminant
analysis, quadratic discriminant analysis, k-nearest neighbors,
penalized logistic regression, random forest, and support vector machine
models to the pixel data to predict which
observations were blue tarps. Two different types of models are compared
for each method, one using the raw RGB values of each pixel, and the
other using a stepwise regression with multiple transformed variables.
These models are then evaluated using 10-fold cross validation for the
purpose of finding the best performing model.

Before assessing models on the holdout data, the data has to be 
prepared and ingested properly, then assessed to ensure that the
holdout data is similar to the training data.

The reported results include a table of performance statistics (and qualities)
during cross validation as well as during holdout testing. 
Results in both tables cover characteristics for each of the best performing models, including
accuracy, true positive rate, false positive rate, precision, AUC,
tuning, and more. 

In its conclusion, this project discusses potential improvements to
consider and possible shortcomings and limitations in the approach to
model creation and evaluation. Additionally, the project hypothesized that
the Support Vector Machine model (with a radial kernel) with no transformed variables
would emerge as the model that would perform best in this scenario. This
was hypothesized with support of performance metrics as
well as a consideration of its balance of false positives and false
negatives in particular.

Upon a fuller assessment of the models with holdout data, it was clear that
model with the best performance was not the SVM model, but the Penalized 
Logistic Regression model with transformed variables. 

Note: For the sake of brevity, many steps will be described but not shown. 
For the full code, please reference the R Markdown file.
