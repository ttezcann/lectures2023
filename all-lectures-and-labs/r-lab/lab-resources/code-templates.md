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

## install and load multiple packages

```r
while (dev.cur() > 1) dev.off()
packages <- c("corrplot", "tidyverse", "ggpubr",
              "Hmisc", "parameters", "performance",
              "psych", "see", "sjlabelled", "sjmisc", "sjPlot")
installed_packages <- rownames(installed.packages())
for (pkg in packages) {if (!(pkg %in% installed_packages)) {
  message(paste("Installing package:", pkg))
  install.packages(pkg, dependencies = TRUE)} else {
    message(paste("Package already installed:", pkg))}
  library(pkg, character.only = TRUE)}
```

## install and load a single package

```r
if (!require("PackageNameHere")) install.packages("PackageNameHere", dependencies = TRUE); library("PackageNameHere")
```

## load GSS

{% hint style="warning" %}
required package(s): "sjlabelled"
{% endhint %}

```r
temp <- tempfile()
download.file("https://drive.google.com/uc?export=download&id=1mF7gMY4aU9amTgYLSVOyVQaHT_opDUbj",temp, mode = "wb")
unzip(temp, files="OrigData/2022/GSS2022.dta",exdir = "OrigData")
gss <- haven::read_dta("OrigData/OrigData/2022/GSS2022.dta")
key <- as.data.frame(get_label(gss))
```

## frequency table (for categorical variables)

{% hint style="warning" %}
required package(s): "sjmisc"
{% endhint %}

```r
frq(gss$sex, out = "v")
```

## descriptive table (for continuous variables)

{% hint style="warning" %}
required package(s): "sjmisc"
{% endhint %}

```r
descr(gss$age, out = "v", show = "short")
```

## recodings

### RECODING EXAMPLE

{% hint style="info" %}
Imagine we want to use “the level of physical effort required at work” (<mark style="color:orange;">phyeffrt</mark>) variable in our analyses. First, check the frequency distribution to see what 1, 2. 3, etc., mean.

**Code:**&#x20;

frq(gss$<mark style="color:orange;">phyeffrt</mark>, out = "v")

![](../../../.gitbook/assets/image.png)\


Higher values should indicate greater physical effort, but this isn't the case. Thus, we need to change the direction of the responses:



the new variable name comes first: <mark style="color:red;">phyeffrtnew</mark>

the original variable name comes second: <mark style="color:orange;">phyeffrt</mark>



**Code:**&#x20;

