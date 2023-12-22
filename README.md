# 80s Song Lyrics Scraper from JOOX Playlist

This repository contains a Jupyter notebook titled `lyrics_scraping.ipynb`, which is designed for scraping song lyrics from the 1980s, specifically from a playlist on JOOX. The notebook demonstrates a two-step process: initially scraping the names and URLs of songs from the JOOX playlist, followed by visiting each URL to scrape the lyrics of each song.

## Run the Notebook in Google Colab

You can run and interact with the notebook directly in your browser using Google Colab:

[![Open In Colab]([[colab.research.google.com/assets/colab-badge.svg](https://colab.research.google.com/drive/1HhWS6zsM7lgsA6b8k4cXAz-nptoVin9R)](https://colab.research.google.com/drive/1UHBxvGJfmF5_o-wbeKwtyuKVC_A9H8BQ))]

## Overview

The notebook is organized as follows:

1. **Setup**: Import necessary Python libraries like `bs4` (Beautiful Soup) for web scraping and `requests` for handling HTTP requests

2. **Initial Data Scraping**: 
   - The first stage involves scraping the JOOX playlist to gather song names and their corresponding URLs which lead to the song lyrics.
   - This data is then stored in a DataFrame, providing a structured format for the list of songs and their respective URLs.

3. **Lyrics Scraping**:
   - In the second stage, the notebook iterates through each URL in the DataFrame.
   - For each song URL, an HTTP request is made, and the HTML content of the page is parsed using Beautiful Soup.
   - The script specifically searches for a `div` tag with the class `'jsx-804686892 renderLyrics'`, which is containing the lyrics.
   - If lyrics are found, they are extracted and added to the DataFrame; otherwise, a placeholder text such as "Lyrics not found" is recorded.

4. **Data Storage**:
   - After completing the scraping process, the enhanced DataFrame, now containing song metadata along with the lyrics, is exported and saved as a CSV file (`song_lyrics_80s.csv`).

## Usage

This notebook can be used as a template or guide for similar web scraping tasks, especially for those interested in collecting data from music streaming websites like JOOX. It demonstrates practical techniques in Python for web scraping, data extraction, and data storage.

## Requirements

- Python 3.x
- Libraries: `bs4`, `requests`
