## Ex.No: 1B CONVERSION OF NON STATIONARY TO STATIONARY DATA
## Name:Tharunish vasan T
## Register no:212224240174
## Date:25/10/26
## AIM:
To perform regular differncing,seasonal adjustment and log transformatio on international airline passenger data

## ALGORITHM:
Import the required packages like pandas and numpy
Read the data using the pandas
Perform the data preprocessing if needed and apply regular differncing,seasonal adjustment,log transformation.
Plot the data according to need, before and after regular differncing,seasonal adjustment,log transformation.
Display the overall results.
PROGRAM:
```
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import tkinter as tk
from tkinter import filedialog
from statsmodels.tsa.seasonal import seasonal_decompose

root = tk.Tk()
root.withdraw()
root.attributes("-topmost", True)

file_path = filedialog.askopenfilename(
    title="Select AirPassengers.csv",
    filetypes=[("CSV files", "*.csv")]
)

root.destroy()
df.head()


data = pd.read_csv(file_path)
    period=12
)
data['passengers_log_seasonal_diff'] = result.resid

plt.figure(figsize=(16, 16))

plt.subplot(6, 1, 1)
plt.plot(data['#Passengers'], label='Original')
plt.legend(loc='best')
plt.title('Original Data')
plt.xlabel('Year')
plt.ylabel('No of passengers')

plt.subplot(6, 1, 2)
plt.plot(data['passengers_diff'], label='Regular Difference')
plt.legend(loc='best')
plt.title('Regular Differencing')
plt.xlabel('Year')
plt.ylabel('Differenced No of passengers')

plt.subplot(6, 1, 3)
plt.plot(data['passengers_sea_diff'], label='Seasonal Adjustment')
plt.legend(loc='best')
plt.title('Seasonal Adjustment')
plt.xlabel('Year')
plt.ylabel('Seasonally adjusted passengers')

plt.subplot(6, 1, 4)
plt.plot(data['passengers_log'], label='Log Transformation')
plt.legend(loc='best')
plt.title('Log Transformation')
plt.xlabel('Year')
plt.ylabel('Log(No of passengers)')

plt.subplot(6, 1, 5)
plt.plot(
    data['passengers_log_diff'],
    label='Log Transformation and Regular Differencing'
)
plt.legend(loc='best')
plt.title('Log Transformation and Regular Differencing')
plt.xlabel('Year')
plt.ylabel('Diff(Log(No of passengers))')

plt.subplot(6, 1, 6)
plt.plot(
    data['passengers_log_seasonal_diff'],
    label='Log Transformation and Seasonal Adjustment'
)
plt.legend(loc='best')
plt.title(
    'Log Transformation, Regular Differencing and Seasonal Adjustment'
)
plt.xlabel('Year')
plt.ylabel('Adjusted differenced log passengers')

plt.tight_layout()
plt.show()

data.plot(kind='line', figsize=(12, 6))
plt.title('Overall Time Series Comparison')
plt.show()
```
OUTPUT:
ORIGINAL DATA:
<img width="1259" height="220" alt="image_3" src="https://github.com/user-attachments/assets/bc230f5e-b690-4809-a8eb-217a9806fd44" />
REGULAR DIFFERENCING:
<img width="1185" height="186" alt="image_4" src="https://github.com/user-attachments/assets/3315438b-3693-43c3-9f84-2b035ae60eae" />
SEASONAL ADJUSTMENT:
<img width="1123" height="187" alt="image_5" src="https://github.com/user-attachments/assets/e7ef17fd-f51b-4b68-9d85-b54ea8c0d36d" />
LOG TRANSFORMATION:
<img width="1166" height="172" alt="image_6" src="https://github.com/user-attachments/assets/5451ce7a-39a9-4e9f-80d9-14485ba2c630" />
LOG TRANSFORMATION AND REGULAR DIFFERENCING:
<img width="1232" height="172" alt="image_7" src="https://github.com/user-attachments/assets/32928e98-2e75-4b76-b1d3-6d9c9b299afa" />


RESULT:
Thus we have created the python code for the conversion of non stationary to stationary data on international airline passenger data.
