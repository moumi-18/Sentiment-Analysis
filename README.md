## Sentiment-Analysis
Mini example demonstrated using Sentiment Analysis 

#### Problem Statement - 
An international E-commerce company (Electronic goods) wants to start their operations in the country. To start with they intend to analyse the sentiments (Positive/Negative) of some of its following competitors:
* Company A
* Company B
* Company C

#### Way Ahead - 
We intend to use *Sentiment Analysis* technique for this problem statement. Following is the approach, to achieve the desired output.

Note: For this project I have not used Twitter API for tweet extraction as I was not getting desired no.of tweets. Instead I have used a library *snscrape*, which scrapped 3500 tweets for each competitor, without requiring any API or user authentication. As I have already extracted, I will be using the extracted tweets directly for further processing.

* Step 1: We are importing some additional libraries needed for this problem statement:
          a. snscrape- for scrapping tweets without using twitter login credentials
          b. nltk- for natural language processing which contains text processing libraries for tokenization,stemming,etc.
          c. re- this module is used to work with Regular Expressions, useful during text preprocessing   
          d. textblob- for processing textual data (for sentiment analysis)
           
* Step 2: For tweet extractions, we have used the following keywords for the competitors. We are extracting 3500 tweets of each competitor for better analysis.
          a. Company A(_compA):  
          b. Company B(_compB):       
          c. Company C(_compc):    
          
* Step 3: Post capturing the tweets, we will be processing them using text processing techniques:
          i. Removing Ascent Letters in text
          ii. Converting text to lowercase
          iii. Removing URL from text
          iv. Removing Punctuation from text
          v. Removing Number from text
          vi. Removing Stopwords from text
          vii. Replacing the similar code from text
          viii. Applying Stemming and Lemmatization in the text
          ix. Removing Extra Whitespace in the text
          
* Step 4: With the processed data of each competitor, we will be computing term document matrix using CountVectorizer() to find words and frequency and plotting WordCloud.

* Step 5: Doing sentiment analysis with each competitor's data.
