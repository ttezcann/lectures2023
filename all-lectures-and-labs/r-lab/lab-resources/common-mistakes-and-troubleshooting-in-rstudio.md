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

## 1. Not installing packages

We need specific packages to conduct our analyses. Installing packages is always the first step. Once we install a package, we don't have to install it again for our personal computers. Whenever we log off from a university lab computer, all the packages will be automatically removed, so we must install them again every time we log in.

You can check the installed packages under “Packages.”

<figure><img src="https://lh5.googleusercontent.com/xH1LXn5VA1K8AViMyYQpYU5TL2ocDl_mk7qC0Zvc4TKtA0fxDd5FhAwkV5EugOR6zxby1zgoxdCudNm1hw2wu_9E0YI-2AHcCEbbY06PwlPmSe_bxSG50JH_1TKVA6exi03_ccv6PcUqa4mdbN2ThA" alt=""><figcaption></figcaption></figure>

RStudio will alert us if we didn't install the required packages. We should always check this area. Click “Install” if this occurs.

<figure><img src="https://lh6.googleusercontent.com/yP7DA4VHaN8micscVwSrqv0wQMmKAWT_7DUNtcfGP0_lab5wYVKl1Kh6CpNRxiG-FPi3WKN2nwRWoz2pJ0vFtzj5WX5y5mZDPkLOtUHu2PEYsxJREOegOVEuvc24KwvC8u-TUmxfFo3kv_1YOwrfiA" alt=""><figcaption></figcaption></figure>

## 2. Not loading package

Every time we open RStudio, we must load the packages.

If we don’t, we will see an error message on the “Console” part. Always check this part to make sure why codes don’t work. This error shows that we didn’t load a specific package. Go to the very top of the Rscript file and load all the packages.

<figure><img src="https://lh3.googleusercontent.com/GaOYc0zbU4p4o8tB58t1biKGtHBYell1K5CTBBzI3qjD0SnFZWKDkzu1ZVUxqNiz_GDG8b9dvPn9wHn4Dqc-tjizeoebnqwt196eDYy69mtwBUZQFhYI9ar-57w5-sdi7Ms0JvBRUUyMFAkLcdwZ_Q" alt=""><figcaption></figcaption></figure>

## 3. Not loading the dataset

Every time we open RStudio, we must load the dataset.

Loaded datasets will appear under “Environment.” If this area is empty, our codes won’t work.

<figure><img src="https://lh3.googleusercontent.com/KGyTjZwngZq1hCfMMRsPkd4TYgk1l4dnN4n4Durr3GtWaSAAw7exdYYmUsbVpF-VwLcH04WHO81dgp2h2LIyN6wmFKTpZTaepd6ejzX4mxnu4GYL2IdrenEy2gqJmybVyxgvW1EN_Ni2Z1xIMMKGuA" alt=""><figcaption></figcaption></figure>

If our environment is empty, we will get the following error:

<figure><img src="https://lh4.googleusercontent.com/jnRy2vOs4mfX0-xEcm3Ky06QBPu4YBBJBo30F1xw2jB4OX4AkGpPlO6aTmwC3JbUhsr1FRTMSltSST7gzt3-OJHSAW5pro79SFUzGuDJeiP7LA08DleZM-yeCyTCwslUo_gvWV1W3fcqjwrlI_SbUw" alt=""><figcaption></figcaption></figure>

## 4. Typing variable names

Never type variable names! It is very common to miswrite codes, forget commas, etc. Always copy the variable names, and paste into your codes.

There is no variable called “seex”, but “sex.” RStudio warns you that “seex” is “unknown.” Copy and paste variable names to avoid this possibility.

<figure><img src="https://lh6.googleusercontent.com/DoH0WGcOoknjHkgKdbtf6s9lpD9EWR7xJDaNdt-wt_vBrhOk6gT1McD-foIFSRGKcac5oqpX_FVVk0FY_TaYvAKO5MoVgcAk9G8iwbKpkM8YLjI6E1UU9lHyH17jWfy1-QrDlWMyugp44s43d12nCw" alt=""><figcaption></figcaption></figure>

