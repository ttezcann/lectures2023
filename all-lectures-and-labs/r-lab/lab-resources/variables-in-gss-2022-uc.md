---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: false
---

# Variables in GSS 2022 uc

## Guideline

### What is this document?

This document lists categorical and continuous variables, what they measure, the full wording and response sets of each question from the GSS dataset (2022). Variables are color coded:

### Table A. Guideline of color codes

<table data-header-hidden><thead><tr><th width="171">Color codes</th><th>It means</th></tr></thead><tbody><tr><td><mark style="background-color:red;"><strong>B</strong></mark> </td><td>Binary variable: it has two responses</td></tr><tr><td><mark style="background-color:green;"><strong>N</strong></mark></td><td>Nominal variable: it has more than two responses</td></tr><tr><td><mark style="background-color:orange;"><strong>O</strong></mark></td><td>Ordinal variable: same as nominal variable, but there is a logical order among categories</td></tr><tr><td><mark style="background-color:orange;"><strong>O</strong></mark> ✅ </td><td>✅ next to an <mark style="background-color:orange;"><strong>O</strong></mark> ordinal variable indicates that these ordinal variables could be treated as continuous</td></tr><tr><td><mark style="background-color:purple;"><strong>C</strong></mark></td><td>Continuous variable: numeric variables; real numbers</td></tr><tr><td><mark style="background-color:blue;"><strong>COMP</strong></mark> </td><td>Indicates that it can be computed together with other variables marked with a <mark style="background-color:blue;"><strong>COMP</strong></mark> in the same color. Note that the computed variable will be continuous.</td></tr><tr><td><mark style="background-color:yellow;"><strong>Recode</strong></mark> </td><td>Indicates that they should be recoded (the direction of the responses should be reversed) before computation or treating them as continuous. After recoding, the new (recoded) variables should be used in analysis.</td></tr></tbody></table>



## Table 1. Basic demographics

<table data-full-width="true"><thead><tr><th width="157">Variable name</th><th width="238">What it measures?</th><th width="128">Color codes</th><th>Full wording of the question</th></tr></thead><tbody><tr><td>age</td><td>age in years</td><td><mark style="background-color:purple;"><strong>C</strong></mark></td><td>What is your age?</td></tr><tr><td>educ</td><td>education in years</td><td><mark style="background-color:purple;"><strong>C</strong></mark></td><td>What is the highest year of school you completed?</td></tr><tr><td>degree</td><td>education degree</td><td><mark style="background-color:orange;"><strong>O</strong></mark></td><td>Do you have less than high school, high school, associate/junior college, bachelor's, or graduate degree? <strong>(0: less than high school; 1: High school; 2: Associate/junior college; 3: Bachelor's; 4: Graduate)</strong></td></tr><tr><td>coninc</td><td>family income in dollars</td><td><mark style="background-color:purple;"><strong>C</strong></mark></td><td>What is your family income in dollars?</td></tr><tr><td>conrinc</td><td>personal income in dollars</td><td><mark style="background-color:purple;"><strong>C</strong></mark></td><td>What is your income in dollars?</td></tr><tr><td>sei10</td><td>socio-economic index score</td><td><mark style="background-color:purple;"><strong>C</strong></mark></td><td>Socio-economic index score of the respondent (calculated)</td></tr><tr><td>spsei10</td><td>socio-economic index score of the respondents’ spouses</td><td><mark style="background-color:purple;"><strong>C</strong></mark></td><td>Socio-economic index score of the respondent's spouse (calculated)</td></tr><tr><td>prestg10</td><td>occupational prestige score</td><td><mark style="background-color:purple;"><strong>C</strong></mark></td><td>Respondent’s occupational prestige score (calculated)</td></tr><tr><td>sppres10</td><td>occupational prestige score of the respondents’ spouses</td><td><mark style="background-color:purple;"><strong>C</strong></mark></td><td>Respondent's spouse occupational prestige score (calculated)</td></tr><tr><td>sex</td><td>sex</td><td><mark style="background-color:red;"><strong>B</strong></mark></td><td>What’s your sex? <strong>(1: male; 2: female)</strong></td></tr><tr><td>sexornt</td><td>sexual orientation</td><td><mark style="background-color:green;"><strong>N</strong></mark></td><td>Which of the following best describes you? </td></tr><tr><td>race</td><td>race</td><td><mark style="background-color:green;"><strong>N</strong></mark>  </td><td>What’s your race? <strong>(1: white; 2: black; 3: other)</strong> </td></tr><tr><td>marital</td><td>marital status</td><td><mark style="background-color:green;"><strong>N</strong></mark> </td><td>Are you currently--married, widowed, divorced, separated, or have you never been married? <strong>(1: married; 2: widowed; 3: divorced; 3: separated; 5: never married)</strong> </td></tr><tr><td>sibs</td><td>The number of brothers and sisters respondents have</td><td><mark style="background-color:purple;"><strong>C</strong></mark></td><td>How many brothers and sisters do you have?</td></tr><tr><td>childs</td><td>The number of children respondents have</td><td><mark style="background-color:purple;"><strong>C</strong></mark></td><td>How many children do you have? </td></tr><tr><td>born</td><td>immigrant status</td><td><mark style="background-color:red;"><strong>B</strong></mark></td><td>Were you born in this country? <strong>(1: yes; 2: no)</strong></td></tr><tr><td>region</td><td>The region of residence</td><td><mark style="background-color:green;"><strong>N</strong></mark>  </td><td>The region respondents lives in <strong>(1: New england; 2: Middle atlantic; 3: East north central; 4: West north central; 5: South atlantic; 6: East south atlantic; 7: West south central; 8: Mountain; 9: Pacific)</strong> </td></tr><tr><td>dwelown</td><td>home ownership</td><td><mark style="background-color:green;"><strong>N</strong></mark> </td><td>(Do you/Does your family) own your (home/apartment), pay rent, or what? <strong>(1: Own or is buying; 2: Pays rent; 3: Other)</strong> </td></tr><tr><td>partyid</td><td>political party affiliation</td><td><mark style="background-color:green;"><strong>N</strong></mark> </td><td>Generally speaking, do you usually think of yourself as a Republican, Democrat, Independent, or what? <strong>(0: Strong democrat; 1: Not very strong democrat; 2: Independent, close to democrat; 3: Independent (neither, no response); 4: Independent, close to republican; 5: Not very strong republican; 6:Strong republican; 7: other party)</strong></td></tr><tr><td>polviews</td><td>conservatism level</td><td><mark style="background-color:orange;"><strong>O</strong></mark> ✅ </td><td>Do you think of yourself as liberal or conservative? <strong>(1: extremely liberal; 7: extremely conservative)</strong> </td></tr></tbody></table>

