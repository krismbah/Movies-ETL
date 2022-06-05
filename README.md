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

1. Create a function to read in the three files and give it a name.
2. Open the Wikipedia JSON file and use the json.load() function to convert the JSON data to raw data.
3. Read in the raw Wikipedia movie data as a Pandas DataFrame.
4. Create a path to the Wikipedia data, the Kaggle metadata, and the MovieLens rating data files.
5. Convert all three files to a DataFrame.
6. Write a list comprehension to iterate through the cleaned wiki movies list.
7. Write a try-except block that will catch errors while extracting the IMDb IDs with a regular expression string and dropping any imdb_id duplicates. If there is an error, capture and print the exception.
8. Write a list comprehension to keep the columns that have non-null values from the DataFrame, then create a wiki_movies_df DataFrame from the list.
9. Create a variable that will hold all the non-null values from the "Box office" column.
10. Convert the box office data created to string values using the lambda and join functions.
11. Write a regular expression to match the six elements of form_one and form_two of the box office data.
12. Add the code that cleans the box office column in the wiki_movies_df DataFrame using the form_one and form_two lists.
13. Add code that cleans the "budget" column in the wiki_movies_df DataFrame.
14. Add code that cleans the "release" column in the wiki_movies_df DataFrame.
15. Add code that cleans the "running time" column in the wiki_movies_df DataFrame.
16. Use the variables provided to create a path to the Wikipedia data, the Kaggle metadata, and the MovieLens rating data files.
17. Set the wiki_movies_df equal to the wiki_file variable.
18. Merge the wiki_movies_df DataFrame and the kaggle_metadata DataFrames, then name the new DataFrame, movies_df.
19. Drop unnecessary columns from the movies_df DataFrame.
20. Add the fill_missing_kaggle_data() function that fills in the missing Kaggle data on the movies_df DataFrame.
21. Call the fill_missing_kaggle_data() function with the movies_df DataFrame and the Kaggle and Wikipedia columns to be cleaned as the arguments.
22. Filter the movies_df DataFrame to keep the necessary columns.
23. Rename the columns in the movies_df DataFrame.
24. Transform and merge the ratings DataFrame with the movies_df DataFrame, name the new DataFrame movies_with_ratings_df, then clean the movies_with_ratings_df DataFrame.
25. Use the variables provided to create a path to the Wikipedia data, the Kaggle metadata, and the MovieLens rating data files.
26. Add the code to create the connection to the PostgreSQL database, then add the movies_df DataFrame to a SQL database.
27. Add the code that prints out the elapsed time to import each row.
28. Run the program.
29. After the program has finished, run a query on the PostgreSQL database that retreives the number of rows for the movies and ratings tables.
