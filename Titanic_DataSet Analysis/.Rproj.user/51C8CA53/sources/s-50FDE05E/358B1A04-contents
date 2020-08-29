
library(data.table)
setDT(titanic)
library(ggplot2)
str(titanic)
unique(titanic$Pclass)

#Numerical to Catgorical data
titanic[,Survived := factor(Survived)]
titanic[,Pclass := factor(Pclass,ordered=T)]
titanic[,Sex := factor(Sex)]

#aesthetic function
# How many people survived , using bar chart since it is a categorical data
ggplot(titanic ,aes(x=Survived)) + geom_bar()
# More people died then survived

#Better view
ggplot(titanic ,aes(x=Survived)) + geom_bar()+ theme_bw()+labs(y= "Passenger Count", title = "Titanic
Survival Rates")


# Taking sex into account
ggplot(titanic ,aes(x=Sex)) + geom_bar()+ theme_bw()+labs(y= "Passenger Count", title = "Titanic
Survival Rates")
#Conclusion : More male survived compared to female

# Sex plus Class they travelled in
ggplot(titanic ,aes(x=Sex,fill = Pclass)) + geom_bar()+ theme_gray()+labs(y= "Passenger Count", title = "Titanic
Survival Rates")
