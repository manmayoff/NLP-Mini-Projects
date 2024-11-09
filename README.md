# Natural Language Processing

This repository contains the code used during the studies of Natural Language Processing.

It is divided into following sub-topics.

## Vectorization and Embeddings

These are the methods that can be used to turn a text in natural human-readable language into numerical data. Some of the methods are used [here](./01.%20Vectorization%20and%20Embeddings)

- **Count Vectorizer**: A bag of words approach where counts of each word are recorded and used for further processing.
- **Stemming & Lemmatization**: Truncating or processing the word in order to get the root word
- **TF-IDF (Term Frequency - Inverse Document Frequency)**: A more sophisticated approach to get the words vectorized, that takes into account frequency of words and thus their value added in the current document

A practical application in NLP using the above concepts:
**Recommender System using TF-TDF**

## Markov Models
Markov models come under the category of probabilistic models. These models consist of an initial distribution of the tokens, and a transition matrix, and an assumption that the distribution of a token is independent of any token before the immediate previous token. Some applications of these models are [here](./02.%20Markov%20Models)

The following applications are explored here:
- **Text Classifier**: Using a generative model for each class of text and computing posteriors for classification
- **Text Generation**: Exploring a second-order Markov model, that can be used to generate text 
- **Article Spinner**: An application of second order-Markov model to change the text such that the meaning remains unchanged

## Spam Classifier
Applying Count Vectorizer and Naive Bayes algorithm to build a spam detector. Also explored analysis of model using confusion matrix and F1 score.

## Sentiment Classifier
Using tf-idf vectorizer and logistic regression to build a multi-class classifier. Explored the interpretation of the model weights to find most positive and most negative words in tweets for an airline company.

## Text Summarization
- Used a tf-idf vectorizer over the sentences of the text, and used their mean values for each sentence as a score to find sentences in decreasing order of importance. Then, a threshlod or count can be used to get sentences with best scores.
- **TextRank**: Implemented TextRank Summarizer from scratch. In this approach, the scores of each sentence is computed in a different way. We consider a Markov model, with states as the sentences, and transitions are between sentences with cosine similarities. Then the limiting distribution of the states is found, by computing eigenvector of the similarity matrix, which serve as the desired scores.