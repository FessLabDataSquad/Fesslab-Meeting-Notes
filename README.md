# Fesslab-Meeting-Notes
 
##Meeting 2: 10/27/16, Fall 2016

####Review of DataSquad Goal: 
Train people to use tools of R for data cleaning so that they can make meaningful contributions. Build institutional memory and record keeping on Github (our source of centralized information) for future RAs.

####What is Rmarkdown? 
**allows you to interweave R code with ordinary text to produce well-formatted data**
* anything that happens between ``` is treated as code (shaded lines, also known as code blocks)
* anything outside code blocks is treated as text

**easy to modify**
* after slightly tweaking the code in Rmarkdown, all of your stats are automatically updated in the live document

####Exercise: This assignment involves merging a bunch of files and to see what nice, clean data looks like. 
* Data is from study on Trust and Social Issues. 
* B/c the programmer worked in a different program, the output files have variables with inconvenient names, and inconvenient responses.  
* Examples: (1) the response showing "1-strongly agree" when we want it to say "1" (2) the response showing "-99" when we want it to say "NA" (3) the variable named "dg1" when we want it to say "ID". 
* These discrepancies will have to be identified and corrected, so that the output files will be in a format that is convenient for our purpose. There should be a file of keys explaining what the variables mean. 

####The goal: All of these files with data should be neatly consolidated, and we should figure out how to merge the dataset (pulling out the valuable data from each of the 5 data files, and merging them together)

**Packages** help base r become more efficient for specific types of activities. Packages modify the working environment towards a specific interest. Tidyr and Dplyer are packages that help the data cleaning process (from raw data files to statistical analyses on publications)
####Tidyr
* written by Hadley Wickham
* http://vita.had.co.nz/papers/tidy-data.pdf
* tidying makes sure each observation is a row and each variable is a column. 
* does not change the data; the exact data is just organized differently. 
* designed to have commands that are simpler and more efficient than base r when creating tidy data files. 

####Dplyr
* comes in handy for big portion of data cleaning (like when you have 2 variables that need to become one)

####By next week: 
* import all 5 data files
* start writing code to clean up the project (put in at least one hour to improve code and/or improve documentation)
* figure out commands in tidyr and dplyer
* you can build your own branches, explore help communities, look for good convention to load all the packages, etc. 
* check in the Github organization periodically for updates

####Additional notes: 
* We are working on public repositories--be professional, keep the data private (but the code public). share data through email or possibly DropBox.  
* Make sure to write description/explanation for your code when opening a pull request
* to enable softwrap: go to Rstudio-> Preferences -> Code -> Soft-wrap R source files (you do not have to do this when using Rmarkdown)
* A useful thing to do is create a directory (the file where all the data is) when importing files. 
* Excel tries to autocorrect data files, so some alternatives to Excel are: LibreOffice, GoogleSheets 
* On Github, changes are color coded: additions are green, deletions are red
* Running certain packages may disrupt other functions or make them less efficient 








