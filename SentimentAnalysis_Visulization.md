## Sentiment Over time plot
Sentence Score is the probability of the corresponding sentiment: {-1:negative 0:neutral 1:positive}.
It can be also understand as the strength of the sentiment.


As a result, we could observe that there is a big difference for the 'positive' part of the plot. It seems that the Chinese Naive Bayes model have some trouble identifying positive sentiment in the fiction while the English model can describe the sentiment progress in a highly accurate manner.
There are some possible cause of this problem, one is the choice of tokenizer, the other problem might be the methodology we appleid, we divide the full text into equal sized chunks and use our model to predict on those chunks; this could have caused some confusion for the model based the nature of Chinese language.

### Chinese ThreeBody01:
<img src="https://github.com/kli486/ThreeBodyProblem_Sentiment_Analysis/blob/main/Figures/Santi_01_Sentiment_Overtime.png" alt="Santi_01_SentimentOvertime" width="600" height="300"/>

### English ThreeBody01:
<img src="https://github.com/kli486/ThreeBodyProblem_Sentiment_Analysis/blob/main/Figures/ThreeBody01_Sentiment_Overtime.png" alt="ThreeBody01_SentimentOvertime" width="600" height="300"/>

### Chinese ThreeBody02:
<img src="https://github.com/kli486/ThreeBodyProblem_Sentiment_Analysis/blob/main/Figures/Santi_02_Sentiment_Overtime.png" alt="Santi_02_SentimentOvertime" width="600" height="300"/>

### English ThreeBody02:
<img src="https://github.com/kli486/ThreeBodyProblem_Sentiment_Analysis/blob/main/Figures/ThreeBody02_Sentiment_Overtime.png" alt="ThreeBody02_SentimentOvertime" width="600" height="300"/>


### Chinese ThreeBody03:
<img src="https://github.com/kli486/ThreeBodyProblem_Sentiment_Analysis/blob/main/Figures/Santi_03_Sentiment_Overtime.png" alt="Santi_03_SentimentOvertime" width="600" height="300"/>

### English ThreeBody03:
<img src="https://github.com/kli486/ThreeBodyProblem_Sentiment_Analysis/blob/main/Figures/ThreeBody03_Sentiment_Overtime.png" alt="ThreeBody03_SentimentOvertime" width="600" height="300"/>
