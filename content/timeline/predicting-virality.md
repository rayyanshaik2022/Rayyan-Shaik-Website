---
title: "Predicting the degree of virality of trending pop songs"
eventname: "🎵 Predict how viral a trending song will be based only on its lyrics"
date: 2024-05-20
publishDate: 2024-06-25
author: "Rayyan Shaik"
draft: false
images: []
tags: ["Python", "Machine Learnings", "Neural Networks", "Music", "Featured"]
projects: ["Programming Projects"]
---

A research and exploration capstone project for `CIS 5190 - Applied Machine Learning` by Rayyan Shaik, Esther Armao, Helen Nguyen

This project aims predict the virality of a given pop song given only its lyrics.

We split this project into 2 main contributions, which are outlined below:

## Contribution 1: Dataset of Pop Songs, Lyrics, Streaming Data
All data (selection of pop songs, their respective lyrics and historical streaming data) was webscraped using python
A link to the dataset generation repository can be found here: [Music-Project-Scraper](https://github.com/rayyanshaik2022/Music-Project-Data)

1. Step 1: Scraping a list of pops songs (names & artists) by year
  - Done by scraping Apple Music
2. Step 2: Scraping lyrics and lyrics meta-data per song
  - Done by scraping Genius and using Genius' API
3. Step 3: Weekly streaming data (global & US) per song
  - Done by scraping kworb.net for spotify streaming data on each of the songs from step 1

Further feature extraction was done across all of the song lyrics
- `Sentiment Analysis` using NLTK’s VADER Sentiment Analyzer
- `Bag of Words` using CountVectorizer from scikit-learn


## Contribution 2: Model to evaluate an input song’s “virality”

### Model Results
- **Accuracy**: ~70%
- **F1 Scores**: 48%, 77%, 0% for classes 0, 1 and 2 respectively


### Our Neural Network Architecture
{{< figure src="../../images/nn-architecture.png" alt="nn-architecture.png" width=600 >}}

---

This was group effort created as a capstone project for `CIS 5190 - Applied Machine Learning` at UPenn
