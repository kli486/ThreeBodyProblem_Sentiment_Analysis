# ThreeBodyProblem_Sentiment_Analysis
Analysis of the Famous science fiction: Three Body Problem Triology with NLP Approach.

Inspired by the Lord Of the Ring Sentiment Anlysis Project, we decided to look at the Chinese version and the Translation of the Three Body Problem Triology.
This project dedicates to Two Main task: Explore the differnece between translation and develop a sentiment analysis model for the fiction.

## Translation Difference
In order to explore the differences between different translation, we plot the top 10 words(Noun) for each book in the Triolology. This was able to give us some insights of writing patterns and the nature between the two language. wordvisulization.ipynb was used to explore top 10 words of each book,we then create Occurence.csv to store the data and the visulizations were plotted using the datafile.

## Sentiment Analysis Model and Application
Based on the complex literature style of this fiction, we decided to apply Supervised Learning to obtain a sentiment analysis model. The key idea is to have experienced audience label selected text with 'Positive','Neutral',or 'Negative'.

Using Sentence_Clustering.ipynb,we were able to output a mathced_sentence.csv; after cleaning out irrelavent clusters, the sentences were labeled and put into Santi_dataset.csv.

Utilizing the 'finiteautomata/bertweet-base-sentiment-analysis' model from HuggingFace Transformer, we had a 60.8% accuracy on predicting the sentiment in Santi_dataset. We performed a 70-30 train test split, and the model increased accuracy to 70% after it was trained with the Santi dataset.

