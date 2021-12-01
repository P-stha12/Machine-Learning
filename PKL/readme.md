# Landslide Prediction using weather variables with ML #

## Dataset Used : ##
1) NASA Global Landslide Catalogue (https://maps.nccs.nasa.gov/arcgis/home/item.html?id=eec7aee8d2e040c7b8d3ee5fd0e0d7b9)
2) District Wise Daily Climate Data for Nepal (https://opendatanepal.com/dataset/district-wise-daily-climate-data-for-nepal)

## Data Preparation: ##
filter_data.ipynb -> add_climate_data.ipynb -> add_false_labels.ipynb -> generateDataGAN.ipynb

## Description: ##
Data from the Global Landslide catalogue was used to get a list of landslides in Nepal. For the weather conditions, data was obtained from the 
“District Wise Climate Data for Nepal” dataset by Open Data Nepal which was accumulated from NASA Langley Research Center (LaRC) POWER Project. These two datasets were merged to 
obtain a dataset with landslide and weather conditions. For the false labels, random data was sampled from the district-wise climate dataset which is not present in the Landslide 
Catalog. There was not enough data to train the model. So, TabGAN was used to generate more data. Finally, the data was trained on shallow XGBoost, Logistic Regression, and 
RandomForest and their ensemble was used to get the final prediction.
