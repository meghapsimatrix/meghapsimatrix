---
title: wildmeta
author: "Megha Joshi"
date: '2021-10-11'
slug: wildmeta
categories: [Software]
tags: [package, R, wildmeta, meta-analysis, bootstrapping]
description: 'Cluster Wild Bootstrapping for Meta-Analysis'
---

[Here](https://meghapsimatrix.github.io/wildmeta/index.html) is the website for the package. 

Typical methods to conduct meta-analysis---pooling effect sizes or analyzing moderating effects with meta-regression---work under the assumption that the effect size estimates are independent. However, primary studies often report multiple estimates of effect sizes. Presence of multiple effect sizes leads to dependence as the estimates within each study are likely correlated (e.g., because the same participants provide multiple outcome scores). The increasingly popular method to handle such dependence, robust variance estimation (RVE), results in inflated Type 1 error rate when the number of studies is small (Hedges, Tipton & Johnson, 2010; Tipton, 2015). 

Tipton (2015) and Tipton & Pustejovsky (2015) examined several small sample correction methods. Tipton (2015) recommended CR2 type correction for RVE as well as the use of Satterthwaite degrees of freedom for single coefficient tests. Tipton & Pustejovsky (2015) examined corrections for [multiple-contrast hypothesis tests](https://cran.r-project.org/web/packages/clubSandwich/vignettes/Wald-tests-in-clubSandwich.html). The authors found that the HTZ test, which is an extension of the CR2 correction method with the Satterthwaite degrees of freedom, controlled Type 1 error rate adequately even when the number of studies was small. However, Joshi, Pustejovsky & Beretvas (2021) showed, through simulations, that the HTZ test can be conservative. We examined another method, cluster wild bootstrapping (CWB), that has been studied in the econometrics literature but not in the meta-analytic context. The results of the simulations from Joshi, Pustejovsky & Beretvas (2021) showed that CWB adequately controlled for Type 1 error rate and had more power than the HTZ test especially for multiple-contrast hypothesis tests.

The goal of this package is to provide applied meta-analytic researchers a function with which they can conduct single coefficient tests or multiple-contrast hypothesis tests using cluster wild bootstrapping. 

## Installation

You can install the development version from [GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("meghapsimatrix/wildmeta")
```