## 5. Changing the original values of the dataset

Never save your data, but your R script file. From time to time, you may accidentally change the values of original variables (especially when you recode variables). When this happens, go to the very top of the R script file and load the dataset again. If you created new variables previously, you will need to run your analysis again since it will be fresh data.

<figure><img src="https://lh4.googleusercontent.com/nrFUyNQCHCTtMFdSX-pOOCNI0095RAv8bHP8_bAS1WGQa6-Qea8o2vbmybZ6BEdvmaRavb4vvDKiLoIE0bJGhildIpSTd5kx0s3QcTfGUmRogjwUv6vDdmbdDdg3C8Bjz0y3whClwPuS44n4w5y7xg" alt=""><figcaption></figcaption></figure>

## 6. Not highlighting all the lines

We need to highlight all the lines and click “run.”

Here's what happens if we don't:

<figure><img src="https://lh6.googleusercontent.com/PHQX2YzGasYcioZA9e6Cx-raa_Vr6lzOEBET3FDIPmE9TtGKGdX3puoEHrmhyDRhxAmBtUdp85QPZ_q9keWkwDYJcPqjDuiNRZvbh2F0TUpPmzK6Dn0CPBB8h8DbL9Z7fVexYhtyHNywVWDWdDyo6w" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh3.googleusercontent.com/1SZECQFL-PX9y7-plyLJdWCrkXwpo3W-12Du39DDSNgSl2tEDFVHEsMzup4rSqG8qhebz-fCGEmyrKsR4ycmPI2p0GmLsLdxS0PNTu8F0N75LGbwSYt7AnJGS3XkPc1TtkIosIFlO6k6NWN3ZB91cA" alt=""><figcaption></figcaption></figure>

It simply shows what you highlighted and run, not a frequency table. Always triple-click on a code line to highlight the all line.

## 7. Not putting hashtags (#) for your notes

Typing notes on your RScript file is encouraged. When we type a note, we must put a hashtag (#) first. Not putting a hashtag (#) will confuse RStudio.

While line 72 will work, line 70 won’t. Here RStudio warns us that there is something wrong. Look at the cross on line 70.

<figure><img src="https://lh3.googleusercontent.com/ZX-tGT53SYcWHXq0QSR-KJ17TCp7r8IRFbecAmAieQCf_H33Jjysn5J7mK_c8XZSDYF1RyTMgtlM8HAvOyoOSFzHgNIo6BqW2bxK5bFoYigiJlfCaUjw1Ef1WXO1JSSgGkGsKE8QAOPQwx-2MW0MDQ" alt=""><figcaption></figcaption></figure>

## 8. Not using a model code

Whenever we run an analysis with a different variable, we simply copy the original code, paste under, change the variable name, and compare them. If our new codes do not work for some reason, we can easily compare them with the working codes. We call this “model” code.

Here the original variable was “sex”. We wanted to run the sample analysis for marital. If we don’t paste the working code for comparison, it’s likely that we may accidentally delete something extra. In this example, the comma was deleted.

<figure><img src="https://lh5.googleusercontent.com/8FzDZFIPE3crXndqIywZ_1s9UD5I77dY1tPU0Xf1vwoRxG3AIlPIVdJw5a4_44iOt9qQCDbqAubR-Bw9E3ACoyOnMByZVJxwTusZh9eJ-K0DkH7f_pDoz76xLYauYGs6dmBQ4X2_lfali6whV6WnlQ" alt=""><figcaption></figcaption></figure>

Instead, we keep the “working” code and compare it with our new code. Here we see that the comma is missing in line 72.

<figure><img src="https://lh4.googleusercontent.com/U0yDED2phXUKh8jLl-x-855f81a7BL1gVB36pNTsX3-62lMG5pFL4qDWv5w9lJDAV3VYfU5ZSbXFFzlAtfJueqpcX42XFp0FFF-0CVd5Vnu16_PRjVHI03KJuTXyAygK9I-qZ8NUvOKxGs45GrS3sA" alt=""><figcaption></figcaption></figure>
