# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date:

# AIM:
To Develop a python program to Plot a time series data of XAUUSD


# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Plot the data according to need and can be altered monthly, or yearly.
4. Display the graph.

   
# PROGRAM:
```py
import pandas as pd
import matplotlib.pyplot as plt

file_path = 'XAUUSD_2010-2023.csv'
data = pd.read_csv(file_path)

data['time'] = pd.to_datetime(data['time'], format='%d-%m-%Y %H:%M')

data.set_index('time', inplace=True)

plt.figure(figsize=(14, 7))
plt.plot(data['close'], label='Close Price', color='blue')
plt.title('XAUUSD Close Price Time Series (2010-2023)')
plt.xlabel('Date')
plt.ylabel('Close Price')
plt.legend()
plt.grid(True)
plt.show()

```

# OUTPUT:
![image](https://github.com/user-attachments/assets/e3074388-1464-4a8b-a78a-dd26f3050108)

# RESULT:
Thus we have created the python code for plotting the time series of given data.
