# Fesslab-Meeting-Notes
##Meeting 4: 11/10/16, Fall 2016

###Important Points/Overview
There maybe two meetings per week in the future, so each member can attend one of the sessions.

When you use the Issues tab to post a question, tag that person(s) (@username) so you can get faster answers. 

Give the branch a descriptive name. Have each branch represent one type of edit. 

*Data cleaning*: Our goal is to reduce manual intervention and make it scripted, automated, and reproducible. Each RA will make valuable contributions through specialized knowledge. 

*GitHub*: It is a centralized organizational tool that promotes collaborative coding. You can make changes through a "branch", which is separate from the "mainline"/master code. You can then issue a pull request to merge the branch into the master, and it is important to provide documentation and annotation of what your proposed code is for. 

*The disgust-style project*: Adam is currently working on revising a paper that deals with the phenomenon of disgust and risk-taking. This project involves stylistic changes on the statistical work (to make it more effective, to make it into a publishable form, and to make it reproducible for future use by Adam and other researchers). 

*Assignment 1*: There are several source files that need to be integrated to be in a publishable form. Each source file involves the output for an economic game that participants took. However, the files are not in a convenient format because the programmer used a different program. One of Adam's collaborators had to type in each participant ID in each of the source files, and manual errors may have resulted from this. In order to combine the different source files, we need to identify and correct the errors in the source files. 

###We discussed what we found over the week: 
Kayla (disgust project)
  1. Changing the magic numbers into variables. For example, if we are looking for 95% confidence, it is better to have a variable name called CONFIDENCE.INTERVAL than to use the value 0.95 in the code. Otherwise, others reading the code may not know what "0.95" is (if the code is public). Also, if we were to change the confidence interval in the future (to say, 90%), it will be easier to make sweeping changes than by repeatedly changing 0.95 into 0.90. Generalizing code in this way is great because it can be used in the future. 
  2. Using = instead of -> when defining a variable. This is more efficient since it has only one character, it is used by other programmers, and there is less room for error. 
  3. Use _ instead of . when naming variables (for consistency). Some convention with regards to capitalization and lowercase perhaps? 

Kai (assignment 1) 
  1. One way to look for manual errors within a dataframe is by using the filter() function in the dplyr package. 
  2. One way to produce useful formatting for each variable's data (and to produce a key comparing the original item to the reformatted item) is by using the DataCombine package. 

###Issues on Github Functionality that need answers:
1. How do we edit the code outside of Github, while retaining Github functionality to highlight the changes? Basically, how do we do offline work in Rstudio, and then upload the modified file such that Github compares the modified version to the old version. Maybe copy/paste? 
2. How to deal with several different changes/cumulative changes to the master code? Need to develop protocols and standardized processes. For example, Kayla made 3 branches for each type of edit. Should all of these branches branch off the master, or should Branch 1 branch off of master, Branch 2 branch off of Branch 1, and Branch 3 branch off of Branch 2? 

###Misc. 
What is as.data.frame? 
  as.data.frame is when you take something that looks like a table and store it in R as a data frame. By coercing the table into a data frame, you can perform certain functions that can only be done with data frames and not on table objects. 










##Meeting 3: 11/03/16, Fall 2016

Use the **Issues** tab to post any questions/concerns you may have. This way, the repository can be modified regularly to resolve any confusions (about the sub-tasks, etc.) before next week's meeting. 

Use the pull request feature to share your code, suggested modification, and any notes/annotations

There is now a new repository, titled **Standard Conventions**, to establish standardized coding conventions for Fesslab. 

The advanced RAs with experience in coding may work on the  **disgust-style** repository. Others will continue with Assignment 1. 

----

####Things to know about Assignment 1: 
* This assignment involves several data source files that are linked by a common ID
* The subtask "locating and using ID variables..." involves identifying and resolving discrepancies caused by manual error (for example, 1grape1230 may be wrongly entered as 1grpe1230). 
* The modifications should be in the script; never change/alter the raw files
* Next week, Adam may provide us with the variable names and their corresponding full items 
* A key could be a 2 column matrix, with one side having the full variable name/response and the other side having the shortened version
* The goal is to produce a script that cleans the raw, untouched data files into a perfectly usable set for data analyses. 

----


 
 
