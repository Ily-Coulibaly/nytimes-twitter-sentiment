# NYTimes Articles vs. Public Comments Sentiment Analysis

This NLP project analyzes the language and emotions used in New York Times coverage on the topic of drones versus reader reactions in comment sections, using Natural Language Processing (NLP) and emotion detection techniques.

## What this project does:

This project explores the difference between media coverage and public sentiment regarding drones by:

- Fetching and analyzing 50 drone-related articles from The New York Times
- Collecting 6,018 public comments from 22 articles with active discussions
- Performing sentiment analysis and emotion detection on both datasets
- Comparing how media frames drone issues versus public reactions

<img width="960" height="591" alt="emotion-analysis-comparison" src="https://github.com/user-attachments/assets/b3aa86e5-bafc-4ea8-a7ea-1384d8856127" /> 

---

## Key Features

- Data Collection: Automated NYT article and comment retrieval using the NYT API
- Text Processing: Advanced text cleaning and preprocessing
- Keyword Analysis: Frequency analysis of the most common terms in articles
- Emotion Detection: Multi-emotion analysis using text2emotion library
- Comparative Analysis: Side-by-side comparison of media vs. public sentiment
- Data Visualization: Charts and graphs showing sentiment distributions

---

## Setup 

1. Clone the repository:
```bash
git clone https://github.com/yourusername/drone-sentiment-analysis.git
cd drone-sentiment-analysis
```

2. Install required dependencies:
```bash
pip install pynytimes
pip install nytimes-scraper
pip install text2emotion
pip install pandas matplotlib
pip install nltk
pip install emoji==1.6.3
```

3. Download NLTK data:
```python
import nltk
nltk.download('stopwords')
nltk.download('punkt')
nltk.download('wordnet')
```

4. Get a New York Times API key:
   - Visit [NYT Developer Portal](https://developer.nytimes.com/)
   - Create an account and generate an API key
   - Replace the API key in the code

## Data Sources

#### Articles Dataset

- Source: New York Times Article Search API
- Query: "drones and drone sightings"
- Count: 50 articles
- Time Range: 2012-2025
- Fields: Headlines, abstracts, URLs, publication dates, sections

#### Comments Dataset

- Source: NYT Comments API via nytimes-scraper
- Total Comments: 6,018 comments
- Articles with Comments: 22 unique articles
- Comment Types: 3,398 top-level comments, 2,620 replies
- Fields: Comment body, timestamps, user info, article metadata

## Technologies Used

- **Python 3.12+**
- **APIs**: NYTimes Article Search API, NYTimes Comments API
- **Libraries**: 
  - `pynytimes` - NYT API wrapper
  - `nytimes-scraper` - Comment extraction
  - `text2emotion` - Emotion detection
  - `pandas` - Data manipulation
  - `matplotlib` - Data visualization
  - `nltk` - Natural language processing
  - `re` - Text processing

## Links

- [New York Times Developer Portal](https://developer.nytimes.com/)
- [text2emotion Documentation](https://pypi.org/project/text2emotion/)
- [NLTK Documentation](https://www.nltk.org/)

