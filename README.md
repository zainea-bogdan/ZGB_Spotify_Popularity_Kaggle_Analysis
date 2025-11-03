# ZGB_Spotify_Popularity_Kaggle_Analysis

## Fictive Context

I am working as part of the analytics team of a fictive music research lab called **SoundPulse**.  
My task is to explore and analyze a dataset of about 1,000 songs collected from multiple streaming platforms.  
The goal is to uncover insights about music trends, artist performance, and the evolution of sound features across time.

The dataset is available on Kaggle:  
[Spotify Popularity Songs Dataset](https://www.kaggle.com/datasets/ahmadrazakashif/spotify-popularity-songs/data)

To follow along, download the dataset from Kaggle and place the CSV file in a folder named `dataset` at the root of the project.  
Rename the file to `data1.csv` so it can be easily referenced in the notebooks.

---

## Color Code

- 🔴 = I couldn’t solve it on my own and didn’t find a working solution.
- 🟡 = My thinking process was on the right track, but I still needed to google or ask GPT for help.
- 🟢 = I solved it by myself, with only minimal googling or GPT input if needed.

---

## Tasks Assigned by Level

### Level 1 — **Getting to Know the Catalog**

1. Load the dataset into a Pandas DataFrame.🟢
2. Display the first 10 rows (`.head()`) and last 10 rows (`.tail()`).🟢
3. Use `.info()` to check dtypes and nullability of columns.🟢
4. Use `.describe()` to get summary statistics of numeric columns.🟢
5. Check the shape of the dataset with `.shape`.🟢

---

### Level 2 — **Picking Out Songs**

6. List all column names in the dataset.🟢
7. Select only the `track_name` column.🟢
8. Select both `track_name` and `artist(s)_name` columns.🟢
9. Retrieve the first 5 songs released after 2020.🟡
10. Use `.iloc[]` to display rows 10 to 20.🟢

---

### Level 3 — **Filtering the Playlist**

11. Filter songs where `streams` is greater than 1 million.
12. Filter songs released before the year 2000.
13. Count how many tracks each artist has using `.value_counts()`.
14. Find the most common release year (`.mode()` or `.value_counts().idxmax()`).
15. Filter songs where `mode = 1` (major key).

---

### Level 4 — **Spotting Trends**

16. Group by `released_year` and calculate the average `streams`.
17. Group by `artist(s)_name` and compute the mean `energy_%`.
18. Find the artist with the highest average streams (minimum 5 tracks).
19. Compare mean `valence_%` between `mode = 0` and `mode = 1`.
20. Create a pivot table showing average `danceability_%` per year.

---

### Level 5 — **Cleaning the Sound**

21. Convert the `streams` column from object to integer (handle commas).
22. Remove rows where `streams` contains non-numeric values.
23. Rename the column `artist(s)_name` to `artist_name`.
24. Create a new column `streams_millions` (divide by 1,000,000).
25. Bin songs into categories (`low`, `medium`, `high`) based on streams.

---

### Level 6 — **Amplifying Insights**

26. Sort songs by `streams` descending and show the top 10.
27. Plot a histogram of `streams_millions` (try both raw and log scale).
28. Plot a bar chart of the 10 most common keys.
29. Create a correlation heatmap of `bpm`, `energy_%`, `danceability_%`, and `valence_%`.
30. Create a new column `is_popular` = 1 if `streams` is in the top 10%, else 0.

---

## Goal

My aim is to practice Pandas fundamentals step by step: loading, inspecting, selecting, filtering, aggregating, cleaning, transforming, and visualizing real-world data.
