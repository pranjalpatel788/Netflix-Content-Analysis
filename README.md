# Netflix-Content-Analysis

##Dataset Details  
The initial dataset, netflix_titles.csv, consists of 8807 rows and 12 columns.
The available columns are: show_id, type, title, director, cast, country, date_added, release_year, rating, duration, listed_in, and description.

##Data Cleaning Workflow  
To prepare the data for exploratory analysis, several cleaning and preprocessing steps were executed:  
Removed rows with missing duration values, as they could not be reasonably filled and represented less than 5% of the data.  
Filled null values in the country column with the label "Unknown".  
Filled null values in the director column with the label "Not Specified".  
Filled missing values in the cast column with the label "Unknown".  
Imputed missing textual data in the rating column using the mode (most frequent value).  
Converted the date_added column to a datetime format to facilitate the extraction of time-based features like the year and month of release.  
Dropped any remaining rows with null date_added values, resulting in a final cleaned dataset of 8706 rows.  
Verified that there were no duplicate records in the dataset prior to analysis.

##Exploratory Data Analysis & Key Insights

**Geographical Content Distribution**  
A bar chart visualization demonstrates that the United States is the leading country in producing Netflix content, with a count of 3640 titles.  
India follows in second place with 1045 titles, followed by "Unknown" (827), the United Kingdom (787), Canada (432), France (389), Japan (314), and Spain (228).

**Production Trends Over Time**  
A pie chart highlights that the years 2019 (1999 titles) and 2020 (1878 titles) were the peak years for content production on Netflix.  
Other significant years include 2018, 2021, and 2017, indicating a substantial surge in content added during this overall period.  
A heatmap analyzing the month and year of releases shows a higher volume of new content releases towards the end of the year, specifically in October, November, and December.  
A line plot comparing Movies and TV Shows from 2008 onwards reveals that movies consistently have a higher number of releases each year compared to TV shows.

**Genre Analysis**  
A bar chart of the top 10 genres reveals that 'International Movies', 'Dramas', and 'Comedies' are the most prominent categories on the platform.  
An analysis of the average number of titles per year for the top 5 genres shows that 'International Movies' has the highest average annual production at 275.2 titles.  
This is followed by 'Dramas' (242.7), 'Comedies' (167.4), 'International TV Shows' (166.0), and 'Documentaries' (86.9).

**Ratings & Durations**  
Content ratings were analyzed, showing that 'TV-MA' is the most frequent rating with 3187 titles, indicating that a significant portion of Netflix's content is aimed at mature audiences.  
'TV-14' is the second most common rating with 2133 titles.  
The project also groups and visualizes the top 10 content durations using a horizontal bar chart.

##Technologies Used  
Python  
Pandas for data manipulation and structure  
NumPy for numerical operations  
Matplotlib & Seaborn for data visualization








