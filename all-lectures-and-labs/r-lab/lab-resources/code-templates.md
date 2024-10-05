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
frq(gss$variable_here, out = "v")
```

## descriptive table (for continuous variables)

{% hint style="warning" %}
required package(s): "sjmisc"
{% endhint %}

```r
descr(gss$variable_here, out = "v", show = "short")
```

## recoding

{% hint style="warning" %}
required package(s): "sjmisc"
{% endhint %}

### (1) merging values (categorical to categorical)

#### 1.2. recoding (merging values with 2 values)

{% code fullWidth="false" %}
```r
gss$new_variable_here <- rec(gss$original_variable_here, rec = 
"1,2=1 [label1]; 
3,4=2 [label2]", append = FALSE)
```
{% endcode %}

#### 1.3. recoding (merging values with 3 values)

```r
gss$new_variable_here <- rec(gss$original_variable_here, rec = 
"1,2,3=1 [label1]; 
2,4,5=2 [label2];
6,7,8=1 [label3]", append = FALSE)
```

#### 1.4. recoding (merging values with 4 values)

```r
gss$new_variable_here <- rec(gss$original_variable_here, rec = 
"1,2=1 [label1]; 
3,4=2 [label2];
5,6=3 [label3]", append = FALSE)
```

#### 1.5. recoding (merging values with 5 values)

```r
gss$new_variable_here <- rec(gss$original_variable_here, rec = 
"1,2=1 [label1]; 
3,4,5=2 [label2];
6=3 [label3];
7,8=4 [label4];
9,10=5 [label3]", append = FALSE)
```

#### 1.6. recoding (merging values with 6 values)

```r
gss$new_variable_here <- rec(gss$original_variable_here, rec = 
"1,2=1 [label1]; 
3,4,5=2 [label2];
6,7,8=3 [label3];
9,10=4 [label4];
11,12=5 [label5];
13,14,15=6 [label6]", append = FALSE)
```

#### 1.7. recoding (merging values with 7 values)

```r
gss$new_variable_here <- rec(gss$original_variable_here, rec = 
"1,2=1 [label1]; 
3,4,5=2 [label2];
6,7,8=3 [label3];
9,10=4 [label4];
11,12=5 [label5];
13,14,15=6 [label6];
16,17,18=7 [label7]", append = FALSE)
```

### (2) reversing values (categorical to categorical)

#### 2.2. recoding (reversing values with 2 values)

{% code fullWidth="false" %}
```r
gss$new_variable_here <- rec(gss$original_variable_here, rec = 
"1=2 [label1]; 
2=1 [label2]", append = FALSE)
```
{% endcode %}

#### 2.3. recoding (reversing values with 3 values)

{% code fullWidth="false" %}
```r
gss$new_variable_here <- rec(gss$original_variable_here, rec = 
"1=3 [label1];
2=2 [label2];
3=1 [label3]", append = FALSE)
```
{% endcode %}

#### 2.4. recoding (reversing values with 4 values)

{% code fullWidth="false" %}
```r
gss$new_variable_here <- rec(gss$original_variable_here, rec = 
"1=4 [label1];
2=3 [label2];
3=2 [label3];
4=1 [label4]", append = FALSE)
```
{% endcode %}

#### 2.5. recoding (reversing values with 5 values)

```r
gss$new_variable_here <- rec(gss$original_variable_here, rec = 
"1=5 [label1]; 
2=4 [label2];
3=3 [label3];
4=2 [label4];
5=1 [label5]", append = FALSE)
```

#### 2.6. recoding (reversing values with 6 values)

```r
gss$new_variable_here <- rec(gss$original_variable_here, rec = 
"1=6 [label1]; 
2=5 [label2];
3=4 [label3];
4=3 [label4];
5=2 [label5];
6=1 [label6]", append = FALSE)
```

#### 2.7. recoding (reversing values with 7 values)

```r
gss$new_variable_here <- rec(gss$original_variable_here, rec = 
"1=7 [label1]; 
2=6 [label2];
3=5 [label3];
4=4 [label4];
5=3 [label5];
6=2 [label6];
7=1 [label7]", append = FALSE)
```

### (3) transforming continuous variables into groups (continuous to categorical)

#### 3.2. recoding (transforming continuous variables into groups with 2 values)

```r
gss$new_variable_here <- rec(gss$original_variable_here, rec = 
"0:40=1 [label1]; 
41:100=2 [label2]", append = FALSE)
```

#### 3.3. recoding (transforming continuous variables into groups with 3 values)

```r
gss$new_variable_here <- rec(gss$original_variable_here, rec = 
"1:10=1 [label1];
11:20=2 [label2]; 
21:100=3 [label3]", append = FALSE)
```

#### 3.4. recoding (transforming continuous variables into groups with 4 values)

```r
gss$new_variable_here <- rec(gss$original_variable_here, rec = 
"0:10=1 [label1];
11:20=2 [label2]; 
21:40=3 [label3]; 
41:100=4 [label4]", append = FALSE)
```

#### 3.5. recoding (transforming continuous variables into groups with 5 values)

```r
gss$new_variable_here <- rec(gss$original_variable_here, rec = 
"1:10=1 [label1];
11:20=2 [label2]; 
21:30=3 [label3]; 
31:40=4 [label4]; 
41:100=5 [label5]", append = FALSE)
```

#### 3.6. recoding (transforming continuous variables into groups with 6 values)

```r
gss$new_variable_here <- rec(gss$original_variable_here, rec = 
"1:10=1 [label1];
11:20=2 [label2]; 
21:30=3 [label3]; 
31:40=4 [label4]; 
41:50=5 [label5]; 
51:100=6 [label6]", append = FALSE)
```

#### 3.7. recoding (transforming continuous variables into groups with 7 values)

```r
gss$new_variable_here <- rec(gss$original_variable_here, rec = 
"1:10=1 [label1];
11:20=2 [label2]; 
21:30=3 [label3]; 
31:40=4 [label4]; 
41:50=5 [label5]; 
51:60=6 [label6]; 
61:100=7 [label7]", append = FALSE)
```

#### 3.8. recoding (transforming continuous variables into groups with 8 values)

```r
gss$new_variable_here <- rec(gss$original_variable_here, rec = 
"1:10=1 [label1];
11:20=2 [label2]; 
21:30=3 [label3]; 
31:40=4 [label4]; 
41:50=5 [label5]; 
51:60=6 [label6]; 
61:70=7 [label7]; 
71:100=8 [label8]", append = FALSE)
```

## computing

{% hint style="warning" %}
required package(s): "tidyverse"
{% endhint %}

### computing 1

```r
gss <- gss %>%
  rowwise() %>% 
  mutate (new_variable_here = mean (c(variable_1_here, variable_2_here, variable_3_here)))
```

### computing 2 (with recoding) - sample 1

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

### computing 3 (with recoding) - sample 2

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
sjt.xtab(gss$independent_variable_here, gss$dependent_variable_here, show.row.prc = TRUE)
```

## sampling: data creation for subsamples

{% hint style="warning" %}
required package(s): "sjPlot"
{% endhint %}

### non-random (last 100 cases)

<pre class="language-r"><code class="lang-r">gsslast100 &#x3C;- gss[3445:3544,]

# use "gsslast100" dataset instead of "gss" in the codes.
# for example: descr(<a data-footnote-ref href="#user-content-fn-1">gsslast100</a>$variable_here, out = "v", show = "short")
</code></pre>

### 25% simple random sample

<pre class="language-r"><code class="lang-r">gssrandom25per &#x3C;- gss[sample(1:nrow(gss), 886, replace=FALSE),]

# use "gssrandom25per" dataset instead of "gss" in the codes.
# for example: descr(<a data-footnote-ref href="#user-content-fn-2">gssrandom25per</a>$variable_here, out = "v", show = "short")
</code></pre>

### 10% systematic random sample

<pre class="language-r"><code class="lang-r">gss10persystematic = gss[seq(1, nrow(gss), 10),]

# use "gss10persystematic" dataset instead of "gss" in the codes.
# for example: descr(<a data-footnote-ref href="#user-content-fn-3">gss10persystematic</a>$variable_here, out = "v", show = "short")
</code></pre>

## ttest

{% hint style="warning" %}
required package(s): "tidyverse"   |   "parameters"
{% endhint %}

```r
t.test(dependent_variable_here ~ independent_variable_here, data = gss) %>% 
  parameters() %>% 
  display(format="html")
```

## bar graph (for categorical variables)

{% hint style="warning" %}
required package(s): "sjPlot"
{% endhint %}

```r
plot_frq(gss$variable_here, type = "bar", geom.colors = "#336699")
```

## histogram (for continuous variables)

{% hint style="warning" %}
required package(s): "sjPlot"
{% endhint %}

```r
plot_frq(gss$variable_here, type = "hist",show.mean = TRUE, show.mean.val = TRUE, normal.curve = TRUE, show.sd = TRUE, normal.curve.color = "red")
```

## stacked bar graphs for multiple likert scales

{% hint style="warning" %}
required package(s): "sjPlot"  |   "tidyverse"
{% endhint %}

```r
graph <- gss %>%  select (variable_1_here, variable_2_here, variable_3_here, variable_4_here, variable_5_here) %>%  
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
graph <- gss %>%  select (variable_1_here, variable_2_here, variable_3_here, variable_4_here, variable_5_here) %>%  
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
plot_xtab(gss$variable_1_here, gss$variable_2_here, show.total=FALSE, show.n = FALSE)
```

## bar graphs between groups (margin=row)

{% hint style="warning" %}
required package(s): "sjPlot"
{% endhint %}

```r
plot_xtab(gss$variable_1_here, gss$variable_2_here, show.total=FALSE, show.n = FALSE, margin = "row")
```

## scatterplot with two variables

{% hint style="warning" %}
required package(s): "sjPlot"
{% endhint %}

```r
plot_scatter(gss, variable_1_here, variable_2_here, jitter = TRUE,
            fit.grps = lm, show.ci = TRUE, grid = TRUE,
             title = "type graph title here")
```

## scatterplot with two variables by groups

{% hint style="warning" %}
required package(s): "sjPlot"
{% endhint %}

```r
plot_scatter(gss, variable_1_here, variable_2_here, groupvar, jitter = TRUE,
            fit.grps = lm, show.ci = TRUE, grid = TRUE,
             title = "type graph title here")
```

## correlation analysis

### correlation analysis table

{% hint style="warning" %}
required package(s):  "sjPlot"
{% endhint %}

```r
tab_corr (gss[, c("variable_1_here", "variable_2_here")],
wrap.labels = 30, p.numeric = TRUE, triangle="lower", na.deletion = "pairwise")
```

### correlation scatterplot graph

{% hint style="warning" %}
required package(s): "ggpubr"
{% endhint %}

```r
scatterplot <- ggscatter(gss, x = "variable_1_here", y = "variable_1_here",
           add = "loess", conf.int = TRUE, color = "black", point=F,
           xlab = "what it measures of variable_1", ylab = "what it measures of variable_2")
           scatterplot + stat_cor(p.accuracy = 0.001, r.accuracy = 0.01)
```

### correlation matrix

{% hint style="warning" %}
required package(s): "sjPlot"
{% endhint %}

```r
tab_corr (gss[, c("variable_1_here", "variable_2_here", "variable_3_here", "variable_4_here", "variable_5_here", "variable_6_here", "variable_7_here", "variable_8_here")], 
wrap.labels = 30, p.numeric = TRUE, triangle="lower", na.deletion = "pairwise")
```

### scatterplot matrix

{% hint style="warning" %}
required package(s): "psych"
{% endhint %}

```r
pairs.panels(gss[, c("variable_1_here", "variable_2_here", "variable_3_here", "variable_4_here", "variable_5_here", "variable_6_here", "variable_7_here", "variable_8_here")],
ellipses=F, scale=F, show.points=F, stars=T, ci=T)
```

### correlogram

{% hint style="warning" %}
required package(s): "corrplot"   |   "Hmisc"
{% endhint %}

```r
selectedvariables <- c("variable_1_here", "variable_2_here", "variable_3_here", "variable_4_here", "variable_5_here", "variable_6_here", "variable_7_here", "variable_8_here")
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

model4 <- lm(dependent_variable_here ~ indepvar1 + indepvar2 + indepvar3 + indepvar4, data = gss)
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

[^1]: this part has been changed

[^2]: this part has been changed

[^3]: this part has been changed
