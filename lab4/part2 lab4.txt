setwd("D:/DSR Lab")
churn_data<-read.csv("Churn_Modelling.csv")
churn_data
colnames(churn_data)
churn_data$EstimatedSalary

salary_group<-vector(mode="character",length=length(churn_data$EstimatedSalary))
salary_group
sal<-churn_data$EstimatedSalary
salary_group[sal<10000]<-"Low"
salary_group
salary_group[sal>=10000 & sal< 100000]<-"Medium"
salary_group[sal>100000]<-"High"
salary_group
spender<-factor(salary_group,levels=c("Low","Medium","High"),ordered=TRUE)
spender
churn_data<-cbind(churn_data,spender)
churn_data
write.csv(churn_data,"D:/DSR Lab/ChurnExportedData.csv")