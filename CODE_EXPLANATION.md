# Cyclistic Bikeshare Analysis

**Project Link**: [Cyclistic Bikeshare Analysis on Tableau](https://public.tableau.com/app/profile/trapti.kapkoti/viz/CyclisticBikeshare-acasestudy/Story1)

**Data Source**: [Divvy Trip Data](https://divvy-tripdata.s3.amazonaws.com/index.html)

**Data Timeline**: August 2022 - July 2023

![Cyclistic Bikeshare](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/7296b11a-a1ec-4676-ae8c-b9d511e401a9)

## Data Analysis

### Importing Libraries

To kick things off, we start by importing two crucial libraries: `os` and `pandas`. These libraries provide the necessary tools for handling files and data frames.

![Importing Libraries](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/7c003b0e-1e58-4af9-aec0-6fb1a9624ba7)

### Specifying Directory Path and CSV Files

We specify the `directory_path` variable to pinpoint the location of your CSV files. Remember to replace it with the actual path to your CSV files.

![Specifying Directory](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/b6d2d181-2032-4850-b5a8-e6c40bb18390)

The `csv_files` list contains the names of the CSV files you want to process. You can add or remove file names as needed.

![CSV Files](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/0c8b5eea-5fb7-46ef-b1e2-7f10983b4324)

### Reading and Combining CSV Files

We read each CSV file specified in `csv_files`, create a pandas DataFrame for each, and then append them to the `dataframes` list.

![Read and Combine CSV Files](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/90ec4dbb-9667-4939-96fe-88bc86d15743)

After processing all the files, we concatenate these DataFrames into one large DataFrame called `combined_df`.

![Concatenate DataFrames](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/26756a62-6fa3-453a-896b-e0135ce3e89c)

### Data Inspection and Cleaning

Next, we perform data inspection and cleaning. This involves checking for duplicate records.

![Check for Duplicates](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/476b23fa-0e17-4b0b-aee2-9ee12d795f49)
*No duplicates found*

We also check for null or missing values in the entire DataFrame.

![Check for Missing Values](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/916b1171-0c22-4c40-9a79-26d9778ae345)
*These values will be handled later.*

Furthermore, we inspect data types and make necessary corrections.

![Check Data Types](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/aa76727d-d35f-430f-9e82-6caa424aa704)

We also convert date-time columns to the appropriate data type.

![Convert Date-Time Columns](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/14a06612-0763-4b51-87c0-76886850732e)

Finally, we handle missing values by filling them with 'Unknown'.

![Handle Missing Values](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/f948587f-63dc-45fb-b431-4f8ff87e15a1)

### Feature Engineering

We extract valuable information from the date-time column, such as weekdays, ride length in minutes, and the month.

#### Extracting Weekdays Info

![Weekdays Info](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/bb28fac9-d644-4843-8d37-9a778a2b0814)

#### Extracting Ride Length Info (in km)

![Ride Length Info](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/9b4f1b00-0479-492e-8630-274755e58450)

#### Extracting Month Info

![Month Info](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/b7902dc3-26dc-4d7f-a554-d1a1f1506461)

#### Extracting Time of the Day

![Time of the Day](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/b817950b-d9ce-4b00-8050-ffd1a21611a1)

### Importing Dask DataFrame for Distance Calculation

We introduce a Dask DataFrame derived from the Pandas DataFrame to calculate distances using Geopy.

![Dask DataFrame](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/1bc977cc-34c3-4abc-8db7-404f53c6c1e4)

### Distance Calculation with Geopy

We define a function called `calculate_distance` for computing distances between latitude and longitude coordinates using the Geopy library.

![Distance Calculation](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/3be89885-deb8-4f80-b973-b67028fd47c3)

Then, we merge the Dask DataFrame back into the original Pandas DataFrame based on an index.

![Merge DataFrames](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/91f3c47c-eeb9-4248-bde4-6a599fc7cbb9)

### Saving the Data

Finally, we save the combined DataFrame to a CSV file named 'combined_df.csv'.

![Save Data](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/1946538c-2949-4510-a743-223dd5f3f663)

**Analysis Completed**

## Visualization on Tableau

Explore the interactive visualizations and insights on [Tableau]([https://public.tableau.com/app/profile/trapti.kapkoti](https://public.tableau.com/app/profile/trapti.kapkoti)
