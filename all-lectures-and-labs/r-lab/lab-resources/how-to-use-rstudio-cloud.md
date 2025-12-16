# How to create RStudio Cloud account and installing all the packages

## General instructions

1. This class will teach you how to use RStudio. You will be able to use this software on your browser.
2. You need to have a RStudio (Posit) Cloud account. The new name of RStudio Cloud is Posit. We will use the name of RStudio Cloud and Posit interchangeably.
3. Lab lectures are listed in the syllabus (Table 3: Course schedule), with topics beginning with “RStudio.”

## Assignment instructions

{% stepper %}
{% step %}
### RStudio website

1. Go to [https://posit.cloud/plans/free](https://posit.cloud/plans/free) and make sure you choose “free.”
2. Click "Sign up"

<figure><img src="../../../.gitbook/assets/SCR-20251216-lzmf-2 (1).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### School email address and a new password

1. Use your school email address.
2. Put a password (at least 10 characters). You will share your password with me, so note somewhere downn. As you see I will have access to your password. That's why you should not use this password somewhere else. You must:
   1. Use upper and lower case letters
   2. Use numbers
   3. Use special characters

{% hint style="success" %}
I recommend [Bitward Free Password Generator](https://bitwarden.com/password-generator/#password-generator).
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (131).png" alt=""><figcaption></figcaption></figure>

3. **DO NOT** use “Sign up with Google." Not now, not during the semester.
4. Click "Sign up."

<figure><img src="../../../.gitbook/assets/SCR-20251216-mayi-2.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Verification

1. Go to your school email inbox and click “Verify.”
2. You will be directed to [https://posit.cloud](https://posit.cloud/plans/free). If not, click on the link.
{% endstep %}

{% step %}
### New project (RStudio labs)

1. Click "New Project."
2. Choose "New RStudio Project."&#x20;
   1. You will wait 10-15 second while RStudio deploys the project. If it takes longer, refresh your page.
3. On the new screen, click on “Untitled Project” and type “RStudio labs”.

<figure><img src="../../../.gitbook/assets/SCR-20251216-mhat (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Note: In previous semesters, many students mistakenly created a separate project for each lab. This is incorrect. You will not create a new project for each lab. Instead, you will always work within the existing 'RStudio labs' project throughout the course.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (133).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Download the specific R script file for this assignment

1. Go to Canvas <mark style="color:red;">➜</mark> Resources module page <mark style="color:red;">➜</mark> “Lab resources” <mark style="color:red;">➜</mark> “All script files” <mark style="color:red;">➜</mark> Click on “Installing the packages” (Under "Setup R script file" and download this file.

<figure><img src="../../../.gitbook/assets/SCR-20251216-mmhp-2.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Upload that R script file to RStudio

1. Click "Upload."
2. Click "Choose file." Find the R script file you just downloaded (script\_installing packages.R) in the previous step and click “Open.”

<figure><img src="../../../.gitbook/assets/SCR-20251216-mnhh-2.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Install and load packages

1. After completing the previous step, you will see "script\_installing packages.R" under "Files."
   1. Click on "script\_installing packages.R."
2. As soon as you click on "script\_installing packages.R," you will see the content of this file on the left side.
   1. Highlight all the lines under the “Install and load packages.”
3. Click "Run."

<figure><img src="../../../.gitbook/assets/SCR-20251216-mpjj-2.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Wait

This process will install all the packages we’ll be using throughout the semester. This process may take 15-20 minutes or shorter depending on your internet connection. This is a one-time process. You won't wait this long again during the semester.

1. You will see a <mark style="color:red;">STOP</mark> sign.
2. And, codes are running in the console (see the highlighted part #2). You should wait until the <mark style="color:red;">STOP</mark> sign in the console disappears and no more code is running in the console.
3. During this process, if you see the pop-up window above (Updating Loaded Packages), click “No” every single time.

<figure><img src="../../../.gitbook/assets/SCR-20251216-muda-2.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Load data

1. When the process above is completed, scroll down on the script file. Highlight all the lines under the “Load data.”
2. And, click "Run."
{% endstep %}
{% endstepper %}



Follow the procedures described in the [RStudio lab assignment: account and packages assignment instructions](https://docs.google.com/document/d/1P0gpXCsAk03u9fSdHNdMpO43TCbHUoJT/edit?usp=sharing\&ouid=100179871492576617561\&rtpof=true\&sd=true).

The process is also shown on the video below:



{% embed url="https://drive.google.com/open?id=1qS2xGpy1h04ojoOoFLOrW8rehxsr6cUL&usp=drive_fs" %}

## <mark style="color:orange;">How to check how many hours left?</mark>

An RStudio Cloud free account allows you 25 hours of connect time per month. Every second the RStudio Cloud is open counts towards this allocated time.&#x20;

Therefore, whenever you are not running code or generating analyses, close the RStudio Cloud browser

Click on your name (see highlighted part #1). The highlighted part #2 shows the time period (e.g., "I will have 25 more hours on Aug 8, 2024"). The highlighted part #3 shows how many hours you have spent.

<figure><img src="../../../.gitbook/assets/ss_2024-07-19 14.13.56.png" alt=""><figcaption></figcaption></figure>

## <mark style="color:orange;">What to do if you exceed 25 hours per month?</mark>

25 hours of connect time is enough for this class. If you exceed this limit, open another free account using a different email address. Follow the procedures described in the [RStudio lab assignment: account and packages assignment instructions](https://docs.google.com/document/d/1P0gpXCsAk03u9fSdHNdMpO43TCbHUoJT/edit?usp=sharing\&ouid=100179871492576617561\&rtpof=true\&sd=true).

### <mark style="color:orange;">What to do if you want your new free account to be identical (files, packages, etc.) to the previous account where you exceeded the time limit?"</mark>

{% hint style="info" %}
There is no need for this in this class.
{% endhint %}

1. Go to the previous account where you exceeded the time limit.
2. Click "Export" (see the highlighted part)

<figure><img src="../../../.gitbook/assets/ss_2024-07-19 14.24.08.png" alt=""><figcaption></figcaption></figure>

3. Click "Download"

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

4. It will download a zip file.
5. Go to your new account.
6. Upload that zip file just like you upload a R script file.
