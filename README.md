# BHDS.2010.Assignment.3
*Final Submission - November 4th, 2025*

**Project Purpose**:
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
We will also generate an added faceted violin plot, to complement the boxplot,
and run a t-test to observe whether the difference in group averages is 
statistically significant.

Questions? 
For questions or replication inquiries, collaborators can open an Issue in this 
repository or contact the project contributors via the team’s Slack channel.

**Direct Objective of Data**:
The dataset **TextMessages.csv** records the number of text messages typed by 
participants at two different time points (Baseline and Six months) across two 
participant groups.  

**Team Members and Roles**: 
**Jona** Visualization 1 (Faceted Boxplots) + README documentation
**Anna** Visualization 2 (Faceted Bar Chart) + Summary statistics

**Raw Data Description**:
Each row represents one participant with their Group assignment (1 or 2), in
addition to the number of text messages sent at Baseline and at Six_months. 
Participant number ranges from 1 to 50, the first 25 of which belong to Group
1, and the second set of 25 belonging to Group 2. Text message counts are 
recorded as simple integer values, with the lowest overall value being 9 and the 
highest being 89. The minimum count at Baseline is 47 text messages for
Group 1, whilst the maximum is 85. For Group 2, the minimum count at Baseline is
46 while the maximum is 89. Shifts occur at the Six_months mark, where Group 1
displays a minimum of 9 and a maximum of 78, whilst Group 2 has a minimum of 46
and a maxmimum of 79. For Group 1, the mean number of text messages decreased 
from 64.84 (SD = 10.68) at Baseline to 52.96 (SD = 16.33) at Six_months, 
showing a notable reduction in messaging activity over time. For Group 2, 
the mean declined more modestly, from 65.60 (SD = 10.84) at Baseline to 61.84 
(SD = 9.41) at Six_months, indicating greater stability in texting behavior 
compared with Group 1.

**Instructions to Run the Code**:
1. Clone or download this GitHub repository onto your local computer.
2. Open the project folder in RStudio.
   -> Clone or download this GitHub repository onto your local computer using:
   File -> New Project -> Version Control -> Git, then paste the repository URL:
   git clone https://github.com/hippkap/BHDS.2010.Assignment.3.git
