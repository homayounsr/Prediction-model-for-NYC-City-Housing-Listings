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

### Handling null values
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


### Addressing outliers

The existing features in the dataset include:

- 'beds': Numerical
- 'full_baths': Numerical
- 'sqft': Numerical
- 'year_built': Numerical
- 'list_price': Numerical
- 'price_per_sqft': Numerical

To address skewness in the data, I applied a log transform to achieve a Gaussian distribution. Below, you can observe the data distribution both before and after the log transformation.



#### 'beds': Numerical
Skewness of original data: 4.739426354647343

Skewness of log-transformed data: 0.017194484194333386

<img src="./EDA/bed_skewness.png"  />

#### 'full_baths': Numerical
Skewness of original data: 9.743926203602364

Skewness of log-transformed data: 1.1508611341350268

<img src="./EDA/full_bath_skewness.png"  />




#### 'sqft': Numerical
Skewness of original data: 12.721288454241067

Skewness of log-transformed data: 0.6630027058848263

<img src="./EDA/sqft_skewness.png"  />


#### 'list_price': Numerical
Skewness of original data: 96.04967635617102

Skewness of log-transformed data: 0.6645397828927238

<img src="./EDA/list_price_skewness.png"  />




#### 'price_per_sqft': Numerical
Skewness of original data: 78.13892297168798

Skewness of log-transformed data: 0.27697626845400514

<img src="./EDA/price_per_sqft_skewness"  />


