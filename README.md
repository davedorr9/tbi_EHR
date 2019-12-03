# tbi_EHR
A collection of algorithms on detecting TBI sequelae from EHR data

This repository contains a selection of key information on how to extract and calculate likelihood of follow-up and potential for sequelae from TBI.
It requires the following capabilities:
 - Access to the Value Set Authority Center OR the OHDSI software suite and common data model (forthcoming)
 - Ability to translate SQL pseudocode to EHR specific queries
 - Ability to implement a logistic regression rule
 
 Description of the Problem or Gap
Although traumatic brain injuries (TBI) occur frequently, negative sequelae – including a number of mental health conditions and symptoms - from mild TBI are often under-detected, making them difficult to manage.1 Recovery trajectories following TBI are complex and variable; consistent follow-up with screening for onset and exacerbations of TBI-related mental health disorders and/or physical conditions (e.g., headaches, sleep disorders, and cognitive impairment) is recommended and shown to improve outcomes.2, 3 
TBI related data elements are difficult to reliably capture in the electronic health record (EHR) making clinical decision support to encourage follow-up and guideline-based treatment challengin.1, 4 In this study we examine the potential of the EHR to provide data to be used for future predictive analyses to determine who gets better or worse follow-up care for mental health related negative sequelae to TBI. 
Methods: What did you do to address the problem or gap?
Patients with a diagnosis of TBI between 2010 and 2018 were identified at Oregon Health & Science University (OHSU) using SNOMED, ICD-9 and ICD-10 code sets derived from the Value Set Authority Center (VSAC). Then, common mental health (MH) conditions known to be related to TBI including depression, anxiety, sleep disorders, post-traumatic stress disorder, and substance abuse moderate to severe TBI codes from defined quality metrics and VSAC code sets.4 An observation study data set was created by defining and querying: 1) initial TBI date; 2) patient demographics; 4) history of MH disorders pre-TBI, 5) frequency of follow up after TBI within the health system, and 6) new MH diagnoses after TBI. To understand the influence of the number of pre-TBI MH on the likelihood of follow up. Descriptive statistics compared key characteristics pre-TBI with follow-up after TBI. A multivariable logistic regression was run on a training dataset to identify the contribution of specific pre-existing conditions on the likelihood of follow up after TBI; and validated on a hold-out dataset. A github repository that contains all the relevant information to reproduce the work is established for dissemination.
