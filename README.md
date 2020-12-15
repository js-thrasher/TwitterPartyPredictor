# TwitterPartyPredictor
Classifies partisan lean from text data

# Intro
I decided to undergo this project after seeing how accurate a model could be at predicting tweets related to COVID (https://news.osu.edu/twitter-posts-reveal-polarization-in-congress-on-covid-19/). I wanted to see if there were more general trends in partisan lean that could be exposed through text data. Additionally, I wanted to use a real-world API instead of a toy data set, so I thought getting data from the twitter API would be a good learning experience.

# Selection of Data
I used a csv of politicians, their party, and their twitter ID to make requests via the twitter API. From there, I gathered the raw text data, created a DF from it, and cleaned the text data. For features, I vectorized this data into a tf-idf (term frequency-inverse documnet frequency) vector.

# Methods
After cleaning and vectorizing the data, I split it into 5 sets for 5-fold validation and trained a Gaussian Naive Bayes classifier. 

# Results
Overall, the max test score I got was about 0.76. I was able to test a few unseen pieces of data and they were mostly correct.

# Discussion
Ultimately, this could have also been better with more feature engineering. Things like Flesch-Kincaid reading level, % of punctuation, and geolocation/time of tweet could be valuable features. I also ran into some trouble trying to generate n-grams with such a large dataset. 
