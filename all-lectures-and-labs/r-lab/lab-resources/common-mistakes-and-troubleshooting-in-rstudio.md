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

# Common mistakes and troubleshooting in RStudio

## <mark style="color:orange;">1. Not installing and loading packages</mark>

We need specific packages to conduct our analyses. Running the "install and run packages" is always the first step.

<figure><img src="../../../.gitbook/assets/image (3) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

We can check the installed packages under “Packages.” Checkmark means that the specific packages are loaded for the session.

<figure><img src="../../../.gitbook/assets/image (4) (1) (1).png" alt=""><figcaption></figcaption></figure>

## <mark style="color:orange;">2. Not loading the data</mark>

Every time we open RStudio, we must load the data.

Even if we see "gss" under “Environment,” we should run "load data" code again. If we do not see "gss" under "Environment," our codes will not work.

<figure><img src="../../../.gitbook/assets/image (5) (1) (1).png" alt=""><figcaption></figcaption></figure>

If the data is not loaded, we will get the following error (under the console):

<figure><img src="../../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

## <mark style="color:orange;">3. Typing variable names</mark>

We **NEVER** type variable names! It is very common to miswrite codes, forget commas, etc. We always copy the variable names, and paste into our codes.

There is no variable called “maritaal”, but “marital.” RStudio warns us that “maritaal” is “unknown.” We copy and paste variable names to avoid this possibility.

<figure><img src="../../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

## <mark style="color:orange;">4. Changing the original values of the dataset</mark>

We do not save your data, but our R script files. From time to time, we may accidentally change the values of original variables (especially when we recode variables).&#x20;

When this happens, we go to the very top of the R script file and load the dataset again (see #2). If we created new variables previously, we will need to run those codes again since it will be a fresh data.

<figure><img src="../../../.gitbook/assets/ss_2024-07-22 11.20.29.png" alt=""><figcaption></figcaption></figure>

## <mark style="color:orange;">5. Not highlighting all the lines when running codes</mark>

We need to highlight all the lines and click “run.”

For single lines, we triple click (clicking three times _really_ fast).

For multiple lines, we highlight the codes with mouse.

Here's what happens if we don't:

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

It simply shows what we highlighted and run (check the console part), not the analysis (check the plots part).

Instead, we should have highlighted all the line:

<figure><img src="../../../.gitbook/assets/ss_2024-07-22 11.41.45.png" alt=""><figcaption></figcaption></figure>

## <mark style="color:orange;">6. Not putting hashtags (#) for our comments</mark>

Typing notes on our RScript file is encouraged. When we type a note, we must put a hashtag (#) first (we can put # anywhere we want). Not putting a hashtag (#) will confuse RStudio.

While line 29 will work, line 27 won’t. Here RStudio warns us that there is something wrong. Look at the cross on line 27. When there is a red cross on the left side of the line number, there is something wrong with our codes.

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

## <mark style="color:orange;">7. Not using a model code</mark>

Whenever we run an analysis with a different variable, we  create a model code and a working code.

<figure><img src="../../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

If we don’t use model code for comparison, it’s likely that we may accidentally delete something extra. In this example, the comma was deleted.

<figure><img src="../../../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Instead, we keep the use model code and compare it with our working code. Here we see that the comma is missing in line 79. Note that RStudio warns us that something is wrong with that red cross.

<figure><img src="../../../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>

After seeing what is missing, we can fix the working code.

<figure><img src="../../../.gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure>
