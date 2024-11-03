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

# Flashcards

## 1) How to create RStudio Cloud account and installing all the packages

### Video guideline:

{% embed url="https://www.youtube.com/watch?v=G7SvmDZrpNE" %}

### Textual guideline:

Follow the procedures described in the [RStudio lab assignment: account and packages assignment instructions](https://docs.google.com/document/d/1P0gpXCsAk03u9fSdHNdMpO43TCbHUoJT/edit?usp=sharing\&ouid=100179871492576617561\&rtpof=true\&sd=true).

***

## 2) How to open and use R script files in RStudio Cloud

### Video guideline:

{% embed url="https://youtu.be/G12HTq6zJ-g" %}

Make sure you have a RStudio Cloud account. Otherwise, get one and install all the packages. [See this guideline](https://ttezcan.gitbook.io/lectures/all-lectures-and-labs/r-lab/lab-resources/how-to-create-rstudio-cloud-account-and-installing-all-the-packages).

### Textual guideline:&#x20;

1. Open [RStudio Cloud website](https://posit.cloud/) and log in. Click "RStudio labs" under "Your content."
2. Download the R script file you need:
   1. Go to Canvas <mark style="color:red;">➜</mark> Resources module page <mark style="color:red;">➜</mark> “Lab resources” <mark style="color:red;">➜</mark> “All R script files” <mark style="color:red;">➜</mark> Click on the R Script file you need and download that file. [“All script files” is here](https://ttezcan.gitbook.io/lectures/all-lectures-and-labs/r-lab/lab-resources/all-r-script-files) for your convenience.
   2. For example, if you need the "Descriptive Statistics" R script file. Click on it and download:

<figure><img src="../../../.gitbook/assets/ss_2024-07-16 16.55.54.png" alt="" width="375"><figcaption></figcaption></figure>

3. **Uploading R script files 1:** On [RStudio Cloud website](https://posit.cloud/), click “Upload” (see highlighted part #2 below).&#x20;

<figure><img src="../../../.gitbook/assets/image (65).png" alt="" width="563"><figcaption></figcaption></figure>

4. **Uploading R script files 2:** Click “Choose File.” Find the R script file you just downloaded (script\_descriptive.R) in the previous step, click “Open” and "OK."

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1).png" alt="" width="563"><figcaption></figcaption></figure>

5. **Opening R script files:** The file is uploaded and at the bottom of the "Files" list (see highlighted part #1). When you click on it, the descriptive R script file will open (see highlighted part #2).

<figure><img src="../../../.gitbook/assets/ss_2024-07-16 17.00.10.png" alt="" width="563"><figcaption></figcaption></figure>

6. **Installing and loading packages:** Whenever we open RStudio, we highlight all the lines under the “Install and load packages” (see highlighted part #1) and click run (see highlighted part #2).

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1).png" alt="" width="563"><figcaption></figcaption></figure>

7. **Loading data:** When the process of installing and loading packages is completed, we highlight all the lines under the “Load data” (see highlighted part #1) and click “Run” (see highlighted part #2).  When you see “gss” and “key” (see highlighted part #3), it means we successfully installed and loaded the packages, and loaded the GSS data.

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1).png" alt="" width="563"><figcaption></figcaption></figure>

8. **Running the analysis codes:** We highlight the codes (see highlighted part #1) and click “Run” (see highlighted part #2). Clicking “Run” generates the analysis (see highlighted part #3).

<figure><img src="../../../.gitbook/assets/image (3) (1) (1).png" alt="" width="563"><figcaption></figcaption></figure>

9.  **Using R script files - “working space” and outline view:** We do not edit or change anything on R script files except under “working space”(see highlighted part #1). Anything above the “working space” is teaching material!\


    The codes for assignments will be put under the “working space”\


    For easy navigation click “Outline” (see highlighted part #2) to see the headings and subheadings.

<figure><img src="../../../.gitbook/assets/ss_2024-07-24 09.40.36.png" alt="" width="563"><figcaption></figcaption></figure>

10. **Saving R script files:** When we make any changes, the font of the file name (shown in the highlighted part #2 above) will be red with an asterisk (\*) - (see the highlighted part #1 below). To save our progress, we click save (see the highlighted part #2 below)

<figure><img src="../../../.gitbook/assets/ss_2024-07-16 17.06.29.png" alt="" width="563"><figcaption></figcaption></figure>

***

## 3) Installing and loading packages (how to work)

We need specific packages to conduct our analyses. Running the "install and run packages" is always the first step.

<figure><img src="../../../.gitbook/assets/image (3) (1) (1) (1) (1) (1).png" alt="" width="563"><figcaption></figcaption></figure>

We can check the installed packages under “Packages.” Checkmark means that the specific packages are loaded for the session. If there is no checkmark, we have the package but it was not loaded.

<figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1) (1).png" alt="" width="375"><figcaption></figcaption></figure>

For troubleshooting, make sure to run "install and run packages" codes, wait until the “STOP” sign in the console disappears, no more code is running in the console, and see "Package already installed: _package name_" (under the console in red font, see the first figure).

## 4) Loading the data (how to work)

Every time we open RStudio, we must load the data. Even if we see "gss" under “Environment,” we should run "load data" code again. If we do not see "gss" under "Environment," our codes will not work.

<figure><img src="../../../.gitbook/assets/image (5) (1) (1) (1) (1).png" alt="" width="563"><figcaption></figcaption></figure>

If the data is not loaded, we will get the following error (under the console):

<figure><img src="../../../.gitbook/assets/image (6) (1) (1).png" alt="" width="313"><figcaption></figcaption></figure>

For troubleshooting, make sure to run "install and run packages" codes and "load data" codes in order.

***

## 5) Working in the "Working space" (how to work)

We do not edit or change anything on R script files except under “working space”(see highlighted part #1). Anything above the “working space” is teaching material!

The codes for assignments will be put under the “working space”

For easy navigation click “Outline” (see highlighted part #2) to see the headings and subheadings.

<figure><img src="../../../.gitbook/assets/image (83).png" alt="" width="563"><figcaption></figcaption></figure>

If we accidentally delete something from the R script file (above the working space), we can undo the changes using ctrl + Z for Windows or command + Z for macOS. If we lose track of the changes or cannot undo them, we simply re-upload the original R script file.

If this happens, we should first rename the current R script file because re-uploading the file will overwrite it and we lose our previous progress. Based on the sample below, we can rename the file to 'script\_scripting\_previous.R' (make sure not to delete the ".R" file extension at the end). Click "check box" (see highlighted part #1) and click "Rename" (see highlighted part #2)&#x20;

<figure><img src="../../../.gitbook/assets/ss_2024-07-24 14.55.33.png" alt="" width="375"><figcaption></figcaption></figure>

***

## 6) Using a model code (how to work)

Whenever we run an analysis with a different variable, we create a model code and a working code.

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1).png" alt="" width="563"><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1).png" alt="" width="563"><figcaption></figcaption></figure>

This is a view from the [Code templates](https://ttezcan.gitbook.io/lect/all-lectures-and-labs/r-lab/lab-resources/code-templates) page. Triple click the code and copy, or click "Copy" (see the highlighted part).

<figure><img src="../../../.gitbook/assets/image (89).png" alt="" width="563"><figcaption></figcaption></figure>

If we don’t use model code for comparison, it is likely that we accidentally delete something extra. In this example, the comma was deleted.

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="273"><figcaption></figcaption></figure>

Instead, we keep the use model code and compare it with our working code. Here we clearly see that the comma is missing in line 79. Note that RStudio warns us that something is wrong with that red cross.

<figure><img src="../../../.gitbook/assets/image (3) (1) (1) (1).png" alt="" width="321"><figcaption></figcaption></figure>

After identifying what is missing, we can fix the working code. Once the working code functions correctly, we can delete the model code.

<figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1).png" alt="" width="320"><figcaption></figcaption></figure>

## 7) Pasting variable names (how to work)

We **NEVER** type variable names! It is very common to miswrite codes, forget commas, etc. We always copy the variable names (from the code templates page or assignments), and paste into our codes.

There is no variable called “maritaal”, but “marital.” RStudio warns us that “maritaal” is “unknown.” We copy and paste variable names to avoid this possibility.

<figure><img src="../../../.gitbook/assets/image (8) (1).png" alt="" width="563"><figcaption></figcaption></figure>

***

## 8) Highlighting all the lines when running codes (how to work)

We need to highlight all the lines and click “Run.”

For single lines, we triple click (clicking three times _really_ fast).

For multiple lines, we highlight the codes with mouse.

Here's what happens if we don't:

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="563"><figcaption></figcaption></figure>

It simply shows what we highlighted and run (check the console part), not the analysis (check the plots part).

Instead, we should have highlighted all the line:

<figure><img src="../../../.gitbook/assets/ss_2024-07-22 11.41.45.png" alt="" width="563"><figcaption></figcaption></figure>

***

## 9) Putting hashtags (#) for our notes (how to work)

Typing notes on our R script files is encouraged. When we type a note, we must put a hashtag (#) first (we can put # anywhere we want). Not putting a hashtag (#) will confuse RStudio.

While line 29 will work, line 27 won’t. Here RStudio warns us that there is something wrong. Look at the red cross on line 27. When there is a red cross on the left side of the line number, there is something wrong with our codes.

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="563"><figcaption></figcaption></figure>

***

## 10) Not changing the original values of the dataset (how to work)

We **never** save our data, but our R script files. From time to time, we may accidentally change the values of original variables (especially when we recode variables).&#x20;

When this happens, we go to the very top of the R script file and load the data again. If we created new variables previously, we will need to run those codes under our working space again in order since it will be a fresh data.

<figure><img src="../../../.gitbook/assets/ss_2024-07-22 11.20.29.png" alt="" width="563"><figcaption></figcaption></figure>

***

## 11) Different recoding codes for different variables (recoding)

Recoding a categorical variable and a continuous variable requires slightly different codes

<figure><img src="../../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

***

## 12) Use the recoded (new) variable in analyses (recoding)

When we want to display, for example, the frequency distribution of a recoded (new) variable, we must use the recoded (new) variable’s name in the frequency code.

This is because, for our analysis, the original variable is no longer relevant. We recoded the original variable and created a new one for our analysis needs.

<figure><img src="../../../.gitbook/assets/image (1) (1) (1).png" alt="" width="375"><figcaption></figcaption></figure>

***

## 13) Recoded variables are always categorical (recoding)

When we recode a continuous variable, the new (recoded) variable is no longer continuous.

It becomes <mark style="color:red;">CATEGORICAL</mark> because we have merged the real numbers, and they no longer remain as real numbers.

Therefore, for example, we use the <mark style="color:red;">FRQ</mark> code to see the frequency distribution.

<figure><img src="../../../.gitbook/assets/image (2) (1) (1).png" alt="" width="375"><figcaption></figcaption></figure>

***

## 14) Not using a model code  (recoding)

<figure><img src="../../../.gitbook/assets/image (43).png" alt="" width="563"><figcaption></figcaption></figure>

Use the [Code templates](https://ttezcan.gitbook.io/lect/all-lectures-and-labs/r-lab/lab-resources/code-templates) page and Model codes:

<figure><img src="../../../.gitbook/assets/image (3) (1).png" alt="" width="563"><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (4) (1).png" alt="" width="563"><figcaption></figcaption></figure>

***

## 15) Pasting the original variable to the correct place (recoding)

<figure><img src="../../../.gitbook/assets/image (5) (1).png" alt="" width="563"><figcaption></figcaption></figure>

***

## 16) Load GSS data again if variables are misplaced in the codes and have thus overwritten the original values (recoding)

If variables are misplaced in the codes and have overwritten the original values, we have to “Load GSS” again, because we lost the values of the original variable and we need a fresh data.

<figure><img src="../../../.gitbook/assets/image (1).png" alt="" width="563"><figcaption></figcaption></figure>

***

\
