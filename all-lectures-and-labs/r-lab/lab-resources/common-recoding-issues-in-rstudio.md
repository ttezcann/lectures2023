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

## <mark style="color:orange;">1. Recoding a categorical variable and a continuous variable requires slightly different code</mark>

<figure><img src="../../../.gitbook/assets/image (39).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (40).png" alt=""><figcaption></figcaption></figure>

## <mark style="color:orange;">2. Not using the recoded (new) variable in analyses</mark>

When we want to display the frequency distribution of a new (recoded) variable, we must use the new variable’s name in the frequency code.&#x20;

This is because, for our analysis, the original variable is no longer relevant. We recoded the original variable and created a new one for our analysis needs.

<figure><img src="../../../.gitbook/assets/image (41).png" alt=""><figcaption></figcaption></figure>

## <mark style="color:orange;">3. Recoded variables are always categorical</mark>

When we recode a continuous variable, the new (recoded) variable is no longer continuous.

It becomes CATEGORICAL because we have merged the real numbers, and they no longer remain as real numbers.\
Therefore, for example, we use the FRQ code to see the distribution.

<figure><img src="../../../.gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure>

## <mark style="color:orange;">4. Not using a model code</mark>

<figure><img src="../../../.gitbook/assets/image (43).png" alt=""><figcaption></figcaption></figure>

[\[Model codes\] instructions](https://ttezcan.gitbook.io/lectures/all-lectures-and-labs/r-lab/lab-resources/model-codes)

Use the [Code templates](https://ttezcan.gitbook.io/lect/all-lectures-and-labs/r-lab/lab-resources/code-templates) page.

Determine how many responses will you need in your new (recoded) variable. In the first example of the recoding lecture, we needed TWO (married and unmarried people) responses.

<figure><img src="../../../.gitbook/assets/image (45).png" alt=""><figcaption></figcaption></figure>

## <mark style="color:orange;">5. Misplacing the original variable</mark>

<figure><img src="../../../.gitbook/assets/image (44).png" alt=""><figcaption></figcaption></figure>

## <mark style="color:orange;">6. Load data again if the variables are misplaced in codes</mark>

After misplacing the original variable…&#x20;

We have to “Load data” again, because we lost the values of the original variable.

From [Common mistakes and troubleshooting in RStudio](https://ttezcan.gitbook.io/lect/all-lectures-and-labs/r-lab/lab-resources/common-mistakes-and-troubleshooting-in-rstudio)

<figure><img src="../../../.gitbook/assets/image (3) (1) (1).png" alt=""><figcaption></figcaption></figure>

\
