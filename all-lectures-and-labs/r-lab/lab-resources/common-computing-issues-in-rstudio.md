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

# Common computing issues in RStudio

## 1. Not using the new (recoded) variables in computation code

<figure><img src="../../../.gitbook/assets/image (53).png" alt=""><figcaption></figcaption></figure>

## 2. Computed variables are always continuous

When we compute variables and create an index, the new (computed) variable is continuous.

It becomes CONTINUOUS because we have created a score, and we treat it as a real number.

Therefore, we use the DESCR code to see the distribution (mean and standard deviation)

<figure><img src="../../../.gitbook/assets/image (54).png" alt=""><figcaption></figcaption></figure>

When we recode a continuous variable, the new (recoded) variable is no longer continuous.

It becomes CATEGORICAL because we have merged the real numbers, and they no longer remain as real numbers.\
Therefore, for example, we use the FRQ code to see the distribution.

<figure><img src="../../../.gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure>

## 3. Not using a model code

Use the [Code templates](https://ttezcan.gitbook.io/lect/all-lectures-and-labs/r-lab/lab-resources/code-templates) page.

<figure><img src="../../../.gitbook/assets/image (55).png" alt=""><figcaption></figcaption></figure>



\
