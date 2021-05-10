# Predicting Apartment Prices on StreetEasy

## MVP (Minimum Viable Product)

### Nicholas Dell'Aquilo

The goal of this project is to understand which features affect the monthly cost of renting an apartment on Brooklyn, New York according to listings on StreetEasy.

![image](https://user-images.githubusercontent.com/22899761/117733329-636eae80-b1bf-11eb-88a6-2926eb248b35.png)

I created a linear regression model of the predicted monthly rent of an apartment depending on its features, such as the number of rooms and whether certain amenities are available. The above figure shows values predicted by this model (x) vs. actual values (y). With my current model, I've achieved an r-squared value of 0.5, and an RMSE of $957.39.

While these values could be much better, this preliminary result shows that there is a clear correlation between the features chosen and the monthly cost of an apartment. Further refinement of the model, by removing unneeded features and including new ones that represent some unseen area, will likely improve these results.
