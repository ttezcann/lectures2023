# Flashcards

{% hint style="success" %}
Maximize your browser window to display the outline on the right side for easier navigation.
{% endhint %}

## A. Setup

{% stepper %}
{% step %}
### How to create RStudio Cloud account and installing all the packages

#### (A) Video guideline

{% embed url="https://drive.google.com/open?id=1qS2xGpy1h04ojoOoFLOrW8rehxsr6cUL&usp=drive_fs" %}

#### (B) Textual guideline

Follow the procedures described in [\[How to create RStudio Cloud account and installing all the packages\]](https://ttezcan.gitbook.io/lectures/all-lectures-and-labs/r-lab/lab-resources/how-to-create-rstudio-cloud-account-and-installing-all-the-packages)
{% endstep %}

{% step %}
### How to open and use R script files in RStudio Cloud

#### (A) Video guideline

{% embed url="https://youtu.be/G12HTq6zJ-g" %}

#### (B) Textual guideline

1. Open [RStudio Cloud website](https://posit.cloud/) and log in. Click "RStudio labs" under "Your content."
2. Download the R script file you need:
   1. Go to Canvas <mark style="color:red;">➜</mark> Resources module page <mark style="color:red;">➜</mark> “Lab resources” <mark style="color:red;">➜</mark> “All R script files” <mark style="color:red;">➜</mark> Click on the R Script file you need and download that file. [“All script files” is here](https://ttezcan.gitbook.io/lectures/all-lectures-and-labs/r-lab/lab-resources/all-r-script-files) for your convenience.
   2.  For example, if you need the "Descriptive Statistics" R script file. Click on it and download:

       <figure><img src="../../../.gitbook/assets/ss_2024-07-16 16.55.54.png" alt="" width="375"><figcaption></figcaption></figure>
3.  **Uploading R script files:** On [RStudio Cloud website](https://posit.cloud/), click “Upload” (see highlighted part #2 below). Click “Choose File.” Find the R script file you just downloaded (e.g., script\_descriptive.R) in the previous step, click “Open” and "OK."

    <figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1).png" alt="A screenshot of the RStudio interface showing the Upload Files dialog open. The dialog displays the target directory /cloud/project, with a red callout highlighting the Choose File button and another highlighting the Upload button in the Files pane, indicating how to upload files into an RStudio cloud project."><figcaption></figcaption></figure>
4.  **Opening R script files:** The file is uploaded and at the bottom of the "Files" list (see highlighted part #1). When you click on it, the descriptive R script file will open (see highlighted part #2).

    <figure><img src="../../../.gitbook/assets/image (2) (1).png" alt="A screenshot of the RStudio interface showing an open script titled script_intro.R in the Source pane on the left, with commented instructions and example R code. Red callouts highlight the script tab in the Source pane and the same file listed in the Files pane on the right, indicating where to open and locate the R script within the RStudio workspace."><figcaption></figcaption></figure>
5.  **Installing and loading packages:** Make sure you click on the R script file name and open it (see highlighted part #1). Whenever we open RStudio, we highlight all the lines under the “Install and load packages” (see highlighted part #2) and click run (see highlighted part #3).

    <figure><img src="../../../.gitbook/assets/image (3).png" alt="A screenshot of the RStudio interface demonstrating how to install packages. The Files pane highlights a script named script_installing packages.R (labeled 1). In the Source pane, a block of code for installing and loading packages is highlighted in red (labeled 2). A large red circle emphasizes the Run button at the top of the Source pane (labeled 3), indicating that the user should select the highlighted code and click Run to execute it."><figcaption></figcaption></figure>
6.  **Loading data:** When the process of installing and loading packages is completed, we highlight all the lines under the “Load data” (see highlighted part #1) and click “Run” (see highlighted part #2).  When you see “gss” and “key” (see highlighted part #3), it means we successfully installed and loaded the packages, and loaded the GSS data.

    <figure><img src="../../../.gitbook/assets/image (4).png" alt="A screenshot of the RStudio interface showing how to load data using an R script. In the Source pane, a block of code labeled “Load data” is highlighted in red (label 1). The Run button at the top of the Source pane is circled and pointed out (label 2), indicating how to execute the selected code. In the Environment pane on the right, two newly loaded objects—gss and key—are highlighted (label 3), confirming that the data were successfully loaded."><figcaption></figcaption></figure>
7.  **Running the analysis codes:** We highlight the codes (see highlighted part #1) and click “Run” (see highlighted part #2). Clicking “Run” generates the analysis (see highlighted part #3).

    <figure><img src="../../../.gitbook/assets/image (139).png" alt="A screenshot of the RStudio interface showing an example of running code and viewing output. A line of code generating a frequency table for respondents’ sex is highlighted in the script editor, the Run button is circled to indicate execution, and the resulting frequency table appears in the Viewer pane with counts and percentages for male and female respondents."><figcaption></figcaption></figure>
8.  **Using R script files - “working space” and outline view:** We do not edit or change anything on R script files except under “working space”(see highlighted part #1). Anything above the “working space” is teaching material!<br>

    The codes for assignments will be put under the “working space”<br>

    For easy navigation click “Outline” (see highlighted part #2) to see the headings and subheadings.

    <figure><img src="../../../.gitbook/assets/SCR-20251226-jmyc-2.png" alt="A warning message states, “Do not edit or change anything on R script files except under ‘WORKING SPACE’ (#1).” The section labeled WORKING SPACE is highlighted in red within the script editor (label 1), indicating where users are allowed to make changes. At the top of the editor, a toolbar area is circled (label 2) showing the outline for easy navigation."><figcaption></figcaption></figure>
9.  **Saving R script files:** When we make any changes, the font of the file name (shown in the highlighted part #2 above) will be red with an asterisk (\*) - (see the highlighted part #1 below). To save our progress, we click save (see the highlighted part #2 below)

    <figure><img src="../../../.gitbook/assets/SCR-20251226-jkop-2.png" alt="A screenshot of the RStudio interface illustrating how file-saving status is indicated. When changes are made, the script file name appears in red with an asterisk, indicating unsaved edits. Clicking the Save button stores the changes, after which the file name turns black, showing that all changes are saved."><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

***

## B. How to work with RStudio

{% stepper %}
{% step %}
### Installing and loading packages

We need specific packages to conduct our analyses. Running the "install and run packages" is always the first step.

For troubleshooting, make sure to run "install and run packages" codes, wait until the “STOP” sign in the console disappears, no more code is running in the console, and see "Package already installed: _package name_" (under the console in red font, see the first figure).

<figure><img src="../../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

We can check the installed packages under “Packages.” Checkmark means that the specific packages are loaded for the session. If there is no checkmark, we have the package but it was not loaded.

<figure><img src="../../../.gitbook/assets/SCR-20251226-jtei-2.png" alt="Packages view" width="375"><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Loading the data

Every time we open RStudio, we must load the data. Even if we see "gss" under “Environment,” we should run "load data" code again. If we do not see "gss" under "Environment," our codes will not work.

<figure><img src="../../../.gitbook/assets/image (4).png" alt="A screenshot of the RStudio interface showing how to load data using an R script. In the Source pane, a block of code labeled “Load data” is highlighted in red (label 1). The Run button at the top of the Source pane is circled and pointed out (label 2), indicating how to execute the selected code. In the Environment pane on the right, two newly loaded objects—gss and key—are highlighted (label 3), confirming that the data were successfully loaded."><figcaption></figcaption></figure>

If the data is not loaded, we will get the following error (under the console):

<figure><img src="../../../.gitbook/assets/image (6) (1) (1) (1).png" alt="The error says &#x22;object &#x60;gss&#x60; not found&#x22;" width="313"><figcaption></figcaption></figure>

For troubleshooting, make sure to run "install and run packages" codes and "load data" codes in order.
{% endstep %}

{% step %}
### Working in the "Working space"

We do not edit or change anything on R script files except under “working space”(see highlighted part #1). Anything above the “working space” is teaching material!

The codes for assignments will be put under the “working space”

For easy navigation click “Outline” (see highlighted part #2) to see the headings and subheadings.

<figure><img src="../../../.gitbook/assets/SCR-20251226-jmyc-2.png" alt="A warning message states, “Do not edit or change anything on R script files except under ‘WORKING SPACE’ (#1).” The section labeled WORKING SPACE is highlighted in red within the script editor (label 1), indicating where users are allowed to make changes. At the top of the editor, a toolbar area is circled (label 2) showing the outline for easy navigation."><figcaption></figcaption></figure>

If we accidentally delete something from the R script file (above the working space), we can undo the changes using ctrl + Z for Windows or command + Z for macOS. If we lose track of the changes or cannot undo them, we simply re-upload the original R script file.

If this happens, we should first rename the current R script file because re-uploading the file will overwrite it and we lose our previous progress. Based on the sample below, we can rename the file to 'script\_scripting\_previous.R' (make sure not to delete the ".R" file extension at the end). Click "check box" (see highlighted part #1) and click "Rename" (see highlighted part #2)&#x20;

<figure><img src="../../../.gitbook/assets/ss_2024-07-24 14.55.33.png" alt="A screenshot of the RStudio Files pane showing a list of files in a project folder. The file script_scripting.R is selected and highlighted (label 1). At the top of the Files pane, the Rename button is highlighted (label 2), indicating the option used to rename the selected file."><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Working on codes in RStudio, not in assignment files

The lab assignments will ask you to paste the code for specific questions. Write and test the code in RStudio, and once it works, paste it into the assignment file. Do not write codes directly in the assignment file.

<figure><img src="../../../.gitbook/assets/Screenshot 2024-11-09 at 1.41.12 PM.png" alt="A slide explaining how to submit code for lab assignments. Text states that students should write and test code in RStudio, then paste the working code into the assignment file, and should not write code directly in the assignment document. Below, an example code block is shown with a note stating, “This code was pasted from RStudio; no changes made in Google Docs,” emphasizing that the code should be copied exactly after it works." width="563"><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Using a model code

Whenever we run an analysis with a different variable, we create a model code and a working code.

<figure><img src="../../../.gitbook/assets/SCR-20251231-ickl.png" alt="A teaching slide explaining how to work with R code using model codes from a separate Code templates page. The slide emphasizes that users should never type or modify code directly in the lab R script; instead, they create a model code and a working code.  Step 1 shows a model code example from the Code templates page for producing descriptive statistics, written with a placeholder variable name. This line is presented as known to work and should not be edited.  Step 2 explains copying this model code into the WORKING SPACE of the R script file twice, with a blank line between them. The first pasted line remains unchanged as the reference model code, and the second line is designated as the working code to be edited.  Step 3 shows editing only the working code by replacing the placeholder variable name with a specific variable, such as “educ.” If the edited working code does not run correctly, the user compares it to the unchanged model code to troubleshoot errors.  The overall message of the slide is that model codes provide a safe, reliable template, while all experimentation and changes should occur only in the working code."><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (1) (1).png" alt="A teaching slide explaining how to work with R code using model code and working code. The slide states that users should never edit the original code in the R script file; instead, they copy a known-working example (called the model code) into a designated “working space.” Step 1 shows a model code line that generates a frequency table. Step 2 explains copying that line twice into the working space so one line remains unchanged as a reference. Step 3 shows editing only the second line to change the variable name (for example, replacing “marital” with “sex”); if the edited code fails, it is compared to the unchanged model code to troubleshoot."><figcaption></figcaption></figure>

This is a view from the [Code templates](https://ttezcan.gitbook.io/lect/all-lectures-and-labs/r-lab/lab-resources/code-templates) page. Triple click the code and copy, or click "Copy" (see the highlighted part).

<figure><img src="../../../.gitbook/assets/image (89).png" alt="A “Code templates” box labeled “descriptive table (for continuous variables)” shows the model code: descr(gss$variable_here, out = &#x22;v&#x22;, show = &#x22;short&#x22;), with a “Copy” button on the right." width="563"><figcaption></figcaption></figure>

If we don’t use model code for comparison, it is likely that we accidentally delete something extra. In this example, the comma was deleted.

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="A single-line code snippet shows an error caused by a missing comma: frq(gss$sex out=&#x22;v&#x22;) (the comma between sex and out is missing). A red X icon appears next to the line number, indicating RStudio flags it as wrong." width="273"><figcaption></figcaption></figure>

Instead, we keep the use model code and compare it with our working code. Here we clearly see that the comma is missing in line 79. Note that RStudio warns us that something is wrong with that red cross.

<figure><img src="../../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1).png" alt="A short list of code lines (77–79) compares a correct “model” line with a faulty “working” line. Line 77 is frq(gss$marital, out=&#x22;v&#x22;) (correct), and line 79 is frq(gss$sex out=&#x22;v&#x22;) (missing comma). A red X icon marks the problematic line." width="321"><figcaption></figcaption></figure>

After identifying what is missing, we can fix the working code. Once the working code functions correctly, we can delete the model code.

<figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1) (1) (1).png" alt="The corrected code line is shown: frq(gss$sex, out=&#x22;v&#x22;), now including the comma after sex, indicating the error has been fixed." width="320"><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Pasting variable names

We **NEVER** type variable names! It is very common to miswrite codes, forget commas, etc. We always copy the variable names (from the code templates page or assignments), and paste into our codes.

There is no variable called “maritaal”, but “marital.” RStudio warns us that “maritaal” is “unknown.” We copy and paste variable names to avoid this possibility.

<figure><img src="../../../.gitbook/assets/image (8) (1).png" alt="An R script example shows the code frq(gss$maritaal, out = &#x22;v&#x22;), where the variable name is misspelled. In the console below, RStudio displays a warning message stating “Unknown or uninitialised column: ‘maritaal’,” illustrating how a typing error causes the code to fail and why copying variable names prevents this problem." width="563"><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Highlighting all the lines when running codes

We need to highlight all the lines and click “Run.”

* For single lines, we triple click (clicking three times _really_ fast).
* For multiple lines, we highlight the codes with mouse.

Here's what happens if we don't:

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="single lines should be selected with a triple click and multiple lines by dragging the mouse. An example screenshot shows code for generating a bar graph, but the output pane displays the message “No bar graph here!” indicating that the graph was not produced because the necessary lines were not highlighted and executed." width="563"><figcaption></figcaption></figure>

It simply shows what we highlighted and run (check the console part), not the analysis (check the plots part).

Instead, we should have highlighted all the line:

<figure><img src="../../../.gitbook/assets/ss_2024-07-22 11.41.45.png" alt="A screenshot of the RStudio interface showing multiple lines of code selected and executed together. The console reflects only the highlighted lines being run, while the Plots pane displays a bar chart of marital status. The image demonstrates that analysis results appear only when all necessary lines of code are highlighted and run, not when partial code is executed." width="563"><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Putting hashtags (#) for our notes (how to work)

Typing notes on our R script files is encouraged. When we type a note, we must put a hashtag (#) first (we can put # anywhere we want). Likewise I use "notes" in R script files to communicate with you.

<figure><img src="../../../.gitbook/assets/SCR-20251226-jdom-2.png" alt="A screenshot of an R script containing comments that begin with a hashtag symbol. A line of code generating a frequency table is shown, followed by a commented note explaining what the code does. The image illustrates that notes must start with a hashtag so RStudio recognizes them as comments rather than executable code."><figcaption></figcaption></figure>

Not putting a hashtag (#) will confuse RStudio.

While line 29 will work, line 27 won’t. Here RStudio warns us that there is something wrong. Look at the red cross on line 27. When there is a red cross on the left side of the line number, there is something wrong with our codes.

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="A screenshot of an R script showing a line of text intended as a note but missing a leading hashtag. RStudio displays a red error indicator next to the line number, signaling a problem. Below, corrected lines show the same text properly commented with a hashtag, indicating that adding the hashtag resolves the error." width="563"><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Not changing the original values of the dataset

We **never** save our data, but our R script files. From time to time, we may accidentally change the values of original variables (especially when we recode variables).&#x20;

When this happens, we go to the very top of the R script file and load the data again. If we created new variables previously, we will need to run those codes under our working space again in order since it will be a fresh data.

<figure><img src="../../../.gitbook/assets/image (4).png" alt="A screenshot of the RStudio interface showing how to load data using an R script. In the Source pane, a block of code labeled “Load data” is highlighted in red (label 1). The Run button at the top of the Source pane is circled and pointed out (label 2), indicating how to execute the selected code. In the Environment pane on the right, two newly loaded objects—gss and key—are highlighted (label 3), confirming that the data were successfully loaded."><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

***

## C. Keyboard and mouse shortcuts

{% stepper %}
{% step %}
### Using keyboard shortcuts

<figure><img src="../../../.gitbook/assets/image (91).png" alt="For Windows, the shortcuts shown are: Control plus C for Copy, Control plus V for Paste, and Control plus Z for Undo. For macOS, the corresponding shortcuts are: Command plus C for Copy, Command plus V for Paste, and Command plus Z for Undo. The slide visually aligns Windows shortcuts on the left and macOS shortcuts on the right to show their equivalence." width="563"><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Keyboard shortcuts: hand and finger positions (how to work)

<figure><img src="../../../.gitbook/assets/SCR-20251231-iect.png" alt="A side-by-side instructional image about using keyboard shortcuts correctly. On the left, a close-up photo shows one hand on a keyboard, with the little finger pressing the Control key and the index or middle finger pressing a letter key, demonstrating the correct hand position. On the right, a close-up photo shows both hands on the keyboard with a large red “X” over the image, indicating incorrect technique. Text explains that users should not use both hands for keyboard shortcuts and should keep the other hand on the mouse or trackpad."><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Using mouse shortcuts

<figure><img src="../../../.gitbook/assets/image (93).png" alt="explaining how to select text in an R script using mouse clicks. The first section explains that to replace an existing variable name, users should double-click the variable name so that only the word is highlighted. The second section explains that to select an entire line of code, users should triple-click anywhere on the line to highlight it all at once. The third section explains that to select multiple lines of code, users should click and drag the mouse to highlight several lines. Each instruction is paired with a code example showing the correct selection result."><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

***

## D. Common recoding issues

{% stepper %}
{% step %}
### Different recoding codes for different variables

Recoding a categorical variable and a continuous variable requires slightly different codes

<figure><img src="../../../.gitbook/assets/image (8).png" alt="Text explaining how to plan a recoding task by first identifying the type of recoding needed—merging categories, reversing categories, or grouping a continuous variable—and then determining how many categories the new recoded variable will have, with examples using marital status, stress, and education."><figcaption></figcaption></figure>

{% hint style="warning" %}
**Troubleshooting:**

* You need to check the "variable type" column of the variable (in "Variables in GSS page") you recode.
  1. If you recode a categorical variable, use comma (,) between the values for merging.
  2. If you recode a continuous variable, use colon (:) between the values.
{% endhint %}
{% endstep %}

{% step %}
### Use the recoded (new) variable in analyses

When we want to display, for example, the frequency distribution of a recoded (new) variable, we must use the recoded (new) variable’s name in the frequency code.

This is because, for our analysis, the original variable is no longer relevant. We recoded the original variable and created a new one for our analysis needs.

{% hint style="danger" %}
Wrong:&#x20;

frq(gss$<mark style="color:yellow;">**marital**</mark>, out = "v")
{% endhint %}

{% hint style="success" %}
Correct:

frq(gss$<mark style="color:yellow;">**maritalgroups**</mark>, out = "v")
{% endhint %}

{% hint style="warning" %}
**Troubleshooting:**

* After the recoding process, use the recoded (new) variable in analyses. Make sure you do not use the original variable name in analyses.
{% endhint %}
{% endstep %}

{% step %}
### Recoded variables are always categorical

When we recode a continuous variable, the new (recoded) variable is no longer continuous.

It becomes <mark style="color:red;">CATEGORICAL</mark> because we have merged the real numbers, and they no longer remain as real numbers.

Therefore, for example, we use the <mark style="color:red;">FRQ</mark> code to see the frequency distribution.

{% hint style="danger" %}
Wrong:&#x20;

descr(gss$<mark style="color:yellow;">**educgroups**</mark>, out = "v", show = "short")
{% endhint %}

{% hint style="success" %}
Correct:

frq(gss$<mark style="color:yellow;">**educgroups**</mark>, out = "v")
{% endhint %}

{% hint style="warning" %}
**Troubleshooting:**

* Recoded variables are always categorical. Therefore, they should be treated categorical in every analyses they are used.
{% endhint %}
{% endstep %}

{% step %}
### Not using a model code

<figure><img src="../../../.gitbook/assets/image (43).png" alt="A composite figure showing an R script with age-group recoding typed manually instead of copied from a model code. One line defining the 50–59 age group is incorrectly formatted, missing required punctuation such as a semicolon or bracket. A console output below displays a syntax error message indicating the problem, illustrating how not using a model code can lead to coding errors." width="563"><figcaption></figcaption></figure>

Use the [Code templates](https://ttezcan.gitbook.io/lect/all-lectures-and-labs/r-lab/lab-resources/code-templates) page and Model codes:

<figure><img src="../../../.gitbook/assets/image (3) (1) (1) (1) (1) (1).png" alt="Text explaining how to plan a recoding task by first identifying the type of recoding needed—merging categories, reversing categories, or grouping a continuous variable—and then determining how many categories the new recoded variable will have, with examples using marital status, stress, and education." width="563"><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1).png" alt="Two code examples showing recoding in R. The first is a model code template from a code templates page, and the second is a working code in RStudio that applies the template to create a new variable called maritalgroups by merging marital status categories." width="563"><figcaption></figcaption></figure>

{% hint style="warning" %}
**Troubleshooting:**

* In code templates page, there are [recoding templates for both categorical and continuous variables](https://ttezcan.gitbook.io/lectures/all-lectures-and-labs/r-lab/lab-resources/code-templates#recoding), with every kind of value possibility.
  1. determine what kind of recoding you need (merging, reversing, or transforming continuous variables into groups)
  2. determine how many values you will need in your recoded (new variables).
{% endhint %}
{% endstep %}

{% step %}
### Pasting the original variable to the correct place

<figure><img src="../../../.gitbook/assets/image (5) (1) (1).png" alt="A figure showing correct and incorrect placement of variable names when recoding in R. The incorrect example assigns the recode back to the original variable “marital,” which would overwrite its values and is marked with an X. The correct example assigns the recoded output to a new variable named “maritalgroups” while using the original variable as input, marked with a check, illustrating how to preserve the original data." width="563"><figcaption></figcaption></figure>

{% hint style="warning" %}
**Troubleshooting:**

1. The original variable you need to recode should be pasted (not typed) into the red area
2. The new variable variable name that RStudio will create when you run the code should be pasted (not typed) into the yellow area.
{% endhint %}
{% endstep %}

{% step %}
### Load GSS data again if variables are misplaced in the codes and have thus overwritten the original values

If variables are misplaced in the codes and have overwritten the original values, we have to “Load GSS” again, because we lost the values of the original variable and we need a fresh data.

We **never** save our data, but our R script files. From time to time, we may accidentally change the values of original variables (especially when we recode variables).&#x20;

When this happens, we go to the very top of the R script file and load the data again. If we created new variables previously, we will need to run those codes under our working space again in order since it will be a fresh data.

<figure><img src="../../../.gitbook/assets/image (4).png" alt="A screenshot of the RStudio interface showing how to load data using an R script. In the Source pane, a block of code labeled “Load data” is highlighted in red (label 1). The Run button at the top of the Source pane is circled and pointed out (label 2), indicating how to execute the selected code. In the Environment pane on the right, two newly loaded objects—gss and key—are highlighted (label 3), confirming that the data were successfully loaded."><figcaption></figcaption></figure>

{% hint style="warning" %}
**Troubleshooting:**

1. Mistakes happen. For example, you could put the new variable name into the wrong part of the code. When this happens, the values of the original variable are lost.
2. Therefore, you should run the "Load data" codes again.
3. Make sure you run each code again before the wrong code, because they are also lost.
{% endhint %}
{% endstep %}
{% endstepper %}

***

## E. Common computing issues

{% stepper %}
{% step %}
### Use the new (recoded) variables in computation code

{% hint style="danger" %}
Wrong:

gss <- gss %>%

&#x20; rowwise() %>%

&#x20; mutate (<mark style="color:red;">hapindex</mark> = mean (c(<mark style="color:red;">happy</mark>,<mark style="color:red;">life</mark>,<mark style="color:red;">satfin</mark>)))
{% endhint %}

{% hint style="success" %}
Correct:

gss <- gss %>%

&#x20; rowwise() %>%

&#x20; mutate (<mark style="color:red;">hapindex</mark> = mean (c(<mark style="color:red;">happynew</mark>,<mark style="color:red;">lifenew</mark>,<mark style="color:red;">satfinnew</mark>)))
{% endhint %}

{% hint style="warning" %}
**Troubleshooting:**

* When creating a computed variable and if the original variables need to be recoded, then make sure you use the new variable names in the computation code. For such analyses, the original variables were not useful. That's why they were recoded.
{% endhint %}
{% endstep %}

{% step %}
### Computed variables are always continuous

When we compute variables and create an index, the new (computed) variable is continuous.

It becomes CONTINUOUS because we have created a score, and we treat it as a real number.

Therefore, we use the DESCR code to see the distribution (mean and standard deviation)

{% hint style="danger" %}
Wrong:

frq(gss$<mark style="color:red;">hapindex</mark>, out = "v", show = "short")
{% endhint %}

{% hint style="success" %}
Correct:

descr(gss$<mark style="color:red;">hapindex</mark>, out = "v")
{% endhint %}

{% hint style="warning" %}
**Troubleshooting:**

* Computed variables are always continuous. Therefore, they should be treated continuous in further analyses.
{% endhint %}
{% endstep %}

{% step %}
### Use a model code

Use the Code templates page.

<figure><img src="../../../.gitbook/assets/image (142).png" alt="A view from the code templates page." width="563"><figcaption></figcaption></figure>

{% hint style="warning" %}
**Troubleshooting:**

* In code templates page, there are [computing templates](https://ttezcan.gitbook.io/lectures/all-lectures-and-labs/r-lab/lab-resources/code-templates#computing) for every kind of value possibility.
* Do not start computing process without using code templates page.
{% endhint %}
{% endstep %}
{% endstepper %}

***

## F. Miscellaneous

{% stepper %}
{% step %}
### Is my p-value less than 0.05?

#### Statistical significance

Statistical significance is a measure of whether your research findings are meaningful. In other words, if the independent variable causes a change in the dependent variable in a statistically significant way.

The lower the p-value, the greater the statistical significance of the observed difference.

We refer to statistical significance as <mark style="color:red;">p < 0.05</mark>

#### Use the following website:

[https://www.whichnumberislarger.com/](https://www.whichnumberislarger.com/)
{% endstep %}

{% step %}
### Data terminologies

<mark style="color:red;">Questionnaire:</mark> A set of written questions used for collecting information from respondents.

<mark style="color:red;">Respondents:</mark> Individuals who respond to the questions in a questionnaire.

<mark style="color:red;">Dataset:</mark> The information collected from respondents. The numbers to be analyzed.

<mark style="color:red;">Full wording of question:</mark> The exact text of a question as it appears in the questionnaire.

<mark style="color:red;">Variable name:</mark> Unique words assigned to each question. We use variable names in data analysis software.

<mark style="color:red;">Values:</mark> Numbers such as 1, 2, 3, etc., that appear in the dataset representing specific responses.

<mark style="color:red;">Labels:</mark> What those values (numbers) mean, e.g., 1: yes, 2: no, etc.

<mark style="color:red;">Response set:</mark> The combination of values and their corresponding labels.

<figure><img src="../../../.gitbook/assets/image (75).png" alt="A conceptual diagram illustrating how survey data are created. On the left is an icon labeled “questionnaire,” representing a set of survey questions. In the center is an icon labeled “respondents,” representing a group of people who answer the questions. On the right is an icon labeled “data,” representing recorded responses. Text below states that researchers ask questions to a group of people and record their responses as data."><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (74).png" alt="A three-part diagram showing a real survey example. On the left is a questionnaire with questions about unfair treatment in the United States, such as being unfairly fired, treated by police, or treated badly at restaurants or stores. In the center is an icon representing respondents, labeled as participants in the Latino National Survey, consisting of 8,634 self-identified Latino or Hispanic residents of the United States. On the right is a dataset shown as a table with columns labeled DFIRED, DBADPOLC, DHOUSING, and DRESTAUR, containing numeric response codes."><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/ss_2024-07-22 13.10.11.png" alt="An explanatory diagram showing how survey questions are transformed into dataset variables. The full wording of a question is shown on the questionnaire side. The variable name, such as DFIRED, is identified as the column name used in the dataset. Numeric values, such as 1, 2, and 3, are shown as the stored responses in the dataset. Labels explain what each value means, for example, 1 equals Yes, 2 equals No, and 3 equals DK or NA. The response set is defined as the complete list of possible responses for the question."><figcaption></figcaption></figure>

[\[Variables in GSS\]](https://ttezcan.gitbook.io/lectures/all-lectures-and-labs/r-lab/lab-resources/variables-in-gss)

<figure><img src="../../../.gitbook/assets/image (76).png" alt="A table titled “Discrimination and harassment at work” demonstrating how a survey variable is analyzed. The variable name “wkageism” is shown and described as measuring perceived discrimination at work because of age. The full wording of the question is displayed: “Do you feel in any way discriminated against on your job because of your age?” Numeric values are shown, where 1 represents Yes and 2 represents No. A frequency table below shows counts and percentages for each response category, illustrating how values and labels are used in statistical analysis."><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### GSS codebooks

* [GSS 2022 Codebook website](https://gssdataexplorer.norc.org/variables/vfilter)
* [GSS 2022 Codebook pdf file](https://drive.google.com/open?id=1_-FMP3vDlPOiD1_KKkZjEIy3KNnnYOSP\&usp=drive_fs)
{% endstep %}
{% endstepper %}

***

## G. RStudio issues and usage&#x20;

{% stepper %}
{% step %}
### Opening all the panes

Sometimes you may accidentally close one of the panes. When that happens, click "View" <mark style="color:red;">➜</mark>  "Panes" <mark style="color:red;">➜</mark> "Show All Panes."

<figure><img src="../../../.gitbook/assets/SCR-20250911-kvqy-2.png" alt="A view from RStudio."><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### What to do if RStudio Cloud crashes?

This may happen if your RStudio Cloud session consumes too much ram.

1.  Save your unsaved RScript file.

    **Saving R script files:** When we make any changes, the font of the file name (shown in the highlighted part #2 above) will be red with an asterisk (\*) - (see the highlighted part #1 below). To save our progress, we click save (see the highlighted part #2 below)

<figure><img src="../../../.gitbook/assets/ss_2024-07-16 17.06.29.png" alt="A view from RStudio." width="563"><figcaption></figcaption></figure>

2.  Click the three dots next to the gear. Click "Relaunch Project."

    <figure><img src="../../../.gitbook/assets/Screenshot 2024-11-06 at 12.10.57 PM.png" alt="A view from RStudio."><figcaption></figcaption></figure>
3. When you work on a R script file right after relaunching project, you need to run "install and load packages" and "load data" (as always).
{% endstep %}

{% step %}
### How to check how many hours left in RStudio Cloud?

An RStudio Cloud free account allows you 25 hours of connect time per month. Every second the RStudio Cloud is open counts towards this allocated time.&#x20;

Therefore, whenever you are not running code or generating analyses, close the RStudio Cloud browser

Click on your name (see highlighted part #1). The highlighted part #2 shows the time period (e.g., "I will have 25 more hours on Aug 8, 2024"). The highlighted part #3 shows how many hours you have spent.

<figure><img src="../../../.gitbook/assets/image (90).png" alt="A view from RStudio." width="563"><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### What to do if you exceed 25 hours per month?

25 hours of connect time is enough for this class. If you exceed this limit, open another free account using a different email address. Follow the procedures described in the [How to create RStudio Cloud account and installing all the packages](https://ttezcan.gitbook.io/lectures/all-lectures-and-labs/r-lab/lab-resources/how-to-create-rstudio-cloud-account-and-installing-all-the-packages).

#### What to do if you want your new free account to be identical (files, packages, etc.) to the previous account where you exceeded the time limit?

1. Go to the previous account where you exceeded the time limit.
2. Click "Export" (see the highlighted part)

<figure><img src="../../../.gitbook/assets/ss_2024-07-19 14.24.08.png" alt="A view from RStudio." width="563"><figcaption></figcaption></figure>

3. Click "Download"

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="A view from RStudio."><figcaption></figcaption></figure>

4. It will download a zip file.
5. Go to your new account.
6. Upload that zip file just like you upload a R script file.
{% endstep %}

{% step %}
### Using RStudio on a university lab computer

Every time you log in to a lab computer, you have to run "install and load packages" codes.

Because when you log out, lab computers revert to their factory settings and deletes the installed packages.

1. First, download the R Script file that you want to use.  [All R Script files here](https://ttezcan.gitbook.io/lectures/all-lectures-and-labs/r-lab/lab-resources/all-r-script-files).
2. Type "RStudio" on the search bar of the computer. Open RStudio.
3. On RStudio, Click File <mark style="color:red;">➜</mark> Open File.
4. Find the Script file that you just downloaded, and click Open.
5. **DO NOT DOUBLE CLICK R SCRIPT FILES.** It may open R, instead of RStudio.

<figure><img src="../../../.gitbook/assets/image (67).png" alt="A view from RStudio."><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Downloading R and RStudio to a personal computer

You can download R and RStudio to your personal computer.  "Install and load packages" codes will install the packages once, but every time you open RStudio on your personal computer, you should run "Install and load packages" again.

#### Mac users

[Check your macOS version](https://support.apple.com/en-us/HT201260)

#### Mac Users (macOS 12+) and Apple silicon (M1-3) Macs:

1\. [Download R ](https://cran.r-project.org/bin/macosx/big-sur-arm64/base/R-4.4.1-arm64.pkg)(4.4.1)

2\. [Download RStudio ](https://download1.rstudio.org/electron/macos/RStudio-2024.04.2-764.dmg)(2024.04.2+764)

#### Mac Users (macOS 12+) and older Intel Macs:

1\. [Download R ](https://cran.r-project.org/bin/macosx/big-sur-x86_64/base/R-4.4.1-x86_64.pkg)(4.4.1)

2\. [Download RStudio ](https://download1.rstudio.org/electron/macos/RStudio-2024.04.2-764.dmg)(2024.04.2+764)

#### Mac Users (macOS El Capitan and older)

[1. Download R](https://cran-archive.r-project.org/bin/macosx/el-capitan/base/R-3.6.3.pkg) (3.6.3)

[2. Download RStudio](https://download1.rstudio.org/desktop/macos/RStudio-1.4.1717.dmg) (1.4.1717)

macOS may want you to allow it to download. Open System Preferences, navigate to Security & Privacy, and then General. See the photo below and hit allow (you may need to click the lock at the bottom to unlock)

#### Video guidance (macOS)

{% embed url="https://www.youtube.com/watch?v=f7cnHWQDQ-U" %}

#### Windows Users

1\. [Download R](https://cran.r-project.org/bin/windows/base/R-4.4.1-win.exe) (4.4.1)

2\. [Download RStudio](https://download1.rstudio.org/electron/windows/RStudio-2024.04.2-764.exe) (2024.04.2-764)

Windows users may need to change some of their settings.

Select Start <mark style="color:red;">➜</mark> Settings <mark style="color:red;">➜</mark> Apps <mark style="color:red;">➜</mark> Apps & features. Under Installing apps, select "Allow apps from anywhere."

#### Video guidance (Windows)

{% embed url="https://www.youtube.com/watch?v=v3SsxSNINO8" %}
{% endstep %}
{% endstepper %}
