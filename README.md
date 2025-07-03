# Forecasting Agirucultural Products in Indonesia using ARIMA models
This project conduct a time series forecasting using ARIMA python, to predict 10 years ahead of each agricultrual yields in indonesia. Using a producer-prices_idn.csv, containing information about many agricultural items in indonesia like month and year values (our target variables), elements, start-end date, etc. At the end the historical and predicted data will be exported to excel to build an interactive dashboard in Power BI

### Tools
Jupyter notebook, Excel, Power BI

### Data preparation
Since the data already cleared, we straight to the preparations like
1. Delete the irrelevant columns that don't contribute to the predictive analysis such as area code, element code etc
2. Knowing the data types of each column
3. Transforming the data types to the type of data that should be like numeric in values, and date time in start-end date
The preparation is as follows
![image](https://github.com/user-attachments/assets/21cd1899-57ed-421c-addf-037241c45ad3)

### Modelling
Straight to modelling, since the dataset contains a large number of items, I selected 21 sample items for prediction.
In the modelling phase, i performed the following code such as
1. Input the item that we want to predict. It allows the user to input a specific item to predict, then filters the data to include only the selected item, the Producer Price Index element, and the annual values. The filtered subset is then used for further analysis or prediction modeling.
2. Removing outliers that contain in the dataset using IQR method
3. Plot the filtered dataset to identify whether the data was seasonal or non-seasonal.
4. Performed ACF and PACF plots to determine appropriate ARIMA parameters for each item.
5. Compared the actual data to the model’s predictions by plotting them together for visual evaluation.
6. Final step of this project is visualize a time series forecast for the next 10 years using Python and Plotly. The plot combines historical data with forecasted values in a single interactive line chart to illustrate both past trends and future projections.

Let me take you to an example tour of this modelling phase
First, we selected ‘Abaca, manila hemp, raw’ as the example item for our model.
![image](https://github.com/user-attachments/assets/aeeac3ab-2373-459b-b517-1daa8f578328)

Removing the outliers

![image](https://github.com/user-attachments/assets/1bdbfacf-959d-4fba-9250-3faa4e308957)

Then we plot the series to identify whether the data was seasonal or non-seasonal, and plot the ACF-PACF to determine appropriate ARIMA parameters for each item.

![image](https://github.com/user-attachments/assets/d08ac405-a1aa-4c36-8d74-a83214a2bfb3)

![image](https://github.com/user-attachments/assets/59b57448-91ca-4a4c-a02d-b45693ae5b98)

![image](https://github.com/user-attachments/assets/cd8cb224-a1c5-4cea-bca6-bfd80f28cc14)

![image](https://github.com/user-attachments/assets/1de5c4e8-f269-449c-8a12-8b4b8679b896)

Then we build the models to compare the actual data to the model’s predictions

![image](https://github.com/user-attachments/assets/940fc487-3c1a-4b86-874b-bdeb9e9f7fce)

![image](https://github.com/user-attachments/assets/6a8413af-dbaa-45d1-ab48-203ac81853af)

The red line is a predicted values, the blue line is the actual/historical values

Then we forecast the item’s values for the next 10 years.

![image](https://github.com/user-attachments/assets/44c1ae04-2319-4fa4-b2cc-ff75a75a3814)

Combine the historical and predicted values using Plot

![image](https://github.com/user-attachments/assets/169588c9-43d1-4a3f-b59b-2d3a33d5e0c9)

The predicted values will be exported to excel to build an interactive dashboard in Power BI

Here is the dashboard that i've made
![image](https://github.com/user-attachments/assets/f239c5e0-03b3-4b72-a514-f2133601136b)

This interactive Power BI dashboard, titled “The Future of Indonesian Agriculture,” provides a comprehensive overview of agricultural commodity trends based on the Producer Price Index (2014–2016 = 100). It combines both historical data and forecasted values to support strategic decision-making.

Key features:
- Total Overview: Displays the total number of items analyzed (21), the total value and average value of all items, and the projected total and average values including forecasts.
- Detailed Breakdown: Shows a breakdown of individual items with their historical value and forecasted value side by side for easy comparison.
- Slicers for Interactivity: Users can interactively filter and compare historical vs. forecast data using slicers, making it easier to analyze specific commodities or time periods.
- Visual Insights:
  - Donut charts highlight the contribution of each item to the overall total, both historically and with predictions included.
  - Line charts display the trend of the sum of value by year, clearly distinguishing between historical data and the 10-year forecast period (2024–2034).
  - Visual cues, such as color coding and labels, make it easy to interpret the projected trends alongside past performance.
This dashboard helps stakeholders understand how Indonesia’s key agricultural commodities have performed historically and how they are expected to develop in the coming decade, providing actionable insights for policy-making and investment planning.






