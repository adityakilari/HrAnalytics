
1. About dataset

The data file "WA_Fn-UseC_-HR-Employee-Attrition.csv" has 
	Number of Rows: 1470 
	Number of Columns: 35

This data set is all about employees working in IBM, has attributes 

Age                         
Attrition                   
BusinessTravel              
DailyRate                   
Department                  
DistanceFromHome            
Education                   
EducationField              
EmployeeCount               
EmployeeNumber              
EnvironmentSatisfaction     
Gender                      
HourlyRate                  
JobInvolvement              
JobLevel                    
JobRole                     
JobSatisfaction             
MaritalStatus               
MonthlyIncome               
MonthlyRate                 
NumCompaniesWorked          
Over18                      
OverTime                    
PercentSalaryHike           
PerformanceRating           
RelationshipSatisfaction    
StandardHours               
StockOptionLevel            
TotalWorkingYears           
TrainingTimesLastYear       
WorkLifeBalance             
YearsAtCompany              
YearsInCurrentRole          
YearsSinceLastPromotion     
YearsWithCurrManager        

The dataset is divided into categorical data and numerical data

categorical data :

['Attrition', 'BusinessTravel', 'Department', 'EducationField', 'Gender',
       'JobRole', 'MaritalStatus', 'Over18', 'OverTime']

numerical data :

['Age', 'DailyRate', 'DistanceFromHome', 'Education', 'EmployeeCount',
       'EmployeeNumber', 'EnvironmentSatisfaction', 'HourlyRate',
       'JobInvolvement', 'JobLevel', 'JobSatisfaction', 'MonthlyIncome',
       'MonthlyRate', 'NumCompaniesWorked', 'PercentSalaryHike',
       'PerformanceRating', 'RelationshipSatisfaction', 'StandardHours',
       'StockOptionLevel', 'TotalWorkingYears', 'TrainingTimesLastYear',
       'WorkLifeBalance', 'YearsAtCompany', 'YearsInCurrentRole',
       'YearsSinceLastPromotion', 'YearsWithCurrManager']


Education

1 'Below College'
2 'College'
3 'Bachelor'
4 'Master'
5 'Doctor'

EnvironmentSatisfaction

1 'Low'
2 'Medium'
3 'High'
4 'Very High'

JobInvolvement

1 'Low'
2 'Medium'
3 'High'
4 'Very High'

JobSatisfaction

1 'Low'
2 'Medium'
3 'High'
4 'Very High'

PerformanceRating

1 'Low'
2 'Good'
3 'Excellent'
4 'Outstanding'

RelationshipSatisfaction

1 'Low'
2 'Medium'
3 'High'
4 'Very High'

WorkLifeBalance

1 'Bad'
2 'Good'
3 'Better'
4 'Best'




Here our dependent variable is 'Attrition', it is a categorical data hence our problem is clasification problem.


The data is imbalanced with 83.9% are retaining and only 16.1% are in attrition.




Data Pre-Processing and Analysis :

Our aim is to analyze the reason why and why not the employee is retaining or attrition

We found that there are few columns in categorical data which does not show any impact in identifying the attrition ('Over18').

There are few rows in numerical data which does not show any impact on attrition and dropped those attributes
(['DailyRate','EmployeeCount','EmployeeNumber','HourlyRate','MonthlyRate','StandardHours'])

With the help of correlation matrix identified the attributes which are highly correlated I,e with the threshold 77% removed those numerical variables. ({'MonthlyIncome', 'PerformanceRating', 'TotalWorkingYears'})

Since the data is imbalanced, used NearMiss() to balance the data.

With the help of mutual_info_classif, identified the attributes which are highly impacting the Attrition.

DataModeling:

We used two different models to train the data to find the Attrition with test train split of (30%,70%)

LogisticRegression : model predicted with the accuracy of 80.41958041958041

DecisionTreeClassifier : model predicted with the accuracy of 68.53146853146853

And on testing with the random sample data both the models predicted the right output

**All the results are shown in Results folder**

 



** code walkthrough and ppt link:
 
 https://drive.google.com/drive/folders/14PDwCn8at5GZRjPmHgew1exAjZDwaBMm?usp=sharing



