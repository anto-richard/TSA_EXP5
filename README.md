### Ex.No: 05 
# <p align="center">  IMPLEMENTATION OF TIME SERIES ANALYSIS AND DECOMPOSITION...</p>

### Date: 29.03.24

### AIM :

To Illustrate how to perform time series analysis and decomposition on the monthly average temperature of a city/country and for airline passengers.

### ALGORITHM :

#### Step 1 :

Import the required packages like pandas and numpy.

#### Step 2 :

Read the data using the pandas.

#### Step 3 :

Perform the decomposition process for the required data.

#### Step 4 :

Plot the data according to need, either seasonal_decomposition or trend plot.

#### Step 5 :

Display the overall results.

### PROGRAM:

```python

!pip install pandas

import pandas as pd
import matplotlib.pyplot as plt
from statsmodels.tsa.seasonal import seasonal_decompose

# Load dataset (replace with your data)
data = pd.read_csv('/content/Temperature.csv')

# Convert 'date' column to datetime format and set as index
data['Month'] = pd.to_datetime(data['Month'])
data.set_index('Month', inplace=True)

# Specify the period for decomposition
period = 12  # Change this to the appropriate period for your data

# Perform decomposition
result = seasonal_decompose(data, model='multiplicative', period=period)

# Plot the decomposition
result.plot()
plt.show()

```

### OUTPUT :

#### FIRST FIVE ROWS :

![img1](https://github.com/anto-richard/TSA_EXP5/assets/93427534/11743d34-8a31-4d5f-a632-2f0694ed230e)

#### PLOTTING THE DATA :

![img2](https://github.com/anto-richard/TSA_EXP5/assets/93427534/8e6b0c3a-5a2f-4dce-b89a-490db0bf45f8)

#### SEASONAL PLOT REPRESENTATION :

![img3](https://github.com/anto-richard/TSA_EXP5/assets/93427534/11cfe909-a550-436c-9265-d9e325946ee3)

#### TREND PLOT REPRESENTATION :

![img4](https://github.com/anto-richard/TSA_EXP5/assets/93427534/16110cca-2799-4f3a-acb3-a09dcbe6c7b1)

#### RESID PLOT REPRESENTATION :

![img5](https://github.com/anto-richard/TSA_EXP5/assets/93427534/02252ebc-c152-43ed-b33b-2c816036f80b)

#### OVERAL REPRESENTATION :

![img6](https://github.com/anto-richard/TSA_EXP5/assets/93427534/5c21bb7a-bf62-474a-990f-bfed687f5a38)

### RESULT :

Thus, we have created the python code for the time series analysis and decomposition.

