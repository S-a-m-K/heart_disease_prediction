![Banner](https://github.com/S-a-m-K/heart_disease_prediction/blob/main/heart%20disease%20prediction%2002.png)

<h1>Heart Disease Prediction</h1> 

**Author: Samuel Kleger**  
**Date: 2024-09-20**


# **Introduction**

According to the World Health Organization, despite significant advances in diagnosis and treatment, mortality from heart disease remains the leading cause of death worldwide, accounting for about one-third of annual deaths. “Heart disease” is a general term used to describe a group of heart conditions and diseases, including Coronary Artery Disease, Arrhythmia, Heart Valve Disease, and Heart Failure, which cause the heart not to pump blood healthily.

The most common type of heart disease is Coronary Artery Disease. The disease is a medical condition in which the coronary arteries that supply blood to the heart muscle become narrowed or blocked due to plaque build-up on their inner walls. This can lead to serious complications such as a heart attack, heart failure, and arrhythmias, as it reduces blood flow to the heart muscle. In some cases, procedures such as angioplasty or bypass surgery may be necessary to improve blood flow to the heart.

The second common heart disease is Arrhythmia. Arrhythmia is caused by disturbances in the normal electrical activity of the heart. The normal beating rhythm of the heart is disrupted because the electrical impulses in the heart responsible for synchronizing the heartbeat are not working properly. As a result, the heartbeat may be faster, slower, or more irregular than normal. Millions of people worldwide are affected by Arrhythmia [(National Library of Medicine)](https://pmc.ncbi.nlm.nih.gov/articles/PMC10378171/). 

---

### **Table of Content**

- [Introduction](#Introduction)
- [Ask](#Ask)
  - [Business Task](#Business-Task)
- [Prepare](#Prepare)
  - [Data Source](#Data-Source)
  - [Confirmation of the ROCCC-Process](#Confirmation-of-the-ROCCC-Process)
- [Process](#Process)
  - [Data Exploration](#Data-Exploration)
  - [Observations](#Observations)
  - [Data Cleansing](#Data-Cleaning)
- [Analysing and Share](#Analysing-and-Share)
  - [Summary](#Summary)
- [Act](#Act)

---

# **Ask**

### **Business Task**

Examine the dataset to gain insights that could aid in developing preventive measures for heart disease.

### **Analysis Questions**

- Is there a relationship between the various risk factors and heart attack outcomes?
- Can the insights gained be used in the future to reduce heart attack risk in this population?

<br>

# **Prepare**


### **Data Source**

This data set dates from 1988 and consists of four databases: Cleveland, Hungary, Switzerland, and Long Beach V. It contains 76 attributes, including the predicted attribute, but all published experiments refer to using a subset of 14 of them.

A simplified version of the dataset is also publicly accessible on [kaggle](https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset/data).

**Additional information:**

Patients were classified as having heart disease if a coronary artery was narrowed by more than 50%. 

To protect privacy, patients' names and social security numbers were removed from the database and replaced with anonymized values.

**Source**: Data provided by the University of California Irvine

**License**: [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/legalcode)

**Type**: CSV

**Format**: Long Data

**Duration**: Data is from 1988

<br>

### **Confirmation of the ROCCC-Process**

* **Reliable and Original**: The data comes from the University of California Irvine

* **Comprehensive**: While some of the datasets are suitable for analysis, additional information such as weight, smoking habits, physical activity, and detailed cholesterol levels would be valuable for making better predictions.

* **Current**: The data dates back to 1988 and is therefore not current. With today's level of knowledge, more comprehensive information could be collected on this topic.

* **Cited**: Original: [UC Irvine](https://archive.ics.uci.edu/dataset/45/heart+disease)

<br>

# **Process**

Given the smaller size of the dataset, I chose to perform the cleansing, analysis, and visualization using Excel.
 
Excel: [Data Exploration](https://github.com/S-a-m-K/heart_disease_prediction/blob/main/01.%20Data%20Exploration.xlsx)

<br>

### Observations:

1. Get a first look at the individual columns
<img width="910" alt="image" src="https://github.com/user-attachments/assets/145aaf97-4640-44f8-97f3-e8e9c89f3214">

<br><br>

2. Explanation of the columns
<img width="609" alt="image" src="https://github.com/user-attachments/assets/786eb8b4-410c-4f3c-8db7-693da2e79aab">

<br><br>

3. I will rename the columns for easier understanding
<img width="876" alt="image" src="https://github.com/user-attachments/assets/b1107a68-0db8-4137-add5-ce00c2acf720">

<br><br>

4. Decoding cell values for better understanding
<img width="466" alt="image" src="https://github.com/user-attachments/assets/8b9e12b4-30ec-4461-b319-26b5ef2c87e5">

<br><br>

5. Check the dataset for null values, empty cells, and unrealistic values
<img width="651" alt="image" src="https://github.com/user-attachments/assets/a57195c0-9fca-4542-be50-511123df98c1">

I found no null values or empty cells, and the information appears realistic. However, two columns contain one additional value beyond what is specified. To analyze these columns, I will remove the rows with the unspecified values.

<br><br>

### Data cleansing

Excel: [Data cleansing](https://github.com/S-a-m-K/heart_disease_prediction/blob/main/02.%20Data%20Cleaning.xlsx)

1. Divide [blood pressure](https://swissheart.ch/so-bleiben-sie-gesund/gesund-leben/blutdruck) values ​​into groups
   
2. Divide [cholesterol](https://www.netdoktor.ch/laborwerte/cholesterinwerte/#:~:text=Wenn%20das%20Gesamt%2DCholesterin%20bei,6%2C21%20mmol%2Fl) levels into groups

3. Remove Maximum Heart Rate Column: According to the [Fox formula](https://www.akademie-sport-gesundheit.de/magazin/maximale-herzfrequenz.html), all patients except one would have an excessively high maximum heart rate. However, since maximum heart rate is influenced by several factors beyond age—such as genetics, size, training level, and altitude—and this information is unfortunately unavailable, this column is not useful, so I have removed it.
   
4. Error in the 'Number of Major Vessels' Column: There is an issue with the 'num_of_major_vessels' column. Although the data description states that there are [four major vessels](https://data.world/informatics-edu/heart-disease-prediction), this column contains five possible values (0-4). To address this inconsistency, I will remove the unnecessary rows. In total, I have removed 18 rows with a value of 0.

5. Another Error with 'Thal': Similarly, there is one additional variable in the 'thal' column than what is [stated](https://data.world/informatics-edu/heart-disease-prediction). To address this issue, I will remove the unnecessary rows. In total, I have removed 7 rows with a value of zero.

<br>

# **Analysing and Share**

For the data visualization process "Analysing" and "Share" I use also Excel

The data has been cleaned, unusable columns removed, and variables grouped into new columns for better clarity. The data is now ready for analysis, and I will investigate whether there are any patterns that could indicate a potential risk of heart disease.

<img width="885" alt="image" src="https://github.com/user-attachments/assets/7b15bf60-3115-485f-95b5-546fbe9d8f70">

This dataset contains information from a total of 1,025 patients, with ages ranging from 29 to 77. The majority of the patients are between 40 and 67 years old, with the most common age being 58.

<img width="910" alt="image" src="https://github.com/user-attachments/assets/f42eafb9-09f6-4bf7-8413-4f9348b4437f">

<img width="907" alt="image" src="https://github.com/user-attachments/assets/71828fe3-0893-4cfe-a350-0c8f79490c67">

Most patients diagnosed with heart disease were between the ages of 40 and 45, as well as between 51 and 54. However, the results might differ if the age groups were more balanced. In contrast, the majority of patients who were not diagnosed with heart disease were aged between 57 and 63.

<img width="909" alt="image" src="https://github.com/user-attachments/assets/bf402396-c3ab-411f-95da-9d4fafe5ae94">

The percentage breakdown offers a clearer overview. Even in this view, the highest rates of heart disease are observed among patients aged 41 to 45 and 51 to 54. 

The age group between 46 and 50 appears relatively balanced, while the numbers for heart disease are lowest among those aged 55 to 63. In the 64 to 66 age range, the data becomes more balanced again.

From age 68 onwards, the number of examined patients is too small to draw any definitive conclusions. The same applies to patients aged 29 to 40, as there were fewer than half as many in this range.

<img width="909" alt="image" src="https://github.com/user-attachments/assets/4500d671-dc33-4e5c-b922-62e0b063d4c5">
<img width="910" alt="image" src="https://github.com/user-attachments/assets/80a8b65f-17d0-49aa-8499-8ece94511e5f">

A total of 312 women and 713 men were examined. Over 72% of the women were diagnosed with heart disease, while the figure for men was less than 43%.

<img width="910" alt="image" src="https://github.com/user-attachments/assets/42a9d376-2c96-4c5b-a077-5735c5275c92">
<img width="910" alt="image" src="https://github.com/user-attachments/assets/a6db1803-07e3-45e9-bdec-906bdc409258">

Among patients with typical anginal chest pain, approximately one-quarter were also diagnosed with heart disease. In cases of atypical anginal pain, over 80% received a heart disease diagnosis. Additionally, more than 77% of patients with non-anginal pain had heart disease, while two-thirds of those with asymptomatic pain were also affected.

<img width="909" alt="image" src="https://github.com/user-attachments/assets/a3c7a220-054a-4021-b825-bc49d463b9fc">
<img width="908" alt="image" src="https://github.com/user-attachments/assets/180eb463-5410-48df-b8d2-e244b735f1b3">

Broken down by gender, over 40% of women with typical anginal chest pain were diagnosed with heart disease. For the other types of chest pain, the probability of having heart disease ranges from 78% to 100%.

For men, the situation is less severe. For those with typical anginal chest pain, the diagnosis rate is comparatively low at only 17%. However, the probability of having heart disease increases significantly with the other types of chest pain, ranging from 59% to 76%.

<img width="910" alt="image" src="https://github.com/user-attachments/assets/0dc2a689-0942-491f-9a6d-ce9f98c2b8e5">
<img width="911" alt="image" src="https://github.com/user-attachments/assets/8e1d3749-9679-40b9-9569-837f9b9caaeb">

The analysis of patients' blood sugar levels yields somewhat sobering results, as both groups are equally affected. There are no significant differences between the sexes, except that women with normal blood sugar levels appear to be more likely to suffer from heart disease. High blood sugar levels alone do not seem to offer clear predictive value.

<img width="910" alt="image" src="https://github.com/user-attachments/assets/3009d70c-d2e9-4883-b967-eb93748a4fd5">
<img width="910" alt="image" src="https://github.com/user-attachments/assets/0c5eaf10-9332-41aa-8503-c9c0f571a3e7">
<img width="911" alt="image" src="https://github.com/user-attachments/assets/eb2f7689-225a-4239-9974-41e54a55e46f">

Blood pressure alone does not provide a clear prediction of heart disease. All patients with low blood pressure are classified as having heart disease; however, the small sample size makes this finding less meaningful. 

Conversely, most patients with severe hypertension do not have heart disease, but again, the limited number of cases prevents us from making a precise assessment.

Overall, it appears that the incidence of heart disease decreases as blood pressure increases. Additionally, I found no significant differences when analyzing the data by sex.

<img width="910" alt="image" src="https://github.com/user-attachments/assets/9436f946-aee7-48ef-9c2e-dfa6d76090e8">
<img width="911" alt="image" src="https://github.com/user-attachments/assets/466b0165-9541-4fb2-865d-cfb547b8e852">
<img width="910" alt="image" src="https://github.com/user-attachments/assets/bd041879-dee2-4213-96ea-3f4b6733008f">

The most striking observation is that most patients have high cholesterol levels. In terms of percentages, there are no significant differences in the prevalence of heart disease. Interestingly, patients with diagnosed hypercholesterolemia seem to be less affected by heart disease.

<img width="910" alt="image" src="https://github.com/user-attachments/assets/f07babee-75ad-4e0f-9ba6-dba8d7d8893a">
<img width="910" alt="image" src="https://github.com/user-attachments/assets/965e26e4-e218-413c-ac08-dc02a6313faa">
<img width="911" alt="image" src="https://github.com/user-attachments/assets/6260e667-84f8-42ca-a64d-e2bb3fd300c4">

A diagnostic resting EKG (electrocardiogram) records the electrical activity of your heart while you are at rest. It provides information about your heart rate and rhythm and can also show whether there is enlargement of the heart or signs of a previous heart attack[(Ascot Cardiology Group)](https://ascotcardiologygroup.co.nz/services/diagnostic-resting-ecg/#:~:text=What%20is%20a%20Diagnostic%20Resting,of%20a%20previous%20heart%20attack.).

An ST-T abnormality on an electrocardiogram (ECG) is known to independently predict subsequent morbidity and mortality from cardiovascular diseases. But how ST-T abnormality develops in relation to chronologic changes in cardiovascular risk factors has not been fully discussed [(National Library of Medicine)](https://pubmed.ncbi.nlm.nih.gov/8623733/#:~:text=An%20ST%2DT%20abnormality%20on,has%20not%20been%20fully%20discussed.). 

Left ventricular hypertrophy is a thickening of the wall of the heart's main pumping chamber, called the left ventricle. This thickening can increase pressure inside the heart. The disease can make it harder for the heart to pump blood. The most common cause is high blood pressure[(Mayo Clinic)](https://www.mayoclinic.org/diseases-conditions/left-ventricular-hypertrophy/symptoms-causes/syc-20374314#:~:text=Left%20ventricular%20hypertrophy%20is%20a,cause%20is%20high%20blood%20pressure.).

Over 60% of patients with ST-T abnormalities on the ECG were diagnosed with heart disease. In contrast, only 20% of patients with left ventricular hypertrophy were classified as having heart disease, although it is important to note that only 15 patients had this condition. A more detailed analysis would require a significantly larger sample size.

Additionally, even 40% of patients with no abnormalities found still suffered from heart disease. This underscores that this examination alone is not sufficiently informative.

<img width="909" alt="image" src="https://github.com/user-attachments/assets/799d00d2-6864-4978-8351-21c8d2f69652">
<img width="909" alt="image" src="https://github.com/user-attachments/assets/1f56a82b-abb8-4e10-84a1-e38b87c39916">
<img width="909" alt="image" src="https://github.com/user-attachments/assets/a6ef4ed0-3d09-4302-8d2c-25fae5f35aba">

Angina pectoris does not appear to be a reliable indicator of early signs of heart disease; in fact, it seems to indicate the opposite, as only 20% of those with angina were classified as having heart disease.

When examining the data by gender, a difference emerges: over 32% of women with angina were diagnosed with heart disease, compared to just 17% of men.

<img width="910" alt="image" src="https://github.com/user-attachments/assets/57daebd0-316a-403d-876a-5a90407158f9">
<img width="867" alt="image" src="https://github.com/user-attachments/assets/9d0f42bd-4977-40ec-9fc9-7f1785bf0fd0">

ST depression occurs when the J point is displaced below baseline. Just like ST elevation, not all ST depression represents myocardial ischemia or an emergent condition. There are multiple conditions associated with ST depression. Some of these include hypokalemia, cardiac ischemia, and medications such as digitalis[(National Library of Medicine)](https://www.ncbi.nlm.nih.gov/books/NBK459364/#:~:text=ST%20depression%20occurs%20when%20the,and%20medications%20such%20as%20digitalis.)

Over 32% of patients were not diagnosed with ST depression, yet more than one-third of them were classified as having heart disease.

The percentage view indicates that most patients with heart disease fall within the first half of the scale. Although there are a few outliers, they do not appear to be particularly significant.

This comparison alone does not yield clear results either. Perhaps we will uncover more definitive insights by examining the ST segment and the resulting waveforms.

<img width="909" alt="image" src="https://github.com/user-attachments/assets/0e443d35-318e-4aa5-af8d-a4709e8ed285">
<img width="868" alt="image" src="https://github.com/user-attachments/assets/e21a42c6-7e71-4340-9d06-e321aca113f8">

The ST segment on an electrocardiogram (ECG) normally represents an electrically neutral area of the complex between ventricular depolarization (QRS complex) and repolarization (T wave). However, it can take on various waveform morphologies that may indicate benign or clinically significant injury or insult to the myocardium.

The ST segment encompasses the region between the end of ventricular depolarization and beginning of ventricular repolarization on the ECG. In other words, it corresponds to the area from the end of the QRS complex to the beginning of the T wave. In clinical terms, the ST segment represents the period in which the myocardium maintains contraction to expel blood from the ventricles[(National Library of Medicine)](https://www.ncbi.nlm.nih.gov/books/NBK459364/#:~:text=ST%20depression%20occurs%20when%20the,and%20medications%20such%20as%20digitalis.). 

This model yields somewhat clearer results. Over 70% of patients with a downsloping course were diagnosed with heart disease. In contrast, the prevalence for patients with a flat or upsloping course ranged between 30% and 40%. It's important to note that only 7.2% of patients exhibited an upsloping course.

<img width="976" alt="image" src="https://github.com/user-attachments/assets/1ae60a14-9dbf-4d8a-9466-95dcef42a849">
<img width="976" alt="image" src="https://github.com/user-attachments/assets/53cd69cf-3842-43bb-9f54-5cb26ff72cd7">
<img width="976" alt="image" src="https://github.com/user-attachments/assets/f9c398fa-251b-454a-83f8-e078b612a4d7">

The vast majority of treatments were performed on patients with Major Vessel 0. The treatment was successful in over 56% of heart patients, with more than 11% experiencing reversible conditions.

<br>

### Summary:

In summary, the following groups are more likely to suffer from heart disease according to these studies:

* **Age Groups:** Individuals aged between 40 and 45 and between 51 and 54 are particularly at risk. While both women and men of all ages are affected, the incidence is highest within these age brackets.

* **Gender Disparity:** Women are more affected than men, with a prevalence of 72% compared to 43% for men.

* **Chest Pain Types:** Patients with typical anginal chest pain are diagnosed with heart disease in just under 25% of cases, whereas the probability increases to between 66% and 80% for other types of chest pain. Notably, over 43% of women with typical anginal pain have heart disease, compared to just under 18% of men.

* **Blood Sugar Levels:** The analysis of blood sugar levels does not yield clear predictions, as very few patients exhibited values that were too high.

* **Blood Pressure:** Similar to blood sugar, no clear conclusions can be drawn regarding blood pressure. In fact, it appears that the rate of heart disease decreases with increasing blood pressure.

* **Cholesterol Levels:** Most patients have elevated cholesterol levels; however, no significant differences are observed. Men with higher cholesterol levels seem to be less affected by heart disease.

* **Electrocardiogram Results:** The resting electrocardiogram provides more definitive results, with 60% of patients exhibiting ST T-wave abnormalities classified as having heart disease. Conversely, patients with left ventricular hypertrophy appear to be less affected.

* **Angina Pectoris:** Angina pectoris is not a reliable indicator of heart disease, which aligns with findings from the comparison of heart pain types.

* **ST Depression Values:** The ST depression values do not provide satisfactory results, as most patients with heart disease did not exhibit fluctuations.

* **ST Segment Course:** The analysis of the ST segment course offers clearer predictions, with over 70% of patients exhibiting a downsloping course being diagnosed with heart disease.

* **Treatment Outcomes:** Major Vessel 0 was the most affected area, and treatments were largely successful.

<br>

# **Act**

I recommend an early routine examination for the following groups of people:

* Individuals over 40 years of age
* Women, who are particularly affected
* Individuals experiencing atypical angina pain
* Women with typical angina chest pain
* Individuals connected to an ECG, especially if a downsloaping course of the ST peak is observed, as this may indicate a potential heart condition.
