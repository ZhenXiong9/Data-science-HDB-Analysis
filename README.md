# Data-science-HDB-Analysis
# About 
This is the mini project for NTU SC1015 (Introduction to Data Science and Artificial Intelligence)

# Introduction
HDB have been a topic of concerns among young adult. Primarly due to Singapore limited land, prices of resale flat can be very compeitive and expensive. According to Straits times, the HDB resale price for the 8 straight month. This project we research into the differnt drivers that drive these HDB resale price. 

![This is an image](https://github.com/ZhenXiong9/Data-science-HDB-Analysis/blob/main/Image/Introduction.PNG?raw=true)



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
3. Core Analysis & Machine Learning
4. Conclusion

# Data Cleaning & Preparation
In this section of the project, we clean and prepare the data so that we can analyze better and also give us a good dataset for machine learning

We did the following:
1. We combine duplicate value (Same name but in upper case)
2. We change data such as Month and Year from Object to DateTime to fit our analysis
3. We also include inflation data so that we can have a more accurate price data

# Exploratory Data Analysis
Resale price is our main dependent variable. We use it to perform many bi-variate with other variable. Such as amount of sale over the year of 1991-2021. As predicted, there is a steady increase in resale price over the years. 
![This is an image](https://github.com/ZhenXiong9/Data-science-HDB-Analysis/blob/main/Image/EDA2.PNG?raw=true)

Similarly, we use it analyze storey data and found that higher the storey, higher the price
![This is an image](https://github.com/ZhenXiong9/Data-science-HDB-Analysis/blob/main/Image/EDA3.PNG?raw=true)

Lastly, we plot a chart using resale price and area per square metre and confirm that larger the area, higher the price
![This is an image](https://github.com/ZhenXiong9/Data-science-HDB-Analysis/blob/main/Image/EDA4.PNG?raw=true)

We perform a correaltion analysis with key column such as Year, Leasing Remaining, Area per square meter and Year Gni (Gross National Income)   
![This is an image](https://github.com/ZhenXiong9/Data-science-HDB-Analysis/blob/main/Image/EDA1.PNG?raw=true)


# Core Analysis & Machine Learning
We explored the data column by column for MRT walking datasets and  perform a train-test split to ensure backtesting.
About ⅓ of the data falls into the test datasets.
Next we create a regression model using train data and apply regression model on test data
From our model, we can observe that there is a weak negative linear relationship, and Mr. and mrs lee can expect House price decreases for about 5-6% for 1 std increase in Walking Distance to MRT;
So the shorter the distance, the higher the resale price of HDB
![This is an image](https://github.com/ZhenXiong9/Data-science-HDB-Analysis/blob/main/Image/CA1.PNG?raw=true)

In Addition to linear regression, we also studied and tested 3 different machine learning algorithms for floor area including 
Decision tree regression, Lasso Regression and Ridge Regression. 
The results have shown that decision tree in particular has the most reduced variance and in increase bias compared to the other models.
And since all correlation coefficient results is above 0.4, we can easily deemed the correlation between floor area and price as relatively strong.
![This is an image](https://github.com/ZhenXiong9/Data-science-HDB-Analysis/blob/main/Image/CA2.PNG?raw=true)

Firstly, we have categorised different towns into 5 distinct categories regions in singapore (including north, north-east, east, west and central). Having only 5 categories has us to prevent generating a train-test datasets with too many columns. 

From the model prediction, 3-room HDB at North area is the cheapest option (~SGD 360,000), while Central is the most expensive option (close to ~SGD 500,000). 
![This is an image](https://github.com/ZhenXiong9/Data-science-HDB-Analysis/blob/main/Image/CA3.PNG?raw=true)

Similarly for 4-room HDB house, North area is the cheapest option (~SGD 360,000), while Central is the most expensive option (close to ~SGD 600,000). Interestingly, higher cost of HDB located in the Centre might be affected by better access and Central Business District (CBD) area is also located in the Central/South region.
![This is an image](https://github.com/ZhenXiong9/Data-science-HDB-Analysis/blob/main/Image/CA4.PNG?raw=true)




# Conclusion 
- We wanted to try other machine learning model such as SVM for Anomaly detection but couldnt due to time constraints
- We discover that Storey, Flat Type, Total Area and Walking distance from MRT as drivers for HDB Resale Price
- We also discover many other factors we could have included to improve our analysis
  1. BTO Development (The development of BTO around the area will surely affect resale price)
  2. Other Amenities (Amenities such as markets, food centre, schools, health care will affect the resale price as well)
  3. Travelling time to key location (Travelling time to location such as CBD, Town Area and central affect the price)
  4. Year anenities is built (Some amenities are not built when the flat are sold, like many mrt stations are built in the last 3 years. Therefore using MRT as a          driver can be inaccurate)
 
  


