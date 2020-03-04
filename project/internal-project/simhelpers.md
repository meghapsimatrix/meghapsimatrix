---
title: gem_scd shiny app
author: "Danny"
date: '2018-02-25'
slug: gem-scd-shiny-app
categories: [Project]
tags: [shiny, R]
description: 'A shiny calculator app'
---

NOTE: This post is quite old, and from a previous version of my website. You can find the published version of this article [here](https://www.tandfonline.com/doi/abs/10.1080/00273171.2018.1466681)

I have a paper under submission with James E. Pustejovsky titled "A gradual effects model for single-case designs" (preprint [here](https://psyarxiv.com/vh964/)). The paper proposes a particular form of nonlinear parametric model for single-case designs that offers some flexibility in functional form and error distribution that many of the other parametric models for single-case designs don't. However, one tricky part of it is that there's not a straightforward way to estimate the particular form of the linear predictor we specify for our proposed model using any of the typical modeling packages in R. To estimate the model we profile the likelihood (or quasi-likelihood), and I wrote functions in R to do that. Those functions can be found in the [SingleCaseES package](https://github.com/jepusto/SingleCaseES). 

Even then, it's a worry that applied practitioners might not want to use R functions. Chances are good that single-case researchers have never touched R in their life, and even with step by step instructions they may go out of their way to avoid it. [So I built a calculator (with some design guidance from James)](https://jepusto.shinyapps.io/gem-scd/). Note: James has a very limited data budget on his shinyapps account so by the mid-to-end of the month the website might not be available. If you want to see it, the following code in R should open it up:

```{r}
install.packages("devtools")
install.packages("sourcetools")
install.packages("shiny")
install.packages("markdown")
install.packages("ggplot2")
install.packages("dplyr")
install.packages("purrrlyr")
devtools::install_github("jepusto/SingleCaseES")
library(SingleCaseES)
shine_gem_scd()
```

The app has self-contained instructions, a calculator for estimating the model for a single data series, as well as a batch calculator for estimating the model for a dataset containing multiple series.

If the paper is accepted for publication, I'll probably write a slightly lengthier blog post/tutorial for its use.