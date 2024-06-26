---
editor_options:
  markdown:
    wrap: 72
---

# (PART\*) Section 1 {.unnumbered}

# Overview {.unnumbered}

::: {style="color: #333; font-size: 24px; font-style: italic; text-align: justify;"}
Section 1: Introduction to Data Science - The Basics of Statistical
Learning
:::

This section is comprised of a demonstration and two practicals.

The two practicals are adapted from exercises from the core textbook for
this course:

James, G., Witten, D., Hastie, T. and Tibshirani, R. (2021). *An
Introduction to Statistical Learning with Applications in R*. 2nd ed.
New York: Springer. <https://www.statlearning.com/>

The demonstration has been developed by Dr. Tatjana Kecojevic, Lecturer
in Social Statistics.

::: ilos
**Learning Outcomes:**

-   appreciate the importance of the mean squared error;\
-   indexing using base R;
-   creating scatterplot matrices;
-   creating new variables;
-   transforming existing variables;
-   using functionals;
-   'calling' on masked functions from specific packages;
-   translating base R code to `tidyverse` and vice versa.
:::

**In this section, you will practice using the functions below. It is
highly recommended that you explore these functions further using the
Help tab in your RStudio console. You can access the R documentation in
the Help tab using? (e.g. `?read.csv`)**

+--------------------+------------------------------+----------------+
| Function           | Description                  | Package        |
+:==================:+:============================:+:==============:+
| `read.csv()`       | read csv files               | utils          |
+--------------------+------------------------------+----------------+
| `read_csv()`       | read csv files               | tidyverse      |
+--------------------+------------------------------+----------------+
| `co l              | convert column to row names  | tidyverse      |
| umn_to_rownames()` |                              |                |
+--------------------+------------------------------+----------------+
| `rownames()`       | obtain names of rows         | base           |
+--------------------+------------------------------+----------------+
| `summary()`        | produce summary results      | base           |
+--------------------+------------------------------+----------------+
| `summarise()`      | object summaries             | tidyverse      |
|                    |                              | (dplyr)        |
+--------------------+------------------------------+----------------+
| `group_by()`       | group by one or more         | tidyverse      |
|                    | variables                    | (dplyr)        |
+--------------------+------------------------------+----------------+
| `pairs()`          | produce a matrix of          | graphics       |
|                    | scatterplots                 |                |
+--------------------+------------------------------+----------------+
| `plot()`           | create a plot                | base           |
+--------------------+------------------------------+----------------+
| `ggplot()`         | generic function for         | tidyverse      |
|                    | creating a plot              | (ggplot2)      |
+--------------------+------------------------------+----------------+
| `mutate()`         | create, modify, and delete   | tidyverse      |
|                    | columns                      | (dplyr)        |
+--------------------+------------------------------+----------------+
| `if_else()`        | condition-based function     | tidyverse      |
|                    |                              | (dplyr)        |
+--------------------+------------------------------+----------------+
| `as_factor()`      | create factor using existing | tidyverse      |
|                    | levels                       | (forcats)      |
+--------------------+------------------------------+----------------+
| `par()`            | set graphical parameters     | graphics       |
|                    | (e.g. `mfrow()`)             |                |
+--------------------+------------------------------+----------------+
| `slice_min()` and  | index rows by location       | tidyverse      |
| `slice_max()`      | (smallest and largest values | (dplyr)        |
|                    | of a variable respectively)  |                |
+--------------------+------------------------------+----------------+
| `sapply()`         | applying a function over     | base           |
|                    | list or vector               |                |
+--------------------+------------------------------+----------------+
| `select()`         | keep or drop columns         | tidyverse      |
|                    |                              | (dplyr)        |
|                    |                              |                |
|                    |                              | *note that     |
|                    |                              | this function  |
|                    |                              | is also        |
|                    |                              | available      |
|                    |                              | through the    |
|                    |                              | MASS package   |
|                    |                              | (we will not   |
|                    |                              | cover this in  |
|                    |                              | this section)* |
+--------------------+------------------------------+----------------+
| `pivot_longer()`   | lengthen data                | tidyverse      |
|                    |                              | (tidyr)        |
+--------------------+------------------------------+----------------+
| `where()`          | selection helper             | tidyverse      |
+--------------------+------------------------------+----------------+
| `median()`,        | median, mean, standard       | stats          |
| `mean()`, `sd()`   | deviation                    |                |
+--------------------+------------------------------+----------------+
