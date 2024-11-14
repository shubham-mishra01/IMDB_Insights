# Movie Industry Metrics Power BI Dashboard

# Problem Statement
This Power BI dashboard offers insights into the movie industry by analyzing metrics such as box office revenue, ratings, genre trends, and awards. It enables users to explore patterns, identify areas for improvement, and understand the factors driving a movie's success. Through the dashboard, users can analyze trends, investigate genre preferences, and evaluate the impact of awards and ratings on box office performance.

### Steps Followed
- Step 1: Load data into Power BI Desktop from CSV files containing detailed information about movies.
- Step 1: Load data into Power BI Desktop from multiple CSV files containing detailed movie information, such as IMDB ratings, box office data, genres, and awards.
- Step 2: In Power Query, enable Column Quality, Column Distribution, and Column Profile to assess data quality and identify issues with missing or inconsistent values.
- Step 3: Replace N/A values with null in columns like Box Office, Released, and Awards to standardize data for transformations.
- Step 4: Convert data types as needed, ensuring Box Office is set to currency, Runtime to duration, and other columns to appropriate formats.
- Step 5: Clean and transform Box Office data by converting currency values from text to numeric format, enabling calculations and statistical analysis.
- Step 6: Label movies with missing Box Office values as "Unknown - Low Rating" or "Unknown - High Rating" based on rating thresholds.
- Step 7: Address missing values in the Released column by filling null values with the most common release date for each year, or defaulting to January 1st if no common date exists.
- Step 8: Convert DVD Release dates from text to date format to ensure consistency across date fields.
- Step 9: Split and categorize awards data into General Award Wins/Nominations and Special Awards (e.g., Oscars, Golden Globes, BAFTAs).
- Step 10: Create calculated columns to differentiate between "Another" wins/nominations and direct mentions of specific awards.
- Step 11: Split complex awards data using delimiters to parse fields with phrases like "Another" or "&" to separate general and special award counts.
- Step 12: Calculate General Award Wins and General Award Nominations by summing parsed values from split awards columns.
- Step 13: Create additional columns for Total Wins and Total Nominations by aggregating both general and special award categories.
- Step 14: Split Genre data into genre_1, genre_2, and genre_3 columns to separate multiple genres associated with each movie.
- Step 15: Create a combined genre list in a separate table to identify the most common genres and facilitate genre-specific filtering.
- Step 16: Calculate genre frequency across the dataset to identify and showcase the most prevalent genres.
- Step 17: Transform the Runtime column to extract and standardize duration in minutes, filling missing values with median runtime where applicable.
- Step 18: Split the Language column to handle multiple languages associated with each movie, allowing for language-specific analysis and counts.
- Step 19: Parse Director and Actor columns to separate multiple individuals, filling missing values with "None" for easier counting.
- Step 20: Create calculated columns to count the number of Directors and Actors associated with each movie.
- Step 21: Set up a relationship between Hotlist and Main Data tables using imdbID as the key, configuring cross-filter direction as single.
- Step 22: Create calculated columns and measures, including Top 5 High-Grossing Movies, Most Common Genre, and aggregate calculations for Total Wins and Total Nominations.
- Step 23: Apply binning on the Box Office Revenue field to group movies into revenue brackets for revenue distribution analysis.
- Step 24: Add slicers for key fields such as Genre, Year, and Rating to enable user-driven exploration and dynamic filtering of visuals.
- Step 25: Convert slicers to Dropdown format for a cleaner, more compact layout, allowing users to filter and interact with the dashboard easily.
- Step 26: Organize visuals across multiple pages to create a structured, easy-to-navigate dashboard:
Overview Page: Summarizes key metrics, highlights high-grossing movies, and displays the most common genres.
Box Office Trends: Showcases box office revenue patterns over time, by genre, and by rating.
Ratings and Genre Analysis: Provides insights into rating distributions, genre correlations, and trends in genre popularity.
Awards Insights: Provides a detailed breakdown of awards and nominations, including both general and special award categories.
- Step 27: Adjust formatting of visuals, ensuring consistent font sizes, color schemes, and alignment across all pages.
- Step 28: Apply conditional formatting in tables and KPIs, such as color-coding Metascore ranges (green for high scores, yellow for medium, red for low scores).
- Step 29: Use KPI cards to display metrics like Total Wins, Total Nominations, and Top Genres, ensuring easy visibility of critical insights.
- Step 30: Publish the dashboard to Power BI Service, enabling full-screen presentation mode for a professional, distraction-free display.
- Step 31: Test all interactive elements, including slicers and filters, to confirm they function as intended and provide a smooth user experience.
# Dashboard Structure
The dashboard is divided into 4 main sections, each focusing on specific analysis dimensions:

## Page 1: Overview / Summary
A high-level summary of key movie metrics:

Total Box Office Revenue
Average Rating
Most Common Genre
Total Wins and Nominations
Top-Grossing and Highest-Rated Movies
## Page 2: Box Office Trends
This page dives into revenue patterns over time and across genres:

Revenue Over Time: Line chart to view trends across release years.
Revenue by Genre: Stacked bar chart to show revenue contributions by genre.
Revenue by Rating: Column chart displaying revenue distribution across different rating categories.
Revenue Distribution: Histogram (using custom visual by MAQ Software) showing the spread of revenue across movies.
Slicers for Interactivity:
Genre, Year, and Rating Slicers allow users to filter and explore specific data segments.
## Page 3: Ratings and Genre Analysis
A focused analysis of movie ratings, genre, and awards:

Rating Distribution: Histogram showing rating spread across all movies.
Rating by Genre: Bar chart depicting average ratings by genre.
Awards vs. Ratings: Scatter plot showing how ratings correlate with total awards.
Slicers:
Genre and Rating Range slicers enable detailed exploration of specific segments.
## Page 4: Awards Insights
An in-depth look at awards:

Total Wins and Nominations for both general and special awards.
Top Award-Winning Movies for quick reference.
Custom Visuals and Features
Histogram by MAQ Software for box office revenue distribution.
Box Plot by MAQ Software for viewing revenue spread across categories.
Dynamic Slicers: Filters for Genre, Year, and Rating allow users to drill down into specific data segments.

# Insights
The dashboard enables users to explore valuable insights into the movie industry:

### [1] Top Metrics
Total Wins and Nominations summarize both general and special awards.
Most Common Genre highlights the genre with the most releases.
Top 5 High-Grossing Movies display the highest box office performers.
### [2] Box Office Trends
Significant revenue trends are visible across genres, ratings, and release years.
High-grossing genres and top-rated genres provide insights into audience preferences.
### [3] Awards and Ratings Analysis
Correlation between ratings and awards highlights how quality, as perceived through ratings, impacts award recognition.
Genre-based analysis reveals which genres tend to perform better both critically and commercially.
### [4] Rating Distribution and Genre Impact
Rating distribution across genres reveals patterns of viewer preferences.
Analysis of box office performance and awards by genre shows how specific genres fare in the industry.
## Project Details
- Author: https://github.com/shubham-mishra01/IMDB_Insights/commits?author=shubham-mishra01
- Technology Stack: Power BI, DAX, Power Query
- Use Case: Business Intelligence Case Study for movie industry insights.
