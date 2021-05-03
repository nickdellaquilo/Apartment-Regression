# Apartment Regression



Data source: StreetEasy Apartment rental listings in Brooklyn, NY (~6,700+ data points)

Data features: 
* Monthly Rent($)
* # Rooms
* # Bedrooms
* # Bathrooms
* Square ft
* Address
* Amenities (Cooling, Heating, Pets, Parking, Laundry, etc.)
* # Days on Market
* Last price change
* Building info (# Units, # Stories, Year Built)
* Price History

Derived Data: 
* Rent/Bedroom; may be more relevant than the rent of an entire unit, since if there are multiple bedrooms it will be shared with roommates.
* ZIP Codes, all in Brooklyn are between 11201 & 11256, and can be standardized easily
