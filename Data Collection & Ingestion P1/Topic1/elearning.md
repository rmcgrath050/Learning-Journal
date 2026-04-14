# L5DE 6.1 - Introduction to data collection and ingestion

n this lesson, we will delve into the intricacies of Data Collection, the art of gathering raw data from various sources, and Data Ingestion, the science of processing and preparing this data for analysis.

<br>
<img width="578" height="484" alt="image" src="https://github.com/user-attachments/assets/63d9a096-6591-4d68-827e-373347e3cea1" />
<br>
<br>

- Data collection is typically a one-time process, whereas data ingestion can be an ongoing process.
- Data collection can involve manual entry of data, while data ingestion is typically an automated process.
- Data collection can be a time-consuming and resource-intensive process, while data ingestion can be faster and more efficient.
- Data collection is often done in a decentralised manner, while data ingestion can be centralised.

#### ETL
ETL (Extract, Transform, Load) tools are used to extract data from various sources, transform the data into a structured format, and load it into a data warehouse or other data storage system. Examples of ETL tools include Talend, Informatica, and Apache NiFi.

### API
API (Application Programming Interface) integrations allow data to be collected from various sources automatically. APIs can be used to extract data from social media platforms, marketing automation tools, or other third-party applications.

### Log File Analysis Tools
Log file analysis tools can be used to ingest and analyse log files from web servers, applications, or other systems. These tools can help identify errors or performance issues and provide insights into user behaviour.

### Data Preparation Tools
Data preparation tools can be used to clean, transform, and prepare data for analysis. These tools can be used to remove duplicates, fill missing values, or convert data to a standardised format. Examples of data preparation tools include Trifacta, OpenRefine, and Google Data Prep.


### Data Integration Platforms
Data integration platforms allow data to be collected from multiple sources and integrated into a single data store.
These platforms can be used to create a unified view of data from various sources, such as Customer Relationship Management (CRM) systems, marketing automation tools, or social media platforms. Examples of data integration platforms include MuleSoft, Dell Boomi, and Informatica Cloud.


## 2. Understanding dirty data

Data that contains many errors or that hasn’t gone through this data-cleaning process is referred to as dirty data. Cleaning your data is a process of removing errors, outliers, and inconsistencies and ensuring that all your data is in a format that is appropriate for your analysis. This step can feel optional to many junior data professionals but be assured that it is crucial!

<br>

- By not taking the time to clean your dataset, you risk your analysis coming to the wrong conclusion.
- neglecting to clean your dataset could result in analyses that suggest launching the wrong product, hiring the wrong number of employees, investing in the wrong stock, or even charging a client the wrong price!

Types of dirty data include:
- <b>Missiing values</b>, additionally, NaN values or missing cells in a DataFrame may break some Python code, causing a lot of frustration while building your model.
- <b>Outliers</b>, Outliers can be the result of a typo or exceptional circumstances. It is important to differentiate true outliers from informative extreme situations. Outliers can skew your results, ultimately suggesting the wrong answer.
- <b>Duplicates</b>, duplicate data entries can overrepresent one entry in your analysis
- <b> Erroneous data </b> , Sometimes, the values in our data set are simply wrong. You may have the wrong spelling for a customer’s name, the wrong product number, outdated information, or incorrectly labelled data. It can sometimes be challenging to determine if your data is erroneous, which is why verification of your source is so important! Remember, your analysis is only as good as your data!
- <b> Inconsistencies </b> There can be inconsistent data entries, which may point to a typo or an error. Example could be some dates recorded mm/dd/yyyy and others dd/mm/yyyy. Can be also inconsistency in the format of the data!


##### 7 step guide for data exploration:

1. First and foremost, look at the source of your dataset and determine if that source has any bias or agenda that may affect the quality or reliability of your data.

2. Learn the context of your data and any other factors that may have affected your data that aren’t internally accounted for.

3. Determine how many different variables you have. In a table-formatted dataset, the variables are typically the columns, while each data entry is a row.

4. Determine how many different categories within each variable you have. For example, if one of your variables is Type of Fruit, you should have a good idea of how many different types of fruit are represented within this variable.

5. Look at the summary statistics for each column, including the mean, median, variance, and standard deviation.

6. If your dataset is part of a relational database, look closely at the relationships and make sure you understand how the different tables relate to each other.

7. If applicable, use the profiling feature of the pandas library to generate a profile report. This will provide you with valuable information about your dataset.

##### Why data exploration matters:

1. Dataset Understanding, Firstly, doing this will give you a great understanding of the limits of your dataset, which is essential if you are to trust the results of your final analyses.
2. Trend Indetification: Secondly, data exploration can point you in the direction of important trends and analyses you hadn’t considered previously. These have the potential to add to your intended analyses or to present a complicating factor that you need to consider.
3. Revelaing Outliers : This pre-analysis can also be your first clue to where you may have dirty data. This can be the first time you see that outlier, realise there are twice as many categories as there should be, or discover that the data collection method was different last year than it was the year before.

## 3. Cleaning data in Python

Best practices for data cleaning:
- Store raw data separately.
- Use version control and always keep the original.
- Document your data-cleaning decisions and justifications.
- Add comments to your code to explain the purpose of each cleaning step and any assumptions made.
- You will want to make sure your data cleaning efforts are not significantly changing the distribution or introducing any unintended biases.
- If you have a long cleaning process or one that is automated, you may want to maintain a separate document where you record the details of each cleaning step. Details such as the date, the specific action taken, and any issues encountered may be helpful down the road. Remember to store this document somewhere easily accessible, such as in the same project folder as the data or the code. In the case of an automated, regularly updated pipeline, consider having this log be an automatic part of the data cleaning process.
- Identify common data cleaning tasks and encapsulate them into reusable functions. This allows you to apply the same cleaning steps to multiple datasets. This is especially helpful if you have company-specific abbreviations you want to map.


##### Dropping unnecessary columns in a DataFrame

  <img width="636" height="534" alt="image" src="https://github.com/user-attachments/assets/bb49c42e-f978-4f8e-a7a6-4dcaac0bfe1e" />

<br>
<br>

##### Tidying up fields in the data

You can use regex to enforce that the fields are always in the right format, and remove field data that is bogus, as illustrated below. Remember, you can review the lesson on regular expressions from Module 3 to refresh your memory!

<img width="708" height="698" alt="image" src="https://github.com/user-attachments/assets/b4e7e123-d06f-448a-be33-47422237d434" />

<br> 
#####  Cleaning the entire dataset using the `applymap` [use code syntax] function

In certain situations, you will see that the 'dirt' is not localised to one column but is more spread out. There are some instances where it would be helpful to apply a customised function to each cell or element of a DataFrame. `pandas .applymap()` [use code syntax] method is similar to the in-built `map()` [use code syntax] function and simply applies a function to all the elements in a DataFrame.


#####   Renaming columns and skipping rows

Often, the datasets you will work with will have either column names that are not easy to understand, or unimportant information in the first few and/or last rows, such as definitions of the terms in the dataset, or footnotes. In that case, we’d want to rename columns and skip certain rows so that you can drill down to the necessary information with correct and sensible labels.


<img width="676" height="552" alt="image" src="https://github.com/user-attachments/assets/5f4e3ac2-a557-4475-b645-64a0784f2506" />
<br>
<br>
