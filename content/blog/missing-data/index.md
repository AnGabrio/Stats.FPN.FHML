---
author: Andrea Gabrio
categories:
- missing data
date: "2021-01-20"
draft: false
excerpt: Missing data can be very annoying.
layout: single
subtitle: The missingness issue
title: Missing data 
tags:
  - missing-data
  - analysis
  - statistics
---

Here I merely summarise some of the key concepts related to missing data analysis problems, mostly taken from the book *Statistical Analysis with Missing Data* - Little and Rubin (2019). 
For more info, check out the book which is a really nice resource!

![Little and Rubin's book](/img/little_rubin_2019.jpg)

## Introduction

Standard statistical methods have been developed to analyze rectangular data sets. Traditionally, the rows of the datamatrix represent units, also called cases, observations, or subjects depending on context, and the columns represent
characteristics or variables measured for each unit. However, when some of the entries in thematrix are not observed, for example when respondents in a household survey refuse to report income in an industrial experiment, some
results are missing because of mechanical failures unrelated to the experimental process.

	**Definition**. Missing data are unobserved values that would be meaningful for analysis if observed; in other words, a missing value hides a meaningful value.

When the definition applies, it makes sense to consider analyses that effectively predict, or "impute" (that is, fill in), the unobserved values.
If, on the other hand, the definition does not apply, then imputing the unobserved values makes little sense, and an analysis that creates strata of the population defined 
by the pattern of observed data is more appropriate.

## Missing data mechanism

It is useful to distinguish the missingness pattern, which describes which values are missing and observed in the data matrix and the *missingness mechanism*
(or mechanisms), which concerns the relationship between missingness and the values of variables in the data matrix. Missingness mechanisms are crucial
because the properties of missing data methods depend very strongly on the nature of the dependencies in these mechanisms. The crucial role of the
mechanismin the analysis of data with missing values was largely ignored until the concept was formalized in the theory of Rubin through the simple
device of treating themissingness indicators as random variables and assigning them a distribution.

Define the complete data matrix *y* and the missingness indicator matrix *m*. The missingness mechanism
is characterized by the conditional distribution of *m* given *y*. 
If missingness does not depend on the values of the data, missing or observed, the data are called *missing completely at random* (MCAR). Let *y0* and *y1* denote the observed and missing components of *y*, respectively.
A less restrictive assumption than MCAR is that missingness depends on *y* only through the observed components *y0*, in which case the missingness mechanism is called *missing at random* (MAR). Finally, the mechanism is called *missing not at random* (MNAR) when 
the distribution of *m* depends on the missing components *y1*. MAR is a sufficient condition for inferences to be the valid without modeling themissingness mechanism.
However, if the data are MNAR, then the analysis based on the responding subsample is generally biased for the parameters of the distribution of *y*, including the mean.

## Missing data methods

Missing data methods proposed in the literature can be usefully grouped as:

	1. Procedures based on completely recorded units.

	2. Weighting procedures.

	3. Imputation procedures.

	4. Model-based procedures.

The first type of procedures simply discards incompletely recorded units and to analyze only the units with complete data, also known as *Complete Case Analysis* (CCA).
CCA is easy to implement and may be satisfactory with small amounts of missing data. It can lead to serious biases, however, and it is not usually very efficient.
The second type modifies the weights in an attempt to adjust for nonresponse as if it were part of the sample design.
The third type fills in the missing values and the resultant completed data are analyzed by standard methods. Common methods include hot-deck imputation, 
mean imputation, and regression imputation. For valid inferences to result, modifications to the standard analyses are required to allow for the differing status of the real and
the imputed values. The last type defines a model for the complete data and bases inferences on the likelihood or posterior
distribution under that model, with parameters estimated by procedures such as maximum likelihood. Advantages of this approach are flexibility;
the avoidance of ad hoc methods, in that model assumptions underlying the resulting methods can be displayed and evaluated; and the availability 
of estimates of sampling variance that take into account incompleteness in the data.

## Conclusions

When dealing with missing data, no general and easy solution is available since assumptions about missing data cannot be checked from the data at hand but any inference
must resort to untestable assumptions in order to draw final inferences. This is way preventive approaches aimed at minimising the number and impact of missing data on 
the results should be adopted prior to perform the analysis. When this is no longer possible, then context-specific information should be used to determine the most plausible 
assumptions about the unobserved data and the related methods to use to handle them. A key element in any missingness analysis is to allow for the uncertainty associated with 
the lack of observed data by means of conducting sensitivity analysis to a range of plausible assumptions to check the robustness of the results across different scenarios.




