# ThreeBodyProblem_Sentiment_Analysis
Analysis of the Famous Science Fiction Trilogy: "The Three-Body Problem" with an NLP Approach.

Inspired by the "Lord Of the Rings" Sentiment Analysis Project, we decided to examine both the Chinese version and the English translation of "The Three-Body Problem" Trilogy. This project is dedicated to two main tasks: Exploring the differences between translations and developing a sentiment analysis model for the fiction.


## Data Collection and Processing
Given the complex literary style of this fiction, we opted for Supervised Learning to develop a sentiment analysis model. The core idea is to have experienced readers label selected texts as 'Positive', 'Neutral', or 'Negative'.


Using [Sentence_Clustering](https://github.com/kli486/ThreeBodyProblem_Sentiment_Analysis/blob/main/Code/SentenceClustering.ipynb), we output mathced_sentence for each book of the trilogy. We examined the data set and found that short sentences tend to be meaningless for our prediction. After cleaning out the irrelavent sentences, the selected sentences were labeled and compiled into the [Santi_dataset](https://github.com/kli486/ThreeBodyProblem_Sentiment_Analysis/blob/main/DataSet/Santi_dataset.csv).

### Translation Difference: Top 10 Words used

In order to explore the differences between different translation, we plotted the top 10 words(Noun) for each book in the Triolology. This was able to give us some insights of writing patterns and the nature between the two language. [Wordvisulization](https://github.com/kli486/ThreeBodyProblem_Sentiment_Analysis/blob/main/Code/Wordvisulization.ipynb) was used to examine top 10 words of each book. We then created a [dataset](https://github.com/kli486/ThreeBodyProblem_Sentiment_Analysis/blob/main/DataSet/Occurence.csv) to store the data, and the visulizations were plotted [here](https://github.com/kli486/ThreeBodyProblem_Sentiment_Analysis/blob/main/Top10Words_Visulization.md).

### Translation Difference:  Sentiment Over Time 
The investigation also encompasses an analysis of the variation in sentiment as the narrative progresses across the two languages. For this purpose, a Naive Bayes model was trained utilizing the Santi Dataset. Although the accuracy of the model hovered around 50%, we still can get useful insight from the probability score. This approach aims to provide a basic understanding of sentiment dynamics within the fiction, reflecting potential linguistic and cultural variations in the story's portrayal. We used [SentimentOverTime](https://github.com/kli486/ThreeBodyProblem_Sentiment_Analysis/blob/main/Code/SentimentOvertime.ipynb) for this task and the analysis could be accessed [here](https://github.com/kli486/ThreeBodyProblem_Sentiment_Analysis/blob/main/SentimentAnalysis_Visulization.md).

## Sentiment Analysis Model and Application
Utilizing the 'finiteautomata/bertweet-base-sentiment-analysis' model from HuggingFace Transformers, we achieved a 60.8% accuracy in predicting sentiment in the Santi_dataset. To preserve features in the pre-trained model, we used the trainer class provided by HuggingFace Transformers. We performed a 70-30 train-test split, and the model's accuracy increased to 70% after being trained with the Santi dataset in [Model_Training& Comment Prediction](https://github.com/kli486/ThreeBodyProblem_Sentiment_Analysis/blob/main/Code/Sentiment_Training.ipynb).


### Applications
Netflix has announced its project to adapt "The Three-Body Problem" into a TV series, and the model we created offers a valuable tool for analyzing feedback and expectations from the audience.

As an example, we used [CommentScraper.ipynb](https://github.com/kli486/ThreeBodyProblem_Sentiment_Analysis/blob/main/Code/CommentScraper.ipynb) to scrape the comment section of Netflix's teaser on YouTube. We then applied our model to the comments to glean possible advice for Netflix's production.

We then examined the Postive_Comments and Negative Comments in [Comment Analysis](https://github.com/kli486/ThreeBodyProblem_Sentiment_Analysis/blob/main/Code/Comment_Analysis.ipynb). The results from the analysis could be viewed [here](https://github.com/kli486/ThreeBodyProblem_Sentiment_Analysis/blob/main/YoutubeCommentAnalysis.md).
