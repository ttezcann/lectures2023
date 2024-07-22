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

# Interpretation templates

## <mark style="color:orange;">Reminder:</mark>

Ensure that your interpretations are clear enough for someone to understand your report **without** referring to the tables.

Use "[Variables in GSS](https://ttezcan.gitbook.io/lect/all-lectures-and-labs/r-lab/lab-resources/variables-in-gss-2022-uc)" document, read the full wording of the questions,  response sets, and use "What it measures" columns in your interpretations,&#x20;

<figure><img src="../../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

<mark style="color:green;">Correct:</mark> <mark style="color:orange;">The perceived discrimination at work because of age</mark> <mark style="color:orange;">variable</mark> shows that 7.93% of the respondents feel discriminated at work because of age and 92.07% do not.

<mark style="color:red;">Wrong:</mark> “The <mark style="color:orange;">wkageism</mark> shows that 7.93% of the respondents reported that they feel discriminated and 92.07% reported that they do not feel discriminated.

* Do not use variable names in the interpretation. Variable names are meant for coding purposes. There's no word called "wkageism." No one would understand what you mean.

<mark style="color:red;">Wrong:</mark> the <mark style="color:orange;">r feels discriminated because of age</mark> shows that 7.93% of the respondents reported that they feel discriminated and 92.07% reported that they do not feel discriminated.

* Do not use the text appears on the top of the table. No one would understand what you mean by "r" here

## Frequency tables

