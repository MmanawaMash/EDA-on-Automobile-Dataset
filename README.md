# EDA-on-Automobile-Dataset

In this project, I was required to do an EDA on an automobile dataset and then present the results of my analysis. To facilitate the analysis, I made use of NumPy, pandas, Matplotlib and seaborn. 

This project was one of the tasks I was required to complete for my Data Science Bootcamp with HyperionDev. 

### SUMMARY
AUTOMOBILE DATASET. 
The three categories of entities in this data set are:
1.	the description of an automobile in terms of various attribute (make, fuel-type, aspiration, etc)
2.	 the insurance risk assessment given to it .
3.	 the normalized losses in usage as compared to other cars.
The second rating reflects how much riskier the car is than its asking price suggests. Cars are first given a risk factor symbol corresponding to their cost. The symbol is then modified by moving it up (or down) the scale if it is more (or less) dangerous. This is referred to as "symboling." An auto is hazardous if its value is +3, and presumably rather safe if it is -1.
This data set includes information about cars that was taken from the 1985 Ward's Automotive Yearbook (Cars).

### DATA SOURCE: https://www.kaggle.com/datasets/toramky/automobile-dataset

### DATA CLEANING
Missing values
In the automobile dataset, missing data is denoted with a question mark "?". We replace "?" with NaN (Not a Number) value, which is the default missing value marker.

There is very little missing data in our columns, making dropping most of the columns unwarranted. I replaced values with the average or frequency value and deleted some rows. 

Data types
Certain columns have incorrect data types. Variables with numbers should be of type "float" or "int," while variables containing strings, like categories, should be of type "object." For instance, the variables "bore" and "stroke" are numerical descriptions of the engines, so we would anticipate that they would be of type "float" or "int," but they are displayed as being of type "object". Using the "astype()" technique, we must transform data types into the appropriate format for each column.

### MISSING DATA
I replaced values with the average or frequency value and deleted some rows.

Replace by mean:
"normalized-losses": 41 missing data, replace them with mean
"stroke": 4 missing data, replace them with mean
"bore": 4 missing data, replace them with mean
"horsepower": 2 missing data, replace them with mean
"peak-rpm": 2 missing data, replace them with mean
Replace by frequency:
"num-of-doors": 2 missing data, replace them with "four". Reason: 84% sedans is four doors. Since four doors is most frequent, it is most likely to occur.
Drop some column:
"price": 4 missing data, simply delete the whole row Reason: price is what we want to predict. Any data entry without price data cannot be used for prediction; therefore any row now without price data is not useful 

### CONCLUSIONS
1. Toyota has more occurences in the dataset and Mercury has the least.
2. he visualization shows that OHC has more occurences in the dataset and rotor has the least. OHC engines are a lot more preferred because it has more power than the other engine types in the database. OHC engines tend to be able to rev higher mostly due to the significantly lower valve train weight which makes for greatly improved valve control and higher potential RPM before float occurs. OHV engines have pushrods and relatively heavy rockers as opposed to OHC which does away with that.
3.  Sedan has more occurences in the dataset than the other car types.
4.  The most expensive body styles are hardtop, followed by convertible and sedan.
5.  The least costly cars are made by Chevrolet, and the most expensive made by Mercedes-Benz. The luxury cars costing more than 20,000 are made by BMW, Jaguar, Mercedes-Benz, and Porsche. Chevrolet, Dodge, Honda, Mitsubishi, Plymoth, and Subaru are the least expensive vehicles, with prices under 10,000. The majority of other vehicles are in the intermediate, between 10,000 and 20,000.
6.   The normalized losses in the vehicle grow linearly with an increase in risk rating. Most losses for covertible and hardtop vehicles have a risk rating above 0. Hatchback vehicles have the highest risk of loss ratings. Sedan and Wagon have losses despite having a safer grade for risk.







