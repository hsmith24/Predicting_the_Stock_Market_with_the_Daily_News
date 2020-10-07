# Predicting_the_Stock_Market_with_the_Daily_News
This repository contains the files related to a project with the goal of using a corpus of headlines from the daily news to predict fluctuations in the Dow Jones Industrial Average. The idea of the project was taken from [kaggle](https://www.kaggle.com/aaron7sun/stocknews).

---
## Folders
### data
This folder contains the various datasets used in the project. The external folder contains the data taken from kaggle link above:

- dow_jones_data.csv: This file contains  information on the Dow Jones Industrial Average taken from Yahoo Finance.

- labelled_headlines_data.csv: This file is the main dataset. The instances are each day from August 2008 until July 2016. The features are daily news headlines from [Reddit World News Channel](https://www.reddit.com/r/worldnews/?hl=). Headlines are ranked by user votes, and the dataset contains the highest ranked 25 headlines on each day.


The processed folder contains intermediate datasets I created in the course of the project:

- document_features_matrix.csv: This file contains the document to features matrix derived from the text in the headlines. Along with the features engineered from sentiment analysis below this was the data used to train the final model.

- sentiment_data.csv: This file is similar to labelled_headlines_data.csv with additional features engineered using sentiment analysis. These features were engineered using a combination of algorithms and rate each days headlines based on a objectivity/subjectivity dimension and a positivity/negativity dimension. The algorithm was taken from [here](https://github.com/ShreyamsJain/Stock-Price-Prediction-Model/blob/master/Sentence_Polarity/sentiment.py).

- sentiment_topic_data.csv: This file contains different topics modelled using NMF and shows how they differ in the sentiment analysis used above. This data was purely for the purpose of creating a vizualization in Tableau.


### notebooks
This folder contains the code for the project:

- modelling.ipynb: This notebook contains all of the modelling.

- topics_sentiment_anomalies: This notebook contains various odds and ends. It contains all of the topic modelling and creates the topic to sentiment data for use in the vizualization. It also contains some experimentation with anomaly detection although this did not end up being directly useful in the project.


### slides
This folder contains the slide deck I used when presenting on this project.


### vizualization
This folder contains a Tableau vizualization displaying the sentiment analysis of the different topics.
