# Apartment Regression

## Project Proposal

### Framing Question

What variables affect the monthly rent of apartment listings on [StreetEasy](https://streeteasy.com)? Can we predict the target variable of rent with data scraped from this website? This benefits anyone who is actively looking for an apartment to determine whether a rental listing is overpriced- or a good deal- depending on the information available.

### Data Description

Data source: StreetEasy Apartment rental listings in Brooklyn, NY (~6,700+ data points)

Data features: 
* Monthly Rent($)
* No. Rooms
* No. Bedrooms
* No. Bathrooms
* ~~Square ft~~ *upon preliminary scraping, it appears most listings don't have this information, unfortunately*
* Address
* Amenities (Cooling, Heating, Pets, Parking, Laundry, etc.)
* No. Days on Market
* Last price change
* Building info (# Units, # Stories, Year Built)
* Price History

Derived Data: 
* Rent($) per Bedroom; may be more relevant than the rent of an entire unit, since if there are multiple bedrooms it will be shared with roommates.
* ZIP Codes, all in Brooklyn are between 11201 & 11256, and can be standardized easily

As a target, I will predict a direct correlation between most features, such as number of rooms and inclusion of amenities, with a higher rental cost. I also expect ther to be an indirect correlation between the number of days a listing has been on the market and its price. Finally, certain ZIP codes may be correlated with a higher rental price; for example, areas closer to downtown should generally be more expensive.

### Tools

StreetEasy blocks direct web scraping, but using a WebDriver with Selenium allows me to get the html, which I can parse with BeautifulSoup. I will then import the data into a dataframe with Pandas, which I can use to train a regression model with Scikit-learn.

### MVP Goal

My goal for the minimum viable product is to train a regression model on a subset of the data (110 rows). As many  data features as possible should be tested, and removed from the model if they are proved to be irrelevant to the model.
