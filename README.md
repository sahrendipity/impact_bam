# repo of very basic function, and how to turn into a package!

library(tidyverse)

#Accounting for multiple measurements - function to find biggest change in value between max and end values
max_diff <- function(data) {  
  data %>%
    group_by(day) %>%
    summarise(maxdiff = (max(temp) - last(temp))) 
}
