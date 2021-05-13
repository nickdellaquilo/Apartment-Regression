# Predicting The Rent of Brooklyn apartment Listings on StreetEasy
Nicholas Dell'Aquilo

## Abstract

The goal of this project was to predict the monthly rent of apartments in Brooklyn, NY, to determine whether an apartment is priced well according to its features. To do this, I scraped data from listings on [StreetEasy](https://streeteasy.com/for-rent/brooklyn). Data available included the number of bedrooms and bathrooms, as well as distinct features such as *(enter common amenities here).* With this data, I was able to build multiple regression models, starting with a simple linear regression and iterating to attempt to improve the model.

## Design



## Data

~3,300 listings scraped from StreetEasy, removing observations with null target and independent variables reduced this to ~3,000. ~50 features, 3 (4 if including time since listed) are numerical, rest are categorical. The numerical features are the number of rooms, bedrooms, bathrooms, and the number of days the listing has been available. Categorical variables include amenities listed, the most common being *(list 5 most common here)*. Many of these features could be combined as they represent a similar feature, but are just worded differently.

## Algorithms

~3,000 observations, split into 80/20 train vs. holdout, calculate scores with 5-fold cross validation on training portion, 

## Tools

## Communication





note: apartment prices tend to be "round" values (divisible by 100 if possible, 50 or 25 otherwise), so linear predictions can't be truly accurate- assume that leaser will round up
