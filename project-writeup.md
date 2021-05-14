# Predicting The Rent of Brooklyn apartment Listings on StreetEasy
Nicholas Dell'Aquilo

## Abstract

The goal of this project was to predict the monthly rent of apartments in Brooklyn, NY, to determine whether an apartment is priced well according to its features. To do this, I scraped data from listings on [StreetEasy](https://streeteasy.com/for-rent/brooklyn). Data available included the number of bedrooms and bathrooms, as well as distinct features such as *(enter common amenities here).* With this data, I was able to build multiple regression models, starting with a simple linear regression and iterating to attempt to improve the model.

## Design

The project was designed to be able to predict the monthly rental cost of apartments. While the models created could be used for any apartments in general, they were trained on data scraped from StreetEasy, filtered to the borough of Brooklyn. Being able to understand what features in an apartment cost could help to understand whether it is worth it to seek such a feature when looking for an apartment; for example, if a balcony adds $100 on average to the monthly rent, is it worth it? If the model is accurate enough, it could ideally be used to predict the cost of an apartment, so one would be able to tell whether a listing is overpriced or a good deal.

## Data

The initial dataset consists of 3,568 listings scraped from StreetEasy. This includes numerical features describing the number of rooms, bedrooms, and bathrooms that an apartment has, as well as how long it has been listed for. Removing rows with null values in these numerical feature columns reduced the dataset to 2,839 listings. Further cleaning consisted of removing outliers (i.e. rows where either the target variable or one of the numerical features was more than 3 standard deviations away from the mean); this reduced to data set to 2,758 rows. Categorical variables include amenities listed, the most common being *(list 5 most common here)*. Several of these columns could be removed as they were present very few times- others would later be nullified by a Lasso regression model.

## Algorithms

2,839 observations were split into 60/20/20 train/validate/testing portions. R-squared scores were calculated with 5-fold cross validation on the training portion and evaluated on the validation portion. Once the best model was found, it was re-trained on the combined training and validation portions and used to predict the testing portion.

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

My web scraping code is located [here](https://github.com/nickdellaquilo/Apartment-Regression/blob/master/Web%20Scraping.ipynb).

My regression code is located [here](https://github.com/nickdellaquilo/Apartment-Regression/blob/master/Final%20Regression.ipynb).
