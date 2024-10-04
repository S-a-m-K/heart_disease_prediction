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

<img width="885" alt="image" src="https://github.com/user-attachments/assets/7b15bf60-3115-485f-95b5-546fbe9d8f70">

In total, this set contains data from 1025 patients with various ages from 29 to 77. Most of the patients studied are between the ages of 40 and 67. Most of the patients are 58 years old.

<img width="910" alt="image" src="https://github.com/user-attachments/assets/f42eafb9-09f6-4bf7-8413-4f9348b4437f">

<img width="907" alt="image" src="https://github.com/user-attachments/assets/71828fe3-0893-4cfe-a350-0c8f79490c67">

Most of the patients with heart disease were between 40 and 45 and between 51 and 54. However, the results could be different if the age groups were more balanced. The patients who were not diagnosed with heart disease were mostly between the ages of 57 and 63.

<img width="909" alt="image" src="https://github.com/user-attachments/assets/bf402396-c3ab-411f-95da-9d4fafe5ae94">

The percentage breakdown provides a better overview. But even in this view, the highest values ​​for a disease are between 41 and 45 and between 51 and 54.

Between 46 and 50 it seems fairly balanced. Between 55 and 63 the numbers for a disease are the lowest. Between 64 and 66 it is more balanced again.

From the age of 68 onwards, the number of patients who were examined is too small to make a clear statement. The same applies to patients aged 29 to 40. In this range too, there were not even half as many.

<img width="909" alt="image" src="https://github.com/user-attachments/assets/4500d671-dc33-4e5c-b922-62e0b063d4c5">
<img width="910" alt="image" src="https://github.com/user-attachments/assets/80a8b65f-17d0-49aa-8499-8ece94511e5f">

A total of 312 women and 713 men were examined. Over 72% of women were diagnosed with heart disease. For men, the figure was less than 43%.

<img width="910" alt="image" src="https://github.com/user-attachments/assets/42a9d376-2c96-4c5b-a077-5735c5275c92">
<img width="910" alt="image" src="https://github.com/user-attachments/assets/a6db1803-07e3-45e9-bdec-906bdc409258">


Of the patients with typical anginal chest pain, about 1/4 also suffered from heart disease. In atypical anginal pain, over 80% were diagnosed with heart disease. In non-anginal pain, over 77% had heart disease and in asymptomatic pain, it was 2/3.

<img width="909" alt="image" src="https://github.com/user-attachments/assets/a3c7a220-054a-4021-b825-bc49d463b9fc">
<img width="908" alt="image" src="https://github.com/user-attachments/assets/180eb463-5410-48df-b8d2-e244b735f1b3">


Broken down by gender, over 40% of women with typical angina chest pain have heart disease. For the other types of chest pain, the probability of heart disease is between 78 and 100 percent.

For men, it is not quite as devastating. For typical anginal chest pain, it is comparatively only 17%. But the probability of heart disease also increases dramatically with the other types of chest pain. There the probability is between 59 and 76 percent.

<img width="910" alt="image" src="https://github.com/user-attachments/assets/0dc2a689-0942-491f-9a6d-ce9f98c2b8e5">
<img width="911" alt="image" src="https://github.com/user-attachments/assets/8e1d3749-9679-40b9-9569-837f9b9caaeb">

If you look at the patients' blood sugar, the result is rather sobering. Both parties are equally affected. There are also no significant differences between the sexes. Except that women with normal blood sugar levels seem to be more likely to suffer from heart disease. High blood sugar levels alone do not seem to provide any clear predictions.

<img width="910" alt="image" src="https://github.com/user-attachments/assets/3009d70c-d2e9-4883-b967-eb93748a4fd5">
<img width="910" alt="image" src="https://github.com/user-attachments/assets/0c5eaf10-9332-41aa-8503-c9c0f571a3e7">
<img width="911" alt="image" src="https://github.com/user-attachments/assets/eb2f7689-225a-4239-9974-41e54a55e46f">

Blood pressure alone does not seem to provide a clear prediction. All patients with low blood pressure are classified as having heart disease. But due to the small number, this is not really meaningful. Most patients with severe hypertension do not have heart disease. But here too, the number is too small to make a precise statement.

In general, it seems that the number of heart diseases decreases the higher the blood pressure rises.

I also did not find any significant differences when breaking down the sexes.

<img width="910" alt="image" src="https://github.com/user-attachments/assets/9436f946-aee7-48ef-9c2e-dfa6d76090e8">
<img width="911" alt="image" src="https://github.com/user-attachments/assets/466b0165-9541-4fb2-865d-cfb547b8e852">
<img width="910" alt="image" src="https://github.com/user-attachments/assets/bd041879-dee2-4213-96ea-3f4b6733008f">

The first thing that is noticeable here is that most patients have high cholesterol levels. In percentage terms, there are no significant differences in measured heart disease. Patients with measured hypercholesterolemia appear to be less affected by heart disease.

<img width="910" alt="image" src="https://github.com/user-attachments/assets/f07babee-75ad-4e0f-9ba6-dba8d7d8893a">
<img width="910" alt="image" src="https://github.com/user-attachments/assets/965e26e4-e218-413c-ac08-dc02a6313faa">
<img width="911" alt="image" src="https://github.com/user-attachments/assets/6260e667-84f8-42ca-a64d-e2bb3fd300c4">

A diagnostic resting EKG (electrocardiogram) records the electrical activity of your heart while you are at rest. It provides information about your heart rate and rhythm and can also show whether there is enlargement of the heart or signs of a previous heart attack.

An ST-T abnormality on an electrocardiogram (ECG) is known to independently predict subsequent morbidity and mortality from cardiovascular diseases. But how ST-T abnormality develops in relation to chronologic changes in cardiovascular risk factors has not been fully discussed [National library of medicine](https://pubmed.ncbi.nlm.nih.gov/8623733/#:~:text=An%20ST%2DT%20abnormality%20on,has%20not%20been%20fully%20discussed.). 

Left ventricular hypertrophy is a thickening of the wall of the heart's main pumping chamber, called the left ventricle. This thickening can increase pressure inside the heart. The disease can make it harder for the heart to pump blood. The most common cause is high blood pressure.

<img width="909" alt="image" src="https://github.com/user-attachments/assets/799d00d2-6864-4978-8351-21c8d2f69652">
<img width="909" alt="image" src="https://github.com/user-attachments/assets/1f56a82b-abb8-4e10-84a1-e38b87c39916">
<img width="909" alt="image" src="https://github.com/user-attachments/assets/a6ef4ed0-3d09-4302-8d2c-25fae5f35aba">

blablabla Angina Pectoris

<img width="910" alt="image" src="https://github.com/user-attachments/assets/57daebd0-316a-403d-876a-5a90407158f9">
<img width="867" alt="image" src="https://github.com/user-attachments/assets/9d0f42bd-4977-40ec-9fc9-7f1785bf0fd0">

blablabla ST Depression

<img width="909" alt="image" src="https://github.com/user-attachments/assets/0e443d35-318e-4aa5-af8d-a4709e8ed285">
<img width="868" alt="image" src="https://github.com/user-attachments/assets/e21a42c6-7e71-4340-9d06-e321aca113f8">

blablabla Peak ST Segment

<img width="976" alt="image" src="https://github.com/user-attachments/assets/1ae60a14-9dbf-4d8a-9466-95dcef42a849">
<img width="976" alt="image" src="https://github.com/user-attachments/assets/53cd69cf-3842-43bb-9f54-5cb26ff72cd7">

blablabla Num Major Vessel and Thallium

### Summary:

...

# **Act**

...
