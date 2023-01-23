# King County Housing Sale Price Analysis

By Nagib Gonzalez

# Overview
For this project we focused on analyzing King County, Washington real estate data to identify trends and patterns that can be used to inform investment decisions. The analysis includes cleaning and preprocessing the data, using statistical methods such as Ordinary Least Squares (OLS) to model the data, and visualizing the results to gain insights into the relationships between different variables and the target variable (price). 

# Business Problem:
Nimble Home Buyers, a real estate investment company, is seeking to expand their operations into the state of Washington. To support this endeavor, they have engaged the services of a data scientist to analyze King County housing data in order to identify the factors that influence home prices and the extent of their impact. This information will be instrumental in making informed decisions and successfully establishing a presence in the Washington market.
   
   ### Nimble Home Buyers Approach to Real Estate Investment:
  
  Nimble Home Buyers has an investment strategy that involves the identification and acquisition of properties, followed by renovation or new construction efforts and ultimately, the sale of these properties for a profit. This approach enables the company to optimize the value of their investments and generate returns for their stakeholders.
  # Data Understanding 
### Column Names and Descriptions for King County Data Set
- `id` - Unique identifier for a house.
- `date` - Date house was sold.
- `price` - Sale price (prediction target).
- `bedrooms` - Number of bedrooms.
- `bathrooms` - Number of bathrooms.
- `sqft_living` - Square footage of living space in the home.
- `sqft_lot` - Square footage of the lot.
- `floors` - Number of floors (levels) in house.
- `waterfront` - Whether the house is on a waterfront. Includes Duwamish, Elliott Bay, Puget Sound, Lake Union, Ship Canal, Lake Washington, Lake Sammamish, other lake, and river/slough waterfronts.
- `view` - Quality of view from house. Includes views of Mt. Rainier, Olympics, Cascades, Territorial, Seattle Skyline, Puget Sound, Lake Washington, Lake Sammamish, small lake / river / creek, and other.
- `condition` - How good the overall condition of the house is. Related to maintenance of house.
See the King County Assessor Website for further explanation of each condition code.
- `grade` - Overall grade of the house. Related to the construction and design of the house.
See the King County Assessor Website for further explanation of each building grade code.
- `sqft_above` - Square footage of house apart from basement.
- `sqft_basement` - Square footage of the basement.
- `yr_built` - Year when house was built.
- `yr_renovated` - Year when house was renovated.
- `zipcode` - ZIP Code used by the United States Postal Service.
- `lat` - Latitude coordinate.
- `long` - Longitude coordinate.
- `sqft_living15` - The square footage of interior housing living space for the nearest 15 neighbors.
- `sqft_lot15` - The square footage of the land lots of the nearest 15 neighbors.
- `month_sold`- Month that the home was sold.
- `City`- City in which the home is located.

# Methods
This project utilizes a combination of statistical and machine learning techniques to analyze and model real estate data. The methods used in this project include:
- Data cleaning and preprocessing: The raw data was cleaned and preprocessed to handle missing values, outliers, and inconsistencies.
- Exploratory data analysis (EDA): EDA was used to gain insights into the structure and relationships in the data. This involved visualizing the data using various plots and summarizing the data using descriptive statistics.
- Linear regression: Linear regression was used to model the relationship between the predictor variables and the target variable (price). The ordinary least squares (OLS) method was used to fit the model to the data.

# Results

<img width="1001" alt=" price_vs_grade" src="https://user-images.githubusercontent.com/45716414/214108313-d7caa6b3-40b4-4db2-b8b1-185d48a248ad.png">

![newplot (4)](https://user-images.githubusercontent.com/45716414/213967062-fb5532bc-b286-48d0-be6b-28f533dea8e7.png)

![newplot (2)](https://user-images.githubusercontent.com/45716414/214108115-e9d6ad0d-9356-4e4f-9a74-7f13949bf7ae.png)

![newplot (4)](https://user-images.githubusercontent.com/45716414/213967062-fb5532bc-b286-48d0-be6b-28f533dea8e7.png)
