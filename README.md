# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 

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

df = pd.read_csv("bmw dataset.csv") 

df_grouped = df.groupby('year')['price'].mean()

plt.figure(figsize=(10, 5))
df_grouped.plot(kind='line', label='Average Price', color='black', marker='o')
plt.title('Average BMW Price per Year')
plt.xlabel('Year')
plt.ylabel('Average Price (£)')
plt.legend()
plt.grid(True)
plt.show()
```


# OUTPUT:

<img width="1212" height="652" alt="image" src="https://github.com/user-attachments/assets/948c8a38-03ad-4dc0-9c9d-46de5508b731" />

# RESULT:
Thus we have created the python code for plotting the time series of given data.
