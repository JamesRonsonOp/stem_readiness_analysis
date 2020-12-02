# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Standardized Test Analysis


### Problem Statement

This project aims to use ACT testing scores for Math and Science from 2019 to analyze California’s current ability to produce college ready STEM graduates in regard to national standing and local output while highlighting a few of the districts that may struggle to produce adequate achievement in Math and Science.

The project will answer three questions: Where does California stand in producing college ready STEM graduates? In what regions can we diversify and improve our college ready STEM population and how do we improve those regions?

--

### Background

Governor Gavin Newsome and The State Superintendent of Public Instruction Tony Thurmond have emphasized that The State of California needs to improve upon California’s past successes in STEM education. STEM industries that rely on a foundation of talent knowledgable in Science, Technology, English and Math (STEM) are an important part of California's economy and future. Historically, the state has been known as a national and internationl leader in STEM education and industry. It is Governor Newsome’s desire to tighten focus on that strength and to compound the state’s prowess in STEM.

Using the ACT test as a benchmark the state would like a report on the state’s current position nationally in producing college ready graduates into STEM programs. Governor Newsome would like additional analysis featuring district profiles that may struggle to achieve high standards of college readiness in STEM. These findings will be presented to the California STEAM Symposium in December, 2020. so that they may be able to relate these findings to Local Education Agencies (LEA’s) for the use of these findings when constructing their Local Control and Accountability Plans.

##### Background on the ACT

The ACT is a standardized test that is often required for admission into many colleges and universities in the United States. The ACT is particularly friendly for measuring STEM readiness because it offers both a math and science portion of the test.

https://www.act.org/content/act/en.html

##### Recent STEM initiatives of Governor Newsom are detailed here:

Governor Newsom proposes new investments into math and science teachers

https://www.ppic.org/blog/governor-newsom-proposes-new-investments-in-math-and-science-teachers/ 

Newsom proposes 1 Billion dollars to tackle teacher shortages

https://edsource.org/2020/california-governor-proposes-nearly-1-billion-to-end-teacher-shortage/621952 

"The governor’s office will use data on student access to technology and STEM education... to help create the plan with the help of the new computer science coordinator.'

https://edsource.org/2019/state-budget-proposal-would-fund-computer-science-czar-broadband-expansion/612434


##### Background on the STEAM Symposium

The California Steam Symposium brings together thousands of educators, administrators, industry representatives and philantropists to discuss best practices and implementation for advancing STEM education in California.  

https://web.cvent.com/event/d4865dc7-c884-458a-b52b-776b799d6ad0/websitePage:c5e8e93a-c9f7-42ea-afa7-09b89fb06b28?RefId=steamcalifornia.org

--

## Data Dictionary for California Data Set

|Feature|Type|Dataset|Description|
|---|---|---|---|
|school|object|CA State ACT Data 2019|The smallest categorical value. A school is within a CA district|
|district|object|CA State ACT Data 2019|A collection of one or more schools in close regional proximity|
|county|object|CA State ACT Data 2019|A collection of districts in close regional proximity|
|g12_enroll|float|CA State ACT Data 2019|Number of students enrolled in G12 per Local Education Agency (LEA)|
|num_tested|float|CA State ACT Data 2019|Number of students tested per Local Education Agency (LEA)|
|avg_read|float|CA State ACT Data 2019|Average per school score for reading portion of ACT|
|avg_eng|float|CA State ACT Data 2019|Average per school score for english portion of ACT|
|avg_math|float|CA State ACT Data 2019|Average per school score for math portion of ACT|
|avg_sci|float|CA State ACT Data 2019|Average per school score for science portion of ACT|
|num_21_plus|float|CA State ACT Data 2019|Number per school of ACT composite score greater than 21|
|pct_21_plus|float|CA State ACT Data 2019|Percent per school of ACT composite score greater than 21|

--

## Data Dictionary for National Data Set

|Feature|Type|Dataset|Description|
|---|---|---|---|
|state|object|National ACT Data 2017 and 2019|U.S. States participating in ACT tests|
|participation|float|National ACT Data 2017 and 2019|ACT participation rates for U.S. States|
|avg_eng|float|National ACT Data 2017 and 2019|AVG per state score for english portion of ACT|
|avg_math|float|National ACT Data 2017 and 2019|AVG per state score for math portion of ACT|
|avg_read|float|National ACT Data 2017 and 2019|AVG per state score for reading portion of ACT |
|avg_sci|float|National ACT Data 2017 and 2019|AVG per state score for science portion of ACT|
|composite|float|National ACT Data 2017 and 2019|Ave composite score per state|
|year|int|National ACT Data 2017 and 2019|Year of participation in ACT| 

--

## Findings on Trends in CA ACT Data

#### District Level Analysis

