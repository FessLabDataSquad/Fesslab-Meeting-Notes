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
