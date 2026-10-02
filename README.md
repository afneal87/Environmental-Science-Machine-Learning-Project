# Environmental-Science-Machine-Learning-Project
Machine learning project exploring the predictive power of satellite imagery on precipitation rates 

Accurate global precipitation measurements are essential for understanding Earth's water and energy cycles and for forecasting extreme events such as tropical cyclones. The Global Precipitation Measurement (GPM) mission initiated by NASA and the Japan Aerospace Exploration Agency (JAXA) is an international constellation of satellites that provides near-global observations of rain and snow. The satellites collect data on precipitation levels using microwave imaging across thirteen frequency channels ranging from 10 to 183 GHz. Observations from these channels are referred to as brightness temperatures (Tb) measured in degrees Kelvin. The observations quantify the intensity of microwave radiation emitted or scattered by Earth's surface at a specific frequency. Atmospheric conditions such as rain, snow, or ice cause different responses in microwave radiation readings across the frequency channels. In practice, the data collected by these frequency channels is known as Level 1 data, which alone does not provide precipitation or atmospheric condition indications. The data from these channels must be combined and converted to Level 2B to determine atmospheric conditions.

The purpose of this project was to predict precipitation rates and frequency using passive microwave measurements without the combination and conversion to Level 2 data. Using Level 1 data from satellites concentrated over the Indo-Pacific Warm Pool and Level 2B combined data, this project includes the construction of machine learning models to predict the Level 2B outcome data using only the Level 1B frequency channels. 

The dataset used here contains 896,712 observations from July 1, 2024 to August 1, 2024. Each observation contains a temperature reading for each of the 13 frequency channels and the Level 2B precipitation rate. All models used the thirteen frequency channel readings as features and the precipitation rate as the outcome. 

## Variables included in dataset

| Variable | Name | Unit | Frequency | Polarization | Variable Type | Typical Sensitivity |
| -------- | ---- | ---- | --------- | ------------ | ------------- | ------------------- |
| Tb1 | Brightness temperature channel 1 | Kelvin | ~10.65 GHz | Vertical | Heavy to moderate rainfall |
| Tb2 | Brightness temperature channel 2 | Kelvin | ~10.65 GHz | Horizontal | Heavy to moderate rainfall |
| Tb3 | Brightness temperature channel 3 | Kelvin | ~18.7 GHz | Vertical | Numeric | Heavy to moderate rainfall |
| Tb4 | Brightness temperature channel 4 | Kelvin | ~18.7 GHz | Horizontal | Numeric | Heavy to moderate rainfall |
| Tb5 | Brightness temperature channel 5 | Kelvin | ~23.8 GHz | Vertical | Numeric | Heavy to moderate rainfall |
| Tb6 | Brightness temperature channel 6 | Kelvin | ~36.5 GHz | Vertical | Numeric | Precipitation mixtures of snow and ice within clouds |
| Tb7 | Brightness temperature channel 7 | Kelvin | ~36.5 GHz | Horizontal | Numeric | Precipitation mixtures of snow and ice within clouds |
| Tb8 | Brightness temperature channel 8 | Kelvin | ~89 GHz | Vertical | Numeric | Precipitation mixtures of snow and ice within clouds | 
| Tb9 | Brightness temperature channel 9 | Kelvin | ~89 GHz | Horizontal | Numeric | Precipitation mixtures of snow and ice within clouds |
| Tb10 | Brightness temperature channel 10 | Kelvin | ~166 GHz | Vertical | Numeric | Water vapor and snowfall |
| Tb11 | Brightness temperature channel 11 | Kelvin | ~166 GHz | Horizontal | Numeric | Water vapor and snowfall |
| Tb12 | Brightness temperature channel 12 | Kelvin | ~183.3+-3 GHz | Vertical | Numeric | Water vapor and snowfall |
| Tb13 | Brightness temperature channel 13 | Kelvin | ~183+-7 GHz | Vertical | Numeric | Water vapor and snowfall |
| pr | Precipitation rate | Millimeters per hour | N/A | N/A | Numeric | N/A |
| lon | Longitude | Degrees east | N/A | N/A | Numeric | N/A |
| lat | Latitude | Degrees North | N/A | N/A | Numeric | N/A |
| time | Time of observation | Standard | N/A | N/A | datetime | N/A | 
