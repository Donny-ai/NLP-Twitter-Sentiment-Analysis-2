# **NLP-Twitter-Sentiment-Analysis**
In this project I performed sentiment analysis on a dataset of 1.6 million tweets from [Kaggle](https://www.kaggle.com/datasets/kazanova/sentiment140) (sampled down to 100,000). I preprocessed them and generated vector embeddings with BERT, then trained a logistic regression model to predict each tweet's sentiment.

With a logistic regression model, I achieved an accuracy score of 0.81:  
![logistic regression scores](logreg_eval.png)  
![histogram of sampled tweets](hist_y_test.png)
![histogram of predicted sentiment](hist_y_pred.png)
_______
## Predicting sentiment on a specific company
From the sampled dataset, I then grabbed only tweets containing "twitter" to see how the model scores them and to get a glimpse of public sentiment towards the company and platform. I was supposed to do this for an AI company, but I couldn't find such a company with over 100 tweets in my sampled dataset. But  twitter is sort of an AI company now...  
![logistic regression scores on twitter tweets](twitter_eval.png)
![histogram of twitter sentiment](hist_twit_y.png)
![histogram of predicted twitter sentiment](hist_twit_y_pred.png)  
**Looks like sentiment is mostly positive. Many twitter users wouldn't have predicted this!**

### Word Cloud
![Word cloud of 100k dataset](cloud_all.png)
### Word Cloud of tweets about Twitter
![Word cloud of tweets about Twitter](cloud_twit.png)

## Training Alternative Models
I trained a **Multinomial Naive Bayes** model and got a score of 0.70
I also trained a **Gradient Boosted Classifier** model and after trying different learning rates, number of estimators, and max depths, got a score of 0.786