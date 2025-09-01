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

## 🛠️ Technical Skills Demonstrated

<div align="center">

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557c?style=for-the-badge&logo=python&logoColor=white)
![NLTK](https://img.shields.io/badge/NLTK-85C1E9?style=for-the-badge&logo=python&logoColor=white)

![NLP](https://img.shields.io/badge/Natural_Language_Processing-FF6B6B?style=for-the-badge&logo=buffer&logoColor=white)
![Emotion Analysis](https://img.shields.io/badge/Emotion_Analysis-FECA57?style=for-the-badge&logo=atom&logoColor=white)
![Text Mining](https://img.shields.io/badge/Text_Mining-FF9FF3?style=for-the-badge&logo=elasticsearch&logoColor=white)

![API Integration](https://img.shields.io/badge/API_Integration-45B7D1?style=for-the-badge&logo=fastapi&logoColor=white)
![Web Scraping](https://img.shields.io/badge/Web_Scraping-54A0FF?style=for-the-badge&logo=scrapy&logoColor=white)
![Data Visualization](https://img.shields.io/badge/Data_Visualization-4ECDC4?style=for-the-badge&logo=plotly&logoColor=white)

![Statistical Analysis](https://img.shields.io/badge/Statistical_Analysis-96CEB4?style=for-the-badge&logo=scipy&logoColor=white)
![Research Methods](https://img.shields.io/badge/Research_Methodology-A8E6CF?style=for-the-badge&logo=academia&logoColor=white)

</div>

### Core Competencies

| Skill Area | Technologies & Methods | Application in Project |
|------------|----------------------|----------------------|
| **Data Collection** | NYT API, Web Scraping, Comment Extraction | Retrieved 50 articles and 6,018 comments with hierarchical processing |
| **Text Processing** | NLTK, Regex, Text Cleaning, Tokenization | Preprocessed and normalized large-scale textual data |
| **Emotion Analysis** | text2emotion, Multi-class Classification | Detected and quantified 5 core emotions across datasets |
| **Statistical Analysis** | Frequency Analysis, Comparative Statistics | Analyzed keyword patterns and emotional distributions |
| **Data Visualization** | Matplotlib, Statistical Plots | Created compelling visual narratives of findings |
| **Research Design** | Comparative Analysis, Hypothesis Testing | Systematic comparison of media vs. public sentiment |

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
