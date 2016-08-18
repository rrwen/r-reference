# R Introduction
  
  
Richard Wen (rwenite@gmail.com)  
  
A quick introduction to R, which includes installation, basic examples, and references to learning resources.  

**Requirements**
* [R](https://www.r-project.org/) [[Download](http://cran.r-project.org/mirrors.html)]: a free programming language that is widely used for statistics and data analysis
* [RStudio](https://www.rstudio.com/products/rstudio/) [[Download](https://www.rstudio.com/products/rstudio/download2/#download)]: a graphical interface and various tools to make writing R code easier
  
**Explore the examples by switching [branches](https://help.github.com/articles/viewing-branches-in-your-repository/) in this repository.**
  
## 1.0 Quick Start
1. Install [R](http://cran.r-project.org/mirrors.html) and [RStudio](https://www.rstudio.com/products/rstudio/download2/#download)
2. Open RStudio and begin coding in R:  
  * **Script Editor**: Run, edit, and save R code using script files (.R)  
  * **Console**: Execute and output code  
  * **Variables/Objects**: Inspect variables and objects in the global environment  
  * **Help/Plots/Misc**: Visualization, help documentation, package, and file interfaces 
  
<img src="https://github.com/rwenite/r-examples/blob/intro/ui.PNG"  width="800;"/>

## 2.0 Basic Examples
The following can be run in either the console or the script editor.

### Help
Get help documentation using `?`
```r
?read.table
?write.table
?vector
?data.frame
?summary
?plot
?lm
```

### Read and Write
Read/write table-formatted data using `read.table`
```r
dataset <- read.table("file.txt")
write.table(dataset, "new_file.txt")
```

### Comments and Output
Commenting using `#` and console output using `print()`
```r
# This is a comment, it does not get executed
print("Some text") # It can be used on the same line as the actual code
```

### Math
Simple arithmetic operations:
* addition `+`
* subtraction `-`
* multiplication `*`
* division `/`
* exponent `^`
```r
1 + 1  # add
2 - 1  # sub
2 * 2  # multiply
10 / 2  # div
4^2  # exp
```

### Variables
Variable assignment using `<-`
```r
x <- 1
x + 1  # output 2
x / 2  # output 0.5
```

### Vectors
Create a vector using `c()`
```r
height <- c(4.8, 4.5, 5.75)
eyeColor <- c("blue", "brown", "green")
eyeColor[1]  # select the 1st eyeColor
height[c(1,3)]  # select 1st and 3rd height
height + 0.1  # add 0.1 to all heights
```

### Dataframes
Create a dataframe (table-like structure) using `data.frame()`
```r
dataset <- data.frame(height=c(4.8, 4.5, 5.75),
                      eyeColor=c("blue", "brown", "green"))
dataset[1, ]  # select 1st row
dataset[, 2]  # select 2nd column
```

### Summaries and Plots
Obtain a summary or plot using `summary()` or `plot()`
```r
summary(dataset)  # mean, median, mode, stdev, etc
plot(dataset)  # height vs eyeColor
```

## 3.0 References
* [Base R Cheatsheet](https://www.rstudio.com/wp-content/uploads/2016/06/r-cheat-sheet.pdf) by Mhairi McNeill for more basic R code
* [RStudio cheatsheets](https://www.rstudio.com/resources/cheatsheets/) for quick R code references
* [Online learning resources](https://www.rstudio.com/online-learning/#R) suggested by RStudio
* A short [12 page introduction to R](https://www.rstudio.com/resources/cheatsheets/) by Paul Torfs and Claudia Brauer
* Google's [R Style Guide](https://google.github.io/styleguide/Rguide.xml) for R coding practices
* [Advanced R](http://adv-r.had.co.nz/) by Hadley Wickham
