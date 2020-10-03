---
layout: single
author_profile: false
title: "Introduction to R"
classes: wide

sidebar:
  nav: "sessions"

---

## Week 1

Welcome to the first week of content! Topics of this week will be an introduction to this series, an overview of Object-Oriented Programming (OOP) and some of the basic programming skills that will form the basis of what we'll learn from here on out.

{% include video id="gxQLZV-qdXw" provider="youtube" %}


Please watch the below videos **before** coming to the synchronous lecture - they are relatively short. Follow along when asked, and write down any questions or difficulties you have that we can discuss in lecture.

### Step 1 - Software Downloads

Ah yes, the dreaded first step! Our first workshop is approaching, and to maximize our time together, we ask that you please come prepared with the necessary software downloaded. Please follow these instructions carefully and if you run into problems you can't solve, please reach out and we'll do our best to help you out.

#### Windows
If you already have R and RStudio installed
* Open RStudio, and click on “Help” > “Check for updates”. If a new version is available, quit RStudio, and download the latest version for RStudio.
* To check which version of R you are using, start RStudio and the first thing that appears in the console indicates the version of R you are running. Alternatively, you can type `sessionInfo()`, which will also display which version of R you are running. Go on the CRAN website and check whether a more recent version is available. If so, please download and install it. You can [check here](https://cran.r-project.org/bin/windows/base/rw-FAQ.html#How-do-I-UNinstall-R_003f) for more information on how to remove old versions from your system if you wish to do so.
If you don’t have R and RStudio installed
* Download R from the [CRAN website](http://cran.r-project.org/bin/windows/base/release.htm).
* Run the `.exe` file that was just downloaded
* Go to the [RStudio download page](https://www.rstudio.com/products/rstudio/download/#download)
* Under Installers select RStudio x.yy.zzz - Windows Vista/7/8/10 (where x, y, and z represent version numbers)
* Double click the file to install it
* Once it’s installed, open RStudio to make sure it works and you don’t get any error messages.
#### macOS
If you already have R and RStudio installed
* Open RStudio, and click on “Help” > “Check for updates”. If a new version is available, quit RStudio, and download the latest version for RStudio.
* To check the version of R you are using, start RStudio and the first thing that appears on the terminal indicates the version of R you are running. Alternatively, you can type sessionInfo(), which will also display which version of R you are running. Go on the CRAN website and check whether a more recent version is available. If so, please download and install it.
* Download R from the [CRAN website](http://cran.r-project.org/bin/macosx/)
* Select the .pkg file for the latest R version
* Double click on the downloaded file to install R
* It is also a good idea to install [XQuartz](https://www.xquartz.org/) (needed by some packages)
* Go to the [RStudio download page](https://www.rstudio.com/products/rstudio/download/#download)
* Under Installers select RStudio x.yy.zzz - Mac OS X 10.6+ (64-bit) (where x, y, and z represent version numbers)
* Double click the file to install RStudio
* Once it’s installed, open RStudio to make sure it works and you don’t get any error messages.
Linux
* Follow the instructions for your distribution from [CRAN](https://cloud.r-project.org/bin/linux), they provide information to get the most recent version of R for common distributions. For most distributions, you could use your package manager (e.g., for Debian/Ubuntu run sudo apt-get install r-base, and for Fedora sudo yum install R), but we don’t recommend this approach as the versions provided by this are usually out of date. In any case, make sure you have at least R 3.3.1.
* Go to the [RStudio download page](https://www.rstudio.com/products/rstudio/download/#download)
* Under Installers select the version that matches your distribution, and install it with your preferred method (e.g., with Debian/Ubuntu sudo dpkg -i rstudio-x.yy.zzz-amd64.deb at the terminal).
* Once it’s installed, open RStudio to make sure it works and you don’t get any error messages

In future weeks, we'll have a few videos for you to watch that have programming concepts or ideas presented, that we will then practice in our synchronous session. This week, we are just getting you set up to be ready to code, and we'll do everything else together in our session! Looking forward to seeing you all soon!


-----------------------------
Please [click here](https://forms.gle/eu9LVRrNmfToRC2fA) to fill out the post-session feedback form here! We take your feedback into account in real time, so any changes we can make to help you learn better next week we will make!


After the session, there will be a static page here with a full summary of what was learned this week:
