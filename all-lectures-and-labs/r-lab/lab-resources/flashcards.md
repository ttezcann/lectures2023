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

## <mark style="color:orange;">1. How to create RStudio Cloud account and installing all the packages</mark>

Follow the procedures described in the [RStudio lab assignment: account and packages assignment instructions](https://docs.google.com/document/d/1P0gpXCsAk03u9fSdHNdMpO43TCbHUoJT/edit?usp=sharing\&ouid=100179871492576617561\&rtpof=true\&sd=true).

The process is also shown on the video below:

{% embed url="https://www.youtube.com/watch?v=G7SvmDZrpNE" %}

### <mark style="color:orange;">1.1. How to check how many hours left?</mark>

An RStudio Cloud free account allows you 25 hours of connect time per month. Every second the RStudio Cloud is open counts towards this allocated time.&#x20;

Therefore, whenever you are not running code or generating analyses, close the RStudio Cloud browser

Click on your name (see highlighted part #1). The highlighted part #2 shows the time period (e.g., "I will have 25 more hours on Aug 8, 2024"). The highlighted part #3 shows how many hours you have spent.

<figure><img src="../../../.gitbook/assets/image (86).png" alt="" width="563"><figcaption></figcaption></figure>

### <mark style="color:orange;">1.2. What to do if you exceed 25 hours per month?</mark>

25 hours of connect time is enough for this class. If you exceed this limit, open another free account using a different email address. Follow the procedures described in the [RStudio lab assignment: account and packages assignment instructions](https://docs.google.com/document/d/1P0gpXCsAk03u9fSdHNdMpO43TCbHUoJT/edit?usp=sharing\&ouid=100179871492576617561\&rtpof=true\&sd=true).

### <mark style="color:orange;">1.3. What to do if you want your new free account to be identical (files, packages, etc.) to the previous account where you exceeded the time limit?</mark>

1. Go to the previous account where you exceeded the time limit.
2. Click "Export" (see the highlighted part)

<figure><img src="../../../.gitbook/assets/image (87).png" alt="" width="563"><figcaption></figcaption></figure>

3. Click "Download"

<figure><img src="../../../.gitbook/assets/image (88).png" alt="" width="563"><figcaption></figcaption></figure>

4. It will download a zip file.
5. Go to your new account.
6. Upload that zip file just like you upload a R script file.

***

## <mark style="color:orange;">2. How to open and use R script files in RStudio Cloud</mark>

### <mark style="color:orange;">2.1. Video guideline:</mark>

{% embed url="https://youtu.be/G12HTq6zJ-g" %}

Make sure you have a RStudio Cloud account. Otherwise, get one and install all the packages. [See this guideline](https://ttezcan.gitbook.io/lectures/all-lectures-and-labs/r-lab/lab-resources/how-to-create-rstudio-cloud-account-and-installing-all-the-packages).

### <mark style="color:orange;">2.2. Textual guideline:</mark>&#x20;

1. Open [RStudio Cloud website](https://posit.cloud/) and log in. Click "RStudio labs" under "Your content."
2. Download the R script file you need:
   1. Go to Canvas <mark style="color:red;">➜</mark> Resources module page <mark style="color:red;">➜</mark> “Lab resources” <mark style="color:red;">➜</mark> “All R script files” <mark style="color:red;">➜</mark> Click on the R Script file you need and download that file. [“All script files” is here](https://ttezcan.gitbook.io/lectures/all-lectures-and-labs/r-lab/lab-resources/all-r-script-files) for your convenience.
   2. For example, if you need the "Descriptive Statistics" R script file. Click on it and download:

<figure><img src="../../../.gitbook/assets/ss_2024-07-16 16.55.54.png" alt="" width="375"><figcaption></figcaption></figure>

3. **Uploading R script files 1:** On [RStudio Cloud website](https://posit.cloud/), click “Upload” (see highlighted part #2 below).&#x20;

<figure><img src="../../../.gitbook/assets/image (65).png" alt="" width="563"><figcaption></figcaption></figure>

4. **Uploading R script files 2:** Click “Choose File.” Find the R script file you just downloaded (script\_descriptive.R) in the previous step, click “Open” and "OK."

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1).png" alt="" width="563"><figcaption></figcaption></figure>

5. **Opening R script files:** The file is uploaded and at the bottom of the "Files" list (see highlighted part #1). When you click on it, the descriptive R script file will open (see highlighted part #2).

<figure><img src="../../../.gitbook/assets/ss_2024-07-16 17.00.10.png" alt="" width="563"><figcaption></figcaption></figure>

6. **Installing and loading packages:** Whenever we open RStudio, we highlight all the lines under the “Install and load packages” (see highlighted part #1) and click run (see highlighted part #2).

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1).png" alt="" width="563"><figcaption></figcaption></figure>

7. **Loading data:** When the process of installing and loading packages is completed, we highlight all the lines under the “Load data” (see highlighted part #1) and click “Run” (see highlighted part #2).  When you see “gss” and “key” (see highlighted part #3), it means we successfully installed and loaded the packages, and loaded the GSS data.

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1).png" alt="" width="563"><figcaption></figcaption></figure>

8. **Running the analysis codes:** We highlight the codes (see highlighted part #1) and click “Run” (see highlighted part #2). Clicking “Run” generates the analysis (see highlighted part #3).

<figure><img src="../../../.gitbook/assets/image (3) (1) (1).png" alt="" width="563"><figcaption></figcaption></figure>

9.  **Using R script files - “working space” and outline view:** We do not edit or change anything on R script files except under “working space”(see highlighted part #1). Anything above the “working space” is teaching material!\


    The codes for assignments will be put under the “working space”\


    For easy navigation click “Outline” (see highlighted part #2) to see the headings and subheadings.

<figure><img src="../../../.gitbook/assets/ss_2024-07-24 09.40.36.png" alt="" width="563"><figcaption></figcaption></figure>

10. **Saving R script files:** When we make any changes, the font of the file name (shown in the highlighted part #2 above) will be red with an asterisk (\*) - (see the highlighted part #1 below). To save our progress, we click save (see the highlighted part #2 below)

<figure><img src="../../../.gitbook/assets/ss_2024-07-16 17.06.29.png" alt="" width="563"><figcaption></figcaption></figure>









## Not using the new (recoded) variables in computation code

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
