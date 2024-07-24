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

We can check the installed packages under “Packages.” Checkmark means that the specific packages are loaded for the session. If there is no checkmark, we have the package but it was not loaded.

<figure><img src="../../../.gitbook/assets/image (4) (1) (1).png" alt="" width="375"><figcaption></figcaption></figure>

For troubleshooting, make sure to run "install and run packages" codes, wait until the “STOP” sign in the console disappears, no more code is running in the console, and see "Package already installed: _package name_" (under the console in red font, see the first figure).

## <mark style="color:orange;">2. Not loading the data</mark>

Every time we open RStudio, we must load the data. Even if we see "gss" under “Environment,” we should run "load data" code again. If we do not see "gss" under "Environment," our codes will not work.

<figure><img src="../../../.gitbook/assets/image (5) (1) (1).png" alt=""><figcaption></figcaption></figure>

If the data is not loaded, we will get the following error (under the console):

<figure><img src="../../../.gitbook/assets/image (6).png" alt="" width="313"><figcaption></figcaption></figure>

For troubleshooting, make sure to run "install and run packages" codes and "load data" codes in order.

## <mark style="color:orange;">3. Not working in the "Working space"</mark>

We do not edit or change anything on R script files except under “working space”(see highlighted part #1). Anything above the “working space” is teaching material!

The codes for assignments will be put under the “working space”

For easy navigation click “Outline” (see highlighted part #2) to see the headings and subheadings.

<figure><img src="../../../.gitbook/assets/image (83).png" alt=""><figcaption></figcaption></figure>

If we accidentally delete something from the R script file (above the working space), we can undo the changes using ctrl + Z for Windows or command + Z for macOS. If we lose track of the changes or cannot undo them, we simply re-upload the original R script file.

If this happens, we should first rename the current R script file because re-uploading the file will overwrite it and we lose our previous progress. Based on the sample below, we can rename the file to 'script\_scripting\_previous.R' (make sure not to delete the ".R" file extension at the end). Click "check box" (see highlighted part #1) and click "Rename" (see highlighted part #2)&#x20;

<figure><img src="../../../.gitbook/assets/ss_2024-07-24 14.55.33.png" alt="" width="375"><figcaption></figcaption></figure>

## <mark style="color:orange;">4. Not using a model code</mark>

Whenever we run an analysis with a different variable, we create a model code and a working code.

<figure><img src="../../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

If we don’t use model code for comparison, it is likely that we accidentally delete something extra. In this example, the comma was deleted.

<figure><img src="../../../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Instead, we keep the use model code and compare it with our working code. Here we clearly see that the comma is missing in line 79. Note that RStudio warns us that something is wrong with that red cross.

<figure><img src="../../../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>

After identifying what is missing, we can fix the working code. Once the working code functions correctly, we can delete the model code.

<figure><img src="../../../.gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure>

## <mark style="color:orange;">5. Typing variable names</mark>

We **NEVER** type variable names! It is very common to miswrite codes, forget commas, etc. We always copy the variable names (from the code templates page or assignments), and paste into our codes.

There is no variable called “maritaal”, but “marital.” RStudio warns us that “maritaal” is “unknown.” We copy and paste variable names to avoid this possibility.

<figure><img src="../../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

## <mark style="color:orange;">6. Not highlighting all the lines when running codes</mark>

We need to highlight all the lines and click “Run.”

For single lines, we triple click (clicking three times _really_ fast).

For multiple lines, we highlight the codes with mouse.

Here's what happens if we don't:

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

It simply shows what we highlighted and run (check the console part), not the analysis (check the plots part).

Instead, we should have highlighted all the line:

<figure><img src="../../../.gitbook/assets/ss_2024-07-22 11.41.45.png" alt=""><figcaption></figcaption></figure>

## <mark style="color:orange;">7. Not putting hashtags (#) for our notes</mark>

Typing notes on our R script files is encouraged. When we type a note, we must put a hashtag (#) first (we can put # anywhere we want). Not putting a hashtag (#) will confuse RStudio.

While line 29 will work, line 27 won’t. Here RStudio warns us that there is something wrong. Look at the red cross on line 27. When there is a red cross on the left side of the line number, there is something wrong with our codes.

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

## <mark style="color:orange;">8. Changing the original values of the dataset</mark>

We **never** save our data, but our R script files. From time to time, we may accidentally change the values of original variables (especially when we recode variables).&#x20;

When this happens, we go to the very top of the R script file and load the data again. If we created new variables previously, we will need to run those codes under our working space again in order since it will be a fresh data.

<figure><img src="../../../.gitbook/assets/ss_2024-07-22 11.20.29.png" alt=""><figcaption></figcaption></figure>
