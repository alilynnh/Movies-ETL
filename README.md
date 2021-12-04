# ETL
## Background
The current project was carried out for the worlds largest online retailer Amazing Prime. The organization has decided to sponsor a "hackathon" in which participants will try to predict which low budget movies being released will become popular. The results of the hackathon will give Amazing Prime insight into which streaming rights should be puchased.

## Purpose
Amazing Prime requires a dataset to be created for the hackathon event. The data for the dataset came from a scrape of Wikipedia for all movies released since 1990, and rating data from the MovieLens website. In order to build the datasets, the following procedures were executed:

- Data was **extracted** from the two data sources   
- The extracted data was **transformed** into one clean dataset  
- The dataset was **loaded** into an SQL table  

## Resources
Data Sources:  
- Wikipedia web scrape JSON file   
- Data from Kaggle.com in two .csv files  

Software:  
- Jupyter Notebook  
- PostgreSQL and PgAdmin  

## Overview of Code

1. [ETL_function_test.ipynb](ETL_function_test.ipynb)  
    - Data is extracted from both data sources  
    - Data is tranformed into Pandas dataframes 
    
2. [ETL_clean_wiki_movies.ipynb](ETL_clean_wiki_movies.ipynb)  
    - Combine alternate language titles into one column
    - Orders columns
    - Uses the function "extract_transform_load" to transform the Wikipedia data   

3. [ETL_clean_kaggle_data.ipynb](ETL_clean_kaggle_data.ipynb)  
    - Addition of tasks to the "extract_transform_load" function which:  
        - Change dataypes 
        - Fill missing values
        - Merge dataframes
        
4. [ETL_create_database.ipynb](ETL_create_database.ipynb)
    - Function now connects to the SQL database
    - Entire ETL process can be completed with the single "extract_transform_load" function
        
    
   
