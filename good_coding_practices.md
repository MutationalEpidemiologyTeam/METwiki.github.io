---
title: High Performance Computing
nav_order: 4
parent: Computing Resources
---


# Good coding practices
Good coding style is like correct punctuation: you can manage without it, butitsuremakesthingseasiertoread. 

## Tidyverse
This site describes the style used throughout the tidyverse: [https://style.tidyverse.org/](https://style.tidyverse.org/)
It was derived from Google’s original R Style Guide - but Google’s [current guide](https://google.github.io/styleguide/Rguide.html) is derived from the tidyverse style guide.
All style guides are fundamentally opinionated. Some decisions genuinely do make code easier to use (especially matching indenting to programming structure), but many decisions are arbitrary. The most important thing about a style guide is that it provides consistency, making code easier to write because you need to make fewer decisions.

You can find information on the style for: 
- Analyses: Files, syntaxm functions, pipes, and ggplot2
- Packages: Files, documentation, tests, error messages, news

Two R packages support this style guide:
- [styler](https://styler.r-lib.org/) allows you to interactively restyle selected text, files, or entire projects. It includes an RStudio add-in, the easiest way to re-style existing code.
- [lintr](https://github.com/r-lib/lintr) performs automated checks to confirm that you conform to the style guide.
