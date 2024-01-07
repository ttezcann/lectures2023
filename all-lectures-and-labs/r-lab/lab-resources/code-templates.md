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

# Code templates

## install packages

```r
install.packages("sjlabelled", dependencies = TRUE)
```

## load packages

```r
library(sjlabelled)
```

## load GSS

{% hint style="warning" %}
required package(s): library(sjlabelled)
{% endhint %}

```r
temp <- tempfile()
download.file("https://gss.norc.org/Documents/stata/2022_stata.zip",temp)
unzip(temp, files="2022/GSS2022.dta",exdir = "OrigData")
unlink(temp);rm(temp)
gss <-  haven::read_dta("OrigData/2022/GSS2022.dta")
key <- as.data.frame(get_label(gss))
```

## frequency table (for categorical variables)

{% hint style="warning" %}
required package(s): library(sjmisc)
{% endhint %}

```r
frq(gss$sex, out = "v")
```

## frequency table by groups aka crosstab (for categorical variables)

{% hint style="warning" %}
required package(s): library(sjPlot)
{% endhint %}

```r
sjt.xtab(gss$sex, gss$marital, show.col.prc = TRUE)
```

## descriptive table (for continuous variables)

{% hint style="warning" %}
required package(s): library(sjmisc)
{% endhint %}

```r
descr(gss$age, out = "v", show = "short")
```

## recodings

{% hint style="warning" %}
required package(s): library(sjmisc)
{% endhint %}

### recoding cat2 (categorical to categorical with 2 responses)

```r
gss$new_variable_name_here <- rec(gss$original_variable_here, rec = 
"number1, number2=1 [label1]; 
number3, number4=2 [label2]", append = FALSE)
```

### recoding cat3 (categorical to categorical with 3 responses)

```r
gss$new_variable_name_here <- rec(gss$original_variable_here, rec = 
"number1, number2=1 [label1]; 
number3, number4=2 [label2];
number5, number6=3 [label3]", append = FALSE)
```

### recoding cat4 (categorical to categorical with 4 responses)

```r
gss$new_variable_name_here <- rec(gss$original_variable_here, rec = 
"number1, number2=1 [label1]; 
number3, number4=2 [label2];
number5, number6=3 [label3];
number7, number8, number9=4 [label4]", append = FALSE)
```

### recoding cat5 (categorical to categorical with 5 responses)

```r
gss$new_variable_name_here <- rec(gss$original_variable_here, rec = 
"number1, number2=1 [label1]; 
number3, number4=2 [label2];
number5, number6=3 [label3];
number7, number8, number9=4 [label4];
number10=5 [label5]", append = FALSE)
```

### recoding cat6 (categorical to categorical with 6 responses)

```r
gss$new_variable_name_here <- rec(gss$original_variable_here, rec = 
"number1, number2=1 [label1]; 
number3, number4=2 [label2];
number5, number6=3 [label3];
number7, number8, number9=4 [label4];
number10=5 [label5];
number11=6 [label6]", append = FALSE)
```

### recoding cat7 (categorical to categorical with 7 responses)

```r
gss$new_variable_name_here <- rec(gss$original_variable_here, rec = 
"number1, number2=1 [label1]; 
number3, number4=2 [label2];
number5, number6=3 [label3];
number7, number8, number9=4 [label4];
number10=5 [label5];
number11=6 [label6];
number12=7 [label7]", append = FALSE)
```

### recoding con2 (continuous to categorical with 2 responses)

```r
gss$new_variable_name_here <- rec(gss$original_variable_here, rec = 
"number1:number2=1 [label1]; 
number3:number4=2 [label2]", append = FALSE)
```

### recoding con3 (continuous to categorical with 3 responses)

```r
gss$new_variable_name_here <- rec(gss$original_variable_here, rec = 
"number1:number2=1 [label1];
number3:number4=2 [label2]; 
number5:number6=3 [label3]", append = FALSE)
```

### recoding con4 (continuous to categorical with 4 responses)

