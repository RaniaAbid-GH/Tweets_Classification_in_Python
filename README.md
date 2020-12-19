# Tweets_Classification_in_Python
Tweets_Classification_using_NLTK-Python_and_K-Means_algorithm

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Binder link :
https://mybinder.org/v2/gh/RaniaAbid-GH/Tweets_Classification_in_Python/master?filepath=Classification_des_tweets_Example2.ipynb

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

* Involves grouping tweets into 3 categories : Computer Science, Telecommunication and Electronic then performing K-Means clustering on the grouped tweets to observe how they behave.

* There are several ways of approaching the problem of grouping the tweets, the adapted approach uses the technique of creating a set of words that can be confidently classified as belonging to a particular category for each of the 3 classes. 

* So the tweets are each compared with the 3 sets and assigned a similarity score. There are 2 main techniques I considered for computing similarity score :

 1. Cosine Similarity : Cosine similarity is a metric used to measure how similar the documents are irrespective of their size. 
 This would involve creating word vectors for the set of words and all the tweets then performing the cosine similarity. 
 TFIDF (bag of words model) Vectorizer would be ideal for this.
 
  2. Jaccard Similarity : Jaccard similarity is defined as size of intersection divided by size of union of two sets. 
  Jaccard similarity takes only unique set of words for each sentence/document while cosine similarity takes total length of the vectors. 
  Jaccard similarity is good for cases where duplication does not matter, cosine similarity is good for cases where duplication matters while analyzing text similarity.
  => In our case, context matters more than duplication thus making Jaccard similarity the most appropriate method to use.
  
  * After classifiying the tweets K-Means clustering comes in.
  
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Step 1 : Importing libraries.

Step 2 : Access to Twitter’s API using Tweepy / Verifying credentials :

Step 3 : Collecting Twitter data.

Step 4 : Merging collected datasets into one csv file / Concate collected datasets.

Step 5 : Cleaning data / Text preprocessing :
* Remove punctuations.
* Tokenizing.
* Remove stopwords.
* Stemming.
* Lemmatizing.

Step 6 : Saving extracted cleaned data.

Step 7 : Defining the sets of words :
* Computer science related words.
* Telecommunication related words.
* Electronic related words.

Step 8 : Preprocessing the sets :
* Tokenizing, Lemmatizing and removing stopwords.
* Deleting duplicates

Step 9 : Cosine Similarity :
* Vectorizing and Standadizing.

Step 10 : Jaccard Similarity :
* Calculating jaccard scores for each group.
* Defining a new dataframe containing names, and the jaccard scores for each group.
* Clustering that dataframe.

Step 11 : Data visualisation :
* Pie chart showing the total number of tweets in each category.
* A bar plot showing top tweets based on volume of tweets.

Step 12 : Distribution :
* Distribution per category (computer science-telecommunication-electronic).
* Teleinformatics (telecommunication & computer science)
* IoT distribution (computer science & electronic)

Step 13 : K-Means clustering :
* Data clustering.
* 2D clustering.
* Clustering with PCA.

