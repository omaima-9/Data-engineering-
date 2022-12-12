# Introduction  
  This dataset covers all modern Olympic Games, from Athens 1896 to Rio 2016.
  The Olympics are more than just a quadrennial multi-sport world championship.
  The data contains 271116 rows and 15 columns.
  In each row Individual athletes compete in individual Olympic events (athlete-events).
 
# Overview of the dataset used:
  we dealed with two datasets, the first one was 'athlete_events.csv' which have 15 attributes and some of them have missing values,and the attributes are (ID: Unique number for each athlete
  
Name:Athlete's name

Sex:Male or Female

Age:Athlete's age in integer

Height:Athlete's height in centimeters

Weight: Athlete's weight in kilograms

Team: Team name

NOC: National Olympic Committee 3-letter code

Games: Year and season

Year: Integer
Season: Summer or Winter

City: Host city

Sport: Sport

Event: Event

Medal: Gold, Silver, Bronze, or NA)

The second dataset was 'noc_regions.csv' which have 2 attributes, and the attributes are(NOC: National Olympic Committee 3-letter code, regions)

# Overview of the project goals:
  1- Explore the dataset that we are dealing with  
  2- visualize individual attributes and figure out the relations between them  
  3- calculate the missing values in the dataset  
  4- cleaning the data(by handling the missing values and the outliers)  
  5- visualize the dataset after cleaning   
  
# steps used for work done :
1- read the csv file  and importing the libraries.

2- count the unique and some attrbuites to explore data by nunique method and count.

3- calculating the missing values by isna() method and see which attributes we will deal with.

4- four attributes have null values : age , height , medal and weight

5- for age we did univariate imputation and get mean for it and put instead of the null in age

6- for medals we fill by no medal since data we want it

7- height and weight by mutual imputation and removing the outliers 

8- after the cleaning steps we ended up with zero missing values.

9- visualization some attributes like : the female and male across the Olympics  and see that male are higher than females by bar chart since they are nominal data
visualization for the  height and sex and count of them done by histogram 

visualization for the age before cleaning by histplot

visualization for height and weight across sex by scatterplot

visualization for medals before and after cleaning and we see that no medals was the higher and almost the other medals are equal


  
# the  questions to be answered via various data analytics methods using python.
  1- Does the Physical attributes affect the winning chances?
     we first need to split our dataframe into 2 one for males and the other for females in order to remove outliers accurately since males and females have       different ranges.
     then we need to remove the outliers from both dataframes using the IQR method and then visualize using box plots
     after that since there are alot of missing values from weight and height attributes. we need to impute them. for that i used multiple imputation            utilising sklearn's experimental multiple imputer which loops through the data and imputing the data based on classes that are generated through nearby      features.(mean imputation)
     after that we plotted a line graph which shows us the medals among the years when increasing or decreasing weight or height.
     from the graph we found that there is a correlation between having higher physical attributes with winning medals
    then we plotted a barplot with each sport and the amount of gold/silver/bronze and no medals for each one at different weights and heights 
    from it we found that in some sports the weight and height really contribute to the chances of winning such as basketball and swimming
    
  2- Is there a consistency in teams won a specific medal over the years?
    By using the method groupby we first count for the top ten teams got no medals 
    then count for the top ten teams how many gold medals have won
    then count for the top ten teams how many bronze medals have won
    then count for the top ten teams how many silver medals have won
    and then group every type of medal and team
    and sort them by the top 10 that have the highest number of medals then visualizing  every type, the visualization done by bar chart     to indicates the number of medals and top 10
    Clearly, the United States, Germany and the Soviet Union have dominated all three medals in the Olympics.
  
 
