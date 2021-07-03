---
title: My Dissertation
author: "Megha Joshi"
date: '2021-07-03'
slug: cwb
categories: [Project]
tags: [meta-analysis, dependence, cluster wild bootstrapping, robust variance estimation]
description: 'Cluster Wild Boostrapping to Handle Dependent Effect Sizes in Meta-Analysis'
---

## Abstract

Meta-regression models work under the assumption that there is only one effect size estimate per study and that the estimates are independent. However, meta-analytic studies in education and social sciences often contain multiple effect size estimates per primary study, leading to dependence in the estimates. Furthermore, meta-analytic studies can include effect sizes from multiple studies conducted by the same lab or investigator, which can also create dependence in the effect sizes. The increasingly popular method to handle dependence, robust variance estimation (RVE), can result in inflated Type I error rates when the number of studies is small. Small sample correction methods for RVE have been shown to control Type I error rates adequately but have been shown to be possibly conservative, especially for tests of multiple-contrast hypotheses. In this dissertation, I examined an alternative method, cluster wild bootstrapping, which has been examined in the econometrics literature but has not been examined under a meta-analytic framework. The results from my simulation studies showed that cluster wild bootstrapping maintained adequate Type I error rates and provided more power than the small sample correction methods that have been proposed in the meta-analytic literature thus far. I have also created an R package that implements cluster wild bootstrapping for meta-analysis.

Full text [here](Cluster_Wild_Bootrstrapping.pdf).
