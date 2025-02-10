# About
- Our project aims to find out what features predict the popularity of a tweet, with a focus on the relationship between the sentiment of tweets and popularity. We chose a Twitter dataset containing tweets with the hashtag #SlavaUkraini, which translates to ‘Glory to Ukraine!’. This dataset offers a unique opportunity to explore the potential link between sentiment and Twitter's recommendation algorithm, given the strong emotions surrounding the Ukraine War. It is important to note that these tweets are by average twitter users and not celebrities so the retweet counts are relatively low (max retweets cap at 1.7k)

# Contributors
- Group members worked together on all steps of the project. The focus of each member:
- Kyna Lim -  Sentiment Analysis
- Chen Yi Wen - Random Forest Classifier with GridSearchCV
- Kho Jia Cheng - Logistic Regression with BoW

# Problem Definition
- Are we able to find out what factors determine the popularity of the tweets and use them to predict a tweet's popularity?

# Features in the dataset for exploration
- User location, user profile, user followers, user friends, user favourites, user verification status, favourites (number of saves a tweet has), date posted, number of retweets

# Data Cleaning and Processing
- Dropped the rows with missing engagement data 
- Added popularity labels (very popular, popular, not popular)
- Conducted text preprocessing for sentiment analysis

# Exploratory Data Analysis (EDA)
- Spot potential hidden patterns in popular tweets: found common words used in popular tweets with WordCloud 
- Conducted time series analysis on tweet sentiments over time, scatterplots and joint boxplots and other EDA techniques to visualise relationship between features and popularity. 

# Machine Learning
- Predict tweet popularity using favourites and common_words_count
- Models Used: Logistic regression with BoW, Random Forest Classifier with GridSearchCV

# Problems encountered and solution
- Adjusted popularity thresholds based on retweet outliers instead of quartiles for better classification accuracy and more sensible results. Separating the tweets by quartile (1st, 2nd and 3rd) meant a tweet only required 3 retweets to be considered very popular compared to 12 retweets by using the outlier method.

# Conclusion
- From our EDA, we observed no clear relationship between a tweet’s sentiment and its popularity level.
- Instead, the most relevant features were favourites count, reflecting the consideration of user preferences in the Twitter’s algorithm, showing its more unbiased and user-centric approach to boosting engagement of tweets.

# Limitations and future possibilities
- Note that this finding, while indicative, may be skewed since our tweet dataset consisted of views from only one demographic (users in support of Ukraine) Without contrasting sentiments, it may be difficult to gauge the impact of sentiment on the popularity of content accurately. To address this issue, the dataset can be expanded to include a more diverse range of sentiments from different hashtags. This can help uncover nuances in how different sentiment levels correlate with popularity.

# Learning outcomes
- learning importance of formulating problem correctly (good scope and focus to find out meaningful answers)
- Logistic Regression and Random Forest with GridSearchCV
- conducting sentiment analysis on text
- new EDA methods such as WordCloud and time series
- learn new ways of defining accuracy of model: recall rate and f1-score

# References
- https://www.kaggle.com/datasets/gpreda/slava-ukraini-tweets
- https://pandas.pydata.org/pandas-docs/stable/user_guide/indexing.html#returning-a-view-versus-a-copy
- https://monkeylearn.com/blog/sentiment-analysis-of-twitter/#:~:text=Twitter%20sentiment%20analysis%20allows%20you,mentions%20before%20they%20they%20escalate
- [NLTK Book](https://www.nltk.org/book/)
- sklearn.feature_extraction.text.CountVectorizer — scikit-learn 1.4.2 documentation
- https://www.kaggle.com/code/ashokkumarpalivela/sentiment-analysis-with-machine-learning#Logistic-Regression-with-BoW
- https://www.datacamp.com/tutorial/random-forests-classifier-python

