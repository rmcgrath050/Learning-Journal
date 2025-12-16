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



