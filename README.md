# This Python Module contains 3 functions  

[![forthebadge made-with-python](http://ForTheBadge.com/images/badges/made-with-python.svg)](https://www.python.org/)                 
[![Python 3.9](https://img.shields.io/badge/python-3.9-yellow.svg)](https://www.python.org/downloads/release/python-360/)   


## All 3 functions of module are  

- First function is - data_doctor --->  (This function is for filling the NAN values in the columns, dropping some rows if the NAN values in % is less than minimum specified %, dropping some of the columns if NAN values % in such columns are greater than the maximum specified % limit, getting dummy variables of all categorical variables and then dropping those categorical variables,converting categorical target column to numeric type and dropping some unwanted columns also.)

- Second function is - data_balance_split --->  (This function is used for balancing the unbalanced dataset if this function is used for classification problem, NO balancing is required in case of Regression problem also this function is used for train and test split of dataset.) 

# NOTE: Make sure that the target output column is in axis otherwise you get error (Not found in axis) when you run this function.

- Third function is - data_report --->  (This function is for getting the pandas profile report of both raw initial data set and final refined dataset which we get from first function as output and also saving the two profile reports in HTML files.)
 

## Usage

- Make sure you have Python installed in your system.
- Run Following command in the CMD.
 ```
  pip install FinalData
  ```
## Example

 ```
## for first function of the module 
data_doctor(a,b,c,d,l1=[],l2=[])

keywords:
    
         a : is Data file in csv format 
    
         b: is minimum percentage for dropping the rows having NAN values 
        
        c : is the maximum percentage for dropping rows and columns respectively for NAN values
        
        l1 : is the list of columns which are need to be removed and are of no use in predicting the result,
                if there are no such columns then give empty list
        
        l2 : is the list of columns which should be numeric type but they are originally given object type,
               if there are no such columns then give the empty list 
        
        d : is the target output column name in string format 

#Give values for all the required input arguments to get result 

## for second function of the module 
data_balance_split(a,v1,v2,c,d,e)

keywords:
    
    v1 and v2 are the lower and the upper limits for the ratio of binary outputs of target column for classification problem.
    
    a : is the dataframe which is obtained using first function and by giving all required i/p arguments by the function.
    
    c : is the target column in string form.
     
    d : is the size of test dataset.
     
    e : for type of problem(Regression or Classification(binary)).

# Give values for all the required input arguments to get result 

## for third function of the module 
data_report(a,b)

keywords:
    
    a : is the dataframe which is obtained as output of first function after providing all the required input arguments by the function.
    
    b : is the original raw dataframe file in csv format for getting the profile report of original dataframe and also final 
    dataframe and we can also compair the difference between the two profile report.
    
    Before using this function make sure that pandas profile is installed in your system or notebook and if the latest 
    version in not working properly then in case you can installed any old version like
    
    !pip install pandas-profiling==2.7.1.
    
    But no need to import the profile report as it is already imported in this function you only have to intall pandas
    profile like
    
    from pandas_profile import ProfileReport
# Give values for all the required input arguments to get result 
  
  ```


## Note 
- I have tried to implement all the functionality, it might have some bugs also. Ignore that or please try to solve that bug.

## NOTE: All these three functions are for regression and binary classification problems in which the data does'nt contain any column for duration, time, date etc. ex-- 21/9/2021, 2h31m, 2:30 etc.