---
layout: single
author_profile: false
title: "Introduction to R"
classes: wide

sidebar:
  nav: "sessions"

---

## Week 1

**Zoom Link:** [https://ualberta-ca.zoom.us/j/97755262261](https://ualberta-ca.zoom.us/j/97755262261)

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

### Introduction to This Series

We want to give you an idea of what this series is for, and how to get the most out of it. Please watch this video where Emma will tell you about what you'll learn and (maybe more importantly!) what you **won't** learn.

**THIS VIDEO WILL BE LIVE AFTER 12PM MT MONDAY, OCT. 05**

{% include video id="iktRaJMu4gA" provider="youtube" %}

### Using RStudio

In this video, Cole will give you a walkthrough of RStudio, so make sure you have R and RStudio downloaded, following the instructions above. Open RStudio and follow along on your own computer. Make a note of any questions you have and we can discuss them in the live session!

{% include video id="zVZK2J9hMwA" provider="youtube" %}

### OOP & Objects in R

Object-Oriented Programming (OOP) is the lens through which we'll approach everything we do in R. Inherent to the principles of OOP is that everything in R is an object. In this video Cole will walk you through the basics of objects and types in R. This will become important later, and we will spent most of the live session practicing using different types of objects in R. Make a note of any questions you have and we can discuss them in the live session!

{% include video id="Ytcr2Nr6lYU" provider="youtube" %}

-----------------------------
Please [click here](https://forms.gle/eu9LVRrNmfToRC2fA) to fill out the post-session feedback form here! We take your feedback into account in real time, so any changes we can make to help you learn better next week we will make!


# An Overview of Data Types, Data Structures, and Reading in Data in R  

# Objects and OOP

To understand what's going on in R, it's important to understand how the things (termed 'Objects') are being stored in R. Everything (yes, literally everything) is an object. Objects are the basis of what we call object-oriented programming. An `object` is a data structure having some attributes and a set of methods that act on those attributes.

Object-oriented programming languages (sometimes called 'high-level' lanaguages) are typically more intuitive and are often used via an IDE (integrated development environment) like RStudio or a GUI (graphical user interface).

## Data Types

There are six major data types:

1. Character
2. Numeric (real or decimal)
3. Integer
4. Logical
5. Complex
6. Raw (We won't talk about this one)

These data types are all used for different things. Their names are somewhat indicitive of their uses. We will only really deal with types 1-4 in this series.

A character is any alphanumeric string that begin with a letter (NOTE: code chunk keyboard shortcut = cntrl+shift+i):
```{r}
x1 = 'a'
```
```{r}
x2 = 'a1b'
```
A numeric type is a non-integer number:
```{r}
x3 = 3.14
```
An integer type:
```{r}
x4 = 3L
```
A logical type is represented by TRUE or FALSE:
```{r}
x5 = TRUE
```
We can test what types of data we're working with here, by using a number of useful commands:

*`class()` (what type of class is it?)
*`typeof()` (what type of data is it?)
*`length()` (how long is it?)
*`attributes()` (does it have any metadata)
```{r}
class(x1) #this will tell us the class
```
```{r}
class(x4)
```
```{r}
typeof(x4)
```

By the way, what we're doing here with these x's and equals signs is called an 'assignment statement'. In R, using the `=` or the `<-` takes whatever is on the right of the assignment, and allows what's on the right to represent it as an object. The things on the left are still objects, but they are often called variables too. This is convenient for representing complex things like long strings. For example:
```{r}
x6 = 'the quick brown fox jumped over the lazy dog'
```
By representing this long string by `x6`, I can now call `x6` again later to look at it or maybe perform some operation on it.
```{r}
length(x6) #this will tell us how long this object is
```
Note that this says length is 1, even though there appears to be nine words here. This seems unintuitive, but remember, R can't tell we've written a sentence here, it just knows there's some information, contained by the '' that it is assigning as a single object to x6. We'll come back to this.

## Data Structures

In R, we frequently combine these data types together into different data structures. There are 4 main data structures that we work with consistently:

1. Vectors
2. Matrices
3. Dataframes
4. Arrays (we won't deal with these much)
They all have dimensions and attributes that we will only talk about sparingly, but some of which are important to understand up front.

### Vectors
Vectors are subset into atomic vectors (collections of data of the same type) and lists (collections of different data types). Vectors are the workshorses of R and mosts other OOP languages use vectors or a very similar structure to hold data. From this point forward, we'll use 'vector' to refer to atomic vectors and call lists by name. We make vectors the same way we make variables, with an assignment statement:
```{r}
x7 = vector('character', length = 5)
```
This way, we're explicitly telling R what type of vector we want. We can let R decide what type we want and use the more commonly used `c()` combine method:
```{r}
x8 = c(1:4)
```
In the same way we looked at characteristics of the data, we can do this with data structures too with the following:
*`typeof()`
*`class()`
*`length()`
*`str()`
```{r}
class(x8)
length(x8)
```
Let's go back to that fun sentence we called `x6`. Like we said, it's just one object, but we can change that if we want.
```{r}
x9 = c('the','quick','brown','fox','jumped','over','the','lazy','dog')
```
We've now taken the same sentence, but we've separated these words into separate data, with each word being a datum, and told R explicitly we've done that. We can see in our environment that the dimensions are [1:9], 1 row, with 9 'columns'.
```{r}
str(x9)
length(x9) #note this has changed
class(x9) #but this has not.
```
What if we want to add to a vector? Well, we can!
```{r}
x9 = c(x9, 'who', 'was','sunning','himself')
x9
```
Can we change a single element of a vector? For sure. This conventiently brings up the topic of indexing. Remember we said all data structures have dimension. Well, vectors have only one dimension, or are 1D. To access any part of any data structure, one option is to access it via the location in X dimensions we want to change. In this case, since it's one dimension, we can specify the dimension location and the thing we want to replace that dimension location object with. Let's change our dog to a cat.
```{r}
x9[9] = 'cat' #indexing uses square brackets
x9
```
We'll see how to do this in multiple dimensions shortly.

**EXERCISE:** Try and replace the 3rd element in x9 ('brown') with 'red'
```{r}
x9[3] = 'red'
x9
```


### Lists
Lists are similar to vectors, but are more general purpose. They can take a variety of data types which makes them versatile and useful. They are created much the same as vectors:
```{r}
l1 = list(1,2,'R is fun', c(1,2,3), TRUE)
l1
class(l1)
```
We can index lists similarly, but using double square brackets:
```{r}
l1[1]
l1[[1]]
str(l1[1])
str(l1[[3]])
```

**EXERCISE:** How would we index a part of a list?
```{r}
l1[[4]][2]
```

### Matrices
Matrices are a logical extension of vectors as they can be thought of as a series of vectors bound together to form a 2D structure made up of rows and columns. Matrices have the same limit as a vector and must contain data of the same type (numeric or character). Let's make a matrix:
```{r}
m = matrix(nrow = 2, ncol = 2)
m
```
We can see that because we haven't filled the matrix with any values, R has filled the matrix with `NA` values, with are R's way of holding the place of missing values.

So we have an empty matrix, what if we want to put some values into it? Let's recall the indexing skills we just learned. Although now, we're working in 2 dimensions, so to access a dimension location, we first specify the first, then the second dimension location, which are always represented as the row, then the column. Let's make the first value in the matrix (top left) equal to 100.
```{r}
m[1,1] = 100
m
```
We could have also made a matrix in another way by the combine method. Note that matrices fill column wise. That is, they will take all supplied numbers, and fill the first column before moving onto the second, fill that and so on.
```{r}
m1 = matrix(c(1,2,3,4),nrow = 2, ncol = 2)
m1
```
```{r}
class(m1)
```
Often, we want to make matrices by binding vectors together.
```{r}
m2 = rbind(c(1,2), c(3,4))
m3 = cbind(c(1,2), c(3,4))
m2;m3
```
```{r}
class(m2)
```

### Dataframes
Ah, dataframes. The darlings of R. These structures are the feature of R that make it so popular for data analysis and statistics. It is the easiest way to store, access, and perform operations on tabular data (the type of data we most often have in biology). Dataframes are actually a type of list, one wherein each element of the list has the same length, making it of dimension 2, which means we easily can look at rows and columns. They're usually created directly by reading in data (we'll get to this shortly), or by creation through the `data.frame` command:
```{r}
c1 = c(1:4)
c2 = c('item1', 'item2', 'item3', 'item4')
c3 = c(11:14)
d1 = data.frame(c1,c2,c3)
d1
```
Because dataframes are lists, we can index elements (columns) using double square brackets `[[]]` or the `$`.
```{r}
d1$c2
d1[[3]]
```
It's easy to add rows or columns using binding:
```{r}
c4 = c('add1', 'add2', 'add3', 'add4')
d2 = cbind(d1, c4)
r5 = c(5,'item5', 15, 'add5')
d2 = rbind(d1,r5)
d2
```
Interesting, so we see an error message here, it says an NA was generated. Why's that? Well, if we take a look at our columns, c2 is the one it got added to. What's up with c2? Let's look:
```{r}
str(d1)
class(d1$c2)
```
So this says that c2 is a factor. What is that? Well, conceptually, factors are variables in R which take on a limited number of different values; such variables are often refered to as categorical variables. Factors in R are stored as a vector of integer values with a corresponding set of character values to use when the factor is displayed. The factor function is used to create a factor. As you continue on your journey in R, both in this series and onward, factors will be very important but also a source of many headaches for you. In this case however, it's easy to see and fix our problem. We tried to add 'item5' to a factor variable that doens't have that level to it. We can go about this a number of ways, the simplest of which is to change the class of c2
```{r}
d1$c2 = as.character(d1$c2) #this is simply re-assignng the variable to itself but as a new class
class(d1$c2)
```
Let's try our row bind again:
```{r}
d2 = rbind(d1,r5)
d2
```
Success. So this was a good taster example of the fact that while dataframes are a powerful and useful concept and tool, all their functionality means there's sometimes a lot going on under the hood that we need to be aware of, especially while manipulating dataframes.

# A Typical Day in R Neighbourhood

So, it's a beautiful day in Edmonton, you sit down in front of your computer with a coffee and the intention of doing something easy (hahaha, good one!) in R. What do you do? This following is a quick process of moving around in R to do some fun things with data!

## Setting a Directory

Let's go on a journey of a full day/session of programming in R! We've now successfully opened R, we've started a script and now it's time to do some work. The first thing we need to do is get our data into R. But a necessary precursor is asking the question of where our data is? To find our data, we first need to tell R where to look for it. Let's do that by setting a directory.
```{r}
#dir = 'YOUR_PATH_HERE'
dir = 'C:/Users/coleb/Documents/GitHub/Introduction-to-Programming-for-Biology/data'
setwd(dir) #the only thing we need to do here is tell the `setwd()` function where to look!


```
Okay cool, we've found our directory! You all should have a nice clean csv for the purpose of this exercise. Let's read that csv into R so we can play around with it.

## Reading In Data

Reading data from a file (most often a csv or txt file, but can be many others) is something you will do many many times. You'll also probably write files from R to csv's or txt (or other) files. However, csv's are the most common, and the following command will soon be second nature to you.
```{r}
setwd(dir)
penguins_data = read.csv('penguins.csv')
```
Great, now we have it in our environment. Let's take a little look.
```{r}
head(penguins_data)
```
```{r}
str(penguins_data)
```
```{r}
dim(penguins_data)
```
```{r}
ncol(penguins_data); nrow(penguins_data)
```
There's a lot of information here that we could parse out if we want, but for now, let's move on a bit and manipulate some of the data. Let's:
Make a new column:
```{r}
new_col = c(1:344)
penguins_data$new_col = new_col
head(penguins_data)
```
Use a built-in (base) function to calculate the average length of a penguin's flipper in this dataset:
```{r}
flipper_mean = mean(penguins_data$flipper_length_mm) #the `mean()` function is a base function in R
flipper_mean
```
Now we notice we're getting a print of `NA`. Why is that? Well, if we look at our preview of the data, we can see that row 4 has an `NA` value in the `flipper_length_mm` column, and we haven't told R how we want to handle NA's yet. Let's do that:
```{r}
flipper_mean = mean(penguins_data$flipper_length_mm, na.rm = TRUE)
flipper_mean
```

And we could do other things too.

What if we want to access parts of our dataframe? If we recall, we can use indexing on 2-dimensional objects, but R also gives us a particular way to get at our dataframe via column indexing.

## Column Operators

In our data, there are columns, and these columns have names. We might find it easier, rather than indexing using square brackets `[]`. Luckily, R provides us a way to do this by using the `$` and the column name. In our case, we can remind ourselves of the column names with
```{r}
names(penguins_data)
```
and select the column `flipper_length_mm`
```{r}
penguins_data$flipper_length_mm
```
We can see it prints the result. We could have also done this using square brackets, and the column position (as the 2nd dimension), as such:
```{r}
penguins_data[, 5] #reminder, the empty first position inside the square brackets simply means all rows
```
Often when looking at parts of our dataframe, we may want to select or view parts of a dataframe that follow some sort of guidelines. For example, I may want to see all of the `flipper_length_mm` data that have a value smaller than 200mm. To do this, I need to use a logical operator. We'll touch more on working with data in this way in the third week, but for now, let's discuss logical operators.

## Logical Operators

There are four main operators that we'll dicuss. Equal to, not *equal to*, *less than*, and *greater than*. In R, it's often the case that we want to ask R to do a particular action if a certain condition is true, and another action if that condition is false. We can enforce this with logical operators. When we ask R to perform a logical operator, it will return a *boolean value *(**True** or **False**) in whatever circumstance you give it.

An example of logical operators are the following:
```{r}
#equal to - will return TRUE
a = 1
b = 1
a == b
```
```{r}
#equal to - will return FALSE
a1 = 2
b1 = 1
a1 == b1
```
```{r}
#not equal to - will return TRUE
a1 != b1
```
```{r}
#not equal to - will return FALSE
a != b
```
```{r}
#less than - will return TRUE
b1 < a1
```
```{r}
#greater than - will return TRUE
a1 > b1
```

We can also combine the *greater/less than* and the *is equal to*, which is a common mathematical expression, and something you may find yourselves wanting to accomplish.

```{r}
a2 = 4
b2 = 4
c2 = 3
d2 = 5
```
```{r}
#greater than or equal to - will return TRUE
a2 >= b2
```
```{r}
#greater than or equal to - will return TRUE
a2 >= c2
```
```{r}
#greater than or equal to - will return FALSE
a2 >= d2
```

And the same holds for less than.

**At Home Practice:** If you want some more practice with the concepts we've worked on here, try the following problems. Keep in mind that there is usually more than one way to achieve a particular result, so there is no 'right' way, but try and use the concepts/principles we talked about in this session.

1. Create a list of float values of length 10 called 'useful_list'
2. Create a fake dataframe with 10 rows and 3 columns. Make one column float values called 'useful_column'
3. Add the list of integers to the dataframe as a new column
4. Make a new column in the dataframe with the mean value of the columns 'useful_list' and 'useful_column'. Call this new column 'useful_mean'.

Try and come up with a solution to this that only uses $\leq 7$ lines of code.
