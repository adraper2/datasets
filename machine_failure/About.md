## About the data

This dataset contains 10,000 unique observations of machine milling processes. It is synthetic data used in a conference paper on Explainable AI. It mimics the settings and attributes of the milling machine and rotary cutters as they cut metal. (See image below from Daniel Smyth.)

![alt text](https://github.com/adraper2/datasets/blob/main/machine_failure/milling.jpg?raw=true)

### Data Dictionary (from Kaggle)
- **UDI**: unique identifier ranging from 1 to 10000
- **Product ID**: consisting of a letter L, M, or H for low (50% of all products), medium (30%) and high (20%) as product quality variants and a variant-specific serial number
- **Air temperature [K]**: generated using a random walk process later normalized to a standard deviation of 2 K around 300 K
- **Process temperature [K]**: generated using a random walk process normalized to a standard deviation of 1 K, added to the air temperature plus 10 K
- **Rotational speed [rpm]**: calculated from a power of 2860 W, overlaid with a normally distributed noise
- **Torque [Nm]**: torque values are normally distributed around 40 Nm with a SD = 10 Nm and no negative values
- **Tool wear [min]**: The quality variants H/M/L add 5/3/2 minutes of tool wear to the used tool in the process
- **Machine failure**: indicates, whether the machine has failed in this particular datapoint for any of the following failure modes

#### Failures
There are a total of 339 fails in 10000 processes. The types include:

- Tool wear: the tool will be replaced of fail at a time between 200-240 minutes (replaced 69 times, fails 51)
- heat dissipation (HDF): if difference between air- and process temp is below 8.6K and tool rotation speed is below 1380 rpm (115 fails)
- power (PWF): if power is below 3500W or above 9000W (95 fails)
- overstrain (OSF): if product of tool wear and torque execeeds 11000 minNm (95 fails)
- random: each process has a chance of 0.1% of a fail (5 fails)


### Credit:

Data retrieved from Kaggle: [Predictive Maintenance Dataset AI4I 2020](https://www.kaggle.com/datasets/stephanmatzka/predictive-maintenance-dataset-ai4i-2020/).

S. Matzka, "Explainable Artificial Intelligence for Predictive Maintenance Applications," 2020 Third International Conference on Artificial Intelligence for Industries (AI4I), 2020, pp. 69-74, doi: 10.1109/AI4I49448.2020.00023.
