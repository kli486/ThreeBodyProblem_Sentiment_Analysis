# ThreeBodyProblem_Sentiment_Analysis
Analysis of the Famous science fiction: Three Body Problem Triology with NLP Approach.

Inspired by the Lord Of the Ring Sentiment Anlysis Project, we decided to look at the Chinese version and the Translation of the Three Body Problem Triology.
This project dedicates to Two Main task: Explore the differnece between translation and develop a sentiment analysis model for the fiction.


## Data Collection and Processing
Based on the complex literature style of this fiction, we decided to apply Supervised Learning to obtain a sentiment analysis model. The key idea is to have experienced audience label selected text with 'Positive','Neutral',or 'Negative'.



Using [Sentence_Clustering](https://github.com/kli486/ThreeBodyProblem_Sentiment_Analysis/blob/main/Code/SentenceClustering.ipynb), we output mathced_sentence for each trilogy of the science fiction; we examined the data set and foundthat short sentences tend to be meaningless for our prediction,after cleaning out the irrelavent sentences, the selected sentences were labeled and put into Santi_dataset.csv.

## Translation Difference
### Top 10 Words used
In order to explore the differences between different translation, we plot the top 10 words(Noun) for each book in the Triolology. This was able to give us some insights of writing patterns and the nature between the two language. wordvisulization.ipynb was used to explore top 10 words of each book,we then create Occurence.csv to store the data and the visulizations were plotted using the datafile.

### Sentiment Over Time 
It is also meaningful to see is there any difference of sentiments when the story is progressing between the two language. We trained an Naive Bayes model based on the Santi Dataset. Even though the result accuracy was around 50%, we seek to use the probability score as a strength indicator of the sentiment.

## Sentiment Analysis Model and Application
Utilizing the 'finiteautomata/bertweet-base-sentiment-analysis' model from HuggingFace Transformer, we had a 60.8% accuracy on predicting the sentiment in Santi_dataset. In an effort to preserve features in the pre-trained model, we utilized the trainer class provided by HuggingFace Transformer.We performed a 70-30 train test split, and the model increased accuracy to 70% after it was trained with the Santi dataset. 

### Applications
Netflix has annouced its project to film the ThreeBody Problem as a TV series, and the model we created offers a good tool to analyze feed back and expectations from the audience.

As an example, we used CommentScraper.ipynb to scrape the comment section of the teaser Netflix released on Youtube. We then apply our model to the comments to explore possible advice for Nefflix's production. We used[CommentScraper.ipynb](https://github.com/kli486/ThreeBodyProblem_Sentiment_Analysis/blob/main/Code/CommentScraper.ipynb) for collecting comments,and the model training and prediction was done using [Model_Training& Comment Prediction](https://github.com/kli486/ThreeBodyProblem_Sentiment_Analysis/blob/main/Code/Sentiment_Training.ipynb).