## Table 2. Respondents’ parents and adolescence years

<table data-full-width="true"><thead><tr><th width="164.5">Variable name</th><th width="227">What it measures?</th><th width="137">Color codes</th><th>Full wording of the question</th></tr></thead><tbody><tr><td>granborn</td><td>third generation immigrant status</td><td><mark style="background-color:orange;"><strong>O</strong></mark></td><td>Were all of your four grandparents born in this country? A. How many were born outside the United States? <strong>(0: none; 1: one; 2: two; 3: three; 4: four)</strong> </td></tr><tr><td>res16</td><td>higher population density of residence during adolescence years</td><td><mark style="background-color:orange;"><strong>O</strong></mark> ✅ </td><td>Which of the categories on this card comes closest to the type of place you were living in when you were 16 years old? (COUNTRY,NONFARM, FARM, TOWN LT 5000…) <strong>(1: country, nonfarm; 2: farm; 3: town less than 50K; 4: 50K to 250K; 5: big city, suburb; 6: city greater than 250K)</strong> </td></tr><tr><td>reg16</td><td>the region of residence during adolescence years</td><td><mark style="background-color:green;"><strong>N</strong></mark> </td><td>In what state or foreign country were you living when you were 16 years old? <strong>(0: foreign country; 1: New england; 2: Middle atlantic; 3: East north central; 4: West north central; 5: South atlantic; 6: East south atlantic; 7: West south central; 8: Mountain; 9: Pacific)</strong> </td></tr><tr><td>family16</td><td>parental cohabitation status during adolescence years</td><td><mark style="background-color:green;"><strong>N</strong></mark> </td><td>Were you living with both your own mother and father around the time you were 16? <strong>(0: other; 1: mother and father; 2: father and stepmother; 3: mother and stepfather; 4: father; 5: mother; 6: male relative; 7: female relative; 8: male and female relatives)</strong></td></tr><tr><td>incom16</td><td>self-assessment of family wealth relative to societal average during adolescence years</td><td><mark style="background-color:orange;"><strong>O</strong></mark> ✅ </td><td>Thinking about the time when you were 16 years old, compared with American families in general then, would you say your family income was--far below average, below average, average, above average, or far above average? <strong>(1: far below average; 2: below average; 3: average; 4: above average; 5: far above average)</strong></td></tr></tbody></table>



