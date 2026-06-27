# 📺 Netflix Content Analysis
## Project Overview
This repository contains a comprehensive data analysis of Netflix titles to explore content production trends, popular genres, target audiences, and geographical content distribution. The analysis uncovers key business and entertainment insights using Python in a Jupyter Notebook environment.

## Dataset Details
The initial dataset, `netflix_titles.csv`, consists of 8,807 rows and 12 columns. 

**Key Features Include:**
* `show_id`: Unique ID for every Movie / TV Show
* `type`: Identifier - A Movie or TV Show
* `title`: Title of the Movie / TV Show
* `director`: Director of the content
* `cast`: Actors involved
* `country`: Country where the movie/show was produced
* `date_added`: Date it was added on Netflix
* `release_year`: Actual release year of the content
* `rating`: TV Rating of the movie/show
* `duration`: Total duration (in minutes or seasons)
* `listed_in`: Genres the content falls under
* `description`: Summary of the content

## Data Cleaning Workflow
To prepare the data for exploratory data analysis (EDA), several preprocessing steps were executed:
* Removed rows with missing `duration` values.
* Handled null values by imputing "Unknown" for `country` and `cast`, and "Not Specified" for `director`.
* Imputed missing textual data in the `rating` column using the mode.
* Converted `date_added` to a datetime format to extract time-based features (year, month).
* Dropped remaining rows with null `date_added` values, resulting in a final cleaned dataset of **8,706 rows**.
* Verified the absence of duplicate records.

## Key Exploratory Insights
Through various visualizations, the following insights were extracted:

* **Geographical Distribution:** The **United States** leads content production (3,640 titles), followed by **India** (1,045 titles) and the **UK** (787).
* **Production Trends:** Content addition peaked in **2019 (1,999 titles)** and **2020 (1,878 titles)**. Late-year months (October, November, December) see the highest volume of new releases.
* **Movies vs. TV Shows:** Movies consistently outpace TV Shows in annual releases.
* **Top Genres:** 'International Movies', 'Dramas', and 'Comedies' dominate the platform. 'International Movies' boasts the highest average annual production (275.2 titles/year).
* **Target Audience:** A significant portion of Netflix's content is aimed at mature audiences, with **'TV-MA'** being the most frequent rating (3,187 titles), followed by 'TV-14'.

## Technologies Used
* **Python**
* **Pandas** (Data manipulation)
* **NumPy** (Numerical operations)
* **Matplotlib & Seaborn** (Data visualization: pie charts, line plots, bar charts, heatmaps)

