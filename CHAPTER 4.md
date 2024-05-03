
# Chapter 4(DATA QUALITY)

WHAT THIS CHAPTER COVERS 

* Understanding the challenges of data quality. 
* Identifying common reasons for cleansing and profiling datasets.
* Executing data manipulation techniques. 
* Applying data quality control concepts.


# Data Quality Challenges
# Duplicate Data

Duplicate data occurs when data representing the same transaction is accidentally duplicated within a system. Suppose you want to open a spreadsheet on your local computer. 
The issue of duplicate data creation, primarily caused by human error.  While systems are designed to prevent duplicates, the best defense is to stop them before they happen.  The example highlights how a simple action like double-clicking can lead to unintended duplicates.  The solution? Visual warnings that alert users of the potential for duplicate entries before they confirm an action.

Duclication data resolution process 

![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/f96e1973-dd41-469a-a093-b8281c03d137)

# HOW TO RESOVE DUPLICATION?

* To resolve duplicate data issues, the company has a duplicate resolution process.
*This process looks for customers with multiple billing addresses, validates the correct address, and updates the Sales database by removing the duplicate record.

# Redundant Data
Redundant data happens when the same data elements exist in multiple places within a system.
* Data redundancy is a function of integrating multiple systems.

# ILLUSTRATION OF TWO TRANSECTIONAL SYSTEEM FEEDING A SING DATA WAREHOUSE

![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/776052f4-eed5-4b22-a2b1-03ca8340c5d2)

* Wayas of resolving redundant data: One approach synchronizes changes to shared data elements between the Accounting and Sales systems.
  
  illustration of resolving redundancy with an integrated ETL process

  
![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/a45cf6f4-4afa-4cb9-b3b0-ba9dfe63796b)

* Another root cause of data redundancy is an inappropriate database design
  
# Missing Values
* Missing values occur when you expect an attribute to contain data but nothing is there.
* Missing values are also known as null values.
* A null value is the absence of a value.
* A null is not a space, blank, or other character. There are situations when allowing nulls makes sense. 


# Invalid Data

* Invalid data are values outside the valid range for a given attribute.
* An invalid value violates a business rule instead of having an incorrect data type
* One has to understand the context of a system to determine whether or not a value is invalid
* Text data is more complex. One thing that leads to invalid character data is an absence of referential integrity within a database
* If two tables have a relationship but no foreign keys, the conditions for invalid character data exist
  
# Nonparametric Data

* Nonparametric data is data collected from categorical variables,
* sometimes they have a rank order associated with them

# Data Outliers

* A data outlier is a value that differs significantly from other observations in a dataset.

# Specification Mismatch

* A specification describes the target value for a component.
* A specification mismatch occurs when an individual component's characteristics are beyond the range of acceptable values.

* When data is invalid, it has values that fall outside a given range. 
* On the other hand, a specification mismatch occurs when data does not conform to its destination data type. 

* If the destination column is numeric and you have text data, you'll end up with a specification mismatch. 
* To resolve this mismatch, you must validate that the inbound data consistently maps to its target data type.


# Data Type Validation

Data type validation ensures that values in a dataset have a consistent data type. 

* Programming languages, including SQL, Python, and R, all have data type validation functions
* Use these functions to validate the data type for each column in a data file before attempting a database load.

* It is the best to detect and remediate data type issues as early as possible to ensure data is ready for analysis

# Data Manipulation Techniques
Recoding Data

* Recoding data is a technique you can use to map original values for a variable into new values to facilitate analysis.
* Recoding groups data into multiple categories, creating a categorical variable.
* A categorical variable is either nominal or ordinal.
* Nominal variables are any variable with two or more categories where there is no natural order of the categories, like hair color or eye color.
* Ordinal variables are categories with an inherent rank. For example, T-shirt size is an example of an ordinal variable, as sizes come in small, medium, large, and extra-large. Variable values fit into a fixed number of categories, similar to how lookup tables work

# Derived Variables

* derived variable is a new variable resulting from a calculation on an existing variable.
* categorical variable is an example of a derived variable.
* However, derived variables don't have to be categorical.

# Data Merge

