---
author: Andrea Gabrio
categories:
- talk
- missing data
date: "2021-06-22"
date_end: "2021-06-22"
draft: false
event: colloquium
event_url: 
excerpt: Department colloquium.
featured: true
layout: single
links:
- icon: door-open
  icon_pack: fas
  name: website
  url: https://agabrioblog.onrender.com/
- icon: github
  icon_pack: fab
  name: code
  url: https://github.com/AnGabrio
- icon: slideshare
  icon_pack: fas
  name: slides
  url: https://github.com/AnGabrio/Talks
location: Department of Methodology and Statistics, FHML, Maastricht University, Maastricht, The Netherlands
show_post_time: false
subtitle: 
title: Statistical methods to handle missing data in HTA
---

**Abstract**

The statistical analysis of health economic data has become an increasingly important component of clinical trials as
 it provides one of the earliest opportunities to assess the cost-effectiveness of alternative treatments and to guide 
the decisions of policymakers. However, data collected alongside clinical trials are almost invariably incomplete and 
analysts are often unaware of why some participants drop out from the study. Standard analyses focus only on the subset of 
complete cases or use some form of single imputation to handle the missing values. These strategies, however, rely on 
specific assumptions about the unobserved data that can never be checked and may lead to incorrect conclusions. In addition,
the modelling task may be further complicated by the presence of complexities in the data (e.g. skewness and spikes) which
may be difficult to capture through standard parametric methods. 

We first provide an overview of the health economic analysis framework from a statistical perspective with a focus on 
the role played by missing data in the analysis. Next, we present a novel Bayesian nonparametric approach to handle 
a missing bivariate longitudinal health economic outcome by jointly modelling the dropout process associated with each 
type of response while also taking into account the complexities of the data. We specify a flexible nonparametric model for 
the observed data and partially identify the distribution of the missing data with identifying restrictions conditional on 
the dropout indicators of each type of variable and sensitivity parameters. We explore alternative nonignorable scenarios 
through different priors for the sensitivity parameters. Our approach is motivated by, and applied to, data from a trial 
assessing the cost-effectiveness of a new treatment for intellectual disability and challenging behaviour.
