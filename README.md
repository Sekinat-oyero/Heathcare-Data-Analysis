# Project: Investigate Medical Appointment No Shows Dataset

## Table of Contents
<ul>
<li><a href="#intro">Introduction</a></li>
<li><a href="#wrangling">Data Wrangling</a></li>
<li><a href="#eda">Exploratory Data Analysis</a></li>
<li><a href="#conclusions">Conclusions</a></li>

<a id='intro'></a>
## Introduction

The <a href="https://d17h27t6h515a5.cloudfront.net/topher/2017/October/59dd2e9a_noshowappointments-kagglev2-may-2016/noshowappointments-kagglev2-may-2016.csv">dataset</a> used in this data analysis project is the No Show Medical appointment dataset. It provides information about 100k plus patients attendance of their medical appointment in Brazil. It contains a variable that states whether the patient came for their appointment or not. Other variable or features as described on the dataset's <a href="https://www.kaggle.com/datasets/joniarroba/noshowappointments?resource=download">website</a> are listed below;

Data Dictionary
1. PatientId- Identification of a patient
2. AppointmentID- Identification of each appointment
3. Gender- Male or Female . Female is the greater proportion, woman takes way more care of their health in comparison to man.
4. DataMarcacaoConsulta- The day of the actuall appointment, when they have to visit the doctor.
5. DataAgendamento- The day someone called or registered the appointment, this is before appointment of course.
6. Age- How old is the patient.
7. Neighbourhood- Where the appointment takes place.
8. Scholarship- True of False more information about it can be found <a href="https://en.wikipedia.org/wiki/Bolsa_Fam%C3%ADlia">here</a>
9. Hipertension- True or False
10. Diabetes- True or False
11. Alcoholism- True or False
12. Handcap- True or False
13. SMS_received- 1 or more messages sent to the patient.
14. No-show- True or False.


This dataset will be useful to understand the factors responsible for a patient absence. It will also be useful to predict whether a patient will show up on their appointed day.
A few questions to ask based on this dataset are;
<ul>
<li> Which gender is most likely to attend their appointment?
<li> Which age group attends their appointments the most?

<li> How does the patient income status affects their appointment?. The scholarship, Bolsa Familia, is a poverty alleviation scheme in Brazil. We could attribute scholarship recipients to people from low income families. Therefore, this could assist us to answer the question.
<li> How well do people with disabilities attend their appointment?
<li> Is SMS an effective reminder?

<a id='wrangling'></a>
## Data Wrangling

### General Properties
The dataset contains 110527 samples with 14 features as described above. There is no missing data point in the dataset. Also, the dataset does not contain any repeated or duplicated value. The number of unique values in each feature conforms with the pre-informed knowledge about the dataset with the exception of "Handcap" column which contains 5 unique values. 

### Data Cleaning

#### Dropping some columns

Some columns have too many unique values and may cause redundancy in our analysis. Therefore, they are to be deleted. This columns are; PatientId, AppointmentID, and ScheduledDay. For Patient ID, I am still trying to understand why there are much fewer unique values than the sample size.

#### Renaming Column
Most times, column renaming is useful to make column names more descriptive or for parity reason. However, in this dataset, the No-show column name contains an hyphen (-) which may interfere with our code or may not be acceptable in some code syntax.

#### Incorrect Data

In the "Handcap" column, 0 means false while 1 means true. The other values of 2,3,4 might be incorrectly recorded. This other incorrectly recorded data was mapped to a value of 2 to create a separate view on them.

<a id='eda'></a>
## Exploratory Data Analysis

For exploring each feature to answer the research questions raised in the introduction part of the report, they were taken as categorical data as they should be. Barplot, Histplot and Countplot were the visuals used in viewing the data. Since there is class imbalance in the target (no_show), it is imperative that we employ the proportion route. For example, the proportion of patients less than 18 years that either shows up or did not show up for their appointment. This gives more meaning to the plots. Attempts were made to explore the relationship between two or more features; however, no much insights could be derived from them since those features are categorical features. 
  

<a id='conclusions'></a>
## Conclusions

With this, we could observe that a high number and proportion of female patients missed their appointment compared to their male counterparts. Children missed their appointments more than both adults and old people. This could be caused by a number of factors such as non-availability of adults to escort them since the proportion of adult that missed their appointment is close to that of children.  Similarly, Scholarship recipients missed their appointments more than non-recipients. As explained in the introduction section, scholarship recipient are beneficiaries of the poverty alleviation scheme, Bolsa Familia. This could mean that people from low income families missed their appointment more.  Also, People with disabilities attend their appointments the most, more like they value their health more considering their underlying condition. From the SMS features, it was observed that a greater number of people that received one or more messages still missed their appointment the most, hence the SMS method of reminder might not be effective. Lastly, there is a strong positive correlation between age and people with diabetes and hypertension. Since old people, i.e. people greater than 60 years, show up on their appointment, we could predict that people with diabetes and hypertension will show up on their appointment.
