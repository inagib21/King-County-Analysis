# King County Housing Sale Price Analysis
![seattle_skyline](https://user-images.githubusercontent.com/45716414/214114074-42d7d110-adf8-4dd6-a940-7357fb93a90a.jpeg)


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
- `city`- City in which the home is located.

# Methods
This project utilizes a combination of statistical and machine learning techniques to analyze and model real estate data. The methods used in this project include:
- Data cleaning and preprocessing: The raw data was cleaned and preprocessed to handle missing values, outliers, and inconsistencies.
- Exploratory data analysis (EDA): EDA was used to gain insights into the structure and relationships in the data. This involved visualizing the data using various plots and summarizing the data using descriptive statistics.
- Linear regression: Linear regression was used to model the relationship between the predictor variables and the target variable (price). The ordinary least squares (OLS) method was used to fit the model to the data.

# Results
## Grade:
The quality and level of finish of a home, as reflected in its grade, has a profound effect on its market value. As the grade of a home improves, there is a clear correlation with an increase in the mean sale price of the property, with each step up in grade level resulting in a significant boost in value.

<img width="1001" alt=" price_vs_grade" src="https://user-images.githubusercontent.com/45716414/214108313-d7caa6b3-40b4-4db2-b8b1-185d48a248ad.png">


## Waterfront:
Properties situated on the waterfront tend to command a premium in the real estate market. This is reflected in the sale prices, which are consistently higher than those of properties located inland, often by a range of $300,000 to $500,000 or more.

![newplot (2)](https://user-images.githubusercontent.com/45716414/214108115-e9d6ad0d-9356-4e4f-9a74-7f13949bf7ae.png)


## View:
A home's view plays a significant role in its sale price, with a clear upward trend observed as the quality of the view increases. A notable increase in sale price can be observed when comparing a property with no view to one with a fair view, as well as when comparing a good view to an excellent view.

![view ](https://user-images.githubusercontent.com/45716414/214108832-38f64a1e-4526-437d-9e31-bf93f3789804.png)


# Modeling
Our model  with the best perfomance had an R-Squared and Adjusted R-Squared score of .839.The F-statistic and a very low p-value indicate that the model is statistically significant and that the predictor variables collectively explain a significant amount of the variation in price. For this model we did not include the date column and we used One Hot encoding on the `city` and `zipcode` columns.

- The coefficient values for the 'condition', 'grade', and 'view' columns represent the average change in the 'price' variable for a unit increase in the respective column.
- The condition of the property was found to have a positive impact on its value, with an incremental increase of 26,400 dollars per unit increase in the condition score, as assessed on a scale of 0 to 4.
- A higher grade level increased the value of a house by 55,670 dollars per unit grade on a scale of 3 to 13
- Properties with a better view had an increase in value of 47,690 dollars per unit increase on a scale form 0 to 4
- Each additional bathroom resulted in an increase of 31,000 dollars in home value.
- Homes located on a waterfront had an increase in value of 359,800 dollars.
- For every 1 sqft increase in living space, the price of the property increases by 62.33 dollars.
- The condition of the property was found to have a positive impact on its value, with an incremental increase of 26,400 dollars per unit increase in the condition score, as assessed on a scale of 0 to 4.
- The coefficient values suggest a negative correlation between the number of bedrooms and floors with the price,it's important to note that this conclusion is most likely incorrect and further analysis is needed.

# Limitations and Further Analysis
   Our final model demonstrated an accuracy rate of 83.9% on the data set utilized. While this level of accuracy is sufficient to generate observations and insights, it is not appropriate to arrive at any definitive conclusions at this time. Our coefficient scores for bedrooms and floors were negative, which warrants further investigation. Our visualizations of various variables allowed us to discern their relationship with the target variable, price. Based on our observations, we believe that an increase in the number of floors and bedrooms would not have a negative impact on the price of a property, but rather the opposite. However, it is possible that this conclusion may be affected by the limited scope of our data, and incorporating additional data into the model could provide further insight. Our future analyses should include incorporating both recent and historical data. The real estate industry is known for its cyclical nature, however, we were unable to detect any statistically significant correlation with the date of sale. This is likely due to the limited scope of our data, which only covered a one-year period. In general, home sales tend to increase during the summer months and decrease during the winter. Therefore, our future analyses should also consider the impact of seasonality on real estate trends.

### Use Alternative data:
 Alternative data can provide valuable insights into the performance and potential of real estate investments. An example of some of the data we should consider using includes:


**Demographic data** : This type of data can provide information about the age, income, and education level of people in a particular area, which can be useful for identifying areas that are likely to experience population growth in the future.

**Social media data**: Platforms like Twitter and Instagram can provide insight into what people are saying about a particular area, which can be useful for identifying areas that are becoming trendy or experiencing a decline in popularity.

**Satellite data**: Imagery and data captured by satellites can be used to track changes in land use, such as the construction of new buildings or the expansion of roads, which can provide insight into the potential for development in a particular area.


### Use Different models:
There are several alternative methods to the ordinary least squares (OLS) method that can be used for modeling real estate data, depending on the specific requirements of the analysis and the nature of the data. Here are a few examples:

1. **Decision tree models**: Decision trees are a popular method for modeling real estate data because they can handle both continuous and categorical variables, and they can also handle non-linear relationships. They can be used to make predictions about the price of a property based on its features and characteristics.

2. **Random Forest models**: Random Forest is an extension of decision trees. It is a collection of decision trees where a random subset of features is used at each split. The final prediction is an average of all the decision trees. They are often more accurate than decision trees.

3. **Gradient Boosting models**: Gradient Boosting is an ensemble method that combines multiple weak models to create a more accurate and robust model. They work well when there are non-linear relationships in the data.

4. **Support Vector Regression (SVR)**: SVR is a type of algorithm that can be used for both linear and non-linear regression problems. It can handle non-linear relationships by mapping the input data into a higher dimensional space where a linear boundary can be drawn between the classes.

5. **Neural Network models**: Neural networks are a type of algorithm that can be used for both linear and non-linear regression problems. They are particularly useful when there are a large number of predictor variables or when the relationships between the predictor variables and the response variable are complex.

### Use One Hot Encoding on  Condition, Grade, View Columnns:
In our final model, we utilized one-hot encoding for the City and zipcode columns, but did not utilize the same method for the Condition, Grade, and View columns. Upon further evaluation, it is plausible that the model performance could be enhanced by implementing one-hot encoding for these variables as well. However, we did not use one-hot encoding, instead, we transformed the categorical variables into numerical ones. This approach was selected to facilitate the modeling process.

**Condition**: 

{'Poor': 0, 'Fair': 1, 'Average': 2,'Good':3, 'Very Good':4}

**Grade**:

{'3 Poor': 3, '4 Low': 4, '5 Fair': 5, '6 Low Average': 6, '7 Average': 7,'8 Good': 8, '9 Better': 9, '10 Very Good': 10, '11 Excellent': 11, '12 Luxury': 12,'13 Mansion': 13}


**View**: {'NONE': 0, 'FAIR': 1, 'AVERAGE': 2, 'GOOD': 3, 'EXCELLENT': 4}

### Adressing Normality:

Our data failed to pass the normality test, indicating that it did not conform to a normal distribution. In light of this, we elected not to transform the data using a logarithmic function, in order to maintain the accuracy of the relationships between our variables. As a next step, we recommend utilizing non-parametric statistical methods, such as the Wilcoxon rank-sum test, the Kruskal-Wallis test, and the Wilcoxon signed-rank test, which are suitable for data that does not follow a normal distribution.

1. **The Wilcoxon rank-sum test** (also known as the Mann-Whitney test) is a non-parametric test used to determine if there is a significant difference between the medians of two groups of data. It is used to compare two independent groups, and it does not assume that the data is normally distributed.

2. **The Kruskal-Wallis test** is a non-parametric test used to determine if there is a significant difference between the medians of two or more groups of data. It is used to compare more than two independent groups and it does not assume that the data is normally distributed.

3. **The Wilcoxon signed-rank test** is a non-parametric test used to determine if there is a significant difference between the medians of two related groups of data. It is used to compare two dependent groups and it does not assume that the data is normally distributed.

# For More information:
Please check out the Jupyter notebook with interactive visualizations: https://nbviewer.org/github/inagib21/dsc-phase-2-project-v2-3/blob/main/student.ipynb

as well as the presentation for the notebook: https://github.com/inagib21/dsc-phase-2-project-v2-3/blob/main/KING%20COUNTY%20REAL%20ESTATE%20ANALYSIS.pdf
