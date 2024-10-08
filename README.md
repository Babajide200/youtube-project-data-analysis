# youtube-project-data-analysis

# Data Cleaning, Data Manipulation, and SQL Query
This SQL query involves several key steps, including data cleaning, data manipulation, and the construction of a query to aggregate YouTube statistics by continent.

# Data Cleaning (Excel to SQL):
Data Import: Initially, data might be gathered from CSV files and imported into Excel. This raw data includes YouTube statistics like subscribers, uploads, video views, and earnings, as well as information about the Country and individual Youtubers.

# Cleaning in Excel
Standardizing Country Names: Some country names may appear with different spellings (e.g., "Congo, Dem. Rep" vs. "Congo, Rep."). Using Excel, you would clean and standardize these names for consistency.
Handling Missing Values: Missing or null values in columns like subscribers, uploads, or earnings could be handled by either filling them with averages, zeroes, or removing those rows entirely.
Removing Duplicates: Excel would also be used to identify and remove duplicate entries, ensuring the dataset is unique for each Youtuber and country.

# Data Formatting
After cleaning, the data is structured in a format ready to be transferred into a SQL database for further querying.

# Data Manipulation in SQL
Once the cleaned dataset is imported into SQL, data manipulation occurs to group, summarize, and categorize the data based on the continent. This involves:
Case Statements: Using CASE statements to map countries to their respective continents (Africa, Europe, Asia, etc.).
Aggregation: The query uses aggregate functions like SUM() to compute the total number of subscribers, uploads, video views, and earnings across different regions.
Rounding: The ROUND() function is applied to the highest yearly earnings for readability.
Counting Youtubers: The query also uses COUNT() to track the number of Youtubers per continent.

# The SQL query is divided into two main parts:

# Main Query to Aggregate YouTube Statistics by Continent:

The query groups countries into continents using the CASE statement and aggregates the YouTube statistics (subscribers, uploads, video views, and earnings) for each continent. The final result is sorted by the number of Youtubers (ORDER BY 5 DESC).

# Calculating Percentages:

A CTE (Common Table Expression) called pct_pay is used to calculate the total earnings per continent. The second query then calculates the percentage share of earnings contributed by Africa (and other continents), using CASE and SUM() functions to aggregate earnings and calculate the percentages.
