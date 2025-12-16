  # Intro to Pandas and DataFrames
  
  Pandas is crucial for tasks like data cleaning, transformation, and analysis. It provides fast and efficient data structures, making it an ideal choice for data science and analytics.
  <br>
  Additionally, Pandas even supports in-built time-series functionalities that render intricate date-related calculations effortless, amplifying its value in real-world data science applications.
  
  #### Benefits:
  - Performance: Faster and more efficient than Excel
  - Flexibility: More customised data manipulation than SQL
  - Python Ecosystem: Broader versatility compared to R, compatibility with other Data Analytic libraries in Python (like NumPy, SciPy, Matplotlib, and Scikit-Learn)
  - Large Datasets: Overcomes Excel's data size limitations
  - Automation: Enables reproducible data pipelines
  - Built-in Features: Native data cleaning and time-series support
  
  Installing Pandas: Installing Pandas is as simple as running a pip install pandas command in your terminal. Importing the Library: To use Pandas, you must import it first. The common alias for Pandas is pd.

## Lession 4 : Data manipulation and subsetting


  
  #### Data Structures:
  - Pandas offers two primary data structures, including series and dataframe.
  - One-Dimensional: A Series is like a single column in a spreadsheet, capable of holding various data types.
  - Series have an 'index' for axis labels, which can be numeric or custom labels.
  - Similar to NumPy arrays, Series support various operations like reindexing and aggregation.
  - Create a Series from Python lists, dictionaries, or NumPy arrays.
  
  <img width="1318" height="702" alt="image" src="https://github.com/user-attachments/assets/c372da8b-b096-4869-b25e-7ea399212bce" />
  
  
  #### DataFrames
  DataFrames are a two-dimensional structure resembling a SQL table consisting of rows and columns with different data types. They allow for quick data reshaping, pivoting, and manipulation, making them ideal for data processing and analysis.
  
  - DataFrames have both row and column labels, where each column is a Series.
  
    <img width="1502" height="1164" alt="image" src="https://github.com/user-attachments/assets/7fab6be2-a2b0-4f1c-a7fb-e2bb9d3f4d3c" />
  
  ## Lession 2: Data import and export
  
  ##### CSV
  Reading CSV: Use pd.read_csv() to read CSV files quickly. This is particularly useful when dealing with plain text files that are delimited by commas or other characters. This is essential when you are working with business data often stored in Excel spreadsheets.
  <br>
  To write to a CSV, use df.to_csv(). Useful for sharing data in a universally accepted format.
  
  ##### SQL Databases
  SQL databases can be read directly using pd.read_sql() and a connection object. This is ideal when your data is stored in a relational database and you want to pull it into Pandas for further analysis.
  <br>
  Save back to Excel using df.to_excel(). This will make it perfect for reports that can be further edited or viewed in Excel.
  
  ##### SQL Databases
  
  The pandas library in Python provides a function called read_excel() that allows you to import data from Excel files into your Python environment.
  This functionality is particularly useful when working with structured data, as it allows you to leverage the powerful data manipulation capabilities of pandas directly on your Excel data.
  <br>
  To store data to an SQL database (or other relational databases), you can use df.to_sql() as follows:
  
  <img width="1172" height="402" alt="image" src="https://github.com/user-attachments/assets/abf5b9c2-2828-4926-a283-399ebb161820" />
  
  
  #### Activity 
  
  - Download a sample CSV file (you can create a simple one or find a public dataset).
  - Use Pandas to read the CSV file and create a DataFrame.
  - Display the first few rows of the DataFrame to verify the import.
  
  
  ## Lession 3 : Data Cleaning in phyton
  
  Data cleaning is the process of preparing your data for analysis by removing or modifying data that is incorrect, incomplete, irrelevant, duplicated, or improperly formatted. This is crucial because dirty data can lead to false conclusions and misinterpretations, including:
  
  - Missing Values
  - Inconsistent Formats
  - Duplicate Data
  - Outliers
  
  - Data consistency: Ensures uniform data structure, facilitating subsequent operations.
  - Easier analysis: Simplifies filtering and classification of records with missing        values.
  - Reability : Makes the DataFrame more human-readable by replacing NaN with a meaningful   placeholder.
  - External Operations: Facilitates integration with systems that can't handle missing     values.
  - Model Training : Preps data for machine learning models that require non-null values.
  - Debugging : Prevents missing values from causing errors during data transformations.
  - Data Export: Ensures that the DataFrame can be cleanly exported to other formats.
  
  ### Missing Values
  
  The fillna() function replaces any NaN values with 'Unknown'. The argument inplace=True allows us to operate directly on the dataframe without having to assign the output to df.
  
  ### Cation!
  - It also fails to preserve the correlation structure between variables, potentially distorting the data's overall structure. 
  
  - Additionally, it ignores patterns in the data that more sophisticated imputation methods could leverage. 
  
  - Consequently, the changed dataset may become less trustworthy for individual entries, impacting the reliability of subsequent analyses or models. 
  
  - This approach is more suitable for general trends rather than precise predictions for individual cases. 
  
  
  ###  Correcting data formats
  
  Often, data might not be correctly interpreted in the right format by Pandas. When we load data from a source e.g. a CSV, pandas tries to infer the data type e.g. assigning a type to a column such as int, float or object.
  
  <img width="1488" height="450" alt="image" src="https://github.com/user-attachments/assets/9f6f4df0-fc7e-43c7-9d8d-3ff7201492af" />
  
  ### Technique 3: Dealing with duplicates
  
  Removing duplicates in data is good practice because it ensures data integrity, improves analysis accuracy, and prevents the skewing of results in subsequent statistical or machine learning models.
  
  The drop_duplicates() function removes rows that have the same values in specified columns (Name and Age). The subset parameter specifies which columns to consider. The keep='first' parameter indicates that we'll keep the first occurrence and remove any subsequent duplicate.
  
  <img width="1500" height="458" alt="image" src="https://github.com/user-attachments/assets/64e6986d-e939-4467-b4b6-bc08ac2dd28c" />
  
  <br>
  
  ### Technique 4: Handling Outliers
  
  Removing outliers from a dataset is often done to improve the accuracy and reliability of statistical analyses and machine learning models by focusing on data that represents the underlying trend or distribution.
  
  For example, if one student scores 1000 on a test out of 100, that single score could wrongly suggest everyone did much better than they actually did if we took an average of the marks.
  
  It is good practice to first identify and examine the outliers as they may have something in common e.g. maybe a formatting error has led to this value being an outlier. You can do this using the following code:
  
  <img width="1366" height="428" alt="image" src="https://github.com/user-attachments/assets/e1b611bc-85e6-4364-bd7b-efe301130a1f" />
  
  ** looking for anyone scoring over 100 as the test can score only up to 100! 
  
  ### Activity 
  
  - Handling missing values
  Remove rows with missing values using dropna().
  Replace missing values with appropriate strategies (e.g., mean, median, mode) using fillna().
  
  - Correcting data formats
  Convert columns to the correct data types (e.g., dates, numeric values).
  
  - Identify and remove duplicate rows using drop_duplicates().
  
  - Detect outliers using statistical methods (e.g., Z-score, IQR).
  Decide whether to keep or remove outliers.
  
  
  import pandas as pd
  import numpy as np
  
  
          # Create a sample DataFrame with missing values, duplicates, and outliers
  data = {
  'ID': [1, 2, 3, 4, 5, 2, 6],
  'Date': ['2022-01-01', '2022-02-15', '2022-03-20', '2022-04-10', '2022-05-05', '2022-02-15', '2022-06-30'],
  'Sales': [1000, 1500, np.nan, 2000, 1800, 1500, 2500]
  }
  df = pd.DataFrame(data)
  
  # Handling missing values
  df.dropna(inplace=True)
  # df.fillna(df.mean(), inplace=True) # Uncomment to replace missing values with mean
  
  # Correcting data formats
  df['Date'] = pd.to_datetime(df['Date'])
  
  # Dealing with duplicates
  df.drop_duplicates(subset=['ID'], keep='first', inplace=True)
  
  # Handling outliers (use appropriate method)
  
  print(df)
