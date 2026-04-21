# Ex.No: 01A PLOT A TIME SERIES DATA

###  Date:21/04/26

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.

# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
   
# PROGRAM:

```

from matplotlib import pyplot as plt
import pandas as pd


df = pd.read_csv("/content/BMW_Car_Sales_Classification.csv")


display(df.head())

# Group data by 'Year' and sum 'Price_USD' for time series analysis
df_yearly_sales = df.groupby('Year')['Price_USD'].sum().reset_index()

# Plot the data
plt.figure(figsize=(12, 6))
plt.plot(df_yearly_sales['Year'], df_yearly_sales['Price_USD'], label='Total Sales (USD)', color='blue', marker='o')

plt.title('Time Series Plot of Total Car Sales (USD) by Year')
plt.xlabel('Year')
plt.ylabel('Total Sales (USD)')
plt.legend()
plt.grid(True)
plt.xticks(df_yearly_sales['Year'].unique(), rotation=45)

# Show plot
plt.tight_layout()
plt.show()
```

# OUTPUT:

<img width="1176" height="738" alt="image" src="https://github.com/user-attachments/assets/7c5d5095-98e7-474f-a7c9-729f76ef70cb" />





# RESULT:
Thus we have created the python code for plotting the time series of given data.
