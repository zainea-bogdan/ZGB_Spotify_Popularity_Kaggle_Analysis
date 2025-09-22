# ZGB_Spotify_Popularity_Kaggle_Analysis

## Fictive Context
I am working as part of the analytics team of a fictive music research lab called **SoundPulse**.  
My task is to explore and analyze a dataset of about 1,000 songs collected from multiple streaming platforms.  
The goal is to uncover insights about music trends, artist performance, and the evolution of sound features across time.

The dataset comes from Kaggle:  
[Spotify Popularity Songs Dataset](https://www.kaggle.com/datasets/ahmadrazakashif/spotify-popularity-songs/data)

The dataset includes the following columns:

- `track_name`  
- `artist(s)_name`  
- `artist_count`  
- `released_year`, `released_month`, `released_day`  
- `in_spotify_playlists`, `in_spotify_charts`, `streams`  
- `in_apple_playlists`, `in_apple_charts`  
- `in_deezer_playlists`, `in_deezer_charts`  
- `in_shazam_charts`  
- `bpm`, `key`, `mode`  
- `danceability_%`, `valence_%`, `energy_%`  
- `acousticness_%`, `instrumentalness_%`, `liveness_%`, `speechiness_%`

---

## Beginner Level

1. Load the dataset and display the first 10 rows. Explore column types (`.info()` and `.describe()`).
2. Count how many unique artists are in the dataset.
3. Find the most common release year for tracks.
4. Plot a histogram of `streams`. Apply a log transformation if the distribution is heavily skewed.
5. Create a bar plot of the top 10 most frequent keys used in songs.

---

## Intermediate Level

6. Find the top 10 tracks with the highest number of Spotify streams.
7. Compare the average danceability of songs released before 2010 vs after 2010.
8. Group by `artist(s)_name` and compute the average `energy_%` for their tracks. Plot the top 15 artists.
9. Find correlations between `bpm`, `energy_%`, `danceability_%`, and `valence_%`. Use a heatmap.
10. Plot a line chart of the number of songs released per year.

---

## Advanced Level

11. Create a scatterplot of `danceability_%` vs `valence_%`, colored by `mode`.
12. Identify which artists have the highest average streams per track (only consider artists with at least 5 tracks).
13. Compare how `acousticness_%` differs between the top 10 streamed artists using a boxplot.
14. Find the most "danceable" year by computing the average `danceability_%` per year.
15. Analyze seasonal patterns by plotting the number of songs released by month.

---

## Expert Level

16. Create a new column `is_popular` = 1 if a track's streams are in the top 10% (instead of 5%, to account for the smaller dataset).  
   Analyze differences in `bpm` and `energy_%` between popular and non-popular songs.
17. Use a rolling or expanding window to analyze trends in average `valence_%` across years.  
18. Build a radar (spider) chart comparing audio features (`danceability_%`, `energy_%`, etc.) for 3 selected artists.
19. Cluster songs using KMeans on audio features (scaled). Visualize clusters with PCA on a 2D scatterplot.  
   Keep the number of clusters small (e.g., 3–5) given the dataset size.
20. Predict `mode` (major/minor) using logistic regression on audio features.  
   Evaluate with accuracy, even though the dataset is small.

---

## Mastery Level

21. Create a dashboard-style visualization showing:
   - Top artists by streams
   - Distribution of keys used
   - Trends in releases per year
   - Correlation heatmap of features

22. Identify outliers in `streams` using IQR or Z-score. Plot them separately from the main distribution.
23. Build a "music fingerprint" profile for each decade (mean audio features). Visualize them with radar plots.
24. Compare feature distributions (`danceability_%`, `valence_%`, `energy_%`) between songs that appear in Spotify playlists vs songs that do not.
25. Final storytelling project: Create an end-to-end notebook that answers the question:  
   **"How has the energy and mood of popular music changed from 2000 to 2025?"**

---

## Goal
My aim is to practice data exploration, visualization, and basic analysis techniques on a real-world dataset,  
using **Python** with **Pandas, NumPy, Seaborn, and Matplotlib** as the main libraries.
