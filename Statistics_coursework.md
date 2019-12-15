# Statistics for Data Analysis Coursework
## Question 1
#### Exploratory data Analysis:

***(a)***

For the level of each variable, calculate the mean of each variable 

Use the code:
    
    getwd()
    setwd("C:/Users/zsw00/Desktop")
    data<-read.csv('protein.csv', header = TRUE)
    subdata <- data[2:10]
    mean_col <- colMeans(subdata)
    print(mean_col)

Result:

![](https://github.com/ARTHURCHOU/100Days-Practices/blob/master/png1.png)

For the spread of each variable, calculate the variance of each variable

Use the code: 
    
    for (i in (1:9))
        print(var(subdata[i])) 

![](https://github.com/ARTHURCHOU/100Days-Practices/blob/master/png2.png)

***(b)***

Boxplot is a good way to show the level and spread of data at the same time. By observing the three quartiles of the data set, you can roughly get the overall situation of the data.

![](https://github.com/ARTHURCHOU/100Days-Practices/blob/master/png3.png)

***(c)***

    cor_pearson <- cor(subdata$Fr.Veg, subdata[1:8],method = 'pearson')
    print(cor_pearson)

Result:

![](https://github.com/ARTHURCHOU/100Days-Practices/blob/master/png4.png)


***(d)***

According to this chart, it can be seen that there is a weak negative correlation between fruits and vegetables and red meat, white meat, eggs, and milk, and a weak positive correlation with fish, cereals, starch, and nuts. The correlation between milk and fruits and vegetables is the highest, which is -0.4084

![](https://github.com/ARTHURCHOU/100Days-Practices/blob/master/png5.png)

#### Inference:

***(e)***

    for (i in (1:9))
        print(t.test(subdata[i]))
        
Categories | 95 percent confidence interval
:-: | :-: 
Redmeat | 8.446394-11.209606
WhiteMeat | 6.371158-9.420842
Eggs | 2.474671-3.397329
Milk | 14.17903-20.04497
Fish | 2.879503-5.688497
Cereals | 27.71783 36.77817
Starch | 3.601483 4.950517
Nuts | 2.252351 3.891649
Fr.Veg | 3.391385 4.880615

***(f)***

    t.test(subdata$Starch, subdata$Nuts,
 	      alternative = 'greater',mu=0)
          
![](https://github.com/ARTHURCHOU/100Days-Practices/blob/master/png6.png)\

From the results of the t-test, the p-value is 0.0118, which is less than 0.05, so the hypothesis (the average consumption of starch is larger than the average consumption of nuts) does not hold.

## Question 2
