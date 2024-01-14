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

# Common recoding issues in RStudio

## 1.Recoding a categorical variable and a continuous variable requires slightly different code

<figure><img src="../../../.gitbook/assets/image (39).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (40).png" alt=""><figcaption></figcaption></figure>

## 2. Not using the recoded (new) variable in analyses

When we want to display the frequency distribution of a new (recoded) variable, we must use the new variable’s name in the frequency code.&#x20;

This is because, for our analysis, the original variable is no longer relevant. We recoded the original variable and created a new one for our analysis needs.

<figure><img src="../../../.gitbook/assets/image (41).png" alt=""><figcaption></figcaption></figure>

## 3. Recoded variables are always categorical

When we recode a continuous variable, the new (recoded) variable is no longer continuous.

It becomes CATEGORICAL because we have merged the real numbers, and they no longer remain as real numbers.\
Therefore, for example, we use the FRQ code to see the distribution.

<figure><img src="../../../.gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure>

## 4. Use a model code

<figure><img src="../../../.gitbook/assets/image (43).png" alt=""><figcaption></figcaption></figure>

## 5. Misplacing the original variable

<figure><img src="../../../.gitbook/assets/image (44).png" alt=""><figcaption></figcaption></figure>

## 6. Load GSS again if the variables are misplaced in codes

After misplacing the original variable…&#x20;

We have to “Load GSS” again, because we lost the values of the original variable.

From [Common mistakes and troubleshooting in RStudio](https://ttezcan.gitbook.io/lect/all-lectures-and-labs/r-lab/lab-resources/common-mistakes-and-troubleshooting-in-rstudio):

<figure><img src="https://lh7-us.googleusercontent.com/cX8vUW2LicQdrviPjgRTXVWDKJAmKjzW24TaADVlA_gx2u8ukumHsaL6IXWPAHM5-rIgZmNZqIMnKPO_2oUky_6EyVgGCGbWC435j30mpTR6IlisW-6gXa4MZfSP9ZUPiHxW6s1JCTdLyAnQk3I6iQ=s2048" alt=""><figcaption></figcaption></figure>

\
