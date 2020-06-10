
<!-- README.md is generated from README.Rmd. Please edit that file -->

# annotater

<img src='man/figures/logo.png' align="right" height="276" /> The goal
of annotater is to annotate package load calls in text strings and R/Rmd
files, so we can have an idea of the overall purpose of the libraries
we’re loading.

### What do my loaded packages do?

<img src='https://raw.githubusercontent.com/luisdva/annotater/master/inst/media/annotcalls.gif' align="center" width="340px" />

### Where did I get them?

<img src='https://raw.githubusercontent.com/luisdva/annotater/master/inst/media/repos2.gif' align="center" width="340px" />

-----

The two annotation types are also available together:

<img src='https://raw.githubusercontent.com/luisdva/annotater/master/inst/media/repostitles.gif' align="center" width="340px" />

## Installation

Install the development version of `annotater` from GitHub with:

``` r
# install.packages("remotes")
remotes::install_github("luisDVA/annotater")
```

Restart RStudio after the installation for the addins to load properly.

### When using the addins, make sure the focus (blinking cursor) is on an open RStudio R file in the ‘source’ pane.

## Example

These are the possible annotations, which can be added to character
strings (with one line per element), or applied to .R or .Rmd files in
RStudio through their correspondng addins.

``` r
library(annotater)
test_string <-c("library(boot)\nrequire(Matrix)")
writeLines(annotate_pkg_calls(test_string))
writeLines(annotate_repo_source(test_string))
writeLines(annotate_repo_source(test_string))
```

Entire .R files can also be parsed and annotated with the
`annotate_script` function.

Try it out\! Feedback welcome

Thanks to [Jonathan Carroll](https://github.com/jonocarroll), [Fırat
Melih Yılmaz](https://twitter.com/fratmelhylmaz), and [Achaz von
Hardenberg](https://github.com/achazhardenberg) for feedback and
suggestions.
