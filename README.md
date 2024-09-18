---
# **Optimizing Taxi Fleet Management Throught Predictive Analytics of NYC Taxi Cab Trip Data 🚖**
---

![TaxiImage](Taxi_Ride.png)

### **Premise** 📁

The project aims to leverage historical NYC taxi cab data to predict the number of rides, facilitating better urban planning and transportation management. Using data from January 2023 to May 2024, the project focuses on analyzing key factors influencing taxi demand and developing predictive models.

### **Problem Statement** 📝

In this project, I focus on predicting the number of rides in NYC using taxi cab data. The dataset is sourced from the [NYC TLC Trip Record Data website](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page), and it includes records from January 2023 to May 2024. For training, I utilized data from January to December 2023, and for testing, I used data from January to May 2024.

The core problem is to accurately predict the number of taxi rides in NYC based on historical data, considering various factors such as weather conditions, trip distance, and fare amounts. This requires thorough data preprocessing, feature engineering, and the application of machine learning and deep learning models to capture patterns and trends in the data.

### **Beneficiaries** 🤝

This project primarily benefits urban planners and transportation managers by providing them with valuable insights into taxi demand patterns. Accurate ride predictions can help optimize resource allocation, improve traffic management, and enhance overall urban mobility in NYC.


### **Preprocessing** 🛠️

During the initial data cleaning process, I identified and corrected instances of invalid dates and filled in missing time slots to ensure the dataset's completeness and accuracy.

### **Exploratory Data Analysis (EDA)** 📊

I conducted an initial exploration of the data, focusing on key columns to understand the factors influencing taxi demand:

- **Temperature**: Analyzed the impact of weather conditions on ride demand.
- **Wind Speed**: Investigated the effect of wind speed on taxi usage.
- **Trip Distance**: Examined the relationship between trip distance and demand.
- **Total Fare Amount**: Explored the correlation between total fare and the number of rides.
- **Trip Duration Hours(Created)**: Calculated a new feature, "trip_duration_hours," to capture the time taken for each ride.

### **Feature Engineering** ⚙️

Based on the insights from EDA, I constructed the target variable, **"No_of_rides"** which was not present in the original dataset. This variable aims to predict the number of rides occurring at specific times and locations. The primary features for prediction are **"pickup_location_id"** and **"pickup_time"**

### **Modeling** 🤖

To address the predictive task, I am using machine learning algorithms such as linear regression and XGBoost. This approach will allow me to evaluate the effectiveness of different models in capturing the patterns in the data and achieving accurate predictions.

### **Further Exploration: Deep Learning** 🧠

In addition to time series models, I am also exploring deep learning model such as **simple neural network**. This comprehensive approach will allow me to compare the performance of various techniques and potentially achieve more accurate predictions.

By employing these models, I aim to develop a robust model that can predict the number of taxi rides in NYC with high accuracy, contributing valuable insights for urban planning and transportation management.


### **Data Dictionary** 📚

This data dictionary describes the yellow taxi trip data used in the project:

- **VendorID**: A code indicating the TPEP provider that provided the record.
  - 1 = Creative Mobile Technologies, LLC
  - 2 = VeriFone Inc.
- **tpep_pickup_datetime**: The date and time when the meter was engaged.
- **tpep_dropoff_datetime**: The date and time when the meter was disengaged.
- **Passenger_count**: The number of passengers in the vehicle. This is a driver-entered value.
- **Trip_distance**: The elapsed trip distance in miles reported by the taximeter.
- **PULocationID**: TLC Taxi Zone in which the taximeter was engaged.
- **DOLocationID**: TLC Taxi Zone in which the taximeter was disengaged.
- **RateCodeID**: The final rate code in effect at the end of the trip.
  - 1 = Standard rate
  - 2 = JFK
  - 3 = Newark
  - 4 = Nassau or Westchester
  - 5 = Negotiated fare
  - 6 = Group ride
- **Store_and_fwd_flag**: This flag indicates whether the trip record was held in vehicle memory before sending to the vendor (store and forward) because the vehicle did not have a connection to the server.
  - Y = store and forward trip
  - N = not a store and forward trip
- **Payment_type**: A numeric code signifying how the passenger paid for the trip.
  - 1 = Credit card
  - 2 = Cash
  - 3 = No charge
  - 4 = Dispute
  - 5 = Unknown
  - 6 = Voided trip
- **Fare_amount**: The time-and-distance fare calculated by the meter.
- **Extra**: Miscellaneous extras and surcharges. This includes the 0.50 and 1 rush hour and overnight charges.
- **MTA_tax**: 0.50 MTA tax that is automatically triggered based on the metered rate in use.
- **Improvement_surcharge**: 0.30 improvement surcharge assessed trips at the flag drop. The improvement surcharge began being levied in 2015.
- **Tip_amount**: Tip amount. This field is automatically populated for credit card tips. Cash tips are not included.
- **Tolls_amount**: Total amount of all tolls paid in trip.
- **Total_amount**: The total amount charged to passengers. Does not include cash tips.
- **Congestion_Surcharge**: Total amount collected in trip for NYS congestion surcharge.
- **Airport_fee**: $1.25 for pick up only at LaGuardia and John F. Kennedy Airports.

### **Conclusion**

In terms of operational costs, **Linear Regression** may be the most cost-effective option due to its simplicity. However, **XGBoost** offers a balance of performance and efficiency, making it a strong candidate for deployment. The **Neural Network**, while potentially more expensive to operate, could be the best choice if the goal is to achieve the highest accuracy in ride demand predictions, particularly when considering long-term operational strategies and customer satisfaction. Ultimately, the choice of model should align with the company's strategic goals, resource availability, and desired level of predictive accuracy.

From a business perspective, accurately predicting ride demand is crucial for optimizing resource allocation, improving customer satisfaction, and enhancing operational efficiency. For instance, a transportation company can use these predictions to ensure that an adequate number of vehicles and drivers are available during peak demand times, reducing wait times for customers and increasing overall service quality. Additionally, accurate demand forecasting can lead to better strategic planning, such as targeted marketing campaigns and **efficient fleet management, ultimately driving profitability and customer loyalty**.
