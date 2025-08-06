# working directory
setwd("C:/Users/INSPIRON/OneDrive/Desktop/AI_Omics_Internship_2025")

getwd()
# making folders 
dir.create("raw_data")
dir.create("clean_data")
dir.create("script")
dir.create("results")
dir.create("plots")
# loading data
data <- read.csv("patient_info.csv")
data
# data strruture
str(data)
# new binaray variable 
data$smoker_num <- factor(data$smoker,
                          levels = c("No", "Yes"),
                          labels = c("0", "1"))
# saving work
write.csv(data, file =  "clean_data/patient_info_clean.csv")

