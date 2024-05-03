# CHAPTER 2 

# Understanding Data 

This chapter will focus on Understand Domain 1.0:
* Data Concepts and Environments
* Compare and contrast different data types
* Compare and contrast common data structures and file formats

for one to understand data types one needs to understand data elements.

# DATA ELEMENTS
A data element is an attribute about a person, place, or thing containing data within a range of values. Data elements also describe characteristics of activities, including orders, transactions, and events. 

example of data elements 
![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/06376ecc-cb78-4f1a-8077-b018eecd22a0)

# Tabular Data

Tabular data is data organized into a table, made up of columns and rows. A table represents information about a single topic. Each column represents a uniquely named field within a table, also called a variable, about a single characteristic. The contents of each column contain values for the data element as defined by the column header.

# Structured Data Types
Structured data is like a well-organized spreadsheet. Imagine a table with rows and columns, where each column has a clear heading defining the type of data it contains (like names, dates, or prices). This makes structured data easy for computers to understand and work with, just like it's easy for us to read and analyze information in a spreadsheet.

# most common data types that give structured data its structure.

# character 

This data type acts like a filter for data entry, ensuring only valid characters are entered. These characters can be letters, numbers, or symbols from your keyboard. There are different character data types available, each with its own limit on the number of characters allowed.

# Alphanumeric

Alphanumeric data type is your go-to for storing text that combines letters and numbers. It's the most common type for character data. Imagine product codes (SKUs) in retail stores. These codes often mix letters representing brands or styles with numbers indicating sizes or variations. The alphanumeric data type ensures you can store these SKUs effectively, allowing you to track inventory across different systems.

Example 
![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/0556a37f-4773-4874-b1ce-f309c0022cd8)
# NEED TO GO OVER FROM HERE DONT UNDERSTAND AS YET



# Unstructured Data Types
Unstructured data types refer to information that doesn't have a predefined format or organization. Unlike the neat rows and columns of structured data (like spreadsheets), unstructured data is more like a messy attic filled with all sorts of things.

Examples of unstructured data include digital images, audio recordings, video recordings, and open-ended survey responses. Analyzing unstructured data creates a wealth of information and insight. Many people have camera-enabled smartphones, and using video for conversations and meetings is commonplace. To capture and analyze unstructured data, we make use of data types designed explicitly for that purpose

![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/fb1711f0-cad1-4e17-bdc8-04449340f0e3)


# Categories of Data

The world of data isn't as clear-cut as structured vs unstructured. Semi-structured data bridges the gap between those two categories.

Imagine a spectrum: on one end, you have highly organized data in tables (structured). On the other end, you have completely free-form information like videos (unstructured). Semi-structured data sits in the middle. It has some organization, but not a rigid structure like a spreadsheet. Emails or social media posts are good examples. They might have elements like sender, recipient, or timestamps, but the content itself is more flexible. This makes semi-structured data easier to work with than completely unstructured data, but it still requires some wrangling before analysis.

explanation of the distinction between quantitative and qualitative data!

* Quantitative data: Expressed in numbers and represents measurable qualities. It answers questions like "how many" or "how much." (e.g., height, weight, temperature)
* Qualitative data: Descriptive information, often in the form of text. It describes characteristics or qualities and answers questions like "why" or "what." (e.g., pet name, color, customer opinion)

  explanation of discrete and continuous data

# Discrete data:
is like counting whole things. You can't have parts of things, so it applies to things you can count (e.g., number of pets, number of chickens in whole or half portions).
  
# Continuous data
 is for measurements that can have any value within a range, often using decimals (e.g., height, weight).
Even though age is continuous (technically has infinite values), we often treat it as discrete by using whole years.

This distinction between discrete and continuous data is important for understanding how we analyze and interpret numbers.


Dimensional modeling helps us organize data for analysis! Here's the gist:

It separates data into two main tables:
# Fact tables:
Store the quantitative measurements we care about (e.g., appointment data for a veterinary clinic).
# Dimension tables: 
Provide context for the facts, describing "who, what, when, where, why" (e.g., details on veterinarians, owners, procedures, and pets in the appointment example).

