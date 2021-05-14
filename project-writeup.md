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

* Simple linear regression (LR1)
* Linear regression with additional feature (LR2)
* Lasso regression
* Ridge regression

Results for 5-fold CV R<sup>2</sup> scores:

* LR1:   [0.28465979 0.1833678 0.30504643 0.22958702 0.23047237],  Mean: 0.24662668197976534
* LR2:   [0.28388198 0.18097879 0.30500836 0.22872147 0.2304566],  Mean: 0.24580943893799315
* Lasso: [0.49804831 0.44783655 0.4972743  0.53026636 0.45429946], Mean: 0.4855449950510766
* Ridge: [0.49047206 0.44821105 0.49420212 0.51774938 0.45261041], Mean: 0.480649006115532

Results of each model on validation data:

* LR1: 0.24
* LR2: 0.24
* Lasso: 0.4655
* Ridge: 0.4644

Lasso was determined to be the best model.

Results of final model when retrained including validation data:

R<sup>2</sup> = 0.48

## Tools

#### Web scraping:
* BeautifulSoup
* Pandas
* Selenium

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

![image](https://user-images.githubusercontent.com/22899761/118211459-1fd3a900-b43a-11eb-9062-7fd317acb268.png)

![image](https://user-images.githubusercontent.com/22899761/118249286-419d5200-b473-11eb-8821-f29bd942e9af.png)
