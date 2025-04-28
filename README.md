This repository contains a machine learning pipeline for predicting stock market movements using Reddit sentiment analysis and historical stock data.

Setup Instructions
Prerequisites
Anaconda or Miniconda installed
GitHub access to clone this repository
Reddit API credentials (for data scraping)
Environment Setup:

CLONE THE REPOSITORY:

git clone https://github.com/YOUR-USERNAME/RedditStocks_v2.0.git
cd RedditStocks_v2.0

CREATE AND ACTIVATE THE CONDA ENVIRONMENT:

conda create -n RedditStocksV2 python=3.8
conda activate RedditStocksV2

Install required packages from environment.yml file.

Create credentials with Reddit API:


  "client_id": "YOUR_CLIENT_ID",
  "client_secret": "YOUR_CLIENT_SECRET",
  "user_agent": "YOUR_USER_AGENT",
  "username": "YOUR_REDDIT_USERNAME",
  "password": "YOUR_REDDIT_PASSWORD"

Then as follows:
Collect posts from reddit with the redditscraper notebook, analyze them with the vaderbert notebook, fetch stock data with the yahoofinance notebook, merge them with the notebook named merge, and then run the models. The script includes MPS specific lines change them to cuda to run on an NVIDA gpu other wise it will run on the systems CPU. Reddit API rate limits may apply and this might increase the sleep timer or the amount of cde that can be scraped.