[Frequency tables](#user-content-fn-1)[^1] are for [categorical variables](#user-content-fn-2)[^2]

<pre class="language-r"><code class="lang-r"><strong>frq(gss$<a data-footnote-ref href="#user-content-fn-3">marital</a>, out = <a data-footnote-ref href="#user-content-fn-4">"v"</a>)
</strong></code></pre>

<figure><img src="../../../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
[The marital status variable](#user-content-fn-5)[^5] shows that 41.43%[^6] of the respondents are married;[^7] 7.23% of the respondents are widowed; 17.23% of the respondents are divorced; 2.92% of the respondents are separated; 31.20% of the respondents are never married.
{% endhint %}

Slides: [descriptive statistics](https://docs.google.com/presentation/d/1\_rePJrPIl7rwTEy3pfbrZopgWMFoamw0/edit?usp=sharing\&ouid=100179871492576617561\&rtpof=true\&sd=true)

***

## Descriptive tables 1

[Descriptive tables](#user-content-fn-8)[^8] are for [continuous variables](#user-content-fn-9)[^9].

<pre class="language-r"><code class="lang-r">descr(gss$<a data-footnote-ref href="#user-content-fn-10">age</a>, out = "v", show = "short")
</code></pre>

<figure><img src="../../../.gitbook/assets/image (46).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
The age in years variable shows that the average age of the respondents is 49.18, with standard deviation 17.97.
{% endhint %}

Slides: [descriptive statistics](https://docs.google.com/presentation/d/1\_rePJrPIl7rwTEy3pfbrZopgWMFoamw0/edit?usp=sharing\&ouid=100179871492576617561\&rtpof=true\&sd=true)

## Descriptive tables 2 (for computed variables)

```r
descr(gss$hapindex, out = "v", show = "short")
```

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Indicate the highest possible score in your interpretation <mark style="color:red;">➜ "Out of 3", "Out of 5", etc.</mark>

Indicate the full name of the index variable:

<mark style="color:green;">Correct:</mark> The happiness index score of the GSS respondents is 2.10 out of 3, with standard deviation 0.47.

<mark style="color:red;">Wrong:</mark> The hapindex score of the GSS respondents is 2.10 out of 3, with standard deviation 0.47.

{% hint style="info" %}
The happiness index score of the GSS respondents is 2.10 out of 3, with standard deviation 0.47.
{% endhint %}

***

## Chi-square (example 1)

We utilize crosstabs for chi-square analysis, which is used to discover if there is a relationship between two categorical variables (we check the p value). We refer to statistically significant as p < 0.05. The Chi-Square Test can only compare categorical variables.&#x20;

```r
sjt.xtab(gss$sex, gss$health, show.row.prc = TRUE)
```

Independent variable first (sex), dependent variable second (health)

<figure><img src="../../../.gitbook/assets/image (5) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Respondents' sex has NO effect on the condition of health since the p value is HIGHER than 0.05. We can conclude that males and females have similar health conditions.
{% endhint %}

Slides: [chisquare](https://docs.google.com/presentation/d/11QlkxBoIM\_-wIoBTLYtdXxaELvX664VD/edit?usp=sharing\&ouid=100179871492576617561\&rtpof=true\&sd=true)

## Chi-square (example 2)

We utilize crosstabs for chi-square analysis, which is used to discover if there is a relationship between two categorical variables (we check the p value). We refer to statistically significant as p < 0.05. The Chi-Square Test can only compare categorical variables.&#x20;

```r
gss$agenew <- rec(gss$age, rec = 
"18:39=1 [18-39 age group];
40:59=2 [40-59 age group]; 
60:89=3 [60-89 age group]", append = FALSE)


sjt.xtab(gss$agenew, gss$health, show.row.prc = TRUE)
```

Independent variable first (agenew), dependent variable second (health)

<figure><img src="../../../.gitbook/assets/image (6) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Age groups have an effect on the condition of health since the p value is LESS than 0.05. We can conclude that age groups have substantially different health conditions.
{% endhint %}

Slides: [chisquare](https://docs.google.com/presentation/d/11QlkxBoIM\_-wIoBTLYtdXxaELvX664VD/edit?usp=sharing\&ouid=100179871492576617561\&rtpof=true\&sd=true)

***

## T-test (example 1)

A t-test is used to determine if there is a significant difference between the means of two groups. A t-test is used when we wish to compare two means (the scores must be continuous).&#x20;

```r
t.test(conrinc ~ sex, data = gss) %>% 
  parameters() %>% 
  display(format="html")
```

Dependent variable first (conrinc), independent variable second (sex)

<figure><img src="../../../.gitbook/assets/image (7) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
The average personal income in dollars of males is $49,306, while the average personal income in dollars of females is $35,277. personal income in dollars differs by respondents' sex in a statistically significant way since the p-value is LESS than 0.05
{% endhint %}

Slides: [ttest](https://docs.google.com/presentation/d/11hFYVZ3y8pig6n8SkDDnZYk\_AoqY2-t9/edit?usp=sharing\&ouid=100179871492576617561\&rtpof=true\&sd=true)

## T-test (example 2)

A t-test is used to determine if there is a significant difference between the means of two groups. A t-test is used when we wish to compare two means (the scores must be continuous).&#x20;

```r
t.test(educ ~ sex, data = gss) %>% 
  parameters() %>% 
  display(format="html")
```

Dependent variable first (educ), independent variable second (sex)

<figure><img src="../../../.gitbook/assets/image (8) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
The average education in years of males is 14.08 year, while the average education in years of females 14.15 year. Education in years does not differ by respondents' sex in a statistically significant way since the p-value is HIGHER than 0.05
{% endhint %}

Slides: [ttest](https://docs.google.com/presentation/d/11hFYVZ3y8pig6n8SkDDnZYk\_AoqY2-t9/edit?usp=sharing\&ouid=100179871492576617561\&rtpof=true\&sd=true)

***

## Bar graph (for categorical variables)

```r
plot_frq(gss$marital, type = "bar", geom.colors = "#336699")
```

<figure><img src="../../../.gitbook/assets/image (37).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Same as frequency table interpretation

\
[The marital status variable](#user-content-fn-11)[^11] shows that 41.43%[^12] of the respondents are married;[^13] 7.23% of the respondents are widowed; 17.23% of the respondents are divorced; 2.92% of the respondents are separated; 31.20% of the respondents are never married.
{% endhint %}

Slides: [visualization](https://docs.google.com/presentation/d/1j8vQxVYCuG0s96EtUgcvMJoB5jN3wgV5iS-xgMyZKtk/edit?usp=sharing)

## Histogram (for continuous variables)

```r
plot_frq(gss$educ, type = "hist",show.mean = TRUE, show.mean.val = TRUE, normal.curve = TRUE, show.sd = TRUE, normal.curve.color = "red")
```

<figure><img src="../../../.gitbook/assets/image (38).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Same as descriptive table interpretation

The education in years variable shows that the average education in years of the respondents is 14.11, with standard deviation 2.89.
{% endhint %}

Slides: [visualization](https://docs.google.com/presentation/d/1j8vQxVYCuG0s96EtUgcvMJoB5jN3wgV5iS-xgMyZKtk/edit?usp=sharing)

***

## Stacked bar graphs for multiple variables

```r
graph <- gss %>%
  select (conbus, coneduc, confed, conmedic, conarmy, conjudge) %>%
  plot_stackfrq(sort.frq = "first.asc", coord.flip = FALSE, geom.colors = "Blues", show.total = FALSE,
                title = "Confidence in major US institutions")

# the second part of the code is to change font sizes

graph + theme(
  axis.text.x = element_text(size=14), # change font size of x-axis labels
  axis.text.y = element_text(size=14), # change font size of y-axis labels
  plot.title=element_text(size=20), # change font size of plot title
  legend.text = element_text(size=14)) # change font size of legend
```

<figure><img src="../../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
When interpreting stacked bar graphs, we generally interpret one response

\
Of the GSS respondents, 44.2% have a great deal of confidence in the military; 33.4% have a great deal of confidence in medicine; 18.2% in education, 16% in the supreme court; 14.1% in major companies, and 10.4% in the executive branch of government.
{% endhint %}

Slides: [visualization](https://docs.google.com/presentation/d/1j8vQxVYCuG0s96EtUgcvMJoB5jN3wgV5iS-xgMyZKtk/edit?usp=sharing)

***

## Stacked bar graphs by different groups

```r
plot_xtab(gss$dependentvar, gss$independentvar, show.total=FALSE, show.n = FALSE)
```

<figure><img src="../../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
30.2% of the 18-39 age group, 32.1% of the 40-59 age group, 38.3% of the 60-89 age group have a great deal of confidence in medicine.
{% endhint %}

Slides: [visualization](https://docs.google.com/presentation/d/1j8vQxVYCuG0s96EtUgcvMJoB5jN3wgV5iS-xgMyZKtk/edit?usp=sharing)

***

## Correlation analysis table

Correlation analysis examines the linear relationship of two continuous variables.

IF the p-value is statistically significant (<0.05);

* .1 < | r | < .3 … weak correlation
* .3 < | r | < .5 … moderate correlation
* .5 < | r | ………. strong correlation

```r
tab_corr (gss[, c("sei10", "spsei10")],
wrap.labels = 30, p.numeric = TRUE, triangle="lower", na.deletion = "pairwise")
```

The order of the variables does not matter.

<figure><img src="../../../.gitbook/assets/image (29).png" alt="" width="563"><figcaption></figcaption></figure>

{% hint style="info" %}
There is a significant correlation between the socioeconomic index score of the respondents and the socioeconomic index score of the respondents’ spouses since the p-value is less than .05.&#x20;

This correlation is positive and moderate since the r-value is 0.382 (between 0.3 and 0.5).

This means that the socioeconomic index score of the respondents and the socioeconomic index score of the respondents’ spouses increase and decrease together.
{% endhint %}

Slides: [correlation](https://docs.google.com/presentation/d/12et6ZrFK7B6pE-Wmlz\_KVawjebAar9rC/edit?usp=sharing\&ouid=100179871492576617561\&rtpof=true\&sd=true)

***

## Correlation analyses

### Correlation scatterplot graph

Correlation analysis examines the linear relationship of two continuous variables.

IF the p-value is statistically significant (<0.05);

* .0 < | r | < .3 … weak correlation
* .3 < | r | < .5 … moderate correlation
* .5 < | r | ………. strong correlation

```r
scatterplot <- ggscatter(gss, x = "sei10", y = "spsei10",
add = "loess", conf.int = TRUE, color = "black", point=F,
xlab = "Socio-economic index score of the respondents", 
ylab = "Socio-economic index score of the respondents’ spouses")
scatterplot + stat_cor(p.accuracy = 0.001, r.accuracy = 0.01)
```

The order of the variables does not matter.

<figure><img src="../../../.gitbook/assets/Screenshot_2023-10-27 17.15.25.png" alt="" width="540"><figcaption></figcaption></figure>

{% hint style="info" %}
There is no significant correlation between the age in years and education in years since the p-value is higher than .05.&#x20;

\
This means that age in years and education in years do not increase and decrease together.
{% endhint %}

Slides: [correlation](https://docs.google.com/presentation/d/12et6ZrFK7B6pE-Wmlz\_KVawjebAar9rC/edit?usp=sharing\&ouid=100179871492576617561\&rtpof=true\&sd=true)

***

### Correlation matrix

Correlation matrix examines the linear relationship of multiple continuous variables.

IF the p-value is statistically significant (<0.05);

* .0 < | r | < .3 … weak correlation
* .3 < | r | < .5 … moderate correlation
* .5 < | r | ………. strong correlation

```r
tab_corr (gss[, c("sei10", "spsei10", "tvhours", "usetech", "age", "educ", "marasiannew", "marhispnew")], 
wrap.labels = 30, p.numeric = TRUE, triangle="lower", na.deletion = "pairwise")
```

<figure><img src="https://lh7-us.googleusercontent.com/tjwUYS-W7rqOGOfKlzHdCGnQEcxL0epZgyHfZeT-YL6918WAR4XlME8SbSPNHGJP9bzJK4cyb4kO9OitFe-CTbgmTXF_3T7NayXK4pH-FJvWEKiEvW3y14zjp79N8kfRBT3M7BOxYQYrMQ1LEMeVaKvzGA=s2048" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Same interpretation as correlation analysis table and scatterplot graph
{% endhint %}

Slides: [correlation](https://docs.google.com/presentation/d/12et6ZrFK7B6pE-Wmlz\_KVawjebAar9rC/edit?usp=sharing\&ouid=100179871492576617561\&rtpof=true\&sd=true)

***

### Scatterplot matrix

Scatterplot matrix examines the linear relationship of multiple continuous variables.

IF the p-value is statistically significant (<0.05);

* .0 < | r | < .3 … weak correlation
* .3 < | r | < .5 … moderate correlation
* .5 < | r | ………. strong correlation

```r
pairs.panels(gss[, c("sei10", "spsei10", "tvhours", "usetech", "age", "educ", "marasiannew", "marhispnew")],
ellipses=F, scale=F, show.points=F, stars=T, ci=T)
```

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Same interpretation as correlation analysis table and scatterplot graph
{% endhint %}

Slides: [correlation](https://docs.google.com/presentation/d/12et6ZrFK7B6pE-Wmlz\_KVawjebAar9rC/edit?usp=sharing\&ouid=100179871492576617561\&rtpof=true\&sd=true)

***

### Correlogram&#x20;

Correlogram examines the linear relationship of multiple continuous variables.

IF the p-value is statistically significant (<0.05);

* .0 < | r | < .3 … weak correlation
* .3 < | r | < .5 … moderate correlation
* .5 < | r | ………. strong correlation

```r
selectedvariables <- c("sei10", "spsei10", "tvhours", "usetech", "age", "educ", "marasiannew", "marhispnew")
testRes = cor.mtest(gss[, selectedvariables])gssrcorr = rcorr(as.matrix(gss[, selectedvariables]))
gsscoeff = gssrcorr$rcorrplot(gsscoeff, p.mat = testRes$p, method = 'pie', type = 'lower', insig='blank',
addCoef.col = 'black', order = 'original', diag = FALSE)$corrPos
```

<figure><img src="https://lh7-us.googleusercontent.com/aEPzIPrFoAyyNBCewhk-nZjZV-9BQ8Y1StIBP-_i6BrHK1U0BM1EGBQDAqUOg6T_0QTy_GXv4JiVo-k4OserXlHSGyN2avps_8e6Qyy8q782JYT5f8JbduWFyFmXAGPeDwX2_wgi96HPEgac8OgFYlr8aA=s2048" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Same interpretation as correlation analysis table and scatterplot graph
{% endhint %}

Slides: [correlation](https://docs.google.com/presentation/d/12et6ZrFK7B6pE-Wmlz\_KVawjebAar9rC/edit?usp=sharing\&ouid=100179871492576617561\&rtpof=true\&sd=true)

***

## Regression analyses

### Linear regression analysis

In regression, we explain the effects of independent variables on the dependent variable by estimating how changes in the independent variables are associated with changes in the dependent variable.

\
Unlike correlation analysis, regression analysis can be used to determine the direction and strength of a potential causal relationship.

```r
model4 <- lm(conrinc ~ god + age + physhlth + educ, data = gss)
tab_model(model4, show.std = T, show.ci = F, collapse.se = T, p.style = "stars")
```

&#x20;Dependent variable (conrinc) first, followed by independent variables separated by a plus (+).

<figure><img src="../../../.gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Age in years, days of poor physical health past 30 days, and education in years are statistically significant predictors of personal income since the p values are less than 0.05. Confidence in the existence of God is not a statistically significant predictor of personal income since the p value is greater than 0.05.

A year increase in age increases personal income by $504. A day increase in poor physical health past 30 days decreases personal income by $857. A year increase in the years of education increases personal income by $4,845.&#x20;

The strongest predictor of personal income is the education in years (std.Beta=0.34), then, then age in years (std.Beta=0.17), and then, the days of poor physical health past 30 days (std.Beta=-0.13).

The adjusted R squared value indicates that 17.2% of the variation in personal income can be explained by education in years, age in years, and days of poor physical health past 30 days.
{% endhint %}

{% hint style="success" %}
When reporting the coefficients, ensure that the sentence includes the units of both the independent and the dependent variable.



* Independent variable (rank - social ranking <mark style="color:orange;">level</mark> - 10: top; 1: bottom)
* Dependent variable (educ - education in <mark style="color:red;">years</mark> - 0-20 years)&#x20;

<mark style="color:orange;">A one unit</mark> increase in social ranking level increases respondents’ education by <mark style="color:blue;">3.19</mark> <mark style="color:red;">years</mark>.



* Independent variable (physhlth - <mark style="color:orange;">days</mark> of physical issues during the past 30 days - 0-30 days) &#x20;
* Dependent variable (conrinc - personal income in <mark style="color:red;">dollars</mark> - $336 - $170,913)

<mark style="color:orange;">A day</mark> increase in physical issues during the past 30 days decreases personal income by <mark style="color:red;">$</mark><mark style="color:blue;">857</mark>.



* Independent variable (age - age in <mark style="color:orange;">years</mark> - 18-89 age)&#x20;
* Dependent variable (polviews - conservatism <mark style="color:red;">level</mark> - 1: extremely liberal; 7: extremely conservative) &#x20;

<mark style="color:orange;">A year</mark> increase in age increases conservatism level by <mark style="color:purple;">2.45</mark> <mark style="color:red;">points</mark>.
{% endhint %}

{% hint style="success" %}
The adjusted R-squared should be reported as a percentage.

Here's a shortcut for converting a number with decimals to a percentage:&#x20;



If 0.007 is the adjusted R-square, then move the dot two times to the right:

0.007 <mark style="color:red;">➜</mark>  0.7%

0.079 <mark style="color:red;">➜</mark> 7.9%

0.172 <mark style="color:red;">➜</mark> 17.2%
{% endhint %}

Slides: [linear regression](https://docs.google.com/presentation/d/16v4ZKqgEw2Ah0i0g9jC8Ex1WY3rMvjPi/edit?usp=sharing\&ouid=100179871492576617561\&rtpof=true\&sd=true)

### Linear regression analysis (with dummy variables)

<figure><img src="../../../.gitbook/assets/image (31).png" alt=""><figcaption></figcaption></figure>

```r
model6 <- lm(conrinc ~ god + age + physhlth + educ + male + veryhappy + prettyhappy , data = gss)
tab_model(model6, show.std = T, show.ci = F, collapse.se = T, p.style = "stars")
```



{% hint style="info" %}
Age of the respondents, days of poor physical health past 30 days, the years of education, being male, being very happy, and being pretty happy are statistically significant predictors of respondents’ income since the p values are less than 0.05. Respondent's confidence in the existence of God is not a statistically significant predictor of respondents’ income since the p value is greater than 0.05.



A year increase in age increases respondents’ income by $489. A day increase in poor physical health past 30 days decreases respondents’ income by $654. A year increase in the years of education increases respondents’ income by $5,185. Being male increases income by $15,624 compared to being female. Being very happy increases income by $15,779 compared to being not too happy. Being pretty happy increases income by $8,908 compared to being not too happy. \


The strongest predictor of respondents’ income is the years of education (std.Beta=0.36), followed by being male (std.Beta=0.19), the age of the respondent (std.Beta=0.17), being very happy (std.Beta=0.16), being pretty happy (std.Beta=0.11), and the days of poor physical health past 30 days (std.Beta=-0.10).\


The adjusted R squared value indicates that 22.2% of the variation in respondents’ income can be explained by the years of education, age of the respondents, and days of poor physical health past 30 days, being male, being very happy, and being pretty happy.
{% endhint %}



{% hint style="success" %}
When reporting the coefficients of the dummy variables, ensure that the sentence includes "being" and the omitted (comparison category) dummy variable:



* <mark style="color:purple;">Being male</mark> increases income by $15,624 <mark style="color:orange;">compared to being female</mark>.&#x20;
* <mark style="color:purple;">Being very happy</mark> increases income by $15,779 <mark style="color:orange;">compared to being not too happy</mark>.&#x20;
* <mark style="color:purple;">Being pretty happy</mark> increases income by $8,908 <mark style="color:orange;">compared to being not too happy</mark>.
{% endhint %}

Slides: [linear regression](https://docs.google.com/presentation/d/16v4ZKqgEw2Ah0i0g9jC8Ex1WY3rMvjPi/edit?usp=sharing\&ouid=100179871492576617561\&rtpof=true\&sd=true)

Slides: [dummy variables](https://docs.google.com/presentation/d/1dJenkvbUDQUmX2HIrHWPK8-cYZ9VQQiqOTH2rJS83\_I/edit?usp=sharing)

### Logistic regression analysis (with dummy variables)

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

```r
frq(gss$class, out = "v")

gss$higherclass <- ifelse(gss$class == 3 | gss$class == 4, 1, 0)
gss$lowerclass <- ifelse(gss$class == 1 | gss$class == 2, 1, 0)

frq(gss$race, out = "v")

gss$white <- ifelse(gss$race == 1, 1, 0)
gss$nonwhite <- ifelse(gss$race == 2 | gss$race == 3, 1, 0)

model4 <- glm(higherclass ~ educ + nonwhite + prestg10, data = gss, family = binomial(link="logit"))
tab_model(model4, show.std = TRUE, show.ci = FALSE, collapse.se = TRUE, p.style = "stars")
```



{% hint style="info" %}
Education in years, being non-white and occupational prestige score are significant predictors of being higher class since the p values are less than 0.05.&#x20;



A year increase in education increases the likelihood of being higher class (OR=1.23; std.Beta=1.81). Being non-white decreases the likelihood of being higher class compared to being white (OR=0.62; std.Beta=0.81). One unit increase in occupational prestige score increases the likelihood of being higher class (OR=1.02; std.Beta=1.38).

\
The Tjur R-squared value indicates that 14.1% of the variation in being higher class can be explained by education in years, being non-white and occupational prestige score.
{% endhint %}

Slides: [logistic regression](https://docs.google.com/presentation/d/1SU-hinA8IkjK5FSST6az104y-gQQIpU33i4nFxGKzhk/edit?usp=sharing)

Slides: [dummy variables](https://docs.google.com/presentation/d/1dJenkvbUDQUmX2HIrHWPK8-cYZ9VQQiqOTH2rJS83\_I/edit?usp=sharing)

[^1]: The “Frequencies” command counts up how many times categories of a variable appears.



    We always check the _**valid.prc**_ column (valid percentage).

[^2]: Categorical variables take on values that are names or labels, not real numbers.



    Check out the numbers under the "val" column. **1** is for married, **2** is widowed, **3** is divorced, etc.&#x20;



    These numbers are arbitrary. In other words, widowed people (2) are **NOT** double of married people (1).

[^3]: replace marital with a new categorical variable.

[^4]: v means "viewer"



    if you replace v with **b**, you will see the output on your browser.

[^5]: use "what it measures" column of Variables in GSS page.

[^6]: Always use "valid.prc" (valid percent) column of the tables.

[^7]: use the response sets.

[^8]: The “Descriptives” command is used to determine mean, standard deviation.

[^9]: Continuous variables are numeric variables that have an infinite number of values between any two values, with each point placed at an equal distance from one another.



    F

[^10]: replace age with a new continuous variable.

[^11]: use "what it measures" column of Variables in GSS page.

[^12]: Always use "valid.prc" (valid percent) column of the tables.

[^13]: use the response sets.
