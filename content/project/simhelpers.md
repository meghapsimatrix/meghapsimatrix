---
title: simhelpers
author: "Megha Joshi"
date: '2020-03-04'
slug: simhelpers
categories: [Software]
tags: [package, R, simhelpers, Monte Carlo, simulation]
description: 'A package to help with simulation studies'
links:
- name: CRAN
  url: https://cran.r-project.org/package=simhelpers
- name: Website
  url: https://meghapsimatrix.github.io/simhelpers/
---

Monte Carlo simulations are computer experiments designed to study the performance of statistical methods under known data-generating conditions (Morris, White, & Crowther, 2019). Methodologists use simulations to examine questions such as: (1) how does ordinary least squares regression perform if errors are heteroskedastic? (2) how does the presence of missing data affect treatment effect estimates from a propensity score analysis? (3) how does cluster robust variance estimation perform when the number of clusters is small? To answer such questions, we conduct experiments by simulating thousands of datasets based on pseudo-random sampling, applying statistical methods, and evaluating how well those statistical methods recover the true data-generating conditions (Morris et al., 2019).

The goal of `simhelpers` is to assist in running simulation studies. The main tools in the package consist of functions to calculate measures of estimator performance like bias, root mean squared error, rejection rates. The functions also calculate the associated Monte Carlo standard errors (MCSE) of the performance measures. These functions are divided into three major categories of performance criteria: absolute criteria, relative criteria, and criteria to evaluate hypothesis testing. The functions use the [`tidyeval`](https://tidyeval.tidyverse.org/index.html) principles, so that they play well with [`dplyr`](https://dplyr.tidyverse.org/index.html) and fit easily into a `%>%`-centric workflow (Wickham et al., 2019).

In addition to the set of functions that calculates performance measures and MCSE, the package also includes a function, `create_skeleton()`, that generates a skeleton outline for a simulation study. Another function, `evaluate_by_row()`, runs the simulation for each combination of conditions row by row. This function uses [`future_pmap()`](https://davisvaughan.github.io/furrr/reference/future_map2.html) from the [`furrr`](https://davisvaughan.github.io/furrr/) package, making it easy to run the simulation in parallel (Vaughan & Dancho, 2018). The package also includes several datasets that contain results from example simulation studies. 