```r
gss$new_variable_name_here <- rec(gss$original_variable_here, rec = 
"number1:number2=1 [label1];
number3:number4=2 [label2]; 
number5:number6=2 [label3]; 
number7:number8=3 [label4]", append = FALSE)
```

### recoding con5+ (continuous to categorical with more than 4 responses)

```r
gss$new_variable_name_here <- rec(gss$original_variable_here, rec = 
"number1:number2=1 [label1];
number3:number4=2 [label2]; 
number5:number6=2 [label3]; 
number7:number8=3 [label4]; 
number9:number10=5 [label5]; 
number11:number12=6 [label6]", append = FALSE)
```

## computing

{% hint style="warning" %}
required package(s): library(dplyr)
{% endhint %}

### computing 1

```r
gss <- gss %>%
  rowwise() %>% 
  mutate (parentseducmean2 = mean (c(maeduc,paeduc)))
```

### computing 2 (with recoding)

```r
frq(gss$happy, out = "v")

gss$happynew <- rec(gss$happy, rec = 
"1=3 [very happy]; 
2=2 [pretty happy]; 
3=1 [not too happy]", append = FALSE)


frq(gss$life, out = "v")

gss$lifenew <- rec(gss$life, rec = 
"1=3 [exciting]; 
2=2 [routine]; 
3=1 [dull]", append = FALSE)


frq(gss$satfin, out = "v")

gss$satfinnew <- rec(gss$satfin, rec = 
"1=3 [satisfied]; 
2=2 [more or less]; 
3=1 [not at all]", append = FALSE)


gss <- gss %>%
  rowwise() %>% 
  mutate (hapindex = mean (c(happynew,lifenew,satfinnew)))
```

### computing 3 (with recoding)

```r
frq(gss$socrel, out = "v")

gss$socrelnew <- rec(gss$socrel, rec = 
"1=7 [almost daily];
2=6 [once or twice a week]; 
3=5 [several times a month]; 
4=4 [about once a month]; 
5=3 [several times a year]; 
6=2 [about once a year];
7=1 [never]", append = FALSE)


frq(gss$socommun, out = "v")

gss$socommunnew <- rec(gss$socommun, rec = 
"1=7 [almost daily];
2=6 [once or twice a week]; 
3=5 [several times a month]; 
4=4 [about once a month]; 
5=3 [several times a year]; 
6=2 [about once a year];
7=1 [never]", append = FALSE)


frq(gss$socfrend, out = "v")

gss$socfrendnew <- rec(gss$socfrend, rec = 
"1=7 [almost daily];
2=6 [once or twice a week]; 
3=5 [several times a month]; 
4=4 [about once a month]; 
5=3 [several times a year]; 
6=2 [about once a year];
7=1 [never]", append = FALSE)


frq(gss$socbar, out = "v")

gss$socbarnew <- rec(gss$socbar, rec = 
"1=7 [almost daily];
2=6 [once or twice a week]; 
3=5 [several times a month]; 
4=4 [about once a month]; 
5=3 [several times a year]; 
6=2 [about once a year];
7=1 [never]", append = FALSE)

gss <- gss %>%  
rowwise() %>%   
mutate (sociallifeindex = mean (c(socrelnew,socommunnew,socfrendnew, socbarnew)))
```

## chi square

{% hint style="warning" %}
required package(s): library(sjPlot)
{% endhint %}

```r
sjt.xtab(gss$var1, gss$var2, show.row.prc = TRUE)
```

## ttest

{% hint style="warning" %}
required package(s): library(dplyr)   |   library(parameters)
{% endhint %}

```r
t.test(depvar ~ indepvar, data = gss) %>% 
  parameters() %>% 
  display(format="html")
```

## bar graph (for categorical variables)

{% hint style="warning" %}
required package(s): library(sjPlot)
{% endhint %}

```r
plot_frq(gss$marital, type = "bar", geom.colors = "#336699")
```

## histogram (for continuous variables)

