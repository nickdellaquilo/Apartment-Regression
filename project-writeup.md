# Predicting The Rent of Brooklyn apartment Listings on StreetEasy
Nicholas Dell'Aquilo

## Abstract

The goal of this project was to predict the monthly rent of apartments in Brooklyn, NY, to determine whether an apartment is priced well according to its features. To do this, I scraped data from listings on [StreetEasy](https://streeteasy.com/for-rent/brooklyn). Data available included the number of bedrooms and bathrooms, as well as distinct features such as *(enter common amenities here).* With this data, I was able to build multiple regression models, starting with a simple linear regression and iterating to attempt to improve the model.

## Design



## Data

The initial dataset consists of 3,568 listings scraped from StreetEasy. This includes numerical features describing the number of rooms, bedrooms, and bathrooms that an apartment has, as well as how long it has been listed for. Removing rows with null values in these numerical feature columns reduced the dataset to 2,839 listings. Further cleaning consisted of removing outliers (i.e. rows where either the target variable or one of the numerical features was more than 3 standard deviations away from the mean); this reduced to data set to 2,758 rows. Categorical variables include amenities listed, the most common being *(list 5 most common here)*. Several of these columns could be removed as they were present very few times- others would later be nullified by a Lasso regression model.

## Algorithms

~3,000 observations, split into 80/20 train vs. holdout, calculate scores with 5-fold cross validation on training portion, 

Models:

* Simple linear regression
* Polynomial regression
* Lasso regression
* Ridge regression

Results for 5-fold CV scores:

Results of each model on validation data:

Results of final model on test data:


## Tools

#### Web scraping:
* Selenium
* BeautifulSoup
* Pandas

#### Regression:
* Numpy
* SciKitLearn

#### Visualization:
* Matplotlib
* Seaborn

## Communication

My presentation is located [here]().
My web scraping code is located [here]().
My regression code is located [here]().