3. Ensure that the file TextMessages.csv is located in the main project 
directory.
4. Begin by installing the required packages if not already installed via:
install.packages(c("tidyr", "ggplot2", "dplyr"))
5. Load the libraries and their dependencies via:
library(dplyr)
library(tidyr)
library(ggplot2)
6. Run each script in sequence:
  * Visualization 1: Faceted Boxplot (Jona's code)
  * Bonus Plot: Faceted Violin plot (Jona's code)
  * Visualization 2: Faceted Bar Charts (Anna's code)
  * Summary Statistics: Descriptive summary table by Group and Time
  * T-test: Assessment of significance (Anna's code)
7. Each visualization will appear in Plots pane.
8. Once all code runs successfully, knit the file Assignment3_2.Rmd to PDF, to
produce the final compiled report.

**Version Control Workflow**: 
1. A repository was created on GitHub under Anna's account. A link was sent over
to Jona to join the repository. Anna populated the BHDS.2010.Assignment.3 folder
with the base of the Assignment3.Rmd file, in addition to uploading the 
TextMessages.csv, the base of the README.md file.
2. Jona joined as a collaborator and also cloned the repository into RStudio. 
3. Within the main branch, Anna provided the preliminary code for the 
text_long object creation, reshaped the data from wide to long format (in order
to allow for easier group and time comparisons using ggplot2), and outputted
the faceted bar-chart of text messages by Group and Time. Anna committed her 
work and pushed her changes into the cloud. 
4. Jona pulled the changes into her RStudio. Tasked with creating the 
faceted boxplot of text messages by Group and Time (Visualization 1), Jona
created the object "text" to read the TextMessages.csv file onto, followed
by running the names() and glimpse() commands, to ensure that the data
was properly loaded, and that the variable titles were explicitly laid out, for
proper coding. The Baseline and Six_months variables were converted into 
numeric format, while Group and Time were treated as factors, to facilitate
comparisons. The data was re-shaped from wide to long for the boxplot visual, 
as well. Interpretations of the faceted boxplot were also included. 
5. Within the main branch, Jona added introductory commentary to the codes
being run, regarding package installations and libraries, and missing
package titles were filled in. Additional commentary was made surrounding
the boxplot coding, and the resulting changes were committed as part of 
the main branch and pushed into the hub. 
6. Within a "Boxplot_Visualization" branch, Jona ran the boxplot code once more,
and amended the interpretation, allowing it to serve as a "succinct baseline"  
before an additional joint numeric-and-descriptive summary is attached, 
following the barchart and summary stats are generated. Changes in this branch
were committed and pushed into the hub. The merge pull request was successfully
managed, with commit ee4a18c merged into the main branch, and the 
BoxPlot_Visualization branch deleted. 
7. Anna created a separate branch, titled "BarChart_and_SummaryStats", wherein
commentary on Visualization 2 was incorporated, alongside interpretation of the 
summary statistics. Additional amendments were made to the pivoting/data
transformation/mutating coding, for streamlining purposes. Changes within 
this branch were committed, pushed into the hub, and a merge pull request
was successfully managed, with commit 32ec5d7 merged into the main branch,
and the BarChart_and_SummaryStats branch deleted. 
8. Anna submitted a conclusion/comprehensive paragraph for all of the findings
across the graphics and summaries, within the main branch. 
9. Jona added assignment title/header section, alongside assignment objectives.
Under a separate branch, titled "Bonus_Plot," Jona included commentary prior
to generating a violin plot to describe its usefulness/purpose in visualization,
followed by the plot-code itself, followed by the interpretation of the violin 
plot's distribution. This plot is intended to expand on the nuances of the 
boxplot's demonstration. Changes within this Bonus_Plot branch were committed,
pushed into the hub, and a merge pull request was successfully managed (with no
errors), with commit 6b3be04 merged into the main branch, and the Bonus_Plot
branch deleted. Jona also made syntactical/aesthetic changes to the document, 
pushing these adjustments out into the hub. 
10. Under a separate branch titled "T_test", Anna conducted a paired-samples
analysis and included interpretive commentary, strengthening the conclusions
drawn from the various visual and statistical summaries prior. Changes within
this "T_test" were committed and pushed into the hub, and a merge pull 
request was successfully managed (with no errors), with commit 75a13fe merged
into the main branch, and the T_test branch deleted. The changes were pulled
into the main branch, wherein Jona added additional details regarding  
reflections and specific branch names involved in each section. 
11. After all branches were merged, both collaborators pulled the latest main 
branch to ensure all local copies were synchronized with the repository.
12. With every section complete and all warning messages being suppressed,
the rmd was knit into a finalized, reproducible pdf report. 

**Commit and Pull Request Protocol**
- Each collaborator committed changes frequently, using clear and descriptive
messages (e.g. "added packages/installation code that was missing; rearranged 
t-test summary to place it before the conlcusion; added branch-titles prior to 
every section (corrected brach typo); added reflections"). 
- All commits were pushed to the remote repository before initiating pull 
requests. 
- Each pull request included a summary of the changes and was reviewed by 
the collaborator prior to merging. 
- Merge conflicts did not occur in these instances, but all changes were
checked and confirmed locally before final approval. 

**Summary of Results**:
Both the faceted box-plots and bar-charts visualize how the number of text 
messages varied across groups, and over time. The distributions indicate that
participants in both groups sent a similar number of text messages at 
Baseline as they did at Six_months, with only a slight reduction in the median
and variability over time. The box-plots show slightly tighter interquartile 
ranges at the Six-month mark, suggesting that participants' texting behavior
became more consistent. These trends are confirmed by the summary statistics,
which reveal that Group 1 experienced a more pronounced decline (from an average 
of 64.84 messages at Baseline (SD = 10.68) to 52.96 at Six_months (SD = 16.33)).
Group 2 demonstrated higher stability, decreasing only slightly from 65.60 
(SD = 10.84) to 61.84 (SD = 9.41). The accompanying violin plots further 
illustrate this patter by highlighting a narrower, more compact distribution
of values at Six_months, reflecting reduced variability. Collectively, the 
graphical and numerical results suggest that texting activity remained 
relatively steady across the observation period, though a mild overall decline 
and increased uniformity in participant behavior emerged over time, with Group 1 
showing the greater reduction. The paired t-test results revealed that Group 1’s 
decrease in texting frequency was statistically significant (p = 0.0024), 
whereas Group 2’s smaller reduction was not (p = 0.0559). This suggests that 
the observed decline in Group 1 reflects a genuine behavioral change over time, 
while Group 2’s messaging patterns remained comparatively stable.

**Concluding/Additional Remarks and Notes**:
This collaborative project not only reinforced our understanding of R’s data 
visualization capabilities but also demonstrated effective teamwork and version 
control through GitHub. We learned to manage branches, assess merge conflicts, 
and maintain clean commit histories while ensuring code reproducibility. The 
integration of several visualizations in addition to summary statistics 
provided a comprehensive view of the statistical trends and subtle behavioral 
shifts within the dataset. We decided to include a violin plot to further
emphasize the distributional "landscape" of the data, in addition to the 
required boxplot. We also decided to run a t-test on the data, to assess
whether the difference in group averages is statistically significant, adding an
inferential dimension to our descriptive findings. This analytical extension 
strengthened the project’s rigor by confirming that Group 1’s decline in texting
behavior was significant while Group 2’s change was not. Altogether, this 
assignment deepened our appreciation for how reproducible research practices 
such as proper documentation, version control, and peer review—contribute to 
clarity, accuracy, and teamwork in data science.