{% hint style="warning" %}
required package(s): library(sjPlot)
{% endhint %}

```r
plot_frq(gss$educ, type = "hist",show.mean = TRUE, show.mean.val = TRUE, normal.curve = TRUE, show.sd = TRUE, normal.curve.color = "red")
```

## stacked bar graphs for multiple likert scales

{% hint style="warning" %}
required package(s): library(sjPlot)   |   library(ggplot2)
{% endhint %}

```r
graph <- gss %>%  select (var1, var2, var3, var4, var5) %>%  
plot_stackfrq(sort.frq = "first.asc", coord.flip = TRUE, geom.colors = "Blues", show.total = FALSE,                
title = "type graph title here")
graph + theme(  axis.text.x = element_text(size=14), # change font size of x-axis labels  
axis.text.y = element_text(size=14), # change font size of y-axis labels  
plot.title=element_text(size=20), # change font size of plot title  
legend.text = element_text(size=14)) # change font size of legend
```

## stacked bar graphs for multiple likert scales (flip coordination

{% hint style="warning" %}
required package(s): library(sjPlot)   |   library(ggplot2)
{% endhint %}

```r
graph <- gss %>%  select (var1, var2, var3, var4, var5) %>%  
plot_stackfrq(sort.frq = "first.asc", coord.flip = FALSE, geom.colors = "Blues", show.total = FALSE,                
title = "type graph title here")
graph + theme(  axis.text.x = element_text(size=14), # change font size of x-axis labels  
axis.text.y = element_text(size=14), # change font size of y-axis labels  
plot.title=element_text(size=20), # change font size of plot title  
legend.text = element_text(size=14)) # change font size of legend
```

## stacked bar graphs by different groups

{% hint style="warning" %}
required package(s): library(sjPlot)
{% endhint %}

```r
plot_xtab(gss$var1, gss$var2, show.total=FALSE, show.n = FALSE)
```

## bar graphs between groups (margin=row)

{% hint style="warning" %}
required package(s): library(sjPlot)
{% endhint %}

```r
plot_xtab(gss$var1, gss$var2, show.total=FALSE, show.n = FALSE, margin = "row")
```

## scatterplot with two variables

{% hint style="warning" %}
required package(s): library(sjPlot)
{% endhint %}

```r
plot_scatter(gss, var1, var2, jitter = TRUE,
            fit.grps = lm, show.ci = TRUE, grid = TRUE,
             title = "type graph title here")
```

## scatterplot with two variables by groups

{% hint style="warning" %}
required package(s): library(sjPlot)
{% endhint %}

```r
plot_scatter(gss, var1, var2, groupvar, jitter = TRUE,
            fit.grps = lm, show.ci = TRUE, grid = TRUE,
             title = "type graph title here")
```

## correlation analysis

### correlation analysis table

{% hint style="warning" %}
required package(s):  library(sjPlot)
{% endhint %}

```r
tab_corr (gss[, c("sei10", "spsei10")],
wrap.labels = 30, p.numeric = TRUE, triangle="lower", na.deletion = "pairwise")
```

### correlation scatterplot graph

{% hint style="warning" %}
required package(s): library(ggpubr)
{% endhint %}

```r
scatterplot <- ggscatter(gss, x = "sei10", y = "spsei10",
           add = "loess", conf.int = TRUE, color = "black", point=F,
           xlab = "Socio-economic index score of the respondents", ylab = "Socio-economic index score of the respondents’ spouses")
           scatterplot + stat_cor(p.accuracy = 0.001, r.accuracy = 0.01)
```

### correlation matrix

{% hint style="warning" %}
required package(s): library(sjPlot)
{% endhint %}

```r
tab_corr (gss[, c("sei10", "spsei10", "tvhours", "usetech", "age", "educ", "marasiannew", "marhispnew")], 
wrap.labels = 30, p.numeric = TRUE, triangle="lower", na.deletion = "pairwise")
```

### scatterplot matrix