* A data merge uses a common variable to combine multiple datasets with different structures into a single dataset. 
* Merging data improves data quality by adding new variables to your existing data.
* Additional variables make for a richer dataset, which positively impacts the quality of your analysis.
* Since a data merge adds columns to a dataset, merging gives you additional data about a specific observation.
* ETL processes commonly append data while transforming data for use in analytical environment.
  
illustration of merging disparate data

![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/c9080566-97fd-4e9c-b5f3-98442fbba993)



# Data Blending

* Data blending combines multiple sources of data into a single dataset at the reporting layer.
*  While data blending is conceptually similar to the extract, transform, and load process
* Data blending differs from ETL in that it allows an analyst to combine datasets in an ad hoc manner without saving the blended dataset in a relational database.
* Data blending can reduce the burden on IT as it gives analysts the ability to merge data.
  
# Illustratuion showing the traditional ETL workflow, the analyst needs to understand the data warehouse's structure to create a visualization

![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/6a5a9587-67d1-40e3-abab-7b00f807c166)

Diagram illustrating data blending

![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/bba4cac7-a6b6-47c2-9e0a-42be4cb65127)

# Concatenation
Concatenation is the merging of separate variables into a single variable. 
Concatenation is a highly effective technique when dealing with a source system that stores components of a single variable in multiple columns. The need for 
* concatenation frequently occurs when dealing with date and time data. 
* Concatenation is also useful when generating address information.


A diagram showing an example of 

![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/1f687d8a-c098-445d-8501-87156f24b863)

# Data Append

* A data append combines multiple data sources with the same structure, resulting in a new dataset containing all the rows from the original datasets.
* When appending data, you save the result as a new dataset for ongoing analysis.
  
![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/4df1cdf2-463a-4e25-a2ef-7c9c1d89acfa)

# Imputation
* Imputation is a technique for dealing with missing values by replacing them with substitutes. When merging multiple data sources, you may end up with a dataset with many nulls in a given column. If you are collecting sensor data, it is possible to have missing values due to collection or transmission issues.
There are many potential reasons why the data is missing. Perhaps the person is using a smart scale, and the scale lost its network connection. It could be that the person is using a manual scale and forgot to record the value. Another possibility is that the person didn't get on the scale on those four days. Regardless of the reason, the analyst has to decide how to handle the missing data.

# few approaches an analyst can use for imputing values:

* Remove Missing Data:  With this approach, you can remove rows with missing values without impacting the quality of your overall analysis.

* Replace with Zero:  With this approach, you replace missing values with a zero. Whether or not it is appropriate to replace missing data with a zero is contextual. In this case, zero isn't an appropriate value, as a person's weight should be a positive number. In addition, replacing a zero in this case has an extraordinary impact on the overall average weight.
  
* Replace with Overall Average:  Instead of using a zero, you can compute the average Weight value for all rows that have data and then replace the missing Weight values with that calculated average.

* Replace with Most Frequent (Mode):  Alternatively, you can take the most frequently occurring value, called the mode, and use that as the constant.
  
* Closest Value Average:  With this approach, you use the values from the rows before and after the missing values. For example, to replace the missing measurements for 2/13/2021 and 2/14/2021, take the values from 2/12/2021 and 2/15/2021 to compute the average.


# Reduction
When dealing with big data, it is frequently unfeasible and inefficient to manipulate the entire dataset during analysis. Reduction is the process of shrinking an extensive dataset without negatively impacting its analytical value. There are a variety of reduction techniques from which you can choose. Selecting a method depends on the type of data you have and what you are trying to analyze. Dimensionality reduction and numerosity reduction are two techniques for data reduction.

# Dimensionality Reduction

* One reduction technique is dimensionality reduction, which removes attributes from a dataset. Removing attributes reduces the dataset's overall size.
  
# Numerosity Reduction

Another technique is numerosity reduction, which reduces the overall volume of data.
One way to reduce the volume of quantitative data is by creating a histogram. You can create a histogram in Python, R, and many visualization-specific tools. A histogram is a diagram made up of rectangles, or bars, that show how frequently a specific value occurs. When creating a histogram, you can conFigure the width of a rectangle to represent a range of values.


# Aggregation

* Data aggregation is the summarization of raw data for analysis. When you are dealing with billions of individual records, a data summary can help you make sense of it all. 

