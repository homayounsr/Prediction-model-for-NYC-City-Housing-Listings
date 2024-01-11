# Prediction model for NYC City Housing Listings
## Data Collection
Data for this project were collected using web scraping techniques from realtor.com. The dataset includes information on houses listed for sale from 2021 to 2024.
###  Number of records for each year
<img src="./EDA/count_data_year.png"  />

### Columns
['property_url', 'mls', 'mls_id', 'status', 'style', 'street', 'unit', 'city', 'state', 'zip_code', 'beds', 'full_baths', 'half_baths', 'sqft', 'year_built', 'days_on_mls', 'list_price', 'list_date', 'sold_price', 'last_sold_date', 'lot_sqft', 'price_per_sqft', 'latitude', 'longitude', 'stories', 'hoa_fee', 'parking_garage', 'primary_photo', 'alt_photos']

### Data shape after web scraping
(17088, 29)

## EDA
## Handling duplicated values
There were 364 duplicate values in the dataset which were removed.

## Handling null values
Before examining null values, irrelevant features were excluded from consideration for the project's objectives. Following this removal, the remaining features were assessed for the presence of null values.
| Feature          | Null Values |
|------------------|-------------|
| list_price       | 4           |
| street           | 14          |
| beds             | 636         |
| full_baths       | 748         |
| year_built       | 1758        |
| sqft             | 5845        |
| price_per_sqft   | 5846        |


After eliminating all null values, the dataset now has a shape of (10867, 14).


## Addressing outliers

The existing features in the dataset include:

- 'beds': Numerical
- 'full_baths': Numerical
- 'sqft': Numerical
- 'year_built': Numerical
- 'list_price': Numerical
- 'price_per_sqft': Numerical

To address skewness in the data, I applied a log transform to achieve a Gaussian distribution. Below, you can observe the data distribution both before and after the log transformation.












