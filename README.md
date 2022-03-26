# School District Analysis
Python Challenge with School District Data

# Objectives

Maria, Chief Data Scientist for the City School District, is responsible to review and analyze standardized test data, along with demographic data for the district to look for performance trends.  The standardized test data includes math and reading scores and can be separated by grade and school.  The schools range in size (student population), per capita spending and administrative type (District or Charter). Maria's analysis has been complicated by the report of academic dishonesty in ninth grade students at Thomas High School.  She has been tasked to analyze the district data with and without the data from the Thomas High School ninth graders. 

# Results

In order to handle the alleged cheating by the Thomas High School 9th graders, the math and reading scores for those students were replaced with "NaN" to indicate no valid score and to ensure that the scores were not included in the summary analytics. 

- As observed in the summary tables below, the removal of the scores of 461 students only has a small impact in the average scores and passing percentage.  These student represent 1.2% of total students tested, so removing those test scores from the analysis does not have a noticeable impact on the overall scores.

  - The district summary before removing the student scores is shown below: 
<img width="766" alt="Disctrict_summary_precorrection" src="https://user-images.githubusercontent.com/98054953/160252358-806677da-b32c-4d1b-81f6-f918ad5b9e97.png">

  - Once the scores from the Thomas High School 9th graders were removed, the district summary was recalculated: 
<img width="770" alt="District_Summary_Postcorrection" src="https://user-images.githubusercontent.com/98054953/160252375-d534f5c8-400d-47b2-8ba9-6ea120568260.png">
 
- In terms of the school summary, Thomas High School's average math and reading scores did not change much.  This result is due to replacing the ninth graders scores with a null value and not replacing them with a zero.  The students who scores were considered valid and calculated (10th-12th graders) were still high performing and, therefore, the average scores did not change much. 

- Replacing the ninth grader's math and reading scored negatively affected Thomas High School's performance relative to the other schools. Thomas High School's overall passing percentage dropped significantly by removing the scores for the ninth graders. When the scores were included, Thomas High School was one of the highest performing schools in the district (Overall Passing Percentage of 90.95%)

<img width="881" alt="BySchool_Precorrection" src="https://user-images.githubusercontent.com/98054953/160252595-104f8034-3815-4bfb-873b-28ee1c2c04bb.png">

With the removal of the ninth grade scores, Thomas High School became one of the lower performing schools (Overall Passing Percentage of 69.66%). 

<img width="884" alt="THS_including9th_graders_NaN" src="https://user-images.githubusercontent.com/98054953/160252632-646424d2-a2ba-4dc7-836c-01f1853ee38b.png">

Rerunning the school district summary for Thomas High School with just the scores from 10th to 12th graders brought the scores back to higher averages. 

- Looking at the district-wide school summaries, replacing the ninth-grade scores for Thomas High School had the following effects:
  - Math and reading scores by grade
    - For Thomas High School, the scores for 9th grade were listed as "NaN"
    - For all other schools, the scores were unchanged
  - Scores by school spending had small decrease (less than .5%) due to the small number of students 
  - Scores by school size had small decrease (less than .5%) due to the small number of students
  - Scores by school type had small decrease (less than .5%) due to the small number of students


# Summary 
The School District was concerned about the affect that the scores from the ninth grade at Thomas High School might have on the district analysis of standardized testing.  In order to evaluate the impact, the scores of the suspect tests were changed to "NaN" or a null value and then the analysis was performed again. The changes noted as a result of the change are summarized below: 

1. The overall district summary scores were not greatly impacted due to the small percentage of scores that were suspect (1.2 % of the total students). 
2. The oveerall performance of Thomas High School was greatly reduced because 25% of the school was determined to not have passing scores when the ninth grade scores were replaced. 
3. The math and reading average scores for Thomas High School 10th to 12th graders were among the best performing in the district. When the school was evaluated on just 10th to 12th grade, the overall passing percentage was over 90%. 
4. The scores, as evaluated by spending per student, school size and school type, were not significantly impacted by the removal of the suspect values. 