# Transposition

* Transposing data is when you want to turn rows into columns or columns into rows to facilitate analysis.
* When transposing, each value from a column becomes a new column.
* To organize the data to be beneficial to leadership, you can combine transposition of the FiscalYear column with aggregation of Sales data to generate the table 


If you're curious about how the min-max normalization, consider its mathematical definition:



Let's walk through it using the Height data for AthleteID 1 in Figure 4.32. The first thing you need to do is find the minimum value of the Height column, which is 68. Then, find the maximum value of the Height column, which is 76. For AthleteID 1, the value you want to convert is 71. Once you have these values, you can plug them into the formula as follows:

![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/c442ebc4-1eef-48ef-8a2c-d6d3738ddaba)


Min-max normalization is one of the most straightforward approaches to normalizing data.



# Managing Data Quality

* There are many techniques you can use to improve data quality.
* To be a successful analyst, you must recognize scenarios that create the conditions for data quality issues.
* To help you develop a mental data quality checklist, let's explore various situations and see how different data quality controls apply.


Circumstances to Check for Quality


* There are numerous circumstances where it is appropriate to implement data quality control checks. Every stop along the data life-cycle journey can impact data quality
* Errors during data acquisition, transformation, manipulation, and visualization all contribute to degrading data quality
* You should recognize the types of quality issues that can occur and have an overarching strategy to ensure the quality of your data.

Data Acquisition 

![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/6a0a7cf6-c099-4a33-b20a-ce8ff8da5695)

# Automated Validation

* Data from various sources: Universities (first passage) and analytics environments (second passage) use data from multiple sources, including human-generated data.
  
* Human input and errors: Human interaction with data entry systems can introduce errors.
  
* Data validation: Automating data validation checks is crucial to prevent these errors from impacting analysis. This involves ensuring data types match and verifying the expected number of data points.
  
* Benefits: Data validation safeguards data quality, leading to more reliable results in student success analysis (first passage) or any other analytics application (second passage).



# Data Quality Dimensions


* It is essential to consider multiple attributes of data when considering its quality. Six dimensions to take into account when assessing data quality are accuracy, completeness, consistency, timeliness, uniqueness, and validity. Understanding these dimensions and how they are related will help you improve data quality.

![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/80a0719a-04ce-4132-8173-2290b7c56bb1)

# Chapter 6 : DATA ANALYTICS TOOLS

* Spreadsheets: These are like electronic tables where you can organize data in rows and columns. They are user-friendly and great for basic data manipulation and calculations. Examples include Microsoft Excel and Google Sheets.

* Programming Languages: For more complex tasks, data analysts and scientists often use programming languages like R and Python. These languages allow for more in-depth analysis and customization of data manipulation.

* SQL (Structured Query Language): This is the language used to interact with databases. It allows users to retrieve, insert, update, and delete data stored in relational databases.

* Statistical Packages: These are specialized software programs designed for advanced statistical analysis. Examples include IBM SPSS, Stata, and Minitab. They offer a wide range of statistical tests, data visualization tools, and functionalities for tasks like hypothesis testing and regression analysis.

* Machine Learning Tools: These tools help automate the process of building models that can learn from data and make predictions. Examples include IBM SPSS Modeler and RapidMiner. They allow users to build and train various machine learning models visually, without necessarily needing to write code.

* Analytics Suites: These are comprehensive platforms that provide a complete environment for data analysis. They offer functionalities for data ingestion, cleaning, exploration, visualization, modeling, and reporting. Examples include IBM Cognos, Microsoft Power BI, and Domo.

* Cloud-Based Business Intelligence (BI) Tools: These tools leverage the cloud's scalability and flexibility for data analysis. Examples include AWS QuickSight and Tableau. They offer user-friendly interfaces for data exploration, visualization, and collaboration, often with pay-as-you-go pricing models.

* Data Visualization Tools: These tools specialize in creating visually appealing and informative charts, graphs, and other visual representations of data. Tableau and Qlik are popular examples. They allow users to communicate data insights effectively to a wider audience.

Choosing the right data analysis tool depends on the specific needs of the project, the expertise of the users, and the size and complexity of the data. This overview provides a starting point for understanding the various options available.
