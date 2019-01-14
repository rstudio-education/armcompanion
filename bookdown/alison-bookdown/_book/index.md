--- 
title: "Notes from the Advanced R Markdown Workshop"
params:
  last_updated: !r Sys.Date()
  event: "rstudio::conf 2019"
  date: "January 15 - 16, 2019"
  place: "Austin, TX"
subtitle: "rstudio::conf 2019 | January 15 - 16, 2019 | Austin, TX"
author: 
- Alison Hill
- Yihui Xie
- the ARM workshop participants
date: "January 15 - 16, 2019"
site: bookdown::bookdown_site
documentclass: book
bibliography: [book.bib, packages.bib]
biblio-style: apalike
link-citations: yes
description: "This is a minimal example using the bookdown package for the rstudio::conf Advanced R Markdown Workshop."
cover-image: images/books.jpg
url: 'https\://alison-bookdown.netlify.com/'
github-repo: rstudio-education/arm-companion-rsc2019
twitter-handle: apreshill
---


# Welcome {-}


<img src="images/books.jpg" width="2456" />

This is a minimal example of using the bookdown package to write a book. The output format for this example is `bookdown::gitbook`.

This is a _sample_ book written in **Markdown**. You can use anything that Pandoc's Markdown supports, e.g., a math equation $a^2 + b^2 = c^2$.

The **bookdown** package can be installed from CRAN or Github:


```r
install.packages("bookdown")
# or the development version
# devtools::install_github("rstudio/bookdown")
```

Remember each Rmd file contains one and only one chapter, and a chapter is defined by the first-level heading `#`.

## Render the book {-}

To render this book, you can use:


```r
bookdown::render_book('index.Rmd')
```

To render this book from within a subdirectory (that is, if the book's files are located in a subdirectory relative to your project root), you'll need to use:


```r
xfun::in_dir('bookdown/alison-bookdown', bookdown::render_book('index.Rmd'))
```

To compile this example to PDF, you need XeLaTeX. You are recommended to install TinyTeX (which includes XeLaTeX): <https://yihui.name/tinytex/>.

## Serve the book {-}

Instead of running `render_book()` each time you want to view the changes, you can use the function `bookdown::serve_book()` to start a live preview of the book. Any time a Rmd file is saved, the book will be recompiled automatically, and the preview will be updated to reflect the changes.^[https://bookdown.org/yihui/bookdown/serve-the-book.html]

## This page {-}

This page is created from the `index.Rmd` file. The `index.Rmd` file has a YAML with configurations you may want to explore. The only required parameter is site: bookdown::bookdown_site. You can see all the YAML parameters here:


```r
rmarkdown::yaml_front_matter(here::here('bookdown/alison-bookdown/index.Rmd'))
```

```
## $title
## [1] "Notes from the Advanced R Markdown Workshop"
## 
## $params
## $params$last_updated
## [1] "Sys.Date()"
## 
## $params$event
## [1] "rstudio::conf 2019"
## 
## $params$date
## [1] "January 15 - 16, 2019"
## 
## $params$place
## [1] "Austin, TX"
## 
## 
## $subtitle
## [1] "`r params$event` | `r params$date` | `r params$place`"
## 
## $author
## [1] "Alison Hill"                   "Yihui Xie"                    
## [3] "the ARM workshop participants"
## 
## $date
## [1] "January 15 - 16, 2019"
## 
## $site
## [1] "bookdown::bookdown_site"
## 
## $documentclass
## [1] "book"
## 
## $bibliography
## [1] "book.bib"     "packages.bib"
## 
## $`biblio-style`
## [1] "apalike"
## 
## $`link-citations`
## [1] TRUE
## 
## $description
## [1] "This is a minimal example using the bookdown package for the rstudio::conf Advanced R Markdown Workshop."
## 
## $`cover-image`
## [1] "images/books.jpg"
## 
## $url
## [1] "https\\://alison-bookdown.netlify.com/"
## 
## $`github-repo`
## [1] "rstudio-education/arm-companion-rsc2019"
## 
## $`twitter-handle`
## [1] "apreshill"
```

The possible YAML parameters are based on Pandoc. For EPUB output formats like `gitbook`, you can see all the possible Pandoc parameters [here](https://pandoc.org/MANUAL.html#creating-epubs-with-pandoc). 

> *It is important to point out that most parameters in this YAML will not have clear visible effects on the HTML output, but they may be useful when you deploy the HTML output as a website.* ^[https://bookdown.org/yihui/bookdown/html.html#gitbook-style]

For example, using the `cover-image` YAML parameter does **not** add a visible cover image to the front of your *rendered* HTML book. In the workshop, we talked more about recommended YAML parameters to feed to Pandoc and why.

You can use any of these YAML parameters with R code, using the rmarkdown package function `metadata`. For example, here I'll show you the title again with inline code: Notes from the Advanced R Markdown Workshop

You can also set up custom parameters in your YAML to use in the text of your book with inline R code. For example, this book was last updated on 2019-01-07, and was most recently used for the rstudio::conf 2019 in Austin, TX.





