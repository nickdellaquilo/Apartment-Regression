# Predicting Apartment Prices on StreetEasy

## MVP (Minimum Viable Product)

### Nicholas Dell'Aquilo

The goal of this project is to understand which features affect the monthly cost of renting an apartment on Brooklyn, New York according to listings on StreetEasy.

![image](https://user-images.githubusercontent.com/22899761/117733329-636eae80-b1bf-11eb-88a6-2926eb248b35.png)

I created a linear regression model of the predicted monthly rent of an apartment depending on its features, such as the number of rooms and whether certain amenities are available. A linear regression model done on the entire dataset produced and R-squared value of approximately 0.5. The above figure shows values predicted by this model (x) vs. actual values (y). A 5-split Kfold test produced the following R-squared scores: 0.44410573, 0.47287143, 0.4436641,  0.32974336, 0.40803675.

This preliminary result shows that there is a clear correlation between the features chosen and the monthly cost of an apartment. However, the variance between the scores shows that there is overfitting taking place. Further refinement of the model, by reducing this overfitting through regularization, manually removing outlier observations and features that are extremely rare, or by including new features that represent some unseen area, will likely improve these results.
