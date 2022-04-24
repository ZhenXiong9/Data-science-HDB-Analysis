# Data-science-HDB-Analysis
# About 
This is the mini project for NTU SC1015 (Introduction to Data Science and Artificial Intelligence)

# Introduction
HDB have been a topic of concerns among young adult. Primarly due to Singapore limited land, prices of resale flat can be very compeitive and expensive. According to Straits times, the HDB resale price for the 8 straight month. This project we research into the differnt drivers that drive these HDB resale price. 

![This is an image](image/Introduction.PNG)



# Problem Definition
- HDB resale prices over the year
- Factor that affect HDB resale price

# Dataset

https://www.kaggle.com/datasets/denzilg/hdb-flat-prices-19902021-march?resource=download

840,000 transactions of HDB resale flats, including address and geolocation

CPI.csv ( Inflation index over the years)

HDBdata with district_coord_dist_full_withMRTName.csv (MRT coordinates across Singapore)

# Table of Contents: 

1. Data Cleaning & Wrangling
2. Exploratory Data Analysis
3. Insights
4. Conclusion

# Data Cleaning & Preparation
In this section of the project, we clean and prepare the data so that we can analyze better and also give us a good dataset for machine learning

We did the following:
1. We combine duplicate value (Same name but in upper case)
2. We change data such as Month and Year from Object to DateTime to fit our analysis
3. We also include inflation data so that we can have a more accurate price data


# Conclusion 
- We wanted to try other machine learning model such as SVM for Anomaly detection but couldnt due to time constraints
- We discover that Storey, Flat Type, Total Area and Walking distance from MRT as drivers for HDB Resale Price
- We also discover many other factors we could have included to improve our analysis
  1. BTO Development (The development of BTO around the area will surely affect resale price)
  2. Other Amenities (Amenities such as markets, food centre, schools, health care will affect the resale price as well)
  3. Travelling time to key location (Travelling time to location such as CBD, Town Area and central affect the price)
  4. Year anenities is built (Some amenities are not built when the flat are sold, like many mrt stations are built in the last 3 years. Therefore using MRT as a          driver can be inaccurate)
 
  


