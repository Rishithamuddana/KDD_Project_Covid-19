## Team Members
Osama Almasri

Sabda Karkera

Rishitha Muddana 

Raga Preethi Potu

Ming Wu


## Project Introduction
COVID-19 is a disease that was identified in Wuhan, China. It is a new strain of coronavirus that has not been previously identified in humans and is now being spread througout the world. Coronaviruses are a large family of viruses that are known to cause illness ranging from the common cold to more severe diseases such as Severe Acute Respiratory syndrome (SARS) and Middle East Respiratory Syndrome (MERS). It is the cause of an outbreak of respiratory illness. The people most affected or at the risk of getting very sick from Covid-19 include older adults and people who have serious chronic medical conditions and the ones in the higher-risk population. 

In the project that we are implementing, we wish to predict if the residents of a nursing home confirmed with Covid-19 have an affect on the staff of that particular nursing home.


## Research Question 
Our main aim is to find if the residents of a nursing home confirmed with Covid-19 have an affect on the staff that have been confirmed of Covid-19 of that particular nursing home.


## Relevant Domain Information 
https://www.theverge.com/2020/3/5/21166088/coronavirus-covid-19-protection-doctors-nurses-health-workers-risk

https://www.latimes.com/california/story/2020-04-10/coronavirus-covid19-hospital-nonclinical-staffers-fear

https://www.msn.com/en-us/health/medical/doctors-nurses-at-high-risk-of-coronavirus-as-the-front-lines-of-medical-care/ar-BB10PElE


## Data and Source Description 
https://data.cms.gov/Special-Programs-Initiatives-COVID-19-Nursing-Home/COVID-19-Nursing-Home-Dataset/s2uc-8wxp
 
We have chosen The Nursing Home COVID-19 Public data that includes data reported by nursing homes to the CDC’s National Healthcare Safety Network (NHSN) system COVID-19 Long Term Care Facility Module, including Resident Impact, Facility Capacity, Staff & Personnel, and Supplies & Personal Protective Equipment, and Ventilator Capacity and Supplies Data Elements. The file contains an individual record for each certified Medicare skilled nursing facility/Medicaid nursing facility and the ending date for each collection week that has been updated weekly. This information is used to assist with national surveillance of COVID-19 in nursing homes, and support actions to protect the health and safety of nursing home residents. There could be some linitation in the data set such as the availability of testing may impact the number of confirmed COVID-19 cases facilities report. For example, facilities that did not have the ability to test all residents a few weeks ago would not be able to report all residents with confirmed cases. Similarly, access to testing can vary by state, region, or facility. This dataset contains 123k rows and 59 columns, where each row is a nursing home.

## Supporting COVID-19 Testing
The data collected through the NHSN system directly supports this initiative by helping to prioritize the nursing homes with testing needs and an increasing number of cases.

## Approach

### Data Understanding
This process is one of the very first steps in the CRISP-DM process model that is required to understand the structure of the data well enough and being able to model data successfully. It obtains data and verifies that it is appropriate for ones needs. This phase includes gathering data, describing it, exploring data and verifying the data quality. Data manipulation and basic statistical techniques are used to further check into the data for their range of values and their distributions. This can be done usimg exploratory data analysis, which is refered to in short as EDA.   


### Data Preparation
Data preparation is one of the most important steps where the data is collected and preserved for other purposes and needs some refinement before it is ready to use for modeling. 
Our dataset contains many missing values. These columns can be imputed using imputation techniques such as mean, median, mode, or advanced imputation methods such as k-nearest imputation, etc. Another important factor to look into a dataset is to find for the missing values. The nursing home dataset contains missing values and hencefoth can be detected and solved with the help of visualization techniques. We used boxplot visualization to analyze some of the columns and detected the ouliers present in them. After they have been detected, they can be removed using other techniques such as histogram, IQR, Z-Score and scatter plots. Finding the relationship between the variables and treating them accordingly in the pre-processing steps is also considered to be an important factor during the process of modelling. To find the relationship or correlation between the attributes in the dataset, we have used correlation matrix. Certain attributes pairs such as 

Residents Weekly Admissions Covid-19 and Residents weekly Covid-19 deaths

Residents Total Admissions Covid-19 and Residents Total Covid-19 deaths

Residents Weekly all Deaths and Residents Weekly Covid-19 deaths

Residents Weekly confirmed and Staff weekly confirmed Covid-19

Residents Total Covid-19 deaths (Vs) Staff Total confirmed covid-19

Staff weekly confirmed Covid-19 (Vs) Residents total Covid-19 deaths have shown a correlation value between 0.5 to 0.7, which is considered to be appropriate.

The dataset also contains many categorical attributes and there are some libraries that do not take categorical variables as input. Thus, we convert them into numerical variables. Therfore, in our dataset we used dummy encoding by converting a categorical input variable into continuous variable or a binary variable. Presence of a level is represented by 1 and absence is represented by 0. Some of the other important things that can also be done to the data before we model it are:

1. Look for high cardinality features and drop them.

2. Use Label Encoder to transform non-numerical labels to numerical labels that are always between 0 and n_classes-1. However this may sometimes decrease the performance of the model


### Machine Learning
We are dealing with Supervised learning model as our nursing home dataset contains both input and output variables. A supervised learning contains two types of learning problems out of which regression model could possibly be related to the dataset as our target varaiable is a real value. Hence, it is used to predict a class label.


### Evaluation
Various model evaluation techniques can be used under the supervised learning setup that helps us in finding how good our model is performing. As our dataset is supervised, we can apply many machine learning techniques such as Linear Regression, Random Forest, Support Vector Machine, etc. to evaluate our model. There are also other ways we could possibly use in evaluating a model by finding the accuracy, which is the difference between the predicted and actual values. We can also find sum squared error, mean squared error and root mean square error which are the most common ways of evaluating a regression model.


## Known Issues
The nursing home Covid-19 dataset is said to have many missing values. This was found by using the n_miss () function and by just looking into the dataset. Other factors related to the datset were of the outliers that were detected using box plot visualization. Some essential variables were said to have outliers, which could be removed by using other visualization techniques as well. There were also some variables that were highly correlated that would be difficult for us to change one variable without having to change the other. There were also variables that were less or not correlated at all. This could lead to unpredictability of the target variable. Our dataset has contains many categorical variables that could be a problem in evaluating our model. This can be solved by simply assigning numbers to categorical variables by performing dummy encoding 


## Conclusion
Our main concern is to have a well-prepared data that has been cleaned and preprecessed, which later could be modelled successfully. We will review our process and findings before we model our data and conclude.  