Imagine a fact table like a big basket holding the key data points, and the dimension tables act like labels stuck on the basket, giving details about the contents. This structure makes it easier to analyze the data and answer questions.


  ![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/f295e27d-0b7d-42d3-84d7-dcfa679a5ad4)


# Dimenstional data:
* it is aall about organizing details arouna a central theme.
* It grou[s individual details(attributes) about a specific subject
* Each group, like the "pets" table with pet info, is called a dimension

  Imagine a filing cabinet for a vet clinic. Each drawer (dimension) holds details about a specific aspect, like pets (their breed, age, etc.) or owners (their contact information). When you combine information from these drawers (dimensions) with the main patient file (fact table), you get a complete picture for each appointment.
  
# Common Data Structures

* Structured data needs a neat and tidy filing system (think database schemas) to be useful.
* Unstructured data, like emails and videos, is more flexible in how it's stored.
Analysts juggle multiple tools, so smooth data exchange (interoperability) is crucial.
To boost efficiency, standardized practices have emerged for both structured and unstructured data organization.

Tabular data is structured data, with values stored in a consistent, defined manner, organized into columns and rows. Data is consistent when all entries in a column contain the same type of value. This method of organization facilitates aggregation

![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/2666c426-0165-448d-b2b1-ca28edbc0662)

# Unstructured Data

* What it is: Descriptive information like images, text, audio/video (qualitative).
  
* Key characteristics: Highly variable and lacks a predefined structure.
  
* Storage: Different from structured data due to its variety.
  
* Importance: Huge potential for businesses to extract value (over 90% according to Forbes).
  
* Example: Machine data (digital footprints from devices) is a goldmine of unstructured data.
  
* Storage Technologies: Utilize unique identifiers to link data elements.

Unstructured data might seem messy, but it holds immense value if we can unlock it!

* Object storage facilitates the storage of unstructured data. The key-value concept underpins the design of object storage. The key is a unique identifier, and the value is the unstructured data itself.

the key is the filename, and the value is the contents of the file itself. Note that in the bellow figure, each file is of a different type. The word document.docx is a Microsoft Word file, textfile.txt contains plain-text data, and the png image.png and lp_image-8.jpeg objects are digital images.

![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/302f40d1-6b77-44ad-a68d-8a94a2475135)


To access the contents of a file, you need to know its key

![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/c6a019fc-e53b-4bf5-ab58-ac5f2fb7688e)

# Semi-Structured Data

* Think of it as: Structured, but not rigid like a table (tabular).
Example: Emails have a sender, recipient, subject, etc. (structured), but the body and attachments can be anything (unstructured).

* Benefits: Easier to work with than completely unstructured data.
  
* Key feature: Uses tags or separators to add context to the data.
Semi-structured data provides some organization without being as strict as a traditional database.

# Common File Formats

* Different file formats exist to store and exchange data efficiently between various tools and applications.
  
* Some formats have become widely accepted standards, and data analysts should be familiar with these for various tasks.

# Text Files

* Super common data format for computers.
* Plain text only (letters, numbers, symbols).
* No fancy formatting or images.
* Opens easily on pretty much any device (PC, Mac, Linux).
* Also called "flat files".

A unique character known as a delimiter 

* Delimiters: Special characters used to separate data points in text files (like commas or tabs).
  
* Why? Makes structured data transmission easier within plain text files.
  
* Common Delimiters: Comma (CSV) and tab (TSV) are widely accepted standards.
  
* Benefits: Many software programs and coding languages can easily read and write these delimited text files.
  
Exporting as CSV or TSV



![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/7f679b11-91c8-4daa-9e2f-fb61faf02f15)

![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/2d667fa4-f0c8-41c6-896a-1ed8945b251d)

![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/1b449707-19cb-4038-92d1-5bf522d84d59)

![image](https://github.com/SesethuPotye/DATA-ANALYTICS/assets/162969678/015c6617-198c-4f2f-9411-dbd56d1fe3c3)


# JavaScript Object Notation

* What it is: A popular file format for storing data in a human-readable and machine-friendly way.
  
Key features:
* Open standard and lightweight.
* Easy for both humans and computers to understand and process.
* Supported by many programming languages (Python, R, Go, etc.).
  
* Uses: Often used to exchange data between applications or store configuration settings.

# Extensible Markup Language (XML)


Extensible Markup Language (XML) is a markup language that facilitates structuring data in a text file. While conceptually similar to JSON, XML incurs more overhead because it makes extensive use of tags. Tags describe a data element and enclose each value for each data element. While these tags help readability, they add a significant amount of overhead.

# HyperText Markup Language (HTML)
HyperText Markup Language (HTML) is a markup language for documents designed to be displayed in a web browser. HTML pages serve as the foundation for how people interact with the World Wide Web. Similar to XML, HTML is a tag-based language


Most people interact with HTML as interpreted by a web browser. HTML has become increasingly sophisticated over the years, with the ability for developers to create web pages that dynamically display content, adjust to different screen sizes, and play videos. Among the many tags that HTML supports is the image tag. It would be possible to display a picture of each pet on the table using image tags



SUMMARY 
Here's a summary of the key points about data types and formats:

Choosing Data Types:

* The type of data (numbers, text, dates, etc.) you're working with influences how you store and analyze it.
* Choosing the right data type (discrete, continuous, categorical) improves data quality.
  
# Structured Data:

* Think of data organized in tables with rows and columns.
* Common formats for structured data include:
  
CSV (Comma-Separated Values): Simple text files for data exchange.
JSON (JavaScript Object Notation): Flexible and human-readable format for structured data.
XML (Extensible Markup Language): Powerful format for complex data structures and metadata.

# Unstructured Data:

* Data like images, audio, and video doesn't have a predefined structure.
Web Data:

* HTML (Hypertext Markup Language) is the standard for structuring web pages, allowing programmatic interaction with data.
Key Takeaway:

Understanding data types and formats is essential for data analysts to effectively work with and analyze information.

# 1. Consider the values of what you will store before selecting data types. 

# Numbers:
* Decimals: Use a numeric data type.
* Whole numbers: Use an integer data type.
* Avoid currency-specific types: They can cause calculation issues.
# Text:
* Use the alphanumeric data type.
# Dates:
* Choose a data type that includes time if needed.
# Non-textual data (audio, video, images): Use a BLOB (Binary Large Object) data type.
By choosing the right data type, you ensure your data is stored efficiently and avoids errors during calculations or analysis.

# . Know that you can format data after storing it.

2. Know that you can format data after storing it.

# Data types:

* Decide how data is stored (e.g., numbers with decimals, whole numbers only).
# Data formatting:

* Controls how data is presented for people (e.g., show all decimals, round to two, display as currency).
Think of it like this:

# Data type:
* is like filing a document in a specific folder (e.g., "numbers" folder).

# Formatting: 
* is like decorating the folder label (e.g., show two decimal places on the label).

# 3. Consider the absolute limits of values that you will use before selecting data types.
When selecting data types, consider the range of values that a data element can contain. Suppose the values need to fall within a given, defined range. In that case, you must select a data element that can support discrete data. If the data element's range is unknown, a data element that supports continuous data is necessary.

4. Explain the differences between structured and unstructured data

# Structured data: 
Highly organized information like a table.

* Think "rectangular": Rows and columns with consistent data types in each column.
* Easier to analyze using traditional techniques.

# Unstructured data:
Lacks a predefined structure, like text documents or images.

* Doesn't fit neatly into columns and rows.
* Requires more advanced analysis techniques to find patterns.
* 
Imagine data as Legos. Structured data is like pre-built sets with clear instructions. Unstructured data is like a box of random Legos - it takes more effort to build something meaningful.

# 5. Understand the differences in common file formats

# Structured data, easy exchange:
These formats make data readable and transferable between different tools.

# Delimiters: 
Special characters (like commas) separate data points in text files.
# CSV (Comma-Separated Values):
A popular format using commas as delimiters, good for simple data exchange.
XML and JSON: For complex data structures and additional information (metadata) about data.
# JSON preferred: 
More lightweight and easier to use compared to XML.
These file formats help organize and share data efficiently, especially when dealing with structured information.


















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

