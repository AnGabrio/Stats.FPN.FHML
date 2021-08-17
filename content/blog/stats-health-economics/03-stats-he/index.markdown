---
title: "Health economics and R"
weight: 3
subtitle: ""
excerpt: "Health economics is a relatively new discipline in which the role played by statistics is constantly growing."
date: 2021-01-03
draft: false
---

## How to perform and economic evaluation using R?

**missingHE** is a package designed to aid in the process of economic evaluations with missing outcome data. The modelling perspective is that of the Bayesian approach, exploiting its natural ability to assess the uncertainty associated with the missing values and its impact on decision making. The **missingHE** package provides different functions to fit Bayesian models for missing data in trial-based HTA.

### How to fit a model

To demonstrate how to fit a model using **missingHE** we use a built-in dataset based on a pilot RCT (the MenSS study) where individual level effectiveness and costs were collected over a one year follow-up at regular intervals. We fit a selection model to handle missing values while also using alternative parametric distributions for the outcomes. More information about selection models and all types of models currently available in **missingHE** can be found on the [GitHub page](https://github.com/AnGabrio/missingHE) of the authors or the [CRAN](https://cran.r-project.org/web/packages/missingHE) repository of the package.

Start with assuming a joint model for the observed data `\(p(e,c\mid \boldsymbol \theta)\)` based on a Normal for the effectiveness `\(e\)` and a Gamma for the cost `\(c\)` while also adjusting for baseline utilities `\(u_0\)`. When specified, covariates are always included at the (conditional) mean level using appropriate link functions for both `\(e\)` and `\(c\)` models and must be fully-observed.


```r
#load the package
library(missingHE)
```



Next, assume a *Missing At Random* (MAR) mechanism for `\(e\)` and `\(c\)` given `age`


```r
#fit the model
NG.sel=selection(data = MenSS, model.eff = e ~ u.0, model.cost = c ~ e, 
                 model.me = me ~ age + e, model.mc = mc ~ age, type = "MAR", 
                 n.iter = 2000, dist_e = "norm", dist_c = "gamma")
```


### How to extract the results

Standardised CEA output (e.g. CE planes, net monetary benefit, etc.) can be obtained by post-processing the results from the model fitted in **missingHE** using functions from the **BCEA** package. For example, CE acceptability curves can be computed by applying the function `ceac.plot` to the object `cea` stored inside the model output


```r
#plot CEAC
library(BCEA)
ceac.plot(NG.sel$cea)
```

<img src="{{< blogdown/postref >}}index_files/figure-html/chunk4-1.png" width="65%" style="display: block; margin: auto;" />

We do it better !

