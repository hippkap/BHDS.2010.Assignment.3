# BHDS.2010.Assignment.3

Project Purpose:
The purpose of this assignment is to provide an opportunity for us to practice 
using GitHub to share, collaborate, and manage changes in an RStudio Project. 
We will to collaboratively analyze a dataset using RStudio and GitHub. 
Each user will have a specific role and contribute to the project using 
branching, committing, and pull requests. We will be working with the data found
in the file TextMessages.csv. We will create two visualizations; 
1) a stratified boxplot of text messages by Group and Time, 
2) stratified bar charts of text messages Group and Time. 
Additionally, we will create summary statistics of Text Messages by Group and 
Time, and update this README.md file with activity details and instructions.

Direct Objective of Data:
The dataset **TextMessages.csv** records the number of text messages typed by 
participants at two different time points (Baseline and Six months) across two 
participant groups.  

Team Members and Roles: 
**Jona** Visualization 1 (Faceted Boxplots) + README documentation
**Anna** Visualization 2 (Faceted Bar Chart) + Summary statistics

Data Description:
Each row represents one participant with their Group assignment (1 or 2), in
addition to the number of text messages sent at Baseline and at Six_months. 
Participant number ranges from 1 to 50, the first 25 of which belong to Group
1, and the second set of 25 belonging to Group 2. Text message counts are 
recorded as simple integer values, with the lowest overall value being 9 and the 
highest being 89. The minimum count at Baseline is 47 text messages for
Group 1, whilst the maximum is 85. For Group 2, the minimum count at Baseline is
46 while the maximum is 89. Shifts occur at the Six_months mark, where Group 1
displays a minimum of 9 and a maximum of 78, whilst Group 2 has a minimum of 46
and a maxmimum of 79. 

Instructions to Run the Code:
1. Clone or download this GitHub repository onto your local computer.
2. Open the project folder in RStudio.
3. Ensure that the file TextMessages.csv is located in the main project 
directory.
4. Begin by installing the required packages if not already installed via:
install.packages(c("tidyverse", "readr", "ggplot2", "dplyr"))
5. Load the libraries and their dependencies via:
library(dplyr)
library(tidyverse)
library(ggplot2)
6. Open and run each team member's R Script
7. 


?. The final reproducible report can be knit to PDF to generate the compiled
analysis. 



Version Control Workflow: 
1. A repository was created on GitHub under Anna's account. A link was sent over
to Jona to join the repository. Anna populated the BHDS.2010.Assignment.3 folder
with the base of the Assignment3.Rmd file, in addition to uploading the 
TextMessages.csv, the base of the README.md file.
2. Jona joined as a collaborator and also cloned the repository into RStudio. 
3. Within the main branch, Anna provided the preliminary code for the 
text_long object creation, reshaped the data from wide to long format (in order
to allow for easier group and time comparisons using ggplot2), and outputted
the faceted bar-chart of text messages by Group and Time. 
4. Anna committed her work and pushed her changes into the cloud. 
5. Jona pulled the changes into her RStudio. Tasked with creating the 
faceted boxplot of text messages by Group and Time (Visualization 1), Jona
created the object "text" to read the TextMessages.csv file onto, followed
by running the names() and glimpse() commands, to ensure that the data
was properly loaded, and that the variable titles were explicitly laid out, for
proper coding. The Baseline and Six_months variables were converted into 
numeric format, while Group and Time were treated as factors, to facilitate
comparisons. The data was re-shaped from wide to long for the boxplot visual, 
as well. Interpretations of the faceted boxplot were also included.
6. Within the main branch, Jona added introductory commentary to the codes
being run, regarding package installations and libraries. The resulting changes
were committed as part of the main branch and pushed into the hub. 
7. With the "Boxplot_Visualization" branch, Jona ran the boxplot code once more,
and amended the interpretation, allowing it to serve as a "succinct baseline"  
before an additional joint numeric-and-descriptive summary is included, after
the barchart and summary stats are generated. Changes within this branch
were committed and pushed into the hub. 

Summary of Results:
Both the faceted box-plots and bar-charts visualize how the number of text 
messages varied across groups, and over time. The distributions indicate that
participants in both groups sent a similar number of text messages at 
Baseline as they did at Six_months, with only a slight reduction in the median
and variability over time. The box-plots show slightly tighter interquartile 
ranges at the Six-month mark, suggesting that participants' texting behavior
became more consistent. These trends are confirmed by 


Concluding Remarks:

Notes:

