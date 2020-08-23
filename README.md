# Unsupervised-and-Supervised-Sentiment-Analysis-of-Yelp-Reviews.
We considered classifying text into sentiments categories of Positive, Negative and Neutral using reviews data set provided by Yelp. We explored Unsupervised and Supervised learning to classify text and impact of different machine learning algorithms on classification and observed variation with different text preprocessing techniques like stemming, lemmatizing, POS tagging and occurrence of words as a mere presence and frequency in document. We concluded results from three machine learning techniques i.e. Naïve Bayes, Logistic regression and SVM.


Humans are driven by opinions and it serve as a key influencer of our behavior. We as a human being rely upon the experiences, opinions and perception of other people to a great extent. This insight can be a root cause of importance of abundant data which is getting generated on a day to day basis on the wave of internet revolution across the world. People are freely expressing their opinions on various subjects in this global world and creating sense of convenience for other people to make decisions. 
This has become an Apple’s eye for managers across the industries for gathering useful information from this valuable data present across the internet platforms and use it for improving their products and services. Popular platforms that can be accessed for such data are twitter, review sites, Amazon marketplace and review websites among others. We chose Yelp reviews website to determine sentiments through yelp reviews. A review site helps people to garner information about a product or a place and helps them in their decision journey. Most of the data available is unstructured and contains lots of information. It becomes challenging to put all this information in business context. Modern technological advances have helped us to understand this kind of data and putting this into context. Potential area of application includes recommendation systems, tweet analysis, disaster management, Marketing and political campaigns.
We had star ratings available with review text. Star ratings are visible cues about sentiments of people, and we identified the same pattern in the data set using Unsupervised learning techniques available in python. We got the gist that in the data, increment in star rating was related to overall increase in sentiment scores (determined by available lexicon-based approaches in Python). Based on this intuition, we approached supervised techniques for sentiment classification and labelled the data set based on star ratings as positive, negative and neutral.
We have put all our efforts into understanding the problem of analyzing texts and sentiments not by mere words only but giving machine a sense of feeling of that sentiment. We have used techniques like Stemming, Lemmatizing, POS tagging, N-gram and tf-idf in different combination to assess their impact on algorithms deployed for classification. We have used several bag-of-words matrices to explore the input to models and check for its impact. We have concluded paper with a comparison table of different model deployed and their result for each case.


Unsupervised Learning
we did not have the convenience of a well-labeled training dataset in start. Hence, we performed unsupervised techniques for predicting the sentiment by using knowledgebases, ontologies, databases, and lexicons that have detailed information, specially curated and prepared just for sentiment analysis. A lexicon is a dictionary, vocabulary, or a book of words. In our case, lexicons are special dictionaries or vocabularies that have been created for analyzing sentiments. Most of these lexicons have a list of positive and negative polar words with some score associated with them, and using various techniques like the position of words, surrounding words, context, parts of speech, phrases, and so on, scores are assigned to the text documents for which we want to compute the sentiment. After aggregating these scores, we get the final sentiment.


We used three dictionaries for unsupervised analysis. 
Afinn:  The Afinn lexicon is perhaps most used and simple lexicon for sentiment analysis. Latest version of it contains 3300+ words for sentiment analysis with polarity score attached with each word.
TextBlob: Text Blob is another excellent open-source library for performing NLP tasks with ease, including sentiment analysis. It also a sentiment lexicon (in the form of an XML file) which it leverages to give both polarity and subjectivity scores. Typically, the scores have a normalized scale as compare to Afinn. The polarity score is a float within the range [-1.0, 1.0]. The subjectivity is a float within the range [0.0, 1.0] where 0.0 is very objective and 1.0 is very subjective. 
VADER: VADER has a lot of advantages over traditional methods of Sentiment Analysis, including: It works exceedingly well on social media type text, yet readily generalizes to multiple domains It doesn’t require any training data but is constructed from a generalizable, valence-based, human-curated gold standard sentiment lexicon It is fast enough to be used online with streaming data, and It does not severely suffer from a speed-performance tradeoff. It gives out four scores including positive, negative, neutral and compound score. We took compound score to classify.

Combined results of three dictionaries are as follow. We can see a general trend in each lexicon’s result that positive sentiment score is rising with star rating. That is a good start for labelling our data set with this insight.
 	Scoring Methodology
 	Afinn	TextBlob	Vader
Positive	>0	>0	>.05
Neutral	0	0	[-.05,.05]
Negative	<0	<0	<-.05

 	Mean Score
 	Afinn	TextBlob	vader
star rating	Sentiment Score	Sentiment score	Compound Score
1	1.04	0.001	0.124
2	5.25	0.153	0.493
3	8.12	0.236	0.658
4	9.57	0.301	0.735
5	8.69	0.349	0.731

Supervised Classifier
We divided supervised learning into multiple parts. We decided to explore different nuances of sentiment and text analytics and check their impact on model results. 

There are multiple ways of handling text and cleaning before feeding into the models. We decided to start from very simple and build model gradually by incorporating different combinations and transformations of data. 
We explored following in this part.
1.	Simple cleaning, i.e. removing punctuation, lowering capital and removing double spaces.
2.	Tokenize and convert in unigram model.
3.	Consider existence of a word in document and frequency of this word for second case.
4.	Consider Bigram and predict accuracy.
5.	Perform Stemming for words.
6.	Cleaning data more sophistically and converting words in Lemmatized form.
7.	Use tf-idf to make bag-of-words matrix with weightage of the words.


















