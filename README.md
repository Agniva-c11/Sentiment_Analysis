Sentiment Analysis of Amazon Reviews Using VADER and RoBERTa

Overview:
This project aims to analyze the sentiment of Amazon product reviews using two different sentiment analysis approaches:

VADER (Valence Aware Dictionary and sEntiment Reasoner) – A lexicon-based sentiment analysis tool.
RoBERTa (Robustly Optimized BERT Approach) – A transformer-based deep learning model fine-tuned for sentiment classification.
By comparing the results of these two approaches, we gain insights into how different sentiment analysis techniques interpret textual data and how they correlate with actual user ratings (1-5 stars).

Dataset:

The dataset used in this project consists of Amazon customer reviews, including:
* Review Text – The actual review provided by the customer.
* Score (1-5 stars) – The rating assigned to the product by the reviewer.
* Other metadata (not used extensively but available for further analysis).
* To optimize processing time, only the first 500 reviews from the dataset are considered for analysis.

Project Structure
1. Data Preprocessing & Visualization
The dataset is loaded and basic cleaning is performed.
A bar chart is created to visualize the distribution of star ratings among the reviews.
These visualizations help us understand the frequency of different ratings and their impact on sentiment analysis.
2. Sentiment Analysis Using VADER
VADER (NLTK SentimentIntensityAnalyzer) is applied to each review.
It calculates four sentiment scores:
Positive Score – Proportion of positive words.
Neutral Score – Proportion of neutral words.
Negative Score – Proportion of negative words.
Compound Score – Overall sentiment polarity (ranges from -1 to +1).
Results are stored in a structured format and merged with the dataset.
3. Visualization of VADER Sentiment Scores
Bar charts are created to show how the compound sentiment score varies across different star ratings.
Individual sentiment components (positive, neutral, and negative) are also visualized to observe patterns.
4. Sentiment Analysis Using RoBERTa
The pre-trained RoBERTa model from Cardiff NLP is used for sentiment classification.
The text is tokenized and passed through the model to generate sentiment scores:
roberta_neg – Probability that the review is negative.
roberta_neu – Probability that the review is neutral.
roberta_pos – Probability that the review is positive.
The results are stored and later merged with the dataset.
5. Comparison of VADER and RoBERTa Results
A pairplot is generated to compare the sentiment scores from both models.
This helps analyze how the lexicon-based VADER approach differs from the transformer-based deep learning model.
6. Hugging Face Sentiment Pipeline
The Hugging Face pipeline("sentiment-analysis") is initialized for further analysis.
This additional method provides another deep learning-based approach for classifying sentiment.
Key Insights
VADER tends to align well with 1-star and 5-star ratings, as extreme sentiment is easier to detect lexically.
RoBERTa provides more nuanced predictions, especially for mixed reviews.
Neutrality is more dominant in RoBERTa compared to VADER, suggesting that deep learning-based models can handle ambiguous sentiment better.
The comparison of models allows us to choose an appropriate sentiment analysis method based on the complexity of the data.


Conclusion:

This project demonstrates the power of NLP (Natural Language Processing) in analyzing textual sentiment. By leveraging both traditional lexicon-based and deep learning-based approaches, we can extract meaningful insights from customer reviews. The comparison between VADER and RoBERTa showcases the advantages and limitations of each method, allowing us to make better choices for real-world applications.