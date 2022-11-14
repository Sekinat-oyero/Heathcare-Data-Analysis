# Project: Investigate Medical Appointment No Shows Dataset

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
