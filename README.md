# STA 323 :: Homework 4

<center>
<img src="images/nasa_image.png" width="400" height="300">
</center>

## Introduction

You will work with semi-synthetic data on meteorite landings comprised by
The Meteoritical Society. The data was not tidy from the start and was made
less tidy by me.

The main purpose of this assignment is to get practice tidying data using
`tidyr`, `purrr`, and regexs. The details
below will give you some hints on how best to achieve tidy data and what it
means in this context.

## Data

To get started, read in the data. It will be in the form of a list.

```r
nasa <- readRDS(file = "data/nasa.rds")
```

Use object `nasa` to complete the following tasks.

## Tasks

The primary objective of this assignment is to convert `nasa` into a tidy data 
frame. The following variables should be included in your final tidy data 
frame: `name`, `id`, `features`, `name_type`, 
`rec_class`, `mass`, `fall`, `year`, `month`, `day`, `hours`, `minutes`, 
`seconds`, `rec_lat`, `rec_long`, `geo_coord`.

#### Task 1

Transform list `nasa` into a data frame called `nasa_df`. Try as much as 
possible to avoid referencing variables explicitly by position or name. Code
with a goal that your workflow be completely reproducible and functional
agaisnt future changes and updates to the dataset.

Unimportant variables may be removed in this process; however, parsing 
individual data values, correcting errors, converting variable types, and so on,
should be left for Task 2.

<i>
Your score will depend on your code's efficiency, quality, and correctness.
In this setting, `map()` and `apply()` variants will earn you more
points than loops.
</i>

#### Task 2

Tidy and clean `nasa_df` so it only contains the relevant variables 
mentioned above.

Below are some hints to help you get `nasa_df` tidy.

1. Each row should be a unique meteorite landing.

2. Your variables should be of a workable and reasonable type. For example,
	 numeric-style variables should not be of type raw.

3. Values may need to be parsed and cleaned; obvious mistakes should be 
	 corrected or handled appropriately. You'll need to play around with the data
	 to find the errors.

5. Create helper functions. R is a functional programming language; try
   to use functionals.

<i>
Your score will depend on your code's efficiency, quality, and correctness.
</i>

#### Task 3

Document your tidying process. Non-obvious choices should be justified. Your
write-up should clearly and concisely reflect your code. This documentation
should supplement your code comments.

## Essential details

#### Deadline and submission

**The deadline to submit Homework 4 is 11:59pm on Wednesday, February 26.** Only
your final commit and code in the master branch will be graded. 
To get your work into branch master (the only branch that will be graded), 
initiate a pull request on GitHub. This will then merge your work into the 
master branch upon approval by one of your teammates.

#### Help

- Post your questions in the #hw4 channel on Slack. Explain your error / problem
  in as much detail as possible or give a reproducible example that generates 
  the same error. Make use of the code snippet option available in Slack.

- Visit the instructor or TAs in office hours.

- The instructor and TAs will not answer any questions unrelated to directions
  and interpretation within the first 12 hours of this homework being assigned, 
  and they will not answer questions within 6 hours of the deadline.

#### Academic integrity

This is a team assignment. You should not communicate with other
teams. As a reminder, any code you use directly or as inspiration must be cited.

To uphold the Duke Community Standard:

- I will not lie, cheat, or steal in my academic endeavors;
- I will conduct myself honorably in all my endeavors; and
- I will act if the Standard is compromised.

#### Grading

| **Topic**                                     | **Points** |
|-----------------------------------------------|------------|
| Task 1                                        | 11         |
| Task 2                                        | 11         |
| Task 3                                        | 6          |
| Code style and format (named code chunks)     | 2          |
| **Total**                                     | **30**     |

*Documents that fail to knit after minimal intervention will receive a 0*.

## References

1. (2020). Data.nasa.gov. Retrieved 17 February 2020, from    
   https://data.nasa.gov/Space-Science/Meteorite-Landings/gh4g-9sfh
