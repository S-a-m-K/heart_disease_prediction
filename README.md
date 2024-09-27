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

Excel: [Data cleaning](https://github.com/S-a-m-K/heart_disease_prediction/blob/main/02.%20Data%20Cleaning.xlsx)

1. Divide [blood pressure](https://swissheart.ch/so-bleiben-sie-gesund/gesund-leben/blutdruck) values ​​into groups
   
3. Divide [cholesterol](https://www.netdoktor.ch/laborwerte/cholesterinwerte/#:~:text=Wenn%20das%20Gesamt%2DCholesterin%20bei,6%2C21%20mmol%2Fl) levels into groups
   
5. Remove max heart frequenz - According to the [Fox formula](https://www.akademie-sport-gesundheit.de/magazin/maximale-herzfrequenz.html), all patients except one would have a maximum heart rate that is too high. However, since the maximum heart rate depends on many other factors than just age, such as genes, height, training level and altitude, this column is of no use. That's why I've removed it.
   
7. Error in the column “number of major vessels” - There is also an error in the column num_of_major_vessel. [Four are described](https://data.world/informatics-edu/heart-disease-prediction). However, there are 5 variables in the column (0-4). For the analysis with this column, I will remove the unnecessary rows. There are a total of 18 rows with 0 values that i have removed.
   
9. Another error with "thal" - Here too, there is one more variable than [stated](https://data.world/informatics-edu/heart-disease-prediction). For the analysis with this column, I will remove the unnecessary rows. There are a total of 7 rows with zero values ​​that I have removed.

<div style="margin-bottom: 40px;">

</div>

# **Analysing and Share**

For the process "Analysing" and "Share" I chose also Excel

The data has been cleaned, unusable columns removed, and variables grouped into new columns for better understanding. The data is now ready for analysis and I will check to see if there are any patterns in this data that could be attributed to a possible heart disease.

<img width="909" alt="image" src="https://github.com/user-attachments/assets/c0c52f21-f24c-4b80-98c3-9038413ebacd">

In total, this set contains data from 1025 patients with various ages from 29 to 77. Most of the patients studied are between the ages of 40 and 67. Most of the patients are 58 years old.

<img width="909" alt="image" src="https://github.com/user-attachments/assets/4500d671-dc33-4e5c-b922-62e0b063d4c5">
<img width="910" alt="image" src="https://github.com/user-attachments/assets/80a8b65f-17d0-49aa-8499-8ece94511e5f">

A total of 312 women and 713 men were examined. Over 72% of women were diagnosed with heart disease. For men, the figure was less than 43%.

<img width="910" alt="image" src="https://github.com/user-attachments/assets/f42eafb9-09f6-4bf7-8413-4f9348b4437f">

<img width="907" alt="image" src="https://github.com/user-attachments/assets/71828fe3-0893-4cfe-a350-0c8f79490c67">

Most of the patients with heart disease were between 40 and 45 and between 51 and 54. However, the results could be different if the age groups were more balanced. The patients who were not diagnosed with heart disease were mostly between the ages of 57 and 63.

<img width="909" alt="image" src="https://github.com/user-attachments/assets/bf402396-c3ab-411f-95da-9d4fafe5ae94">

The percentage breakdown provides a better overview. But even in this view, the highest values ​​for a disease are between 41 and 45 and between 51 and 54.

Between 46 and 50 it seems fairly balanced. Between 55 and 63 the numbers for a disease are the lowest. Between 64 and 66 it is more balanced again.

From the age of 68 onwards, the number of patients who were examined is too small to make a clear statement. The same applies to patients aged 29 to 40. In this range too, there were not even half as many.

<img width="909" alt="image" src="https://github.com/user-attachments/assets/f3e5db6e-2826-4026-b3a9-f3835a940867">
<img width="909" alt="image" src="https://github.com/user-attachments/assets/7372857d-8206-4ca8-99d7-e3593ed205af">



<img width="908" alt="image" src="https://github.com/user-attachments/assets/ef9f1fc1-e0c5-444a-8534-582d4ae896b2">



### Summary:

...

# **Act**

...
