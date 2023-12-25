# ThreeBodyProblem_Sentiment_Analysis
Analysis of the Famous science fiction: Three Body Problem Triology with NLP Approach.

Inspired by the Lord Of the Ring Sentiment Anlysis Project, we decided to look at the Chinese version and the Translation of the Three Body Problem Triology.
This project dedicates to Two Main task: Explore the differnece between translation and develop a sentiment analysis model for the fiction.


## Data Collection and Processing
Based on the complex literature style of this fiction, we decided to apply Supervised Learning to obtain a sentiment analysis model. The key idea is to have experienced audience label selected text with 'Positive','Neutral',or 'Negative'.



Using [Sentence_Clustering](https://github.com/kli486/ThreeBodyProblem_Sentiment_Analysis/blob/main/Code/SentenceClustering.ipynb), we output mathced_sentence for each of the trilogy; we examined the data set and found that short sentences tend to be meaningless for our prediction,after cleaning out the irrelavent sentences, the selected sentences were labeled and put into [Santi_dataset](https://github.com/kli486/ThreeBodyProblem_Sentiment_Analysis/blob/main/DataSet/Santi_dataset.csv).

## Translation Difference
### Top 10 Words used
In order to explore the differences between different translation, we plot the top 10 words(Noun) for each book in the Triolology. This was able to give us some insights of writing patterns and the nature between the two language. [Wordvisulization](https://github.com/kli486/ThreeBodyProblem_Sentiment_Analysis/blob/main/Code/Wordvisulization.ipynb) was used to explore top 10 words of each book,we then create a [dataset](https://github.com/kli486/ThreeBodyProblem_Sentiment_Analysis/blob/main/DataSet/Occurence.csv) to store the data and the visulizations were plotted [here](https://github.com/kli486/ThreeBodyProblem_Sentiment_Analysis/blob/main/Top10Words_Visulization.md)

### Sentiment Over Time 
The investigation also encompasses an analysis of the variation in sentiment as the narrative progresses across the two languages. For this purpose, a Naive Bayes model was trained utilizing the Santi Dataset. Although the accuracy of the model hovered around 50%, we still can get useful insight from the probability score. This approach aims to provide a basic understanding of sentiment dynamics within the fiction, reflecting potential linguistic and cultural variations in the story's portrayal. We used [SentimentOverTime](https://github.com/kli486/ThreeBodyProblem_Sentiment_Analysis/blob/main/Code/SentimentOvertime.ipynb) for this task and the analysis could be accessed [here](https://github.com/kli486/ThreeBodyProblem_Sentiment_Analysis/blob/main/SentimentAnalysis_Visulization.md).

## Sentiment Analysis Model and Application
Utilizing the 'finiteautomata/bertweet-base-sentiment-analysis' model from HuggingFace Transformer, we had a 60.8% accuracy on predicting the sentiment in Santi_dataset. In an effort to preserve features in the pre-trained model, we utilized the trainer class provided by HuggingFace Transformer.We performed a 70-30 train test split, and the model increased accuracy to 70% after it was trained with the Santi dataset in [Model_Training& Comment Prediction](https://github.com/kli486/ThreeBodyProblem_Sentiment_Analysis/blob/main/Code/Sentiment_Training.ipynb).


### Applications
Netflix has annouced its project to film the ThreeBody Problem as a TV series, and the model we created offers a good tool to analyze feed back and expectations from the audience.

As an example, we used CommentScraper.ipynb to scrape the comment section of the teaser Netflix released on Youtube. We then apply our model to the comments to explore possible advice for Nefflix's production. We used [CommentScraper.ipynb](https://github.com/kli486/ThreeBodyProblem_Sentiment_Analysis/blob/main/Code/CommentScraper.ipynb) for collecting comments.

We then examine the Postive_Comments and Negative Comments in[Comment Analysis](https://github.com/kli486/ThreeBodyProblem_Sentiment_Analysis/blob/main/Code/Comment_Analysis.ipynb). The results from the analysis could be seen [here](https://github.com/kli486/ThreeBodyProblem_Sentiment_Analysis/blob/main/YoutubeCommentAnalysis.md)
