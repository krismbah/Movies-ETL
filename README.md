# Movies-ETL_Analysis

## Overview

The purpose of this analysis is  to create an automated pipeline that takes in new data, performs the appropriate transformations, and loads the data into existing tables. It’ll need to refactor the code from this module to create a function that takes in the three files—Wikipedia data, Kaggle metadata, and the MovieLens rating data—and performs the ETL process by adding the data to a PostgreSQL database. The following tasks are to be completed: 

1. Write an ETL Function to Read Three Data Files.
2. Extract and Transform the Wikipedia Data.
3. Extract and Transform the Kaggle data.
4. Create the Movie Database.

## Results

***Deliverable 1: Write an ETL Function to Read Three Data Files***
Using knowledge of Python, Pandas, the ETL process, and code refactoring, write a function that reads in the three data files and creates three separate DataFrames.

Figure 1:

![Deliverable1kaggle](https://raw.githubusercontent.com/krismbah/Movies-ETL/main/Deliverable1kaggle.png)

Figure 2:

![Deliverable2wiki_df](https://raw.githubusercontent.com/krismbah/Movies-ETL/main/Deliverable2wiki_df.png)

Figure 3:

![Deliverable1ratings](https://raw.githubusercontent.com/krismbah/Movies-ETL/main/Deliverable1ratings.png)


***Deliverable 2: Extract and Transform the Wikipedia Data***
Using knowledge of Python, Pandas, the ETL process, and code refactoring, extract and transform the Wikipedia data so you can merge it with the Kaggle metadata. While extracting the IMDb IDs using a regular expression string and dropping duplicates, use a try-except block to catch errors.

Figure 4:

![Deliverable2wiki_df](https://raw.githubusercontent.com/krismbah/Movies-ETL/main/Deliverable2wiki_df.png)

Figure 5:

![Deliverable2wiki_df_columns](https://raw.githubusercontent.com/krismbah/Movies-ETL/main/Deliverable2wiki_df_columns.png)


***Deliverable 3: Extract and Transform the Kaggle data***
Using knowledge of Python, Pandas, the ETL process, and code refactoring, extract and transform the Kaggle metadata and MovieLens rating data, then convert the transformed data into separate DataFrames. Then, you’ll merge the Kaggle metadata DataFrame with the Wikipedia movies DataFrame to create the movies_df DataFrame. Finally, you’ll merge the MovieLens rating data DataFrame with the movies_df DataFrame to create the movies_with_ratings_df.

Figure 6:

![Deliverable3wiki_df](https://raw.githubusercontent.com/krismbah/Movies-ETL/main/Deliverable3wiki_df.png)

Figure 7:

![Deliverable3ratings_df](https://raw.githubusercontent.com/krismbah/Movies-ETL/main/Deliverable3ratings_df.png)

Figure 8:

![Deliverable3movies_df](https://raw.githubusercontent.com/krismbah/Movies-ETL/main/Deliverable3movies_df.png)


***Deliverable 4: Create the Movie Database***
Use knowledge of Python, Pandas, the ETL process, code refactoring, and PostgreSQL to add the movies_df DataFrame and MovieLens rating CSV data to a SQL database.

Figure 9:

![Deliverable4ETL](https://raw.githubusercontent.com/krismbah/Movies-ETL/main/Deliverable4ETL.png)

Figure 10:

![movies_query](https://raw.githubusercontent.com/krismbah/Movies-ETL/main/movies_query.png)

Figure 11:

![ratings_query](https://raw.githubusercontent.com/krismbah/Movies-ETL/main/ratings_query.png)


## Summary

To summarize, the following tasks were made to help Britta clean the data and perform an ETL:

1. A set of 2000 random latitude and longitude cominations were generated and added to a list.
2. A request for Open Weather Map's API was run for each of those cities and data was parsed regarding max temperature, humidity, cloudiness, wind speed, country, and weather description.
3. 703 rows of data were generated and converted to a Pandas DataFrame. This dataframe then was used to create a csv file.
4. The csv file was imported and beta testers were prompted to chose a minimum and maximum location temperature of cities for vacation. The following cities were then created into a dataframe of preferred cities. The data was cleaned of rows with missing data.
5. A request for Google's API was run for each of those cities to search for hotels with 5000 meters.
6. The aforementioned process generated 414 cities. The data was created into a dataframe. Locations without a hotel name were removed.
7. The aforementioned dataframe was used to generate a csv.
8. A Google map with a marker layer was generated.
9. The aforementioned csv of vaction cities was then used to create a vaction dataframe.
10. Four cities from the map of the dataframe were picked to create a vacation itinerary route to travel between the four cities.
11. A direction layer map using the start and end latitude-longitude pairs was created. Mode of travel chosen was "Bicycling".
12. A marker layer map between the four cities was created and used to combine the four city DataFrames into one DataFrame with the concat() function.
13. Maps of the bicycling route between the four cities and a map of the region were created.