gss$<mark style="color:red;">phyeffrtnew</mark> <- rec(gss$<mark style="color:orange;">phyeffrt</mark>, rec =&#x20;

"1=5 \[very hard];&#x20;

2=4 \[hard];

3=3 \[somewhat hard];

4=2 \[fairly light];

5=1 \[very light]", append = FALSE)

\
Running the code above will create a new variable, <mark style="color:red;">phyeffrtnew</mark>, that we will use in our analysis.
{% endhint %}

<figure><img src="https://lh7-us.googleusercontent.com/48NuP2iAmjMh3rDSuVo-dP9gjMoYOFk7fV73EfyrlmNaGkg5H-7xjgyiJdsRUKMd4YssBOXZoz0A88Or6Po7LiCCYh1_FTZ7FVoqZ7T_DjrCWop9MamImTksXY8wPZmUBhjKibFDoaDX_TUK1Y_U4gs" alt=""><figcaption></figcaption></figure>



{% hint style="warning" %}
required package(s): "sjmisc"
{% endhint %}

### recoding cat2 (categorical to categorical with 2 responses)

{% code fullWidth="false" %}
```r
gss$new_variable_name_here <- rec(gss$original_variable_here, rec = 
"1=2 [label1]; 
2=1 [label2]", append = FALSE)
```
{% endcode %}

### recoding cat2 with merging (categorical to categorical with 2 responses)

{% code fullWidth="false" %}
```r
gss$new_variable_name_here <- rec(gss$original_variable_here, rec = 
"1,2=1 [label1]; 
3,4=2 [label2]", append = FALSE)
```
{% endcode %}

### recoding cat3 (categorical to categorical with 3 responses)

```r
gss$new_variable_name_here <- rec(gss$original_variable_here, rec = 
"1=3 [label1]; 
2=2 [label2];
3=1 [label3]", append = FALSE)
```

### recoding cat3 with merging (categorical to categorical with 3 responses)

```r
gss$new_variable_name_here <- rec(gss$original_variable_here, rec = 
"1,2=1 [label1]; 
3,4=2 [label2];
5,6=3 [label3]", append = FALSE)
```

### recoding cat4 (categorical to categorical with 4 responses)

```r
gss$new_variable_name_here <- rec(gss$original_variable_here, rec = 
"1=4 [label1]; 
2=3 [label2];
3=2 [label3];
4=1 [label4]", append = FALSE)
```

### recoding cat4 with merging (categorical to categorical with 4 responses)

```r
gss$new_variable_name_here <- rec(gss$original_variable_here, rec = 
"1,2=1 [label1]; 
3,4=2 [label2];
5,6=3 [label3];
7,8,9=4 [label4]", append = FALSE)
```

### recoding cat5 (categorical to categorical with 5 responses)

```r
gss$new_variable_name_here <- rec(gss$original_variable_here, rec = 
"1=5 [label1]; 
2=4 [label2];
3=3 [label3];
4=2 [label4];
5=1 [label5]", append = FALSE)
```

### recoding cat5 with merging (categorical to categorical with 5 responses)

```r
gss$new_variable_name_here <- rec(gss$original_variable_here, rec = 
"1,2=1 [label1]; 
3,4=2 [label2];
5,6=3 [label3];
7,8=4 [label4];
9=5 [label5]", append = FALSE)
```

### recoding cat6 (categorical to categorical with 6 responses)

```r
gss$new_variable_name_here <- rec(gss$original_variable_here, rec = 
"1=6 [label1]; 
2=5 [label2];
3=4 [label3];
4=3 [label4];
5=2 [label5];
6=1 [label6]", append = FALSE)
```

### recoding cat6 with merging (categorical to categorical with 6 responses)

```r
gss$new_variable_name_here <- rec(gss$original_variable_here, rec = 
"1,2=1 [label1]; 
3,4=2 [label2];
5,6=3 [label3];
7,8=4 [label4];
9,10,11=5 [label5];
12,13,14=6 [label6]", append = FALSE)
```

### recoding cat7 (categorical to categorical with 7 responses)

```r
gss$new_variable_name_here <- rec(gss$original_variable_here, rec = 
"7=1 [label1]; 
6=2 [label2];
5=3 [label3];
4=4 [label4];
3=5 [label5];
2=6 [label6];
1=7 [label7]", append = FALSE)
```

### recoding cat7 with merging (categorical to categorical with 7 responses)

```r
gss$new_variable_name_here <- rec(gss$original_variable_here, rec = 
"1,2=1 [label1]; 
3,4,5=2 [label2];
6,7,8=3 [label3];
9,10=4 [label4];
11,12=5 [label5];
13,14,15=6 [label6];
16,17,18=7 [label7]", append = FALSE)
```

### recoding con2 (continuous to categorical with 2 responses)

```r
gss$new_variable_name_here <- rec(gss$original_variable_here, rec = 
"0:40=1 [label1]; 
41:100=2 [label2]", append = FALSE)
```

### recoding con3 (continuous to categorical with 3 responses)

```r
gss$new_variable_name_here <- rec(gss$original_variable_here, rec = 
"1:10=1 [label1];
11:20=2 [label2]; 
21:50=3 [label3]", append = FALSE)
```

### recoding con4 (continuous to categorical with 4 responses)

```r
gss$new_variable_name_here <- rec(gss$original_variable_here, rec = 
"0:15000=1 [label1];
15001:25000=2 [label2]; 
25001:45000=2 [label3]; 
45001:90000=3 [label4]", append = FALSE)
```

### recoding con5+ (continuous to categorical with more than 4 responses)

```r
gss$new_variable_name_here <- rec(gss$original_variable_here, rec = 
"1:10=1 [label1];
11:20=2 [label2]; 
21:30=2 [label3]; 
31:40=3 [label4]; 
41:50=5 [label5]; 
51:60=6 [label6]", append = FALSE)
```

## computing

{% hint style="warning" %}
required package(s): "tidyverse"
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
required package(s): "sjPlot"
{% endhint %}

```r
sjt.xtab(gss$var1, gss$var2, show.row.prc = TRUE)
```

## ttest

{% hint style="warning" %}
required package(s): "tidyverse"   |   "parameters"
{% endhint %}

```r
t.test(depvar ~ indepvar, data = gss) %>% 
  parameters() %>% 
  display(format="html")
```

## bar graph (for categorical variables)

{% hint style="warning" %}
required package(s): "sjPlot"
{% endhint %}

```r
plot_frq(gss$marital, type = "bar", geom.colors = "#336699")
```

## histogram (for continuous variables)

{% hint style="warning" %}
required package(s): "sjPlot"
{% endhint %}

```r
plot_frq(gss$educ, type = "hist",show.mean = TRUE, show.mean.val = TRUE, normal.curve = TRUE, show.sd = TRUE, normal.curve.color = "red")
```

## stacked bar graphs for multiple likert scales

{% hint style="warning" %}
required package(s): "sjPlot"  |   "tidyverse"
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
required package(s): "sjPlot"  |   "tidyverse"
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
required package(s): "sjPlot"
{% endhint %}

```r
plot_xtab(gss$var1, gss$var2, show.total=FALSE, show.n = FALSE)
```

## bar graphs between groups (margin=row)

{% hint style="warning" %}
required package(s): "sjPlot"
{% endhint %}

```r
plot_xtab(gss$var1, gss$var2, show.total=FALSE, show.n = FALSE, margin = "row")
```

## scatterplot with two variables

{% hint style="warning" %}
required package(s): "sjPlot"
{% endhint %}

```r
plot_scatter(gss, var1, var2, jitter = TRUE,
            fit.grps = lm, show.ci = TRUE, grid = TRUE,
             title = "type graph title here")
```

## scatterplot with two variables by groups

{% hint style="warning" %}
required package(s): "sjPlot"
{% endhint %}

```r
plot_scatter(gss, var1, var2, groupvar, jitter = TRUE,
            fit.grps = lm, show.ci = TRUE, grid = TRUE,
             title = "type graph title here")
```

## correlation analysis

### correlation analysis table

{% hint style="warning" %}
required package(s):  "sjPlot"
{% endhint %}

```r
tab_corr (gss[, c("sei10", "spsei10")],
wrap.labels = 30, p.numeric = TRUE, triangle="lower", na.deletion = "pairwise")
```

### correlation scatterplot graph

{% hint style="warning" %}
required package(s): "ggpubr"
{% endhint %}

```r
scatterplot <- ggscatter(gss, x = "sei10", y = "spsei10",
           add = "loess", conf.int = TRUE, color = "black", point=F,
           xlab = "Socio-economic index score of the respondents", ylab = "Socio-economic index score of the respondents’ spouses")
           scatterplot + stat_cor(p.accuracy = 0.001, r.accuracy = 0.01)
```

### correlation matrix

{% hint style="warning" %}
required package(s): "sjPlot"
{% endhint %}

```r
tab_corr (gss[, c("sei10", "spsei10", "tvhours", "usetech", "age", "educ", "marasiannew", "marhispnew")], 
wrap.labels = 30, p.numeric = TRUE, triangle="lower", na.deletion = "pairwise")
```

### scatterplot matrix

{% hint style="warning" %}
required package(s): "psych"
{% endhint %}

```r
pairs.panels(gss[, c("sei10", "spsei10", "tvhours", "usetech", "age", "educ", "marasiannew", "marhispnew")],
ellipses=F, scale=F, show.points=F, stars=T, ci=T)
```

### correlogram

{% hint style="warning" %}
required package(s): "corrplot"   |   "Hmisc"
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
required package(s): "sjPlot"
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

### DUMMY EXAMPLE

{% hint style="info" %}
<mark style="background-color:orange;">First step:</mark> Check the frequency distribution of the original variable to see what the values (1, 2, 3, etc.) mean.

**Code:**&#x20;

```r
frq(gss$happy, out = "v")
```

![](<../../../.gitbook/assets/image (32).png>)



<mark style="background-color:orange;">Second step</mark>: Create dummy variables for each category.

**Codes:**

```r
gss$veryhappy <- ifelse(gss$happy == 1, 1, 0)
gss$prettyhappy <- ifelse(gss$happy == 2, 1, 0)
gss$nottoohappy <- ifelse(gss$happy == 3, 1, 0)
```



<mark style="background-color:orange;">Third step:</mark> Do not include (omit) one of the dummy variables in your model. The omitted dummy variable is called “comparison category” and should be used in interpretation as well.
{% endhint %}

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
