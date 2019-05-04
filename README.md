The slumdown package
================
Danielle Navarro
21 April 2019

[![Travis build
status](https://travis-ci.org/djnavarro/slumdown.svg?branch=master)](https://travis-ci.org/djnavarro/slumdown)
[![Codecov test
coverage](https://codecov.io/gh/djnavarro/slumdown/branch/master/graph/badge.svg)](https://codecov.io/gh/djnavarro/slumdown?branch=master)

The *slumdown* package is an experiment in creating a simple “blogdown
native” Hugo theme, one that assumes that posts are written using R
Markdown. It extends the [slum theme for
Hugo](https://github.com/djnavarro/hugo-slum) by providing an interface
for customising the blog within R and a system for generating plots that
use the same colour scheme as the blog post. The *slumdown* package is
not on CRAN and so needs to be installed from GitHub:

``` r
# devtools::install_github("djnavarro/slumdown")
library("slumdown")
```

By default, the *slumdown* package assumes the source code for the site
takes the form of an RStudio project, and will be deployed to GitHub
pages, though neither is strictly necessary. To get started:

``` r
slum_new(dir = "path/to/my/slumblog") 
```

This will create a new RStudio project called `slumblog` (or whatever),
download the slum theme and the example site. From within the project,
initialise the blog using `blogdown`:

``` r
blogdown::serve_site()
```

Blogdown will then generate the [example
site](https://djnavarro.github.io/hugo-slum/) in the `docs` folder,
which provides a short tutorial on how to get started using the package
and what it is capale of.
