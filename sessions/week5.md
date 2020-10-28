---
layout: single
author_profile: false
title: "Introduction to R"
#header:
    #og_image: /assets/images/cross-val-logo-v4.jpg
    #overlay_image: /assets/images/joel-filipe-small-warmer.jpg
    #caption: "Photo by [Joel Filipe](https://unsplash.com/@joelfilip) on [Unsplash](https://unsplash.com)"
classes: wide

sidebar:
  nav: "sessions"

---

## Week 5

Well, you made it! This is the last session of the workshop series. We would very much have liked to do this workshop especially in person, as getting feedback/help in person is by far more useful. However, it wasn’t to be for us this year, so we’ll be offering this final exercise work-sheet as a remote delivery.

You will have received a dataset that goes along with this set of questions. This is a novel dataset that we haven’t worked with yet in previous sessions. Using this dataset, you can walk through the below questions that will let you apply what you’ve learned in class to somewhat novel problems. Obviously there is no requirement that you do this, but practicing coding in R is the only way you will truly learn the language. To help you through this set of questions, our live session on Nov. 04 will be a drop-in help session. We encourage you to get started on these questions as soon as you can after Session 4 on plotting is wrapped up.

Below are the questions as well as a set of answers that don’t tell you how to do the problem, but do let you check if you’re on the right track. Once you think you’ve completed the question, check your answer against the answer key. Set yourself a frustration threshold, and if you cannot get the right answer, only work on the problem until you’ve reached your threshold. If you can’t get the problem (some of them are meant to be tricky, because a lot of real-world data problems ARE tricky), then bring your problem to the live session next week and both Cole & Emma will be available to help you.

By Sunday, Nov. 08, there will be a series of videos posted here on the website which walk you through how to do each question in detail. We encourage you to try all the problems yourself beforehand, and then use the videos to either double check your approach or if you couldn’t solve the problem. 

You can also reach out to us via the (contact)[/Contact/] tab and we can try to help you via email.

Good luck, and thanks for a great series!

 1. Perform basic data manipulation tasks.


 Note that we didn’t go over how to rename columns in our session on data management. So we’ll briefly cover it here, but this is also a very google-able problem. To rename a column, we use the a familiar structure. The following function will do the trick:

 names(DATAFRAME_NAME)[names(DATAFRAME_NAME) == “OLD_NAME”] = “NEW_NAME”

 This is calling the function names() which returns a vector of the names of the dataframe. Here we’re going into that vector, finding where it is equal to the value we’re looking for, and replacing it with our new value.

  a) Load the dataset into R and call it ‘final_df’

  	Rename the columns as follows:

    `State.Province` → `state_province`
    `temp..C` → `temp_C`
    `dia..cm.` → `diam_cm`
    `ht.cm.` → `ht_cm`
    `total..g.` → `total_g`
    `gonad.vol..ml.` → `gonad_vol_ml`
    `gonad.wt..g.` → `gonad_wt_g`
    `food.vol..ml.` → `food_vol_ml`
    `jaw.cm` → `jaw_cm`

  b) What is the data type of the 4th and 5th columns respectively?

  c) Make a new dataframe with only the first 6 rows of ‘final_df’ and call it `subset_final`. What are the dimensions (number of rows and columns) of  `subset_final`

  d) How many observations are in ‘final_df’? (hint: an observation is the content of a single cell in a dataframe)

  e) What is the value of the cell in the 13th column in the 38th row?
