# Customer Sentiment Analysis on Starlink Reviews from Jumia Kenya

## Project Overview

This project performs customer sentiment analysis on reviews for the Starlink product, sourced from Jumia Kenya. [Click here](https://www.jumia.co.ke/catalog/productratingsreviews/sku/BR269EA1PRKULNAFAMZ/) to get the link. Using a web scraping approach, it extracts reviews from multiple pages and processes them to determine sentiment polarity, providing insights into customer opinions. This analysis demonstrates proficiency in data acquisition, natural language processing (NLP), and visualization.

## Features
- Web Scraping: Collects customer reviews for a specified product from Jumia.
- Sentiment Analysis: Implements sentiment analysis using multiple NLP techniques to assess customer sentiment.
- Data Visualization: Visualizes sentiment distributions to communicate insights effectively.
- CSV Export: Saves raw data and processed sentiments to a CSV file for further analysis.

## Installation
1. Clone the repository:
   ```https://github.com/The-alpha-male/Starlink_customer_sentiment_analysis.git```

2. Install dependencies: This project uses Python libraries such as `requests`, `BeautifulSoup`, `nltk`, `pandas`, and `matplotlib.`

   ```!pip install -r requirements.txt```

3. Download NLTK data files: The project relies on NLTK's stopwords and sentiment lexicon, which need to be downloaded:

   ```
    nltk.download('stopwords')
    nltk.download('vader_lexicon')
    nltk.download('punkt')
    ```
## Usage
1. Run the Notebook: Open and execute the Jupyter Notebook Sentiment_Analysis.ipynb to perform the entire analysis.
2. Web Scraping: Modify the web scraping code to target specific products or pages.
3. Analyze Sentiments: The notebook walks through data processing, cleaning, and sentiment analysis steps.

## Project Structure


## Data Pipeline

### Web Scraping
The project uses the requests library to fetch HTML content from Jumia’s product pages. `BeautifulSoup` extracts relevant review data, storing each review in a structured list. Data is fetched from multiple pages, as shown in the loop that iterates over paginated URLs.

### Data Cleaning
Text preprocessing is essential to improve analysis accuracy. Steps include:

- Tokenization: Breaking down text into individual words.
- Stopword Removal: Filtering out common, uninformative words using nltk.corpus.stopwords.
- Text Normalization: Converting text to lowercase, removing special characters, and handling punctuation.

### Sentiment Analysis
This analysis employs two methods:

- VADER Sentiment Analysis (from `nltk.sentiment`): Classifies reviews as positive, negative, or neutral based on polarity scores.
- TextBlob Analysis: Cross-validates sentiment polarity and subjectivity.

The output includes sentiment scores and labels saved to a CSV file for visualization.

#### Examples
Sample Review Data:

- Positive Review: "Amazing internet speed, very reliable!"
- Negative Review: "Terrible service, frequently disconnects."
  
Sentiment Output:

| Review                  | Sentiment | Score |
|-------------------------|-----------|-------|
| Amazing internet speed! | Positive  | 0.89  |
| Terrible service        | Negative  | -0.75 |


## Results
The project outputs sentiment distributions in a graphical format, providing insights such as:

- Percentage of Positive vs. Negative Reviews: Useful for gauging overall customer satisfaction.
-  Word cloud of sentiments made: Useful for checking the dominant sentiments made by customers reviewing the product.
  
