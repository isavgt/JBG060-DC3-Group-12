# South Sudan Project 

## DISCLAIMER
On the day of the deadline, we found that the 'sentiment_analysis' file was not saved correctly. Therefore, we miss the code of the figures on the poster. However, the figures itselve were saved in the figs folder. We have tried everything to get the code back, but were unsuccessful. 


## Code description
This code has been extended by testing sentiment analysis on a test set of articles and article summaries. The random test set is created in creation_test_set.py. This file produces 2 csv files:
1. Random_summaries.csv: a csv with a random selection of summaries from articles_summary_cleaned. 
2. Random_pars.csv: a csv with a random selection of paragraphs from all_africa_southsudan. 

The summaries and paragraphs in these csv files were evaluated by our group and have been given sentiment scores: 1 for positive, 0 for neutral, -1 for negative. These results are saved to test_set_paragraphs.csv and test_set_summaries.csv. These files are used in sentiment_analysis.ipynb to evaluate 2 different sentiment analysis models. 

Firstly, topic_modelling.ipynb could be used later to combine topic modelling and sentiment analysis. In this notebook, a BERTopic model is fit on _articles_summary_cleaned.csv_, then four categories/keywords (hunger, refugees, humanitarian, and conflict) are defined. These categories are used for categorising articles (or none if the article doesn’t match any of the categories) and thus creating features from the news articles. Secondly, the _predictions.ipynb_ notebook can be run for some very basic data exploration, along with fitting several linear models on the data, with- and without the news features. The notebook uses the _food_crises_cleaned.csv_ dataset and the csv file obtained from the  _topic_modelling.ipynb_ notebook.

## Requirements
To install the requirements open Terminal (macOS)/Command Prompt (Windows) and run pip install -r requirements.txt. If you create a new environment in PyCharm, an icon should appear to install requirements. The code runs with Python 3.9.16.

Required libraries:
- bertopic == 0.15.0 
- pandas == 1.4.4 
- geopandas == 0.13.2 
- matplotlib == 3.7.2 
- seaborn == 0.12.2
- statsmodels == 0.14.0 
- sklearn == 0.0.post5
- nltk == 3.8.1
- vaderSentiment == 3.3.2

## Troubleshooting

If you encounter any issues while running the notebooks, try the following:
- check that you have all the necessary libraries installed and the correct versions of them
- check your Python version. In principle, the code should work with any Python versions higher than 3.9.16. If this is not the case, create a virtual environment that uses Python 3.9.16.