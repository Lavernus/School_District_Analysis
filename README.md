# Analysis of School District
## Overview of Project
The client has created two datasets pertaining to a school district: one with information on the students, and another with information on the schools. I had already completed an analysis combining both datasets and creating summary statistics based on this, but the client uncovered academic dishonesty within the ninth graders of Thomas High School. They have requested the datasets to be edited to reflect this and new summary statistics to be calculated.
### Purpose
This analysis will be completed in python utilizing the pandas library in order to remove the ninth grade reading and math scores for Thomas High School and replace them with NaN. This new dataset will then be used to produce a district summary, a summary for each school, a school ranking by grades, and the scores of the students grouped by grade, school spending, school size, and school type. Finally, I will compare how the statistics changed after the ninth grade scores for Thomas High School were removed.
## Results
- District Summary
    - Since the only thing that was removed was the scores of the ninth graders in Thomas High School, the district summary had the base statistics remain the same, which was total schools, total students, and the total budget. However, once we get to the statistics regarding scores, such as average math score, average reading score, percent passing math, percent passing reading, and percent overall passing, we can see that all except one decreased once the ninth graders' scores were taken out. The only score statistic that did not change was the average reading score, or at least the change was so small it became insignificant. All of the changed statistics did not change by much, with the largest change being the overall passing percentage decreasing by 0.3 points. We can see this with the difference in the first district summary:

        and the new district summary :
- School Summary
    - In the school summary, we can focus on Thomas High School, since that was the only school accused of academic dishonesty. Again, only the scores were affected, so the base stats remained the same, such as school type, total students, total school budget, and per student budget. Two of the stats that did change were average math score and average reading score. The first rose by 0.06 points and the second fell by 0.05 points. The percentages of passing students were much more thrown off, with the percent passing math rising by 26.36 points, the percent passing reading rising by 27.65 points, and the overall percent passing rising by 25.87. 
- Thomas High School in Relation
    - Given the large difference between the new overall percent passing and the old one, it is no surprise that Thomas High School reflects this in the school rankings. With the old passing percentage, Thomas High School was ranked 8th compared to other schools with 65.08% of their students passing both math and reading. 

        With the new passing percentage, Thomas High School ranks 2nd, with 90.63% of their students passing both math and reading.

- Grouped Scores
    - Math and Reading by Grade
        - The average math and reading scores sorted by grade for each school have a fairly straight forward change between the old data and the new data. Everything is exactly the same, except the ninth grade scores for Thomas High School have been replaced by nan. For example, the old data displays as this:

            and the new data displays as this: 
    - Scores by School Spending
        - The scores of each school were sorted into bins that separated them by how much each school spent on an individual student. Surprisingly, there was no change to the average scores and percentage of students passing based on the spending ranges. The old data appeared as this:

            and the new data appeared as this:
    - Scores by School Size
        - I then sorted the schools by how many students they had and how that impacted the score statistics. Again, there was no change between the old and new data, with the old data appearing as this:

            and the new data appearing as this:

    - Scores by School Type
        - The schools were then sorted based on what type of school they were, which was Charter or District. The score statistics based on this did not change between the old and new data, with the old data appearing as this:

            and the new data appearing as this:

## Summary
At first glance, there doesn't seem to be much difference in the district summary once the ninth grade scores for Thomas High School are taken out. However, considering that there are only 461 ninth graders at Thomas High School compared to the 39,170 total students in the district, having any change in the percentages of the passing scores could imply that the difference between that taking out those ninth graders' scores had a sizeable effect in bringing down the district averages. 

One area in the data that was hugely impacted by taking out the ninth grade scores was the school summary of Thomas High School. While the averages didn't change much, the percentages did. Each percentage increased around 27 points, which implies that the ninth grade scores were low enough that taking them out greatly increased how the entire school did. This is interesting, since you could expect academic dishonesty to mean that someone artificially increased their scores, since there would be no benefit to decreasing their score. This could make artificial success apparent if compared to the rest of the grade that seems to have done,unilaterally, badly.

Since the percentages, including the overall percentage, increased so much for Thomas High School, it is not surprising that the school rankings changed drastically as well. Going from 8th to 2nd is a drastic leap, and brings up questions as to what is causing the 9th graders in Thomas High School to do so badly if the rest of the school seems to be doing very well compared to other schools.

Finally, the scores of the entire district, when grouped by different criteria, did not seem to change at all with the ninth graders of Thomas High School removed. This is interesting since Thomas High School itself was changed so substantially, but it does imply that Thomas High School does not have enough weight to affect any change upon the statistics. This could be due to the size of their student population. 


