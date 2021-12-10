
# Looking at the 2019 SAT/ACT scores for students in California



## Problem Statement

As an analyst for the princeton review, I was asked to conduct research on whether high schools maintained a necessary academic level for their students to succesfully take the ACT/SAT and how can we improve their skills through better developped test preps. More specifically the question asked is, does the level of academics taught in Californian high schools englobe the necessary level to succesfully study and complete the SAT/ACT and how does it compare to the rest of the nation ?

*NOTE*: This is a thought experiment, I have no affiliation with the princeton review. This was a theoretical situation to make this project as fun and realistic as possible. 


## Background information

"Despite the College Board’s description, the Writing and Language Test remains disproportionately focused on grammar, a subject that most high school students have not had the chance to master.  

Because the SAT continues to test on issues not sufficiently covered in high school, it is essential that students preparing for the SAT approach the test for what it is: a test not of their intelligence or of what they’ve learned in high school, but of a collection of certain kinds of questions that, for better or worse, serve as a gatekeeper standing between students and their college goals. "
Copy and Pasted from: https://www.eliteprep.com/blog/2017/1/3/does-high-school-prepare-students-for-the-sat

"While tests should not be the sole basis for admissions, studies show they have real predictive validity and should indeed be part of admissions processes. Pretending that all students can handle the same challenges helps nobody reach his or her full potential. Students with different preparation should attend universities that cater to different needs, and social policy should address the K-12 and home environments that result in unequal preparation for tests like the SAT and ACT."
Copy and Pasted from: https://www.latimes.com/opinion/story/2019-11-29/sat-act-tests-uc

Counter Argument from the College Board:

"There has been much talk of how colleges’ use of SAT scores places underprivileged applicants at a disadvantage. The assumption is a student cannot perform well on these tests without expensive tutors and prep classes.

This is a complete falsehood, as the College Board, which owns the SAT, makes practice tests and preparation materials available through Khan Academy for everyone to use free of charge. The only thing required is internet access (available at public libraries) and the discipline to study hard for these tests."
Copy and Pasted from: https://www.latimes.com/opinion/story/2019-11-29/sat-act-tests-uc

## Data Dictionaries

### Data dictionary for df_sat

| Feature| Type |  Description |
|---|---|---|
|county  | string  | Name of county in California |
|enroll_12  |   float64 | Enrollement of students in grade 12  |
|attended_12|float 64|Number of test takers in grade 12|
|erw_benchmark_12_%|   float64 |  Percentage of student that met or exceeded the benchmark for english, reading, and writing in grade 12|
|math_benchmark_12_%   |  float64  | Percentage of student that met or exceeded the benchmark for math in grade 12  |
|enroll_11   |  float64  | Enrollement of students in grade 11  |
|attended_11	   |  float64  |  Number of test takers in grade 12 |
|erw_benchmark_11_%  |   float64 | Percentage of student that met or exceeded the benchmark for english, reading, and writing in grade 11  |
|math_benchmark_11_%  |   float64 | Percentage of student that met or exceeded the benchmark for math in grade 12 |
|combined_benchmark_12_%  |  float64  | Percentage of student that met or exceeded the benchmark for math and english, reading, and writing for grade 12|
|combined_benchmark_11_% |   float64 | Percentage of student that met or exceeded the benchmark for math and english, reading, and writing for grade 11  |

### Data dictionary for df_act

|Feature|Type|Description|
|---|---|---|
|count|string|Name of the county in California|
|enroll_12|float64|Enrollement of students in grade 12|
|attended|float64|Number of test takers |
|avg_score_reading|float64|Average reading ccore for ACT|
|avg_score_english	|float64|Average english ccore for ACT|
|avg_score_math|float64|Average math score for ACT|
|avg_score_science|float64|Average science score for ACT|
|composite_greater_21|float64|Number of test takers that score greater or equivalent to 21 on the ACT|
|composite_greater_21_%|float64|Number of test takers that score greater or equivalent to 21 on the ACT|

### Data dictionary for sat

|Feature|Type|Description|
|---|---|---|
|state|string|Average SAT score by state|
participation_%|float64|Participation rate in percentage (i.e. 0.1=10%)|
erbw|float64|Score for evidence based reading and writing|
math|float64|Score for math|
total|float64|Total score|

### Data dictionary for act
|Feature|Type|Description|
|---|---|---|
|state|string|Average SAT score by state|
participation_%|float64|Participation rate in percentage (i.e. 0.1=10%)|
composite|float64|Total score of ACT|

## Analysis

Looking at the scatter plot representing the participation rate and total scores for both the SAT and ACT we are able to see a negative correlation between the two variables. This was further verified by taking the '.corr()' value of each data frame. What this shows is that students that apply to optional SAT/ACT schools are less likely to take it, however the few students that take the tests score relatively high. On the other hand looking at states with a high participation rate, we understand that these students are applying to universities that are asking for standardized tests. With that said, the participation rate is higher, which in turn brings the average of the total score down. Next we have seen that for the SAT, students in grade 12 have done better in english proficiency sections than math. This is not the case for grade 11. The histogram representing the distribution of student math scores for grade 11 shows a uniform distribution which shows that they do a better job at satisfying the benchmark for their grade. Overall, grade 12 and 11 scored reasonable well in english proficiency sections.The ACT shows a uniform distribution for the science and reading sections. When it comes to math we are able to see that students did not satisfy the benchmarks as well as previous sections. Looking at the box plot for grade 12, we can see that the math benchmark 50% range is much lower than the math benchmark seen in grade 11. When it comes to English proficiency, the box plot shows a similar standing for both grades. Finally, looking at the combined benchmarks for both grade 11 and grade 12, we can say that grade 11 did better on the SAT.

## Conclusions and Recommendations

Looking at both the EDA and the visualized data we can make the following conclusions. California has a strong benchmark for reading, writing, and english based sections.This was true for the SAT and ACT and for both grade 11 and grade 12. This would not of been predicted after reading the first sentence of the background section. With that said, we were able to closely examine the math section for both tests. Although the SAT scores for grade 11 appears slightly higher than for grade 12, overall math is a section Californian high schools should focus on more closely. As part of the Princeton review, in order to facilitate and help students score better on their standardized exams, here are my recommendations to be implemented if agreed upon. 

The first point to take into consideration is that the UC system and other educational institutions in California have decided to make the SAT and ACT optional tests. With that said, we can expect the participation score and the overall test scores to drop. California being the most populated state in America will have a deep impact on the Princeton review. How can we still keep our customers in the loop? First I suggest we drop our prices when it comes to tea preps. By doing so not only will we be able to interest a wider variety of students but we will be able to compete with other online services that aim in helping students, such as Khan Academy. The next suggestion I am making is the development of an online and interactive platform that will not only help the students actively study for these exams but rank them and give them the opportunity to climb the ladder. This of course, will be entirely optional, if the student deems to maintain anonymity that is entirely possible. Doing so will not only motivate the student to get better but it is also something that could be sent to Universities. By doing so, Universities will be able to explore two side of the student that is applying, the side of a student in a testing environment, and the side of a student working in a more familiar environment. Being in a more familiar environment, students will perform better, which can be reflected on their test prep. This can help students put themselves in value and further strengthen their college applications.
