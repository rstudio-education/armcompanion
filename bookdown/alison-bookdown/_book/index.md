--- 
title: "Notes from the Advanced R Markdown Workshop"
subtitle: "rstudio::conf 2019 | January 15 - 18, 2019 | Austin, TX"
author: 
- Alison Hill
- Yihui Xie
- the ARM workshop participants
date: "2019-01-01"
site: bookdown::bookdown_site
documentclass: book
bibliography: [book.bib, packages.bib]
biblio-style: apalike
link-citations: yes
description: "This is a minimal example of using the bookdown package to write up some notes from the rstudio::conf Advanced R Markdown Workshop. The output format for this example is bookdown::gitbook."
cover-image: images/books.jpg
url: 'https\://alison-bookdown.netlify.com/'
github-repo: rstudio-education/arm-companion-rsc2019
---


# Welcome {-}

<p style="text-align: center;"><a href="https://github.com/rstudio-education/arm-workshop-rsc2019"><img src="images/books.jpg" alt="Just some book spines" /></a></p>

This is a _sample_ book written in **Markdown**. You can use anything that Pandoc's Markdown supports, e.g., a math equation $a^2 + b^2 = c^2$.

The **bookdown** package can be installed from CRAN or Github:


```r
install.packages("bookdown")
# or the development version
# devtools::install_github("rstudio/bookdown")
```

Remember each Rmd file contains one and only one chapter, and a chapter is defined by the first-level heading `#`.

To compile this example to PDF, you need XeLaTeX. You are recommended to install TinyTeX (which includes XeLaTeX): <https://yihui.name/tinytex/>.


