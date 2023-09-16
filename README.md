# Cyclistic-Bikeshare-Analysis
LINK: https://public.tableau.com/app/profile/trapti.kapkoti/viz/CyclisticBikeshare-acasestudy/Story1
DATA SOUCE: https://divvy-tripdata.s3.amazonaws.com/index.html
DATA TIMELINE: from AUGUST 2022 to JULY 2023
![image](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/7296b11a-a1ec-4676-ae8c-b9d511e401a9)

## **DATA ANALYSIS**

# Importing Libraries:

The code begins by importing two essential libraries: os and pandas. These libraries provide functions and data structures to work with files and data frames, respectively.

![image](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/7c003b0e-1e58-4af9-aec0-6fb1a9624ba7)


Specifying Directory Path and CSV Files:

The directory_path variable specifies the directory where your CSV files are located. You should replace this with the actual path to your CSV files.

![image](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/b6d2d181-2032-4850-b5a8-e6c40bb18390)

The csv_files list contains the names of the CSV files you want to process. You can add or remove file names as needed.

![image](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/0c8b5eea-5fb7-46ef-b1e2-7f10983b4324)

# Reading and Combining CSV Files:

The code reads each CSV file specified in csv_files, creates a pandas DataFrame for each, and appends them to the dataframes list.

![image](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/90ec4dbb-9667-4939-96fe-88bc86d15743)

After looping through all the files, it concatenates these DataFrames into one large DataFrame called combined_df.

![image](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/26756a62-6fa3-453a-896b-e0135ce3e89c)

# Data Inspection and Cleaning:

The code then performs data inspection and cleaning steps. It checks for duplicate records.

![image](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/476b23fa-0e17-4b0b-aee2-9ee12d795f49)
NO DUPLICATES FOUND


Check for null or missing values in the entire DataFrame

![image](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/916b1171-0c22-4c40-9a79-26d9778ae345)

These values will we taken care of later!

Check Datatypes and later we will change the ones with wrong datatypes

![image](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/aa76727d-d35f-430f-9e82-6caa424aa704)

This code converts into date-time Data type

![image](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/14a06612-0763-4b51-87c0-76886850732e)

Handling missing values by filling with 'Unknown'

![image](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/f948587f-63dc-45fb-b431-4f8ff87e15a1)

RESULT

![image](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/9c13c93b-aa0a-4cd0-8e6e-6414b66bb0de)

# Feature Engineering:

The code extracts information from the date-time column, such as weekdays, ride length in minutes, and month.

EXTRACTING WEEKDAYS INFO

![image](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/bb28fac9-d644-4843-8d37-9a778a2b0814)

EXTRACTING RIDE LENGTH in km INFO 

![image](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/9b4f1b00-0479-492e-8630-274755e58450)

EXTRACTING MONTH INFO

![image](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/b7902dc3-26dc-4d7f-a554-d1a1f1506461)

EXTRACTING TIME OF THE DAY

![image](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/b817950b-d9ce-4b00-8050-ffd1a21611a1)

# Importing Dask Dataframe for Distance Calculation:

It creates a Dask DataFrame from the Pandas DataFrame to perform distance calculation using Geopy.

![image](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/1bc977cc-34c3-4abc-8db7-404f53c6c1e4)

Distance Calculation with Geopy:

The code defines a function calculate_distance to calculate distances between latitude and longitude coordinates using the Geopy library. 

![image](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/3be89885-deb8-4f80-b973-b67028fd47c3)

Merging the Dask DataFrame back into the original Pandas DataFrame based on an index

![image](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/91f3c47c-eeb9-4248-bde4-6a599fc7cbb9)

# Saving the Data:

Finally, the code saves the combined DataFrame to a CSV file named 'combined_df.csv'.

![image](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/1946538c-2949-4510-a743-223dd5f3f663)

ANALYSIS COMPLETED 

## **VISUALIZATION ON TABLEAU**
https://public.tableau.com/app/profile/trapti.kapkoti/viz/CyclisticBikeshare-acasestudy/Story1

Here are some snaps from Dashboard:

![image](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/61aaeb1f-1424-495a-bebf-d59d2f8a9b51)
![image](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/60bef6b0-3e36-4dce-af2f-f98ea85fa987)



