{% hint style="warning" %}
required package(s): library(psych)
{% endhint %}

```r
pairs.panels(gss[, c("sei10", "spsei10", "tvhours", "usetech", "age", "educ", "marasiannew", "marhispnew")],
ellipses=F, scale=F, show.points=F, stars=T, ci=T)
```

### correlogram

{% hint style="warning" %}
required package(s): library(corrplot)   |   library(Hmisc)
{% endhint %}

```r
selectedvariables <- c("sei10", "spsei10", "tvhours", "usetech", "age", "educ", "marasiannew", "marhispnew")
testRes = cor.mtest(gss[, selectedvariables])
gssrcorr = rcorr(as.matrix(gss[, selectedvariables]))
gsscoeff = gssrcorr$r
corrplot(gsscoeff, p.mat = testRes$p, method = 'pie', type = 'lower', insig='blank',
addCoef.col = 'black', order = 'original', diag = FALSE)$corrPos
```

## regressions

{% hint style="warning" %}
required package(s): library(sjPlot)
{% endhint %}

### linear regression

```r
model4 <- lm(depvar ~ indepvar1 + indepvar2 + indepvar3 + indepvar4, data = gss)
tab_model(model4, show.std = T, show.ci = F, collapse.se = T, p.style = "stars")
```

### logistic regression

```r
model4 <- glm(depvar ~ indepvar1 + indepvar2 + indepvar3 + indepvar4, data = gss, family = binomial(link="logit"))
tab_model(model4, show.std = TRUE, show.ci = FALSE, collapse.se = TRUE, p.style = "stars")
```

## dummy variables

{% hint style="warning" %}
required package(s): no package needed
{% endhint %}

### dummy variable: categorical (binary)

```r
gss$var1newname <- ifelse(gss$var1 == 1, 1, 0)
gss$var2newname <- ifelse(gss$var1 == 2, 1, 0)
```

### dummy variable: nominal/ordinal 1

```r
gss$var1newname <- ifelse(gss$var1 == 1, 1, 0)
gss$var2newname <- ifelse(gss$var1 == 2, 1, 0)
gss$var3newname <- ifelse(gss$var1 == 3, 1, 0)
```

### dummy variable: nominal/ordinal 2 (merging categories)

```r
gss$var1newname <- ifelse(gss$var1 == 1, 1, 0)
gss$var2newname <- ifelse(gss$var1 == 2 | gss$var1 == 3 | gss$var1 == 4, 1, 0)
gss$var3newname <- ifelse(gss$var1 == 5, 1, 0)
```

### dummy variable: continuous

```r
gss$var1newname <- ifelse(gss$var1 <= 10, 1, 0)
gss$var2newname <- ifelse(gss$var1 >= 11 & gss$var1 <= 15, 1, 0)
gss$var3newname <- ifelse(gss$var1 >= 16, 1, 0)
```

## scientific notations (e.g., 2e-16)

```r
options(digits=5, scipen=15)
```

## mean centering

```r
gss$age_cent <-scale(gss$age, center = TRUE, scale = FALSE)
```

## delete the environment

```r
rm(list = ls())
```

## remove categories from a variable

```r
gss <- gss[gss$marital != 2 & gss$marital != 3,]
```

## remove label

```r
gss$educ <- remove_all_labels(gss$educ)
```

## rename variables

```r
gss <- newvariablename(gss, agenew = "age_groups")
```

## change the variable from continuous to categorical

```r
gss$var1 <- to_factor(gss$var1)
```

## change the variable from categorical to continuous

```r
gss$var1 <- as.numeric(as.character(gss$var1))
```

## show codebook

```r
view_df(gss, show.frq = TRUE, show.prc = TRUE, use.viewer=FALSE, show.na = TRUE, max.len = 300)
```

## remove packages

```r
remove.packages ("package_you_want_to_remove")
```

## assigning labels

```r
gss$sex<- set_labels(gss$sex,
labels = c("male" = 1, "female" = 2))
```
