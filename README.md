# NYTimes vs. Twitter Sentiment Analysis using VADER

This project explores how professional journalism compares with public opinion by analyzing sentiment in **New York Times articles** and **Twitter comments** on the same topic.  
The goal is to see whether the tone used by journalists aligns with, or diverges from, the reactions of the general public.

For this study, the topic of **drones** was chosen. In early 2025, drones were frequently in the news for their growing roles in military operations, commercial applications like delivery, and public safety programs. Their prominence made them an ideal case study for testing how news framing contrasts with public response.  

---

## What the project does
- Collects articles and comments from the **New York Times API**.  
- Gathers Twitter discussions on drones for the same timeframe.  
- Applies the **VADER sentiment analyzer** to classify text as positive, negative, or neutral.  
- Compares sentiment across both sources to reveal differences in framing and perception.  
- Provides visualizations of sentiment distributions for clear comparison.  

---

## Why this matters
Media not only reports on events but also shapes how we perceive them. By looking at drones, a subject tied to both innovation and controversy, this project highlights the gap that can exist between **editorial tone** and **audience sentiment**.  

---

Perfect — I went through your notebook and pulled out the real setup steps someone needs to replicate your work. Instead of vague “install requirements,” your README can now walk through the exact flow. Here’s a rewritten **Setup** section for your README, based on your notebook:

````markdown
## Setup

To reproduce the analysis, follow these steps:

1. **Clone this repository**
   ```bash
   git clone https://github.com/your-username/nytimes-twitter-sentiment.git
   cd nytimes-twitter-sentiment
````

2. **Install dependencies**
   The notebook uses Python with Jupyter. Install the required libraries:

   ```bash
   pip install pandas matplotlib nltk text2emotion
   pip install pynytimes nytimes-scraper
   ```

3. **Download NLTK resources**
   Inside Python:

   ```python
   import nltk
   nltk.download('vader_lexicon')
   nltk.download('stopwords')
   ```

4. **Get a New York Times API key**

   * Sign up at [NYTimes Developer](https://developer.nytimes.com/)
   * Create an app and copy your API key.
   * Replace the placeholder API key in the notebook with your own:

     ```python
     nyt = NYTAPI("YOUR_API_KEY_HERE", parse_dates=True)
     ```

5. **Run the notebook**
   Open Jupyter and start the analysis:

   ```bash
   jupyter notebook _NYTDronesAnalysisIly.ipynb
   ```

6. **Outputs generated**

   * A CSV of drone-related NYTimes articles.
   * A CSV of reader comments linked to those articles.
   * Sentiment distributions and keyword frequency plots.

---

### Notes

* The notebook includes custom functions to fetch articles, pull reader comments, and save them with metadata.
* By default, it looks for the topic **“drones”**, but you can change the query to analyze other keywords.
* Results include both **article framing** (headlines + abstracts) and **public sentiment** (reader comments + tweets).

```


