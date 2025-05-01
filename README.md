# Twitter Toxicity Analysis: Tracking Ideological Drift Through NLP

This repository contains code and data for analyzing toxicity in tweets from public figures with a focus on tracking ideological drift through natural language processing techniques. This project is the implementation for the thesis "Signals of Shift: A Natural Language Processing-Driven Quantification of the Ideological Drift in Elon Musk's Online Presence."

## Overview

This project analyzes over 36,000 tweets from Elon Musk (2010-2025), with additional data from Barack Obama and Donald Trump as comparative benchmarks. Using Perspective API and Detoxify AI for toxicity measurement and machine learning for topic categorization, we track changes in rhetoric over time to detect signs of ideological drift.

### Key Findings

- Musk's toxicity levels show a clear upward trend beginning around late 2022, occasionally exceeding levels that previously led to platform suspensions.
- His language has evolved from technical discussions (Tesla, SpaceX) toward politically charged communication (government, media, culture wars).
- Words associated with toxicity have shifted from expressions of frustration to targeted derogatory terms and moral condemnation.

## Repository Structure

- `Analysis.ipynb`: Main Jupyter notebook containing the full analysis pipeline
- `prepare_github_repo.sh`: Bash script to prepare this repository for GitHub

### Data Files

- Original tweet data:
  - `trump_tweets.csv`: Donald Trump's tweets
  - `Tweets-BarackObama.csv`: Barack Obama's tweets
  - `elon musk full tweet history/all_musk_posts_2010-06-04_2025-03-21.csv`: Elon Musk's tweets

- Cleaned data:
  - `musk_clean_v2.csv`: Cleaned Musk tweets
  - `trump_clean_v3.csv`: Cleaned Trump tweets  
  - `obama_clean_v2.csv`: Cleaned Obama tweets

- Toxicity scores from Perspective API:
  - `musk_scored_progress.csv`: Perspective API scores for Musk's tweets
  - `trump_scored_progress.csv`: Perspective API scores for Trump's tweets
  - `obama_scored_progress2.csv`: Perspective API scores for Obama's tweets

- Toxicity scores from Detoxify:
  - `musk_unbiased_results.csv`: Detoxify scores for Musk's tweets
  - `trump_unbiased_results2.csv`: Detoxify scores for Trump's tweets
  - `obama_unbiased_results.csv`: Detoxify scores for Obama's tweets

- Topic classification:
  - `musk_categorized_llm.csv`: Topic classification of Musk's tweets

## Setup and Installation

### Prerequisites

- Python 3.8+
- Jupyter Notebook/Lab

### Dependencies

Install the required packages using:

```bash
pip install -r requirements.txt
```

The main dependencies include:
- pandas
- numpy
- matplotlib
- seaborn
- google-api-python-client (for Perspective API)
- langdetect
- tqdm
- wordcloud
- scikit-learn
- scipy
- emoji

### API Keys

**Note:** To run the Perspective API analysis, you will need your own API key. Replace the placeholder in the notebook:

```python
API_KEY = 'INSERT-KEY-HERE'
```

with your actual Perspective API key from Google Cloud.

## Running the Analysis

1. Open `Analysis.ipynb` in Jupyter Notebook:
   ```
   jupyter notebook Analysis.ipynb
   ```

2. Run the cells sequentially to:
   - Load and clean the data
   - Calculate toxicity scores (or use pre-computed scores)
   - Generate visualizations for toxicity trends
   - Analyze topic evolution and linguistic patterns

## Methodology

The analysis combines several NLP techniques:

1. **Toxicity Scoring**: Using both Google's Perspective API and Detoxify AI to measure toxic content in tweets.
   
2. **Topic Modeling**: Classifying tweets into categories like Politics, Tech/AI, Tesla/EVs, etc.
   
3. **Linguistic Analysis**: Tracking evolution of word usage and rhetoric over time.
   
4. **Time Series Analysis**: Tracking toxicity trends and comparing across different public figures.

## Citation

If you use this code or data in your research, please cite:

```
Ayiah, M. (2025). Signals of Shift: A Natural Language Processing-Driven 
Quantification of the Ideological Drift in Elon Musk's Online Presence. 
Yale University, Department of Statistics & Data Science.
```

## License

This project is for academic and research purposes only. The tweet datasets are used under fair use principles for research.

## Contact

For questions about this research, please contact [your-email@example.com].