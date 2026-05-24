## BENGALURU URBAN FLOOD RISK PREDICTOR 

## DESCRIPTION 
* This project is a machine learning pipeline used to predict risk of flooding in urban bengaluru areas
* The ML model uses a spatial cross verification with random forest algorithm to generate a reliable classification report.
* Using this model , the predict.ipynb creates a risk map and generates the areas with high flood risk.

## DATASETS USED 
* CHIRPS PRECIPITATION DATASET (https://www.chc.ucsb.edu/data/chirps)
* CARTOSAT - 1 DEM FROM BHOONIDHI WEBSITE (30 m X 30 m)
* BBMP FLOOD POINTS (https://data.opencity.in/dataset/flooding-locations-in-bengaluru-urban) [ GIVEN IN THE REPO]

## DEPENDENCIES (PYTHON MODULES)

* rasterio
* numpy
* matplotlib
* fiona
* sklearn
* geopandas
* pandas
* joblib
* scipy.ndimage
* requests

  ```bash
  pip install rasterio geopandas fiona scikit-learn numpy pandas scipy matplotlib geopy joblib requests
  ```

  ## HOW TO WORK WITH THE PROJECT

  * RUN THE NOTEBOOK predict.ipynb after pulling the entire repo.
  * THERE IS NO NEED TO TRAIN THE MODEL AGAIN. USE THE .pkl file
  * HOWEVER, IF YOU WISH TO TRAIN THE MODEL USE THE ABOVE DATASETS OR DATASETS OF YOUR CHOICE AND CHANGE train.ipynb accordingly 

  ## FEATURES USED FOR ML MODEL

  * TOTAL RAINFALL - RAINWATER ACCUMULATES OVER TIME TO CLOG DRAINS CREATING STAGNATE WATER
  * MEAN RAINFALL - HIGHER RAINFALL IN AVERAGE WILL LEAD TO A HIGHER CHANCE OF FLOODING
  * SLOPE - STEEP SLOPES DRAIN QUICKLY WHILE LOW SLOPES BECOME WATER COLLECTION SPOTS
  * HEIGHT FROM SEA LEVEL - LOWER ELEVATION AREAS BECOME NATURAL WATER COLLECTION POINTS
  * MAX RAINFALL - PEAK RAINFALL IN ONE DAY CAN TRIGGER FLASH FLOODING