While investigating the data I decided to focus on the district level in my research. I felt the school level was too vast considering the scope of this project and the County level, although rich with data, may not be targeted enough. I assumed that if I found something interesting I could dive down to school level data or jump up to county level and if provided more time it would likely be fruitful to do both. 

#### District Size and Poor Performance
In the district level data it was hard to observe any notable relationship within the initial features of the dataframe. I did notice that there was a pretty significant spread in average scores so I decided to drop down to the lowest levels of scores to find relationships. After drilling down to 21 districts who scored below the 10th percentile in both math and science I found that they seemed to mostly be smaller schools and largely in rural districts and some in economically disadvantaged districts. If I spent more time on this I would look at more segments of the population including the upper 10 percent and the middle 50 percent among others. 

--

## Findings on Trends in National ACT Data

* Looks to be a strong negative correlation between avg scores and participation.This matches up with the anecdotal evidence.
* English math and reading are very highly correlated with each other. 
* Science is significantly less correlated to the other scores but an elevated correlation does exist. 

--

## Conclusions and Recommendations Regarding the California State Notebook

When LAU was included in the Averages there seemed to be no relationship between large and small. After LAU was eliminated the largest 6 to 10 districts failed to reach the mean average but somehow the regression line showed up upward relationship with larger districts. It is my theory that districts in the 1000 to 3500 12th grade enrollment range have a higher average score and that once districts exceed that range score tends to decrease. It is also seen in the under 3500 chart that smaller districts are more plentiful but also have a bit a drag on the average score. 

When you drive down to the school level as does the chart only analyzing LAU does you begin to see a story of small schools driving down the average. So we have two trends, small districts seem to be driving down the score and small schools in large districts seem to be driving down the score. 

I need to dig more into this but most of the smaller districts come from rural and industrial areas and the small schools in the large districts likely come from impoverished areas in their respective districts. Due the size of the education system at the county and district levels these schools and districts may be being overlooked. 

Because of this it is recommended that the State of California reconsider it's districting to account for size and special needs of underprivileged or rural schools. 

--

## Conclusions and Recommendations Regarding National Notebook

The National ACT data is used here to supplement an analysis on California State Data. Therefore a broad-based analysis is not warranted in this notebook. In light of that, however, it is seen by studying California's position in Math and Science ACT scores in 2017 and 2019 that California ranks near the top in terms of average score. Anecdotal evidence indicates that this is due to california's low testing percentage (23%). Anecdotal evidence also indicates that as testing percentage increases average score decreases. Therefore, if California tested at the same rate as its peers (some testing as high as 100 percent) the state would likely see it's average score decrease. 

There is also room for improvment in regards to current national standing. California is widely viewed as a national and international leader in STEM industries yet ranks 15th overall in Math and Science ACT scores.

--

## Datasets


* [`act_2017.csv`](./data/act_2017.csv): 2017 ACT Scores by State ([source](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows))
* [`act_2019_part.csv`](./data/act_2019_part.csv): 2019 ACT Scores by State with Participation Rates ([source](https://nces.ed.gov/programs/digest/d19/tables/dt19_226.60.asp)
* [`sat_2019_ca.csv`](./data/sat_2019_ca.csv): 2019 SAT Scores in California by School ([source](https://www.cde.ca.gov/ds/sp/ai/) | [data dictionary]

--

## Outside Research

Average ACT Scores Drop As Participation Increases:
https://www.insidehighered.com/news/2016/08/24/average-act-scores-drop-more-people-take-test

ACT Scores in Ohio Drop as Participation Rate Increases as a result of a mandate:

"the changes can be attributed largely to the increasing number of students taking the test. Among the class of 2017, ACT estimates that 75 percent took the test. But thanks to a change in state policy that required all juniors to take either the ACT or the SAT, this year’s percentage was much higher."

https://fordhaminstitute.org/ohio/commentary/ohios-average-act-score-dropped-thats-not-bad-thing


California Ranked 16th from bottom in overall education spending
https://www.governing.com/topics/education/gov-education-funding-states.html

California's participation rate in ACT for 2019 is 23%
https://www.act.org/content/dam/act/unsecured/documents/National-CCCR-2019.pdf

"California’s future STEM educator pipeline may be in danger—only 273 students planned to enter math education, and only 96 science education."

Moreover, "the future of STEM qualified candidates looks potentially weak as well."

"Research indicates only 20% of students had both an expressed and measured interest in a STEM career." (their ACT Interest Inventory score pointed to a STEM field).
https://www.act.org/content/dam/act/unsecured/documents/STEM/2017/California-State-of-STEM-2017.pdf

ACT test takers who are interested in STEM, scored around 50 % higher on college readiness benchmarks than test-takers not interested in STEM. 
https://www.act.org/content/dam/act/unsecured/documents/National-CCCR-2019.pdf

Create Culture and use Family STEM Nights was inspired by:
https://www.earlymathca.org/engaging-families-in-early-math-a-f


---

