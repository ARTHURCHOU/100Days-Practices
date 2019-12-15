# Statistics for Data Analysis Coursework
## Question 1 

**The file protein.csv contains data from several European countries in the 1980s on consumption of different categories of food.**

**Exploratory data Analysis:**

***(a) For each variable, calculate appropriate summary statistics to show the level and spread of the data (one statistic for each is enough).***

For the level of each variable, calculate the mean of each variable 

Use the code:
    
    subdata <- data[2:10]
    mean_col <- colMeans(subdata)
    print(mean_col)

Result:

![](https://github.com/ARTHURCHOU/100Days-Practices/blob/master/png1.png)

For the spread of each variable, calculate the variance of each variable

Use the code: 
    
    var(data$RedMeat)…

![](https://github.com/ARTHURCHOU/100Days-Practices/blob/master/png2.png)

***(b)	For each variable, plot the data in a suitable way to illustrate the level and the spread.

![](https://github.com/ARTHURCHOU/100Days-Practices/blob/master/png3.png)

***(c)	Calculate a summary statistic to show the association of the consumption of fruit and vegetables with each of the other food categories.

    cor_pearson <- cor(subdata$Fr.Veg, subdata[1:8],method = 'pearson')
    print(cor_pearson)

Result:

![](https://github.com/ARTHURCHOU/100Days-Practices/blob/master/png4.png)


***(d)	Show a plot illustrating the association of the consumption of fruit and vegetables with each of the other food categories. 
