# School_District_Analaysis
## Overview 
After completing the school district analysis for Maria and her supervisor, they were notified by the school board that the [students_complete.csv](https://github.com/Bulzeye89/School_District_Analaysis/blob/main/Resources/students_complete.csv) contained data for which there was of evidence of academic dishonesty.  Specifically, math and reading grades for the ninth graders at Thomas High School are in question.  In order to uphold state-testing standards, they have asked Maria to remove these students grades while keeping the rest of the data intact.  Maria in turn, has asked me to replace these students grades with Nans and repeat the analysis to discover if this potential academic dishonsesty has any impact on the results.  



## Results
After refactoring the original code to replace Thomas High school ninth graders reading and math scores, we reviewed the results and saw that was only miniscule changes.  The image shows the district summary dataframe with the scores included,  

<img src="https://github.com/Bulzeye89/School_District_Analaysis/blob/main/Resources/Module%20District_Summary_df.png">
<br>
<br>
while this second image is the district summary dataframe with the scores changed to Nans.
<br>
<br>
<img src="https://github.com/Bulzeye89/School_District_Analaysis/blob/main/Resources/Challenge%20District_summary_df.png">

<br>
<br>

The school summary saw similar miniscule changes that can be seen below.
<p float="left">
<img src="https://github.com/Bulzeye89/School_District_Analaysis/blob/main/Resources/Module%20per%20school%20summary%20df.png" width=40% height=50%>
<img src="https://github.com/Bulzeye89/School_District_Analaysis/blob/main/Resources/Challenge%20per%20school%20summary%20df.png" width=40% height=50%>
</p>

<br>
<br>

The results also slightly affected, by fractions of a percentage, the following:
- Math and reading scores for 9th grade
- Scores for medium school size when filtering by school size
- Scores for charter schols when filtering by school type 
<br>

In addition, when running the following code:
    
    '# Sort and show top five schools.
        top_schools = per_school_summary_df.sort_values(["% Overall Passing"], ascending=False)
        top_schools.head()

The removal of 461 9th grade Thomas High students' scores being changed to NaNs similarly resulted in fractional percentage differences, but Thomas High School still remained the 2nd school overall.  



## Summary: 
In an effort to uphold state testing standards in light of the evidence of academic dishonesty, only small fractional percentage changes were made that ultimately had no significant change to results of the data.  The school board can be advised that the 9th grade students from Thomas High School reading and math scores have been removed.  With the removal of the data, Thomas High still ranked second out of all the schools while other insights of the analysis held true and and virtually almost unchanged such as the district's overall scores, 9th grade overall scores, school sizes scores, and charter school scores.  In addition, I would like to note that while the scores of the 9th grade Thomas High students were changed to Nans, their count was not deducted from overall student count column as this would have affected other things suchs as per student budget.  


