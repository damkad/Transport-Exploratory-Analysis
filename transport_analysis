library(tidyverse)
data <- read.csv("TravelSurveyThess.csv", stringsAsFactors = T, header = TRUE, sep = ";", fileEncoding = "latin1")
data <- data[,2:39]
data$HouseHoldSize = as.factor(data$HouseHoldSize)
data$HouseHold16 = as.factor(data$HouseHold16)
data$driversLicense = as.factor(data$driversLicense)
data$Income = as.factor(data$Income)
data$carAvail <- ifelse(data$carAvail==TRUE, 1,0)
data$carAvail <- as.factor(data$carAvail)
names(data)
summary(data)
str(data)
unique(data$Income)
#a <- drop_na(data)
datas = cor(data)
plot(y=data$Occupation, x=data$Age)
#trip duration per age
ggplot(data)+ geom_boxplot(aes(x=Age, y=tripDuration))

#trip per income
ggplot(data)+ geom_boxplot(aes(x=Income, y=tripDuration))+
  theme(axis.text.x = element_text(angle = 90))
#plot of graph
heatmap(scale(data))
str(data)
ggplot(data)+ geom_bar(aes(x=mode))
data$InZone
ggplot(data)+ geom_bar(aes(x=mode, fill=Gender))

ggplot(data)+ geom_bar(aes(x=mode, fill=Occupation))

ggplot(data)+ geom_bar(aes(x=mode, fill=Education))

ggplot(data)+ geom_bar(aes(x=mode, fill=Age))

ggplot(data)+ geom_bar(aes(x=mode, fill=HouseHoldSize))

ggplot(data)+ geom_bar(aes(x=mode, fill=carAvail))

ggplot(data)+ geom_bar(aes(x=mode, fill=HouseHold16))

ggplot(data)+ geom_bar(aes(x=mode, fill=driversLicense))


ggplot(data)+ geom_bar(stat = "identity", aes(x=mode, y= tripDuration))


#for motorcycle
ggplot(data)+ geom_bar(aes(x=realTravelTime.MrC))
ggplot(data)+ geom_bar(aes(x=realShortestDistance.MrC))

#for bus
ggplot(data)+ geom_bar(aes(x=realTravelTime.Bus))
ggplot(data)+ geom_bar(aes(x=realShortestDistance.Bus))

#for walk
ggplot(data)+ geom_bar(aes(x=realTravelTime.Walk))
ggplot(data)+ geom_bar(aes(x=realShortestDistance.Walk))


#for car
ggplot(data)+ geom_bar(aes(x=realTravelTime.Car))
ggplot(data)+ geom_bar(aes(x=realShortestDistance.Car))


