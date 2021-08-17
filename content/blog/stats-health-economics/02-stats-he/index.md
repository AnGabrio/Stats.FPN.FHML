---
date: "2021-01-02"
draft: false
excerpt: Health economics is a relatively new discipline in which the role played by statistics is constantly growing.
subtitle: ""
title: Decision making in health economics
weight: 2
---

## What is health economics and why is it important?

Concerns about the rising healthcare costs and the desire to secure access to high quality and affordable medical care, have prompted the interest of the public towards the need to establish the most appropriate way to identify how to best invest limited healthcare resources for the benefit of Society. 
To this extent, many stakeholders have expressed interest in, and devoted efforts to use *Health Technology Assessment* (HTA) processes to guide these decisions. 
HTA has been defined as "a multidisciplinary field of policy analysis, studying the medical, economic, social and ethical implications of development, diffusion and use of health technology".

In many countries, the organizations that perform HTAs are public sector agencies, reflecting the financing and/or provision of healthcare. For example, in the United Kingdom (UK), the *National Institute for Health and Care Excellence* (NICE) relies on HTAs to formulate guidance on the use of health technologies in the National Health Service for England and Wales. 
Similar agencies exist in Europe, the North American continent, South America and Australia. The extent to which HTA activities are linked to a particular decision about the reimbursement, coverage, and use of a health technology influences the extent to which firm recommendations are made on the basis of the assessment and "appraisal" processes.
HTA inherently requires consideration of the integration of medical interventions into clinical care and, as such, involves balancing a number of factors, including societal values, clinical and organizational context in which the technology will be used. 
An important element that informs the decision-making process in HTA is the *economic evaluation*, which has been defined as the comparative analysis of alternative courses of action in terms of both their costs and consequences.

The type of data used in economic evaluations typically come from a range of sources, whose evidence is combined to inform HTA decision-making. Traditionally, relative effectiveness data are derived from *randomised controlled clinical trials* (RCTs), while healthcare resource utilisation, costs and preference-based quality of life data may come from the same study that estimated the clinical effectiveness or not. 
A number of HTA agencies have developed their own methodological guidelines to support the generation of the evidence required to inform their decisions. For example, the NICE guidelines on the analytical methods to be used have been derived from the normative framework the Institute has adopted to increase consistency in analysis and decision making by defining a set of standardised methods for HTA. 
In this context, the primary role of economic evaluation for HTA is not the estimation of the quantities of interest (e.g. the computation of point or interval estimation, or hypothesis testing), but to aid decision making. 
The implication of this is that the standard frequentist analyses that rely on power calculations and $P$-values to estimate  statistical and clinical significance, typically used in RCTs, are not well-suited for addressing these HTA requirements. 
It has been argued that, to be consistent with its intended role in HTA, economic evaluation should embrace a decision-theoretic paradigm and develop ideally within a Bayesian statistical framework to inform two decisions: 

	1. whether the treatments under evaluation are cost-effective given the available evidence and 

	2. whether the level of uncertainty surrounding the decision is acceptable (i.e. the potential benefits are worth the costs of making the wrong decision).  

This corresponds to quantify the impact of the uncertainty in the evidence on the entire decision-making process (e.g. to what extent the uncertainty in the estimation of the effectiveness of a new intervention affects the decision about whether it is paid for by the public provider).  

---

## The process

The general process of conducting the analysis (with a view of using the results of the model to perform an economic evaluation) can be broken down in several steps.

### Decision problem

The starting point is the identification of the decision problem, which defines the objective of the economic evaluation (e.g. the interventions being compared, the target population, the relevant time horizon). 

### Statistical model

In line with the decision problem, a statistical model is constructed to describe the (by necessity, limited) knowledge of the underlying clinical pathways. 
This implies, for example, the definition of suitable models to describe variability in potentially observed data (e.g. the number of patients recovering from the disease because of a given treatment), as well as the epistemic uncertainty in the population parameters (e.g. the underlying probability that a random individual in the target population is cured, if given the treatment under study).
At this point, all the relevant data are identified, collected and quantitatively sytnthesised to derive the estimates of the input parameters of interest for the model. 

### Economic model

These parameter estimates (and associated uncertainties) are then fed to the economic model, with the objective of obtaining some relevant summaries indicating the benefits and costs for each intervention under evaluation. 

### Uncertainty analysis

Uncertainty analysis represents some sort of "detour" from the straight path going from the statistical model to the decision analysis: if the output of the statistical model allowed us to know with perfect certainty the "true" value of the model parameters, then it would be possible to simply run the decision analysis and make the decision. 
Of course, even if the statistical model were the "true" representation of the underlying data generating process (which it most certainly is not), because the data may be limited in terms of length of follow up, or sample size, the uncertainty in the value of the model parameters would still remain. 

The results of the above analysis can be used to inform policy makers about two related decisions: 

	a. Whether the new intervention is to be considered (on average) "value for money", given the evidence base available at the time of decision, and 

	b. Whether the consequences (in terms of net health loss) of making the wrong decision would warrant further research to reduce this "decision uncertaint".  

While the type and specification of the statistical and economic models vary with the nature of the underlying data (e.g. individual level versus aggregated data), the decision and uncertainty analyses have a more standardised set up.

