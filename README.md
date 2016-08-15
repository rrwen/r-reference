# R Introduction
  
  
Richard Wen (rwenite@gmail.com)  
  
A quick introduction to R, which includes setting up R/RStudio and references for learning R.  
* [R](https://www.r-project.org/) is a free programming language that is widely used for statistics and data analysis
* [R Studio](https://www.rstudio.com/products/rstudio/) provides a graphical interface and various tools to make writing R code easier
  
**Requirements**  
* [R](http://cran.r-project.org/mirrors.html)  
* [R Studio Desktop](https://www.rstudio.com/products/rstudio/download2/#download)
  
**Explore the examples by switching [branches](https://help.github.com/articles/viewing-branches-in-your-repository/) in this repository.** 
  
## 1.0 Installation 
1. Download and install [R](http://cran.r-project.org/mirrors.html) followed by [RStudio Desktop](https://www.rstudio.com/products/rstudio/download2/#download)
2. Run RStudio and a similar interface should be shown:
  
<img src="https://github.com/rwenite/r-examples/blob/intro/quickstart.PNG"  width="600;"/>
  
## 2.0 Basic Examples

### Help
Get help documentation using `?`
```r
?read.table
?write.table
?vector
?data.frame
?plot
?summary
```

### Read and Write
Read/write table-formatted data using `?read.table`
```r
dataset <- read.table("file.txt")
write.table(dataset, "new_file.txt")
```

### Vectors
Create a vector using `c()`
```r
height <- c(4.8, 4.5, 5.75)
eyeColor <- c("blue", "brown", "green")
eyeColor[1]  # select the 1st eyeColor
height[c(1,3)]  # select 1st and 3rd height
```

### Help
Creating a dataframe (table-like structure) using `data.frame()`
```r
dataset <- data.frame(height=c(4.8, 4.5, 5.75),
                      eyeColor=c("blue", "brown", "green"))
dataset[1, ]  # select 1st row
dataset[, 2]  # select 2nd column
```
Obtain a summary or plot using `summary()` or `plot()`
```r
summary(dataset)  # mean, median, mode, stdev, etc
plot(dataset)  # height vs eyeColor
```
Perform linear regression using `lm` (See more at [Quick-R](http://www.statmethods.net/stats/regression.html))
```r
fit <- lm(heights ~ eyeColor, data=dataset)
coefficients(fit)
residuals(fit)
confint(fit, level=0.95)  # confidence intervals
fitted(fit)  # predicted
anova(fit)  # anova table
```
See Mhairi McNeill's [Base R Cheatsheet](https://www.rstudio.com/wp-content/uploads/2016/06/r-cheat-sheet.pdf) for some more basic examples.
  
## 3.0 References
* [Online learning resources](https://www.rstudio.com/online-learning/#R) suggested by RStudio
* A short [12 page introduction to R](https://www.rstudio.com/resources/cheatsheets/) by Paul Torfs and Claudia Brauer
* Google's [R Style Guide](https://google.github.io/styleguide/Rguide.xml) for R coding practices
* [RStudio cheatsheets](https://www.rstudio.com/resources/cheatsheets/) for quick references when working with R
* [Advanced R](http://adv-r.had.co.nz/) by Hadley Wickham
