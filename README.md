# Netflix-data-analysis


# Ohoud aljawi

# 9.10.2020


# load bakage:
library(tidyverse)


# Explore the data:
glimpse(netflix)
summary(netflix)
print(netflix)
str(netflix)

print(netflix)

arrange(netflix)  



#Load the input data and look at the first few rows
netflix <- read.csv(list.files(path = "../input", recursive = T, full.names = T)[1])
netflix$date_added <- as.Date(netflix$date_added, format = "%B %d, %Y")
head(netflix)

type <- netflix %>%
  filter(type == "TV Show") 
netflix %>%
  arrange(type)

  #add to repo