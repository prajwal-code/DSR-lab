x <- c(50,53,54,55,56,59,62,65,67,72,72,74,75,76,79)
y <- c(122,118,128,121,125,136,144,142,149,161,167,168,162,171,175)
relation <- lm(y~x)
print(summary(relation))
a <- data.frame(x = 85)
result <- predict(relation,a)
result
plot(x,y,col="blue",main = "Temparature and yield", abline(lm(y~x)),cex= 1.3,pch=16,xlab="Temparature",ylab="Yield")