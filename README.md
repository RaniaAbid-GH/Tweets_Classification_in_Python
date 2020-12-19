# Tweets_Classification_in_Python
Tweets_Classification_using_NLTK-Python

# Binder link :
https://mybinder.org/v2/gh/RaniaAbid-GH/Tweets_Classification_in_Python/master?filepath=Classification_des_tweets_Example2.ipynb

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
