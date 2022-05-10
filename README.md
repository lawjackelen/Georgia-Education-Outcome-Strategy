# Project 1: Georgia Education Outcome Strategy

### Contents:
- [Problem Statement](#Problem-Statement)
- [Executive Summary](#Executive-Summary)
- [Conclusions and Recommendations](#Conclusions-and-Recommendations)
- [Data Dictionary](#Data-Dictionary)
- [Sources](#Sources)

### Problem Statement

Our great State of Georgia is at a crossroads. Education outcomes of our schools’ students is in increasingly under the microscope and we’ve just received a huge windfall in Federal Education funding.
What actions can the administration take using that funding to move the needle on education outcomes for the better? Specifically, our college acceptance numbers?

### Executive Summary

The workbook imports SAT scores by state for the years 2017-2019 and 2019 SAT scores by intended college major. All of these datasets were cleaned and the 3 state scores datasets merged. During this phase, 'Virgin Islands' and 'Puerto Rico' data were purged due to lack of completeness as they were only present in one of the three years.
<br><br>
Exploratory data analsysis was performed where it was found that participation rates were negatively correlated with total SAT score by state; since ACT is a more popular test in some states, the dataset was refocused to the 23 states that had 50% or more participation all three years. A similar filtering happened with the college major set where only 18 of the 38 majors were kept since they had over 1% of the total test takers; this was done to ensure we were dealing with large sections of the data.
<br><br>
With both datasets filtered to a more-focused state, conclusions were able to be drawn.

### Conclusions and Recommendations

Increasing college acceptance numbers will require either a boost in test scores or a boost in test takers, the analysis focused on the latter. Boosting test takers will come with an excpected decrease in average SAT score, which could hurt us with the public. By focusing on college majors with lower average SAT scores, we can accommodate the decreased average score with increased acceptances.

Three areas of study were identified:
  *  Security and Protective Services
  *  Agriculture, AgricultureOperations, and Related Sciences
  *  Education
  
Armed with these three areas, there are 4 recommendations:<br>
- Boost SAT participation through sign-up drives and preparatory classes
- Increase interest in the identified areas through:
  *  themed classwork
  *  additional elective courses
  *  sponsored after-school programs and initiatives:
    *  Partnership with TSA in Atlanta
    *  Membership drive with 4H
    *  After-school programs and internships with Teach for America (TFA)

### Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**state**|&nbsp;*str*|sat_scores|The state in which the test scores were reported|
|**participation_rate**|*float*|sat_scores|The percent of seniors who graduated in the year being reported that participated in the exam<sup>1</sup>|
|**ebrw**|*int*|&nbsp;sat_scores, sat_2019_major|&nbsp;The average (mean) score of the SAT's "Evidence-Based Reading and Writing" portion (scale from 0-800)|
|**math**|*int*|sat_scores, sat_2019_major|The average (mean) score of the SAT's "Math" portion (scale from 0-800)|
|**total**|*int*|sat_scores, sat_2019_major|The average (mean) total SAT score (scale from 0-1600)|
|**year**|*str*|sat_scores, sat_2019_major|The year in which the test scores were reported|
|**intendedcollegemajor**|*str*|sat_2019_major|The college major a test taker intends to pursue|
|**testtakers**|*int*|sat_2019_major|The number of persons taking the test|


<font size = "1.5"> <sup>1</sup>https://blog.prepscholar.com/average-sat-scores-by-state-most-recent </font>


### Sources
2017 ACT Scores by State, 2018 ACT Scores by State, 2019 ACT Scores by State ([source](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows))<br>
2019 SAT Scores by Intended College Major ([source](https://reports.collegeboard.org/pdf/2019-total-group-sat-suite-assessments-annual-report.pdf))<br>
boom_readme ([source](https://git.generalassemb.ly/DSIR-425/project_1/blob/master/example_readmes/boom_readme.md))