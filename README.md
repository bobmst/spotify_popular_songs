# About Code

## Introduction

- The main.ipynb is the main script to run the data retrieval pipeline. 
- The code contains exception handling and process display in addition to the data acquisition code, and there are function descriptions below each function.

- spotify.py and genius.py are modules that use the Spotify API and Genius API to retrieve information we needed.

- Change the client id and secretes for API in secrets.py to yours before run the script.

## Requirements

The codes are built on python 3.10.4

The request libraries are listed in requirements.txt

The code to install all libraries provide below for your convience

```python
pip install lyricsgenius pandas retry spotipy tqdm 
```



# About Dataset

## Dataset Information

There are two csv data set. 

**track.csv**: The top 1000 popular songs on Spotify on year 2021, with artist information and song features ranked by Spotify

**lyrics.csv**: Song lyrics for the 1000 songs provide by Genius API

## Content

### track.csv

There are 20 variables:
- **artist_name**: Artist's full name
- **track_name**: Track's full name
- **track_id**: Spotify track id
- **track_popularity**: Track's popularity on Spotify
- **artist_id**: Spotify artist id
- **artist_followers**: Number of artist's followers on Spotify
- **artist_genres**: Artist's track genres
- **artist_popularity**: Artist's popularity on Spotify
- **danceability**: Danceability describes how suitable a track is for dancing based on a combination of musical elements including tempo, rhythm stability, beat strength, and overall regularity. A value of 0.0 is least danceable and 1.0 is most danceable.
- **energy**: Energy is a measure from 0.0 to 1.0 and represents a perceptual measure of intensity and activity. Typically, energetic tracks feel fast, loud, and noisy
- **key**: The key the track is in. Integers map to pitches using standard [Pitch Class notation](https://en.wikipedia.org/wiki/Pitch_class). E.g. 0 = C, 1 = C♯/D♭, 2 = D, and so on. If no key was detected, the value is -1
- **loudness**: The overall loudness of a track in decibels (dB)
- **mode**: Mode indicates the modality (major or minor) of a track, the type of scale from which its melodic content is derived. Major is represented by 1 and minor is 0
- **speechiness**: Speechiness detects the presence of spoken words in a track. The more exclusively speech-like the recording (e.g. talk show, audio book, poetry), the closer to 1.0 the attribute value
- **acousticness**: A measure from 0.0 to 1.0 of whether the track is acoustic
- **instrumentalness**: Predicts whether a track contains no vocals. The closer the instrumentalness value is to 1.0, the greater likelihood the track contains no vocal content
- **liveness**: Detects the presence of an audience in the recording. Higher liveness values represent an increased probability that the track was performed live
- **valence**: A measure from 0.0 to 1.0 describing the musical positiveness conveyed by a track. Tracks with high valence sound more positive (e.g. happy, cheerful, euphoric), while tracks with low valence sound more negative (e.g. sad, depressed, angry)
- **tempo**: The overall estimated tempo of a track in beats per minute (BPM). In musical terminology, tempo is the speed or pace of a given piece and derives directly from the average beat duration
- **duration_ms**: Track duration by milliseconds

  

### lyrics.csv

There are 5variables:

- **artist_name**: The artist's full name
- **track_name**: The completed track name
- **track_id**: The track id by Spotify
- **artist_id**: The artist id by Spotify
- **lyrics**: The lyrics provides by Genius



## Inspiration

Some ideas for exploration:

1. How are the track attributes affect the track popularity?
2. What are the average popularity for each genre?
3. NLP on song lyrics



# References

[Welcome to Spotipy! — spotipy 2.0 documentation](https://spotipy.readthedocs.io/en/master/)

[Web API Reference | Spotify for Developers](https://developer.spotify.com/documentation/web-api/reference/#/operations/get-several-audio-features)

[Getting Audio Features from the Spotify API - The Information Lab](https://www.theinformationlab.co.uk/2019/08/08/getting-audio-features-from-the-spotify-api/)

[What do Spotify’s audio features tell us about this year’s Eurovision Song Contest? 🤔 | by Bo Plantinga | Medium](https://medium.com/@boplantinga/what-do-spotifys-audio-features-tell-us-about-this-year-s-eurovision-song-contest-66ad188e112a#:~:text=Spotify Audio Analysis&text=Danceability%3A Danceability describes how suitable,and 1.0 is most danceable.)

[LyricsGenius: a Python client for the Genius.com API — lyricsgenius documentation](https://lyricsgenius.readthedocs.io/en/master/)





