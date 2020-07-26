## Team Members
Osama Almasri

Sabda Karkera

Rishitha Muddana 

Raga Preethi Potu

Ming Wu

# Covid-19 Prediction 
COVID-19 is a disease that was identified in Wuhan, China. It is a new strain of coronavirus that has not been previously identified in humans and is now being spread througout the world. Coronaviruses are a large family of viruses that are known to cause illness ranging from the common cold to more severe diseases such as Severe Acute Respiratory syndrome (SARS) and Middle East Respiratory Syndrome (MERS). It is the cause of an outbreak of respiratory illness. The people most affected or at the risk of getting very sick from Covid-19 include older adults and people who have serious chronic medical conditions and the ones in the higher-risk population. 



# Research Question 





# Relevant Domain Information 


# Data and Source Description 
We have chosen The Nursing Home COVID-19 Public data that includes data reported by nursing homes to the CDC’s National Healthcare Safety Network (NHSN) system COVID-19 Long Term Care Facility Module, including Resident Impact, Facility Capacity, Staff & Personnel, and Supplies & Personal Protective Equipment, and Ventilator Capacity and Supplies Data Elements. The file contains an individual record for each certified Medicare skilled nursing facility/Medicaid nursing facility and the ending date for each collection week that has been updated weekly. This information is used to assist with national surveillance of COVID-19 in nursing homes, and support actions to protect the health and safety of nursing home residents. There could be some linitation in the data set such as the availability of testing may impact the number of confirmed COVID-19 cases facilities report. For example, facilities that did not have the ability to test all residents a few weeks ago would not be able to report all residents with confirmed cases. Similarly, access to testing can vary by state, region, or facility.

### Supporting COVID-19 Testing

The data collected through the NHSN system directly supports this initiative by helping to prioritize the nursing homes with testing needs and an increasing number of cases. 


### Link to the dataset: 


# Data Understanding
 
This process is one of the very first steps in the CRISP-DM process model that is required to understand the structure of the data well enough and being able to model data successfully. It obtains data and verifies that it is appropriate for ones needs. This phase includes gathering data, describing it, exploring data and verifying the data quality. Data manipulation and basic statistical techniques are used to further check into the data for their range of values and their distributions.  


# Data Preparation

Data preparation is one of the most important steps where the data is collected and preserved for other purposes and needs some refinement before it is ready to use for modeling. Exploratory data analysis (EDA) is first process to analyze data, summarize the main characteristics, and understand the structure and distribution of the data, often with visual methods.
Our dataset contains many missing values. These columns can be imputed using imputation techniques such as mean, median, mode, or advanced imputation methods such as k-nearest imputation, etc. Another important factor to look into a dataset is to find for the missing values. The nursing home dataset contains missing values and hencefoth can be detected and solved with the help of visualization techniques. We used boxplot visualization to analyze some of the columns and detected the ouliers present in them. After they have been detected, they can be removed using other techniques such as histogram, IQR, Z-Score and scatter plots. Finding the relationship between the variables and treating them accordingly in the pre-processing steps is also considered to be an important factor during the process of modelling. To find the relationship or correlation between the attributes in the dataset, we have used correlation matrix. Certain attributes pairs such as 

Residents Weekly Admissions Covid-19 and Residents weekly Covid-19 deaths

Residents Total Admissions Covid-19 and Residents Total Covid-19 deaths

Residents Weekly all Deaths and Residents Weekly Covid-19 deaths

Residents Weekly confirmed and Staff weekly confirmed Covid-19

Residents Total Covid-19 deaths (Vs) Staff Total confirmed covid-19

Staff weekly confirmed Covid-19 (Vs) Residents total Covid-19 deaths have shown a correlation value between 0.5 to 0.7, which is considered to be the appropriate.

The dataset also contains many categorical attributes and there are some libraries that do not take categorical variables as input. Thus, we convert them into numerical variables. Therfore, in our dataset we used dummy encoding by converting a categorical input variable into continuous variable or a binary variable. Presence of a level is represented by 1 and absence is represented by 0. Some of the other important things that need to be done to the data before we model it are:

1. Look for high cardinality features and drop them.

2. Use Label Encoder to transform non-numerical labels to numerical labels that are always between 0 and n_classes-1. However this may sometimes dcrease the performance of the model

3. 


# Machine Learning




# Evaluation


# Known Issues


# Conclusion




|Name     | 
|---------|
|[Rishithamuddana](https://github.com/Rishithamuddana)| 
|[xxxxxxxxxxxxxxx](https://github.com/xxxxxxxxxxxxxx) |    
|[xxxxxxxxxxxxxxx](https://github.com/xxxxxxxxxxxxxx) |    
|[xxxxxxxxxxxxxxx](https://github.com/xxxxxxxxxxxxxxx)|    
|[xxxxxxxxxxxxxxx](https://github.com/xxxxxxxxxxxxxx) |


