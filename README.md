# Forecast-Country-index-for-2021-2039-year
When the most contributed World development indicators which tell us about country worth find out then applying various time series analysis method study the behavior of country worth is possible. And by studying the behavior of country index as per variation of time then it is possible to apply different forecasting method on it. And results of that forecasting model will gives the forecasting data and on that forecasting when again Applied MCDM technics.  Like TOPSIS then it is very possible that behavior country Index(Country Worth ) will be predicted for next some of year.
# FORECASTING THE COUNTRY DATA FOR NEXT 20 YEAR.

## Selection Of Forecasting Model For Indicators
 In time serious analysis method there are five best suitable model for our data set, which are Trend analysis model, Autoregressive model, double exponential smoothing model, triple exponential smoothing model and fifth one is simple linear regression model. Our data has 127 indicator column and each indicator has different characteristics like in one indicator has trend characteristics and other indicator shows seasonal characteristics or there is exponential increasing characteristics or exponential decries characteristics so likewise prediction of which characteristics can be present in which indicators data is not possible.so which one forecasting method is applied to which indicator is quite difficult. 
  The solution for this problem is we have to use python coding in that coding first of all there is need to make two part of our data one is testing data and second one training data. testing data is must less in size in compare of training data. So distribution of data is done in which 30% is testing data and 70% is training data. Next is to developed forecasting model and fed that data to that forecasting model. By fetching the data to that model it predict data. As the predicted data is available for all 127 indicators then compare this predicted data to the testing data and calculate root mean square error. Error which we get is from the first foresting model. When applied this same process for all five-forecasting model we get five different rmse error value for each indicator. So which forecasting model shows less rmse value that indicator then this model is consider as the best forecasting model for this particular indicator. Use this foresting model and predict the futuristic data of that indicator. This process is repent for each indicator in each country so we can get hole next 20 year of futuristic data.

## Model 1. Trend Analysis
 Trend analysis is a mathematical method used to calculate future value  as a linear function of previous samples. 

## Model 2. Autoregressive (AR)
Autoregressive modelling is training a regression model on the value of response variable itself. Autoregressive is made of the word, Auto and Regressive which represents the linear regression on itself (auto). In context of time-series forecasting, autoregressive modelling will mean creating the model where the response variable Y will depend upon the previous values of Y at a pre-determined constant time lag. The time lag can be daily (or 2, 3, 4… days), weekly, monthly etc.
Y_t=β_0+β_1*Y_(t-1)+error

In the above model, the value at the last time lag is taken. If the time lag is weekly, the
 Y_t-1 will represent the value of Y of the last week. Such an AR models where the value of response variable of just one time lag is taken are called as AR models of first model or AR (1) models.AR models have the parameter termed as p. The parameter p represents the previous values of p number of time lags when training the model. The AR model of 2nd order will have the value of response variable at any particular time depend upon the values of last two lags. Thus, AR (2) model will look like the following:
 
Y_t=β_0+β_1*Y_(t-1)+β_2*Y_(t-2)+error.
Generalizing the above for p, the AR (p) model will look like the following:
Y_t=β_0+β_1*Y_(t-1)+β_2*Y_(t-2)+⋯+β_p*Y_(t-p)+error

## Model 3. Double exponential smoothing
This smoothing method start with setting S2 to y1, where Si stands for smoothing observation , and y is original observation. And the time periods is , 1,2,…,n. For the 3rd  period,
 S3=αy2+(1-α)S2;
 and it continued ..
For every time period the smoothing as follows:
St=αyt-1+(1-α)St-10<α≤1t≥3.
This is the model of exponential smoothing and  α is smoothing constant.

## Model 4. Triple Exponential Smoothing
 In double exponential smoothing will not applicable. For controlling such situation we need to introduce seasonality . and the equation called as the Holt Winter method.
The basic holt winter equation:
St=a  y_t/I_(t-L) +(1-a)(S_(t-1)+b_(t-1))………overall exponential smoothing
b_t=γ(S_t-S_(t-1) )+(1-γ)b_(t-1)      …………. trend exponential smoothing
I_t=β y_t/S_t +(1-β)I_(t-L)        …………..seasonal exponential smoothing
F_(t+m)=〖(S〗_t+mbt)I_(t-L)+m         …. …..  ……..exponential forecast,

where
•	y is observation
•	S is  smoothing observation
•	b is trend factor
•	I is seasonal index
•	F is  forecast
•	t is an time period index
 α,β,and γ are constants that must be forecast as the error value must be minimum.

## Model 5. Simple Linear Regression 
Simple Linear Regression models have the following components:
unknown parameters, in linear regression is denoted as a scalar or vector .β.
Independent variables, in linear regression is denoted as a vector  X_i   
Dependent variable, in the linear regression denoted as a scalar Y_(i .)
error terms, In linear regression denoted as a scalar .e_i
Simple linear regression model shows the specification that the dependent variable,  y_i  is a linear combination of the parameter. In simple linear regression for getting  n data points there is one independent variable: 〗x_i, and two unknown parameters,  β_0  and β_1:
straight line equation: y_i=β_0+β_1 x_i+ε_i,    i=1,2,……,n

