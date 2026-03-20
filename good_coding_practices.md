---
title: Good coding practices
nav_order: 4
parent: Computing Resources
author: Laura Torrens
---

# Good coding practices in R
Good coding style is like correct punctuation: you can manage without it, butitsuremakesthingseasiertoread. 

*“Always code as if the guy who ends up maintaining your code will be a violent psychopath who knows where you live”* - Martin Golding

## Tidyverse
This site describes the style used throughout the tidyverse: [https://style.tidyverse.org/](https://style.tidyverse.org/).
The most important thing about a style guide is that it provides **consistency**, making code easier to write because you need to make fewer decisions.

You can find information on the style for: 
- **Analyses**: Files, syntaxm functions, pipes, and ggplot2
- **Packages**: Files, documentation, tests, error messages, news

Two R packages support this style guide:
1. [styler](https://styler.r-lib.org/):
  - Allows you to interactively **restyle** selected text, files, or entire projects to the tidyverse style.
  - It helps to keep the coding style consistent across projects.
  - It includes an RStudio add-in, the easiest way to re-style existing code:  ![styler_0 1](https://github.com/user-attachments/assets/bea6d8ca-7a66-4971-ba0e-dbe89cd69713)


2. [lintr](https://github.com/r-lib/lintr):
- It checks for adherence to a given style, identifying syntax errors and possible semantic issues, then **reports** them to you so you can take action.
- lintr is complementary to the styler package which eliminates some of the problems that lintr can detect.

## Google’s R Style Guide
Google’s [R style guide](https://google.github.io/styleguide/Rguide.html) is derived from the tidyverse one, but with some differeces. Their guide eexplains Google’s primary differences with the Tidyverse one, and why these differences exist.


## IARC's resources
[Git Started course](https://code.iarc.fr/farnudia/scientific_software_development_iarc_2024/-/tree/main/Git_Started?ref_type=heads) - Author: Ali Farnudi



