# Problem Statement:
## Overview
This Project aims to map and analyze areas with limited access to affordable and nutritious food, known as food deserts. Within this project, we focus on understanding the impact of food deserts on local communities. By leveraging geospatial data analysis and machine learning algorithms, this initiative aims to uncover insights into the distribution and characteristics of food deserts. These findings can assist community leaders in developing strategies and interventions to address food insecurity and improve access to nutritious food options.

## Inspiration:
Inspiration for this project comes from a publication [Using Social Media to Predict Food Deserts in the United States Infodemiology Study of Tweets](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC9297137/)

## Objectives
#### Food Desert Mapping Application:
- Develop an interactive application to visually represent the geographic distribution of food deserts.
#### Demographic Disparity Analysis:
- Identify and analyze demographic groups disproportionately affected by food deserts.
#### Impact Assessment:
- Evaluate the socio-economic and health-related effects of food deserts on local communities.
#### Model Development:
- Utilize a Logistic Regression model to classify areas as food deserts or non-food deserts.
- Employ Clustering models (e.g., K-means) to discover spatial patterns within food deserts.
- Conduct Geospatial Data Analysis to analyze spatial data and visualize trends.
#### Future Work: 
#### Time-Series Analysis:
- Explore time-series analysis techniques to showcase temporal trends over time, focusing on state-level data.

### Sample Dataset Dictionary
|Field|LongName|Description|
|-----|--------|-----------|
|CensusTract|Census tract|Census tract number|
|State|State|State name|
|County|County|County name|
|Urban|Urban tract|Flag for urban tract|
|POP2010|Population, tract total|Population count from 2010 census|
|OHU2010|Housing units, total|Occupied housing unit count from 2010 census|
|GroupQuartersFlag|Group quarters, tract with high share|Flag for tract where >=67%|
|NUMGQTRS|Group quarters, tract population residing in, number|Count of tract population residing in group quarters|
|PCTGQTRS|Group quarters, tract population residing in, share|Percent of tract population residing in group quarters|
|LILATracts_1And10|Low income and low access tract measured at 1 mile for urban areas and 10 miles for rural areas|Flag for low-income and low access when considering low accessibilty at 1 and 10 miles|
|LILATracts_halfAnd10|Low income and low access tract measured at 1/2 mile for urban areas and 10 miles for rural areas|Flag for low-income and low access when considering low accessibilty at 1/2 and 10 miles|
|LILATracts_1And20|Low income and low access tract measured at 1 mile for urban areas and 20 miles for rural areas|Flag for low-income and low access when considering low accessibilty at 1 and 20 miles|
|LILATracts_Vehicle|Low income and low access tract using vehicle access or low income and low access tract measured at 20 miles|Flag for low-income and low access when considering vehicle access or at 20 miles|
|HUNVFlag|Vehicle access, tract with low vehicle access|Flag for tract where >= 100 of households do not have a vehicle, and beyond 1/2 mile from supermarket|
|LowIncomeTracts|Low income tract|Flag for low income tract|
|PovertyRate|Tract poverty rate|Share of the tract population living with income at or below the Federal poverty thresholds for family size|
|MedianFamilyIncome|Tract median family income|Tract median family income|
|LA1and10|Low access tract at 1 mile for urban areas and 10 miles for rural areas|Flag for low access tract at 1 mile for urban areas or 10 miles for rural areas|
|LAhalfand10|Low access tract at 1/2 mile for urban areas and 10 miles for rural areas|Flag for low access tract at 1/2 mile for urban areas or 10 miles for rural areas|
- Read more about [Data dictionary](../csv_data/food_data_dictionary.csv)
#### <u>Data Sources</u>
- [Food Desert Data](https://www.ers.usda.gov/data-products/food-access-research-atlas/download-the-data/)
- [500_Cities_data](https://data.cdc.gov/widgets/sfcy-rqbb)

Shape of the data: 72531, 147
#### The following Python libraries has been used for this project:

- pandas
- numpy
- matplotlib
- seaborn
- geopandas
- scikit-learn

### Methodology

The methodology involves several steps:

1. Data Cleaning:
    - Impute missing values
    
2. Exploratory Data Analysis (EDA):
    - Features correlation
    - Population distribution
    - Numerical features statisticical summary
    - Categorical features distribution
     
3. Train-Test Split:
    - The dataset is divided into training and testing sets to assess model performance accurately.

4. Model Selection:
    - Several classification algorithms are utilized for model training, Logistic Regression, Desicion Tree Classification, Random Forest Classification, ExtraTrees Classification and Neural Network 
    
5. Model Evaluation:
    - Each classification model is trained using the training data and evaluated using testing data.
    - Model performance metrics such as training score, testing score, and accuracy is calculated to assess the effectiveness of each model.

### Interactive Map: 
[Here](https://datawrapper.dwcdn.net/qiQhy/3/)

<img src="https://datawrapper.dwcdn.net/qiQhy/full.png" alt="% of Food Insecurity" />


#### Reference
- Lasso Feature [Code Reference](https://towardsdatascience.com/feature-selection-techniques-in-machine-learning-with-python-f24e7da3f36e)