## Table 3. Quality of life - Living standards

<table data-header-hidden data-full-width="true"><thead><tr><th></th><th></th><th></th><th></th></tr></thead><tbody><tr><td>lifenow</td><td>quality of life rating</td><td>O ✅ </td><td>If you were asked to rate your overall life from 0-10, where 10 represents the best possible state and 0 represents the worst possible state, how would you rate your life today?</td></tr><tr><td>lifein5</td><td>rating of quality of life in five years</td><td>O ✅ </td><td>If you were asked to rate your overall life from 0-10, where 10 represents the best possible state and 0 represents the worst possible state, how do you think you would rate your life five years from today?</td></tr><tr><td>goodlife</td><td>the level of optimism about economic opportunity</td><td>O ✅ Recode</td><td>The way things are in America, people like me and my family have a good chance of improving our standard of living -- do you agree or disagree? (1: strongly agree; 2: agree; 3: neither agree nor disagree; 4: disagree; 5: strongly disagree)</td></tr><tr><td>finrela</td><td>attitude towards higher family income</td><td>O ✅ </td><td>Compared with American families in general, would you say your family income is far below average, below average, average, above average, or far above average?  (1: far below average; 5 far above average)</td></tr><tr><td>parsol</td><td>the level of higher living standard compared to parents</td><td>O ✅ Recode</td><td>Compared to your parents when they were the age you are now, do you think your own standard of living now is much better, somewhat better, about the same, somewhat worse, or much worse than theirs was? (1: much better; 5 much worse)</td></tr><tr><td>rank</td><td>social ranking level</td><td>O ✅ Recode</td><td>In our society there are groups which tend to be towards the top and those that are towards the bottom. Where would you put yourself on this scale? (1: top; 10: bottom)</td></tr></tbody></table>

###

## Table 4. Social life

<table data-header-hidden data-full-width="true"><thead><tr><th></th><th></th><th></th><th></th></tr></thead><tbody><tr><td>socrel</td><td>the frequency of social evening with relatives</td><td>O ✅ Recode</td><td>How often do you spend a social evening with relatives (1: almost daily; 2: once or twice a week; 3: several times a month; 4: about once a month; 5: several times a year; 6: about once a year; 7: never)</td></tr><tr><td>socommun</td><td>the frequency of social evening with neighbors</td><td>O ✅ Recode</td><td>How often do you spend a social evening with neighbors (1: almost daily; 2: once or twice a week; 3: several times a month; 4: about once a month; 5: several times a year; 6: about once a year; 7: never)</td></tr><tr><td>socfrend</td><td>the frequency of social evening with friends</td><td>O ✅ Recode</td><td>How often do you spend a social evening with neighbors (1: almost daily; 2: once or twice a week; 3: several times a month; 4: about once a month; 5: several times a year; 6: about once a year; 7: never)</td></tr><tr><td>socbar</td><td>the frequency of going to a bar</td><td>O ✅ Recode</td><td>How often do you go to a bar? (1: almost daily; 2: once or twice a week; 3: several times a month; 4: about once a month; 5: several times a year; 6: about once a year; 7: never)</td></tr><tr><td>hrsrelax</td><td>leisure time hours after work day</td><td>C</td><td>After an average work day, how many hours do you have to relax or pursue activities that you enjoy?</td></tr><tr><td>wkvsfam</td><td>the level of job interfering with family life</td><td>O </td><td>How often do the demands of your job interfere with your family life? (1: often; 2: sometimes; 3: rarely; 4: never)</td></tr></tbody></table>



## Table 5. Work



## Table 6. Quality of working life



## Table 7. Discrimination and harassment at work



## Table 8. Government spending



## Table 9. Civil liberties - Freedom of speech



## Table 10. Abortion



## Table 11. Affirmative action - concern and support



## Table 12. Religion, religiosity, and spirituality



## Table 13. Intermarriage attitudes



## Table 14. Immigration related questions



## Table 15. Happiness and satisfaction



## Table 16. Health



## Table 17. Same sex couples



## Table 18. Technology and media use



## Table 19. Confidence in institutions



## Table 20. Eldercare



## Table 21. Family and gender roles



## Table 22. Police abuse



## Table 23. Government responsibility - Opposition to social state



## Table 24. Miscellaneous



##
