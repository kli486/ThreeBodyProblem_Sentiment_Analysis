# ThreeBodyProblem_Sentiment_Analysis
Analysis of the Famous science fiction: Three Body Problem Triology with NLP Approach.

Inspired by the Lord Of the Ring Sentiment Anlysis Project, we decided to look at the Chinese version and the Translation of the Three Body Problem Triology.
This project dedicates to Two Main task: Explore the differnece between translation and develop a sentiment analysis model for the fiction.


## Data Collection and Processing
Based on the complex literature style of this fiction, we decided to apply Supervised Learning to obtain a sentiment analysis model. The key idea is to have experienced audience label selected text with 'Positive','Neutral',or 'Negative'.

Using Sentence_Clustering.ipynb,we output a mathced_sentence.csv for each trilogy of the science fiction; we then examine the data set and find that short sentences tend to be meaningless for our prediction,after cleaning out the irrelavent sentences, the selected sentences were labeled and put into Santi_dataset.csv.

## Translation Difference
### Top 10 Words used
In order to explore the differences between different translation, we plot the top 10 words(Noun) for each book in the Triolology. This was able to give us some insights of writing patterns and the nature between the two language. wordvisulization.ipynb was used to explore top 10 words of each book,we then create Occurence.csv to store the data and the visulizations were plotted using the datafile.

### Sentiment Over Time 
It is also meaningful to see is there any difference of sentiments when the story is progressing between the two language. We trained an Naive Bayes model based on the Santi

## Sentiment Analysis Model and Application
Utilizing the 'finiteautomata/bertweet-base-sentiment-analysis' model from HuggingFace Transformer, we had a 60.8% accuracy on predicting the sentiment in Santi_dataset. In an effort to preserve features in the pre-trained model, we utilized the trainer class provided by HuggingFace Transformer.We performed a 70-30 train test split, and the model increased accuracy to 70% after it was trained with the Santi dataset.

### Applications
