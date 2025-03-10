# ScrapeAdventure

This repository contains code for scraping, analyzing, and visualizing movie data from IMDb's popular movies chart.

## Overview

The project is divided into two main parts:
1. Web scraping and data wrangling
2. Exploratory and predictive analytics

## Features

- Scrapes movie data from IMDb's "Most Popular Movies" chart
- Extracts key information including titles, genres, directors, release years, ratings, and vote counts
- Cleans and preprocesses the data for analysis
- Provides descriptive statistics
- Visualizes data distributions and relationships

## Requirements

- requests
- beautifulsoup4
- pandas
- matplotlib
- seaborn
- json

## How It Works

### Web Scraping Process

The script uses the requests library to fetch IMDb's popular movies page and BeautifulSoup to parse the HTML. Movie data is extracted from a JSON object embedded in the page, which provides structured access to movie details.

### Data Preprocessing

- Missing values are handled and replaced with pandas NA
- Data types are properly converted (strings to numeric values where appropriate)
- Rows with critical missing data are removed
- All data is organized into a pandas DataFrame for analysis

### Analysis and Visualization

The code performs several analyses:
- Descriptive statistics for both numerical and categorical variables
- Distribution of movie release years
- Distribution of IMDb scores
- Relationship between release year and IMDb score

## Example Output

The analysis produces a DataFrame with 87 movies containing the following attributes:
- Title
- Genre
- Director
- Release Year
- IMDb Score
- Vote Count

## Limitations

- Data quality depends on the IMDb page structure; changes to the website might break the scraping process
- Web scraping may violate website terms of service if not done responsibly
- The current approach may face scalability issues with larger datasets due to rate limits

## Future Work

- Scrape additional data points such as cast, crew, and user reviews
- Implement machine learning models to predict movie success
- Develop real-time data scraping and analysis capabilities

## Why IMDb?

IMDb is an excellent source for movie data because:
- It offers extensive information on movies
- Data is presented in a consistent, structured format
- It's regularly updated with the latest information
- It's widely recognized as a reliable source for movie information

## Legal Note

Remember that web scraping may violate a website's terms of service. Always respect robots.txt files and rate limits when scraping websites.
