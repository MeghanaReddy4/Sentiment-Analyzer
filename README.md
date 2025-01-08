# Sentiment-Analyzer



This project allows you to analyze the sentiment of any given text using the `TextBlob` library in Python. It classifies the sentiment of the input text into **Positive**, **Negative**, or **Neutral** categories based on the polarity score.

## Features

- **Text Input**: Accepts user input for sentiment analysis.
- **Sentiment Classification**: Classifies text sentiment as Positive, Negative, or Neutral based on the sentiment polarity score.
- **Polarity Score**: Outputs the polarity score that helps determine the sentiment strength.
  
## Requirements

- Python 3.x
- `TextBlob` library

### Install Required Libraries

You can install the required library using the following command:

```bash
!pip install textblob
```

## Usage

### 1. Clone the Repository (Optional)
If you want to clone the repository, run the following command:

```bash
git clone https://github.com/your-username/sentiment-analyzer.git
```

### 2. Run the Script

To use the Sentiment Analyzer, run the following Python script:

```python
# Import the necessary library
from textblob import TextBlob

# Prompt the user to input text for sentiment analysis
text = input("Enter the text for Sentiment Analysis:")

# Create a TextBlob object using the input text
blob = TextBlob(text)

# Perform sentiment analysis on the text
sentiment = blob.sentiment  # This returns a namedtuple with 'polarity' and 'subjectivity'

# Classify sentiment based on the polarity score:
# - Positive sentiment if polarity > 0
# - Negative sentiment if polarity < 0
# - Neutral sentiment if polarity == 0
print(f"sentiment: {'Positive' if sentiment.polarity > 0 else 'Negative' if sentiment.polarity < 0 else 'Neutral'}")

# Display the polarity score:
# - A score closer to 1 means more positive sentiment
# - A score closer to -1 means more negative sentiment
# - A score of 0 means neutral sentiment
print(f"Polarity: {sentiment.polarity}")
```

### 3. Example Usage

#### Example 1: Positive Sentiment

```bash
Enter the text for Sentiment Analysis: I love Python programming, it's so fun and easy to learn!
sentiment: Positive
Polarity: 0.85
```

#### Example 2: Negative Sentiment

```bash
Enter the text for Sentiment Analysis: I really dislike the new update, it's full of bugs!
sentiment: Negative
Polarity: -0.7
```

#### Example 3: Neutral Sentiment

```bash
Enter the text for Sentiment Analysis: The weather is cloudy today.
sentiment: Neutral
Polarity: 0.0
```

### 4. How It Works

- The script takes user input for a piece of text.
- It then analyzes the text's **sentiment** using **TextBlob**'s built-in sentiment analysis.
- The **polarity** score is used to classify the sentiment:
  - A **positive polarity** score (greater than 0) indicates a positive sentiment.
  - A **negative polarity** score (less than 0) indicates a negative sentiment.
  - A **neutral polarity** score (exactly 0) indicates neutral sentiment.

### 5. Polarity Scores

The **polarity** score ranges from **-1 to 1**:
- **1** indicates a very positive sentiment.
- **0** indicates a neutral sentiment.
- **-1** indicates a very negative sentiment.

## License

This project is licensed under the MIT License.

