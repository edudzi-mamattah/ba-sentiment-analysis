# Sentiment Analysis of British Airways' Customer Reviews on Skytrax.com

*Project Duration: January 2023*
## About this project

In this project, I conducted sentiment analysis of <a href = "https://www.britishairways.com/travel/home/public/en_gb/"> British Airways'</a>  customer reviews that were uploaded by customers of the airline to <a href = "https://www.airlinequality.com/airline-reviews/british-airways/page/1/">skytrax.com</a>.

The reviews captured in this project are reviews that were posted between 6th May 2014 and 9th January 2023.


## Data Processing & Preprocessing

I used the BeautifulSoup package in Python to extract the reviews from the Skytrax website and put each review into a cell within a Pandas dataframe.

After all the data was collected, I saved that dataframe as a .csv file to be used in a separate notebook (and to ensure that I had a consistent checkpoint of my data).


Cleaning of the dataset commenced with removal of unwanted characters from the data frame. Emojis, stopwords, and certain words that were persistent throughout the dataset - such as "trip verified" and the name of the airline for instance - were removed. 
Those pieces of text were cleaned from the dataset as they were not required to accomplish the goal of the project.

From that point, tokenization and then lemmatization were conducted for the dataset.

---

## Exploratory Data Analysis

The main EDA I conducted involved using word clouds to inspect the most common words used in the reviews. This was just to give a rough idea of what the data consisted of.

Word Cloud

![WC1-image](https://github.com/edudzi-mamattah/ba-sentiment-analysis/blob/master/data/BA_WordCloud.png)

## Sentiment Analysis

The VADER and TextBlob packages were both utilised to conduct analyses of sentiments found within the reviews. They both work slightly differently but their results were not too dissimilar.

Vader Analysis Results ![Vader-image](https://github.com/edudzi-mamattah/ba-sentiment-analysis/blob/master/data/VaderPieAnalysis.png)

TextBlob Analysis Results ![Textblob-image](https://github.com/edudzi-mamattah/ba-sentiment-analysis/blob/master/data/TextBlobPieAnalysis.png)

I also analysed the most common emotions expressed within the sentiments and the most common topics discussed within the reviews and generated their results in a word cloud to allow for easy data digestion.

Word Cloud of Most Common Emotions Expressed Within Dataset ![emotions-image](https://github.com/edudzi-mamattah/ba-sentiment-analysis/blob/master/data/Emotions_WordCloud.png)

Word Cloud of Most Common Topics Discussed Within Dataset ![topics-image](https://github.com/edudzi-mamattah/ba-sentiment-analysis/blob/master/data/Topics_WordCloud.png)





## Appendix

As an appendix to the project (although this comes after EDA within the notebook), I used BERTopic to conduct “smarter” topic modelling on the data, to gain more insight from the data. 
This involved clustering the most similar groups of topics using cosine similarities, plotting the cluster hierarchies, investigating the intertopic distance map, and investigating the TF-IDF term score decline per topic graph.

A snapshot of one of the hierarchical clustering graphs generated from that can be found below.

Hierarchical BERTopic Cluster ![HC-image](https://github.com/edudzi-mamattah/ba-sentiment-analysis/blob/master/data/hClust.png)




