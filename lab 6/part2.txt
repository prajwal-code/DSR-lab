library(ggplot2)
install.packages("mtcars")
mtcars
dotchart(mtcars$mpg,labels=row.names(mtcars),xlab="MPG",main="Miles per Gallon of Car",cex=0.8,bg='gray90',pch=21)