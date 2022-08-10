# Importing-a-fixed-with-file-into-R-programming
# Importing a Fixed- with- files into R programming 

library(tidyverse)

### Salaries of City of Chicago  employees

### Reading the data 

### reading the names
### Using your own names for the columns 
names <- c('Name', 'Title', 'Department', 'Salary')

### Telling the charater for each column
length <- c(32, 50, 24, NA)

width <- fwf_widths(length, names)

employees <- read_fwf('http://594442.youcanlearnit.net/chicagoemployees.txt', 
                      width)

glimpse(employees)

### you can see that all the variable names can be seen in the first line
### so we use the skip command to remove the first column or variable
employees <- read_fwf('http://594442.youcanlearnit.net/chicagoemployees.txt', 
                      width, skip = 1)
view(employees)

glimpse(employees)
