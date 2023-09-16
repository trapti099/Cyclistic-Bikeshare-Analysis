# Cyclistic-Bikeshare-Analysis
Importing Libraries:

The code begins by importing two essential libraries: os and pandas. These libraries provide functions and data structures to work with files and data frames, respectively.

![image](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/7c003b0e-1e58-4af9-aec0-6fb1a9624ba7)


Specifying Directory Path and CSV Files:

The directory_path variable specifies the directory where your CSV files are located. You should replace this with the actual path to your CSV files.

![image](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/b6d2d181-2032-4850-b5a8-e6c40bb18390)

The csv_files list contains the names of the CSV files you want to process. You can add or remove file names as needed.

![image](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/0c8b5eea-5fb7-46ef-b1e2-7f10983b4324)

Reading and Combining CSV Files:
The code reads each CSV file specified in csv_files, creates a pandas DataFrame for each, and appends them to the dataframes list.

![image](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/90ec4dbb-9667-4939-96fe-88bc86d15743)

After looping through all the files, it concatenates these DataFrames into one large DataFrame called combined_df.

![image](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/26756a62-6fa3-453a-896b-e0135ce3e89c)

Data Inspection and Cleaning:
The code then performs data inspection and cleaning steps. It checks for duplicate records.

![image](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/476b23fa-0e17-4b0b-aee2-9ee12d795f49)
NO DUPLICATES FOUND


Check for null or missing values in the entire DataFrame

![image](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/916b1171-0c22-4c40-9a79-26d9778ae345)

These values will we taken care of later!

Check Datatypes and later we will change the ones with wrong datatypes

![image](https://github.com/trapti099/Cyclistic-Bikeshare-Analysis/assets/63699608/aa76727d-d35f-430f-9e82-6caa424aa704)








