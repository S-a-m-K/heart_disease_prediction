<h1>Heart Disease Prediction</h1> 

**Author: Samuel Kleger**  
**Date: 2024-09-20**


# **Introduction**

This is a data set used to predict heart disease.

The data is from 1988 and consists of four databases: Cleveland, Hungary, Switzerland, and Long Beach V. It contains 76 attributes, including the predicted attribute, but all published experiments refer to using a subset of 14 of them.

---

#### Table of Content

...

---

# **Ask**

### **Buisness Task**

Explore the dataset and gain insights that could contribute to improved health outcomes and preventive measures.

### **Analysis Questions**

- Is there a relationship between the different risk factors and heart attack outcomes?
- Can the insights found be used in the future to reduce the heart attack risk of this population?

# **Prepare**


### **Data Source**

This dataset comes from the University of California Irvine data repository and is used to predict heart disease. This database contains 76 attributes, but all published experiments involve using a subset of 14 of them. Notably, the Cleveland database is the only one used by ML researchers to date. One file has been "processed," that being the one with the Cleveland database. All four unprocessed files are also present in this directory.

A stripped down version of the dataset is available on [kaggle](https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset/data) for public use.

**Additional information:**

If a coronary artery was narrowed by more than 50%, they were assigned heart disease.

Patients' names and social security numbers were removed from the database and replaced with dummy values.

**Source**: Data provided by the University of California Irvine

**License**: [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/legalcode)

**Type**: CSV

**Format**: Long Data

**Duration**: Data is from 1988

<div style="margin-bottom: 40px;">

</div>

### **Confirmation of the ROCCC-Process**

* **Reliable and Original**: The data comes from the University of California Irvine

* **Comprehensive**: Some of the data sets are suitable for analysis. For better predictions, information such as weight, smoking status, exercise level and detailed cholesterol values ​​would be beneficial.

* **Current**: The data is from 1988 and is therefore not current. Given today's level of knowledge, more information could be collected on this topic.

* **Cited**: Original: [UC Irvine](https://archive.ics.uci.edu/dataset/45/heart+disease)

<div style="margin-bottom: 40px;">

</div>

# **Process**

Since it is a smaller dataset, I decided to do the cleaning, analysis and visualization using Excel.

### Data Exploration
Excel: [Data Exploration](https://github.com/S-a-m-K/heart_disease_prediction/blob/main/01.%20Data%20Exploration)  

### Observations:

1. Get a first look at the individual columns
<img width="910" alt="image" src="https://github.com/user-attachments/assets/145aaf97-4640-44f8-97f3-e8e9c89f3214">

2. Explanation of the columns

<img width="609" alt="image" src="https://github.com/user-attachments/assets/786eb8b4-410c-4f3c-8db7-693da2e79aab">

3. For easier understanding, I change the column names
<img width="876" alt="image" src="https://github.com/user-attachments/assets/b1107a68-0db8-4137-add5-ce00c2acf720">

4. Decoding cells for better communication
<img width="466" alt="image" src="https://github.com/user-attachments/assets/8b9e12b4-30ec-4461-b319-26b5ef2c87e5">

5. Check the set for null values, empty cells and unrealistic values.
<img width="651" alt="image" src="https://github.com/user-attachments/assets/a57195c0-9fca-4542-be50-511123df98c1">

I found no null values, no empty cells and the information seems realistic. But two columns have one additional value than specified. To analyze these columns, I will remove the rows with the unspecified cells.


### Data cleaning

Excel: [Data cleaning]()

...

# **Analysing**

Excel: [Data Analysing]()

...

# **Share**

### Data Visualization 

For the analysis process "Share" I chose [Excel]().

...

### Summary:

...

# **Act**

...
