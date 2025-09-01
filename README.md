# NYTimes Articles vs. Public Sentiment Analysis - Drones

Ever wonder if news articles on a specific topic aligns with how people really feel about actual topic ? 

This project analyzes how drones are framed in New York Times articles versus how the public perceives them through online discussions. Using [Natural Language Processing (NLP)](https://web.stanford.edu/~jurafsky/slp3/) techniques, specifically [emotion detection](https://ieeexplore.ieee.org/document/8456602) and keyword analysis, we compare media coverage with public sentiment to identify disparities in discourse.

---

<img width="953" height="430" alt="Screenshot 2025-09-01 at 9 09 09 AM" src="https://github.com/user-attachments/assets/840cf1cd-147f-4bbb-8368-4b701deb844d" />

---

## Research Questions

- How do news articles frame drone-related topics compared to public comments?
- What emotions dominate media coverage versus public discourse about drones?
- What are the most frequently discussed aspects of drones in both contexts?

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
   - Replace `YOUR_API_KEY` in the notebook with your actual key
  
5. Run your own analysis

```python
# Open the main notebook
jupyter notebook _NYTDronesAnalysisIly.ipynb

# Or run programmatically
from pynytimes import NYTAPI
import text2emotion as te
import pandas as pd

# Initialize API and fetch data
nyt = NYTAPI("YOUR_API_KEY", parse_dates=True)
articles = nyt.article_search(query="drones", results=50)

# Run emotion analysis
df_articles['emotions'] = df_articles['text'].apply(lambda x: te.get_emotion(x))
df_comments['emotions'] = df_comments['text'].apply(lambda x: te.get_emotion(x))

# Generate comparison
results = compare_sentiment(df_articles, df_comments)
print(f"Media vs Public Fear Level: {results['fear_ratio']:.1f}x difference")
```

**Expected Output:**
```
Total Comments: 6,018
Unique Articles with Comments: 22
Media vs Public Fear Level: 2.7x difference
Charts saved to: visualizations/
```

## Tech Stack

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

## Contact

For questions about my work or collaborations, please contact me at [icoulibaly1@babson.edu].
