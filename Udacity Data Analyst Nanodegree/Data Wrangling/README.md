# Wrangle Act by Chiebuka Okoro

## WRANGLE REPORT
My wrangling for this project began by Gathering (first data wrangling process) data from 3
different source: CSV file, URL, and JSON file. These data were imported into the following
dataframe respectively: twitter_archive_df, extract_df, and tweet_df. Upon gathering the data,
I went ahead to carry out the first data wrangling process – Assessment.

## ASSESSMENT
After assessing the 3 dataframes separately, I discovered a sum of nine (9) and two (2) data
quality issues and data tidiness issues respectively.

## 1. Data Quality Issues
This is categorized based on the various dataframes:

# twitter_archive_df:
1. The columns (doggo, floofer, pupper, and puppo) should be combined rather than standalone,
as they are all different dog stages.
2. The timestamp and retweeted_status_timestamp column has an inappropriate datatype
(object) and should be changed to datetime if need be.
3. Columns with relatively empty data such as in_reply_to_status_id, in_reply_to_user_id,
retweeted_status_id, retweeted_status_user_id, retweeted_status_timestamp should be
dropped as they are not relevant to our analysis as well.
4. Some of the column names are not descriptive enough and should be changed to names that
are descriptive enough.
5. From the statistical summary, the max values of the rating_numerator and
rating_denominator seem to be outliers when compared to the first, second, and third quartiles.
All data in the rating_denominator column having data other than 10 should be replaced with
10 and those of the rating_numerator be deleted.
6. Upon visual inspection, some of the data in the name column are filled with none and other
with erroneous data such as a.

# tweet_updated_df:
7. The id column is not descriptive enough and should be changed.

# extract_df:
8. Some records are not dog related.
9. Majority of the column headers are not descriptive and should be changed.

## 2. Data Quality Issues

# twitter_archive_df:
1. Since variable(s) form a column, the columns having a higher percentage of empty data pose
tidiness issues and should be removed.
2. The tweet_df dataframe contains observations that should be on different tables or standalone
for the sake of tidiness.
After figuring out these issues, I moved on to the final data wrangling process – Cleaning.

## CLEANING
All the above issues were fixed by following the Define, Code, and Test cleaning approach.
