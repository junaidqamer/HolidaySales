# *Holiday Sales*



## BACKGROUND

Holiday sales numbers have long been regarded as a strong GDP growth indicator. If sales numbers are high there's a strong correlation to growth in GDP. When there is a downturn in GDP, gold prices tend to rise. Gold has long been used as a safety net during times of economic downturn by investors.
Using this information, we will test out 28 years worth of data to build various machine learning (supervised and unsupervised) to attempt to predict holiday sales numbers. In turn it can be infer from this information whether there will be GDP growth and whether gold prices will rise or fall.

## QUESTIONS TO BE ANSWERED:

1. Is there a correlation between high holiday sales number and GDP growth?

2. Is there a negative correlation between GDP and gold prices and the retail index and gold prices?

3. Can we predict gold prices by predicting holiday sales?

4. Which is the best model to make our predicitons?

## RESOURCES

1. *Vader Sentiment Analysis*
2. *Python*
3. *NLK library*
4. *NER*
5. *SpaCY library*
6. *NYT API Client*
7. *Pandas*
8. *bea GDP numbers*
9. *Regression modeling such as Random forest, Decision tree, Gradient boosted Regression and Linear regression*
10. *Unsupervised learning- LSTM


## PROCEDURE

Using 28 years of past holiday sales data, NYT news sentiment(NLP), GDP raw data, unemployment numbers, gas prices, consumer sentiments,inflation, retail index, and gold returns we use this data to predict 2020 holiday sales. If the holiday sales are high, we can assume there will be growth in GDP, therefore gold prices will drop and vice versa.


## FINDINGS

After using various machine learning models, these were our finding with each model:

## *Linear Regression*

After running a linear regression model with all our features (10 columns: NYT sentiment, unemployment rate, CPI, consumer debt service, GDP growth, retail index, GDP, gas prices, consumer sentiments and gold prices) as our X and using holiday sales numbers as our Y. We found the following:

R2 score: .96

MAE:

RMSE:

### Linear Regression Predictive

After seeing our model had a high R2 score, we decided to utilize this model and build a predictive linerar regression. We accomplished this by shifting our Y and running a new model by dropping retail_index, consumer_sentiments, and gas_prices. We found the following:

R2 score: .88

MAE: 14322.72408070424

RMSE:19658.106063704592

## *Decision Tree*

![alt text](https://github.com/junaidqamer/HolidaySales/blob/main/Graphs/DECISION%20TREE%20MODEL.png)


We ran a decision tree with all our 10 features described above. Our results were:

R2 score: 0.745755446603428

MSE:409789556.65769035

RMSE: 20243.259536391128

### Decision Tree Predictive

![alt text](https://github.com/junaidqamer/HolidaySales/blob/main/Graphs/PREDIC%20DECISION%20TREE.png)

We wanted to see if we could possibly improve the outcome of this model. So we also built a predictive model: By dropping the same columns as our last model:

R2 score: 0.8786481710499019

MAE:243538750.19026047

RMSE:15605.728121118234

our model improved score after dropping 3 features.

## *Random Forest*

![alt text](https://github.com/junaidqamer/HolidaySales/blob/main/Graphs/RANDOM%20FOREST.png)


We ran a Random Forest with all our 10 features described above. Our results were:

R2 score: 0.9554075279949993

MAE:71873828.12550409

RMSE:8477.843365237653

### Random Forest Predictive Model

![alt text](https://github.com/junaidqamer/HolidaySales/blob/main/Graphs/PREDIC%20RANDOM%20FOREST.png)

We performed the same procedure, shifted our y and dropped 3 features in our X.
 
R2 score: 0.9628939513351432

MAE:74467445.56321658

RMSE: 8629.452216868494
 
## *Gradient Boost Regressor*

![alt text](http://url/to/img.png)

Same procedure: Using the following learning rates, learning_rates = [0.05, 0.1, 0.25, 0.5, 0.75, 1] in a function.

R2 score: 0.7951030399567943

MSE:330251457.8774289

RMSE: 18172.82195690666

### Predictive Gradient Boost Model

![alt text](https://github.com/junaidqamer/HolidaySales/blob/main/Graphs/predict%20gradient%20boost.png)

R2 score: 0.5995808818136175

MSE:627821243.6266602

RMSE: 25056.361340519103

## LSTM Unsupervised learning

![alt text](http://url/to/img.png)

R2 score: 0.6446572681010527

MSE:80028449.50779356

RMSE: 8945.86214446621

### Predictive LSTM

![alt text](http://url/to/img.png)


