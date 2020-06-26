# Spotify-Music-Analysis
Objective : In this project, Spotify top 200 music data used to identify patterns, perform clustering of similiar songs and classification of the new track into one of the cluster.

Motivation : I was interested to find out which songs reach the Top 200 in Spotify, what made a number one song and what is the lifetime of the number one song over the year.

Data : The data for the songs comes from the Spotify Charts https://spotifycharts.com/regional. For this project I have considered only the US region data from Jan 2019 - May 2020
I used Python's BeautifulSoup to scrape each days data and append each day to create a single csv file. This file contains the Top200 songs each day along with Track Name, Artist, 
Position of the Track on that day.

Next, I used the Spotify API to get track features which includes values acousticness, danceability, duration_ms, energy, instrumentalness, key, liveness, loudness, mode,	speechiness, tempo, time_signature. There is  description for each of the feature on https://developer.spotify.com/documentation/web-api/reference/tracks/get-audio-features/

I also used the API to pull the artist information which contains the artist name, popularity, followers and genre

Analysis and Results : The following analysis was performed:

1. An animated scatter plot was created to identify the patters in which the number one songs change position over the year
2. A looping bar chart was created using funcanimation to show the top15 songs-artist based on streams 
3. A radar chart was created for all the number one tracks to identify the what track features make a song popular
4. Clutering was performed on the tracks to group them into similiar clusters. Different clustering algorith was explored : KMeans, Affinity Propagation, 
Agglomerative Clustering, BIRCH, DBSCAN, HDBSCAN, Mini Batch K-Means, OPTICS, Spectral, Gaussian Mixture Model. Based on the Silhoutette score, K-means was selected as the best
performing algorithm
5. Finally, decision tree classifier was used to classify new songs into one of the above clusters. The model was trained on the data from 2019 and resulted 95% accuracy score.
Top 200 Tracks from Jan 2020 - May 2020 were used as the test set for prediction






