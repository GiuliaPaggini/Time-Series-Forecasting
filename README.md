# On the Granularity of Data: a Comparison between Classical and Deep Learning approaches for Time Series Forecasting
This repository contains all the supporting material I have used for my final work. Time series analysis is the core of the project, in particular ARIMA, SARIMA and LSTM models are compared across three financial datasets with different granularities.
The structure goes as follows:

📈 DATA
  - NASDAQ 100 Index : minute frequency 
  - AAPL Stock Price : daily frequency 
  - WTI Crude Oil Price : monthly frequency 
  
💻 Prophet Models 
- This folder contains the notebooks of the Prophet model. In particular, for both AAPL and WTI Crude Oil data, Prophet is tested both on log returns and adjusted closing price. The plot of the predictions, together with Prophet's components are displayed and extensively commented.

💻 LSTM Models
- This folder contains the notebooks where Long-Short Term Memory model is implemented, using keras and the Sequential object. The model is further wrapped in a KerasRegressor module to be further cross-validated using BlockTimeSeries procedure. The idea behind the model is to consider a look-back period, namely the number of days to use as a training set for making predictions, and a look-forward period, namely the number of minutes, days or months to predict. Lastly, RMSE metric is used to compare the performance of the models against the proposed baseline.

📝 Final Paper 
- The final paper can be visualized at https://www.overleaf.com/project/63f61fd58fcc2803bc84841d)











Colab: https://colab.research.google.com/drive/157etElqtW29wuqbNWBybqjqWhdMsBMpJ#scrollTo=5cn2GzSeFTnu
https://colab.research.google.com/drive/1jkrD2I6Kn4cNpBI0BuamBmp5FSBwkciO#scrollTo=ZwcMcDIcSuGH 

LSTM new https://colab.research.google.com/drive/1eTMbGWu9db1ql_oMTuNwzhn2H7a5QKuJ#scrollTo=12jBIRxyyVII

https://colab.research.google.com/drive/1KzfqZRZfSvFtYxtrnUH-mAXSaiqGVa6t#scrollTo=XTgmNCx3mhkp



