# Exploratory-Data-Analysis-Project-2
Final Project for the course

# Question 1
Have total emissions from PM2.5 decreased in the United States from 1999 to 2008? Using the base plotting system, make a plot showing the total PM2.5 emission from all sources for each of the years 1999, 2002, 2005, and 2008 ?

NEI <- readRDS("summarySCC_PM25.rds") # reading the data 
TotalEm <- aggregate(Emissions ~ year , data = NEI, sum) #aggregating for year and emission using sum
png(filename='plot1.png')
barplot(height = TotalEm$Emissions/10^6,names.arg = TotalEm$year ,width = TotalE$year, xlab = "Years", ylab = "PM2.5 (10^6Tons)", main = "Total US PM2.5 emission from all Sources")
dev.off()


