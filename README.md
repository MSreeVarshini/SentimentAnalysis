# SentimentAnalysis

Sentiment Analysis, also known as opinion mining, is a subfield of Natural Language Processing (NLP) that automates the process of identifying and extracting feelings, attitudes, and subjective opinions from text data. It plays a significant role in understanding customer feedback, brand perception, and social media trends.

Websites are a treasure trove of customer reviews, offering valuable insights into how people perceive products, services, or brands. By applying sentiment analysis to this data, we can gain a deeper understanding of overall customer satisfaction, identification of strengths & weaknesses and tracking trends. The targeted approach to sentiment analysis, focusing on website reviews, provides a focused and relevant view of customer perception compared to analyzing generic text data.

The workflow of this project is as follows:

### 1. Setting Up the Environment:

* Install all necessary libraries and dependencies.
* Import required libraries
* Install additional libraries for NLP (transformers), making HTTP requests (requests), web scraping (BeautifulSoup4) and data manipulation.
* Import specific classes of Transformers library to tokenize text and load pre-trained model for sequence classification.


### 2. Initializing Sentiment Analysis Model:

* Initialize tokenizer and model required for sentiment analysis using BERT (Bidirectional Encoder Representations from Transformer).
* Tokenizer converts raw text into tokens.
* Initialize a tokenizer for BERT model specifically trained for Sentiment Analysis.
* Initialize a BERT model, which is pre-trained for sequence classification (sentiment classification).


### 3. Retrieving the Reviews from the Web:

Let's collect reviews using web scraping tehniques.
* Retrieve the HTML content of a web page using requests library.
* Here, I'm retrieving the contents from Yelp Page.
* Parse the html content using BeautifulSoup to extract relevant information from the HTML structure.
* Compiling the regex expression to match elements with the class 'comment'.
* Find all paragraph elements (<p>) with the class 'comment'.
* Extract all text content of page and store them in a list.


### 4. Analyzing Reviews:

* Load the colleted reviews to a dataframe and define a function to compute sentiment scores.
* Encode the data to tokens.
* Retrieve the raw output (logits) from the model.
* Logits represents the scores assigned to each class by the model.
* Calculate the sentiment score by finding the index of the maximum value in logits and add 1 (assuming the sentiment classes are 1-indexed). This determines the sentiment class with the highest probability.


### 5. Conclusion:

This project demonstrates the power of sentiment analysis on website reviews, providing businesses with valuable insights into customer sentiment. By analyzing real-world customer opinions, bussinesses can make data-driven decisions, stay ahead of trends, and foster positive relationships. This paves the way for further exploration of aspect-based sentiment analysis, comparative analysis, and real-time monitoring, ultimately leading to a deeper understanding of customers and improved decision-making.

I hope you liked this article on Sentiment Analysis using Customer Reviews :)
