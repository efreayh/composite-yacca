# composite-yacca

`composite-yacca` is a fork of the `yacca` package developed by Carter T. Butts. The fork extends the functionality of the `helio.plot` function, allowing the `cv` parameter to accept a vector specifying the canonical variates to include in the plot. 

## Install

Check your working directory in R with `getwd()`. Download the package [here](https://github.com/efreayh/composite-yacca/releases) and place it in your working directory. 

Remove any existing `yacca` package installations:
```
remove.packages("yacca")
```

Install the `composite-yacca` package:
```
install.packages("yacca_1.4-3.tar.gz", repos = NULL, type = "source")
```

Load the library:
```
library(yacca)
```

## Example

```
helio.plot(
    c = data,
    cv = c(1,2,3),            # Plot the first 3 canonical variates
    xvlab = x_labels,
    yvlab = y_labels,
    x.name = "X Label", 
    y.name = "Y Label", 
    main = "Helio Plot with Multiple Canonical Variates",
    zero.rad = 20,            # Adjust for spacing of circles
    range.rad = 12,           # Adjust for spacing of circles
    lab.cex = 1,              # Adjust for variable label size
    name.cex = 1              # Adjust for variable set label size
)
```
&nbsp;

# yacca (Original README)

<!-- badges: start -->
[![R build status](https://github.com/CarterButts/yacca/workflows/R-CMD-check/badge.svg)](https://github.com/CarterButts/yacca/actions)
[![CRAN status](https://www.r-pkg.org/badges/version/yacca)](https://CRAN.R-project.org/package=yacca)
<!-- badges: end -->

### Yet Another Canonical Correlation Analysis Package for R

The `yacca` package contains basic functionality for canonical correlation analysis and related calculations (e.g., canonical redundancy, loadings, etc.).  As the name implies, this is one of many (including the cancor function of base R).  `yacca` is not necessarily superior to the others, but supplies various bits of functionality that are convenient and otherwise difficult to find in one place (e.g., helio plots for loadings, redundancy score calculation, regularization support).  If you prefer a different package, rest assured that the author is not offended.

`yacca` was originally hosted on CRAN, but was mothballed due to lack of active maintenance.  This version is refreshed, apparently functional with recent R versions, and now back on CRAN.  It may hence be installed directly thence, but is also available via this fine repository.  If you use this package in your research, it would be greatly appreciated if you could cite it.  E.g.:

> Butts, Carter T.  2008.  "yacca: Yet Another Canonical Correlation Analysis Package."  Software package.

(Or the `citation()` command in R, to specifically cite the current version.)

More information regarding the package and its use may be found within the package documentation.

## Installing Within R

To install the `yacca` package from the comfort of your own home or office, you may proceed using CRAN by the usual method, i.e.:

	install.packages("yacca")

To instal from GitHub, first ensure that you have the `devtools` package installed and loaded.  Then, type the following:

	install_github("carterbutts/yacca", subdir="yacca")

Alternately, cloning this repository and building/installing the package locally is another option.  But in that case, you don't need my help to tell you what to do, now do you?

\-CTB, 3/7/22
