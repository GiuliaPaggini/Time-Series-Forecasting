# On the Granularity of Data: a Comparison between Classical and Deep Learning approaches for Time Series Forecasting
This repository contains all the supporting material I have used for my final work. Time series analysis is the core of the project, in particular ARMA and LSTM models are compared across three financial datasets with different granularities.
The structure goes as follows:

**📈 DATA**
  - NASDAQ 100 Index : minute frequency 
  - AAPL Stock Price : daily frequency 
  - WTI Crude Oil Price : monthly frequency 
  
**💻 ARMA Models**
- This folder contains the notebook where ARMA and a hybrid model ARMA-GARCH are implemented. After a brief exploratory analysis, ARMA(1,1) is fitted on data and subsequently a GARCH(1,1) model is fitted on the residuals. As expected, the coefficient are significative and the model reproduces almost zero returns. According to the literature (see also RiskMetrics by J.P.Morgan) these model orders should be enough to deal with such data. Using a rolling window approach, ARMA is fitted using a look back and look forward period, and subsequently, the results are plotted againsta true data and confidence intervals at 90%.


**ARMA Notebook on Colab:**
- Nasdaq-100: https://colab.research.google.com/drive/1vk59OA905Ef-sAxpqRpDRvzVSLFkA9SB?usp=sharing
- APPL: https://colab.research.google.com/drive/12LYQrW6jNCPRZl5ZqutiJIVdD-bCaoqO?usp=sharing
- WTI: https://colab.research.google.com/drive/17-jIyzVTTBSOr-ZJiuMUBEkwfAGK4AV-?usp=sharing


**💻 LSTM Models**
- This folder contains the notebooks where Long-Short Term Memory model is implemented, using keras and the Sequential object. The model is further wrapped in a KerasRegressor module to be further cross-validated using BlockTimeSeries procedure. The idea behind the model is to consider a look-back period, namely the number of days to use as a training set for making predictions, and a look-forward period, namely the number of minutes, days or months to predict. Lastly, RMSE metric is used to compare the performance of the models against the proposed baseline.

**LSTM Notebook on Colab:**
- Nasdaq-100: https://colab.research.google.com/drive/1IqdDwXIG66M38LbZxOSPeG13MD3iPwwO#scrollTo=Q_dmEStEXyYL
- AAPL: https://colab.research.google.com/drive/1eHXABMXdknTMtFB4HvrzTroudYuT0t6h#scrollTo=90BFT3O2fhZw
- WTI: https://colab.research.google.com/drive/1qAcYKTP6a6i2OyB0BGBALsY49FQv8MYJ#scrollTo=hfaFQFMBf04b


**💻 Prophet Models**
- This folder contains the notebooks of the Prophet model. In particular, for both AAPL and WTI Crude Oil data, Prophet is tested both on log returns and adjusted closing price. The plot of the predictions, together with Prophet's components are displayed and extensively commented.

**Prophet Notebook on Colab:**
- AAPL: https://colab.research.google.com/drive/1A8qiJSabdD7HFMQtS-pqYczNHf6EBoMK?usp=sharing
- WTI: https://colab.research.google.com/drive/1OzfKJRkRCW3tswjcVCEibh6LJgrso47L?usp=sharing

**📝 Final Paper**
- The final paper can be visualized at https://www.overleaf.com/project/63f61fd58fcc2803bc84841d)














