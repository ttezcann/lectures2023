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

<figure><img src="../../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>



## <mark style="color:orange;">2. Not using the recoded (new) variable in analyses</mark>

When we want to display, for example, the frequency distribution of a recoded (new) variable, we must use the recoded (new) variable’s name in the frequency code.

This is because, for our analysis, the original variable is no longer relevant. We recoded the original variable and created a new one for our analysis needs.

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1).png" alt="" width="563"><figcaption></figcaption></figure>



## <mark style="color:orange;">3. Recoded variables are always categorical</mark>

When we recode a continuous variable, the new (recoded) variable is no longer continuous.

It becomes <mark style="color:red;">CATEGORICAL</mark> because we have merged the real numbers, and they no longer remain as real numbers.

Therefore, for example, we use the <mark style="color:red;">FRQ</mark> code to see the frequency distribution.

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1).png" alt="" width="563"><figcaption></figcaption></figure>



## <mark style="color:orange;">4. Not using a model code</mark>

<figure><img src="../../../.gitbook/assets/image (43).png" alt=""><figcaption></figcaption></figure>



Use the [Code templates](https://ttezcan.gitbook.io/lect/all-lectures-and-labs/r-lab/lab-resources/code-templates) page and [Model codes](https://ttezcan.gitbook.io/lectures/all-lectures-and-labs/r-lab/lab-resources/model-codes)

<figure><img src="../../../.gitbook/assets/image (3) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure>



## <mark style="color:orange;">5. Misplacing the original variable</mark>

<figure><img src="../../../.gitbook/assets/image (5) (1).png" alt=""><figcaption></figcaption></figure>



## <mark style="color:orange;">6.</mark> <mark style="color:orange;">Load GSS data again if variables are misplaced in the codes and have thus overwritten the original values</mark>

If misplacing the original variable (Common recoding issues (5))…&#x20;

We have to “Load GSS” again, because we lost the values of the original variable and we need a fresh data.

From [Common mistakes and troubleshooting in RStudio](https://ttezcan.gitbook.io/lect/all-lectures-and-labs/r-lab/lab-resources/common-mistakes-and-troubleshooting-in-rstudio):

<figure><img src="../../../.gitbook/assets/image (6) (1).png" alt=""><figcaption></figcaption></figure>

\