##Meeting 2: 10/27/16, Fall 2016

####Review of DataSquad Goal: 
Train people to use tools of R for data cleaning so that they can make meaningful contributions. Build institutional memory and record keeping on Github (our source of centralized information) for future RAs.

----
####What is Rmarkdown? 
**allows you to interweave R code with ordinary text to produce well-formatted data**
* anything that happens between ``` is treated as code (shaded lines, also known as code blocks)
* anything outside code blocks is treated as text

**easy to modify**
* after slightly tweaking the code in Rmarkdown, all of your stats are automatically updated in the live document

----
####Exercise: This assignment involves merging a bunch of files and to see what nice, clean data looks like. 
* Data is from study on Trust and Social Issues. 
* B/c the programmer worked in a different program, the output files have variables with inconvenient names, and inconvenient responses.  
* Examples: (1) the response showing "1-strongly agree" when we want it to say "1" (2) the response showing "-99" when we want it to say "NA" (3) the variable named "dg1" when we want it to say "ID". 
* These discrepancies will have to be identified and corrected, so that the output files will be in a format that is convenient for our purpose. There should be a file of keys explaining what the variables mean. 

####The goal: All of these files with data should be neatly consolidated, and we should figure out how to merge the dataset (pulling out the valuable data from each of the 5 data files, and merging them together)

----
**Packages** help base r become more efficient for specific types of activities. Packages modify the working environment towards a specific interest. Tidyr and Dplyer are packages that help the data cleaning process (from raw data files to statistical analyses on publications)
####Tidyr
* written by Hadley Wickham
* http://vita.had.co.nz/papers/tidy-data.pdf
* tidying makes sure each observation is a row and each variable is a column. 
* does not change the data; the exact data is just organized differently. 
* designed to have commands that are simpler and more efficient than base r when creating tidy data files. 

####Dplyr
* comes in handy for big portion of data cleaning (like when you have 2 variables that need to become one)

----
####By next week: 
* import all 5 data files
* start writing code to clean up the project (put in at least one hour to improve code and/or improve documentation)
* figure out commands in tidyr and dplyer
* you can build your own branches, explore help communities, look for good convention to load all the packages, etc. 
* check in the Github organization periodically for updates

----
####Additional notes: 
* We are working on public repositories--be professional, keep the data private (but the code public). share data through email or possibly DropBox.  
* Make sure to write description/explanation for your code when opening a pull request
* to enable softwrap: go to Rstudio-> Preferences -> Code -> Soft-wrap R source files (you do not have to do this when using Rmarkdown)
* A useful thing to do is create a directory (the file where all the data is) when importing files. 
* Excel tries to autocorrect data files, so some alternatives to Excel are: LibreOffice, GoogleSheets 
* On Github, changes are color coded: additions are green, deletions are red
* Running certain packages may disrupt other functions or make them less efficient 

----
----

##Meeting 1: 10/20/16, Fall 2016

###2 Main Goals of Data Squad: 

####1. Documentation/record keeping; building institutional memory
* Create a functional organization to combat personnel turnover by building resource guides/instructions (so new RAs can easily adapt) 

####2. Get people to make contributions to live code as soon as possible

---
RAs will first develop R skills and then use that developing expertise to make contributions. Contributions in the form such as data cleaning (taking raw file from raw output and reorganizing it in a format) or even figuring out how to make figures blue (someone with more advanced training can benefit from these “simple” expertise b/c it will save time). RAs will document these skills to make them sustainable for future members.  

---
###The End Point: 
Archiving/curating data to make accessible to other researchers (open science framework; making things public) 

---

###Meetings:
* A regular part will be people presenting what they are working on  
* Discuss conventions for how to share and how to talk to each other (such as consistent coding styles)  
* Learn how to write excellent notes within the code, since it is important to properly annotate what the code is doing. (# or $ at beginning of line: text line (non-functional))

---
###Resources: 
* R: computational engine/programming language   
* Rstudio: graphical interface/integrated development environment; visually handy way to build scripts for R    
* Rmarkdown: package/add-on that makes it easier to produce documents in various formats (such as word doc, html, etc.) 

---
###Questions:  
* How to communicate with each other (i.e. with private information) because free Github repositories are public. Textwrangler + Email(?)  





