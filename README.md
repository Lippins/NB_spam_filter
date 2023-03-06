# Building a Spam Filter with Naive Bayes
## Overview
This project aims to develop a spam filter for SMS messages using machine learning algorithms to classify messages as either spam or non-spam. The goal is to achieve an accuracy greater than 80% using the Multinomial Naive Bayes algorithm along with a dataset of 5,572 pre-labelled SMS messages.

## The Dataset
The [dataset](https://dq-content.s3.amazonaws.com/433/SMSSpamCollection), compiled by Tiago A. Almeida and José María Gómez Hidalgo, is available for download from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/sms+spam+collection). The creators' page provides more information on how the data was collected and includes useful papers on the dataset.

> _It's worth noting that the dataset may contain offensive content due to the nature of spam messages._

## Workflow
We followed a step-by-step process to build a spam filter for SMS messages. First, we created a training dataset and a test dataset to train the algorithm and evaluate its accuracy, respectively. Then, we removed irrelevant or duplicate data to clean the dataset.

After cleaning the dataset, we calculated the constants required for the multinomial Naive Bayes algorithm, such as the total number of spam and non-spam messages, the total number of unique words, and the total number of words in spam and non-spam messages.

Next, we computed the parameters for each word in the dataset, including the number of times a word appears in spam and non-spam messages and the probability of a word being spam or non-spam. Additionally, we identified the most common words in spam messages to gain insight into the characteristics of spam messages.

Once we trained the algorithm, we could classify a new message by calculating the probability of it being spam or non-spam using the parameters computed earlier. We then measured the accuracy of the spam filter by testing it on the test dataset and comparing the predicted classifications to the actual classifications.

## Results
While we acknowledge the limitations of our spam filter in terms of language and word processing, it has actually shown great potential. Our filter, based on the multinomial Naive Bayes algorithm, and a labeled dataset of 5,572 SMS achieved an impressive accuracy of 97.16%.

In addition to this success, we gained valuable insights from this project. Our analysis of incorrectly classified messages provided valuable information for further improvements. For instance, we discovered that our algorithm struggles to correctly classify messages that are very short, and contain typical spam-like words or neutral words previously detected in spam messages. Meanwhile, it erroneusly favours messages that tend to be longer and have a higher percentage of neutral words or words absent from the vocabulary. Additionally, we found that making our algorithm sensitive to letter case actually decreased our accuracy.

Through our analysis of the most popular words in spam messages, we observed common patterns such as encouraging people to take action, promising alluring offers, urging them, and promoting sexual content to entice people. 

## Next steps
By continuing to improve our filter and adding more data to the trained model, we can work towards an optimal ratio of 50% spam and 50% ham for even greater accuracy. The insights gained from this project will serve as a stepping stone towards the development of an improved and more sophisticated spam filter that can more effectively handle the nuances of language and word processing.