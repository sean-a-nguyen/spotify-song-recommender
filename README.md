# Song Recommender System

![Spotify_Logo_CMYK_Green](https://user-images.githubusercontent.com/69729732/135726711-32867519-b2b9-483c-ae61-a26c3c74b550.png)
### Intent of this project is to fully understand how to build a recommender system from scratch; with all the resources I used, I attempt to summarize the information for a general audience.

## Introduction

As someone who uses Spotify daily, I always wondered what makes me come back to the app. For me, it's the ability to find new music. I have discovered my favorite artists through Spotify's Daily Mixes and song recommendations based on my playlists, but how do they do this? How do they give song recommendations based on what I like? 

**The goal of this project is to understand how Spotify might recommend a set of songs based on a user playlist and to create a system that might be used.**

Data can be found [here](https://www.kaggle.com/rodolfofigueroa/spotify-12m-songs)

**Limitations to the data**:
- Doesn't cover all songs in the Spotify's catalog
- Doesn't cover all songs in my specifc playlists
- No metadata provided (genres for each song, etc.)

## Overview of what a recommender system is

What is a recommender system? To put it simply, a system that has information about a user or a product and provides a relevant item based on the features of them. As mentioned before, I was able to find some of my favorite songs on Spotify. Spotify provides personalized playlists dependent on my listening activity and those songs in those playlists are the outputs of the recommender system.

You can see how a recommender system can be valuable to many other companies, such as YouTube, Netflix, Hulu, and Amazon just to name a few. They increase user engagement and sales, ultimately helping their business grow. 

There are 2 types of recommender systems. Collaborative and content-based. 

We are going to build a **content-based recommender system** which takes information about the user and/or items to make recommendations rather than using user activity, since we don't have access to Spotify's user activity data. 

Later in the notebook, we will go over what kind of specific features of the user/item that will drive our recommender system and how we need to prepare our data to do so. 

## Steps to build content-based recommender system
1. **Gather the data**
    - Add genres to Kaggle Dataset
    - **Performed in another notebook**
    
    
2. **Connect to Spotify API and spotipy**
    - Get my playlist information
    - Get Spotify song data to add to the Kaggle data
    
    
3. **Data cleaning/preparation**
    - Summary statistics
    - Regex cleaning
    - Data types
    
    
4. **Feature engineering**
    - Dummy variables or One Hot Encoding for Year feature https://machinelearningmastery.com/why-one-hot-encode-data-in-machine-learning/
    - Normalizing the numeric features
    - TF-IDF (Term frequency - Inverse Document Frequency) for the artists https://www.youtube.com/watch?v=D2V1okCEsiE
    
    
5. **Create playlist vector**
    - This vector defines the attributes of our playlist
    - Add recency bias
    
    
6. **Make recommendations**
    - Based on cosine similarity https://www.youtube.com/watch?v=ieMjGVYw9ag
    - Recommender system 1: Only genres + song features
    - Recommender system 2: Adding an artist recommender to song recommender
    
    
7. **Evaluate performance of the model**
    - How do we know our models are performing well?
    - Research on how to do that


## Methods
- Data Cleaning and Preparation
- Feature Engineering
- Content based recommender

## Technologies
- Python
    - pandas
    - spotipy
    - sklearn

## Acknowledgements
1. https://github.com/madhavthaker/spotify-recommendation-system/blob/main/spotify-recommendation-engine.ipynb
2. https://www.youtube.com/watch?v=xdq6Gz33khQ&t=494s
3. https://github.com/codingforentrepreneurs/30-Days-of-Python/tree/master/tutorial-reference/Day%2019
