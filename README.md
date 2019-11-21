---
title: "MT5762 Project 2 - linear models, selection and inference"
author: "C. Donovan"
output:
  html_notebook:
    number_sections: yes
    toc: yes
    toc_depth: 2
    toc_float: yes
  html_document:
    df_print: paged
    toc: yes
    toc_depth: '2'
    highlight: tango
  word_document:
    toc: yes
    toc_depth: '2'
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```


# Introduction

This is a data analysis project, which focusses mainly on fitting linear models. The data relate to birth-weights, which can be downloaded from [here](https://www.stat.berkeley.edu/~statlabs/data/babies23.data) and descriptor [here]( https://www.stat.berkeley.edu/~statlabs/data/babies.readme). 


The data are part of a larger group of studies: the Child Health and Development Studies (CHDS). There is substantial analysis of this already (refer various works by [Yerushalmy](https://www.ajog.org/article/0002-9378(64)90509-5/fulltext)) and it seems, some controversy (see [here](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4200064/)).




----------------------


# What is required

This is a group project. You have been allocated (by pseudo-number generator) to groups. Only one project submission is required for each group - so you will be free to divide the analysis, research, coding, report writing etc. amongst yourselves.

To start:

*  Import the data into your analysis package, and ensure it has read in correctly. Note this data has particular codings for missing values and some oddities - check the data carefully.
*  Do some preliminary exploration of the data and identify interesting relationships or unusual datapoints that might require further investigation (imagine there might be peculiarities in the data you could query the investigators about).  

The principal question is:

> What relationships are there between the measured variables and the birth weight of babies?

You are to produce a model that describes potential drivers of low birth-weight babies.


----------------------


As part of this process, you should:

* Do some model selection. Your final model(s) should be justified on statistical and logical grounds. You should use AIC as at least one of your measures.

* Consider at least some first-order interactions as part of your pool of models. Even if these are not in your final model, interpret one fitted interaction effect that you considered _a priori_ logical.

* Research _validation datasets_ and _Mean Square Error (MSE)_ and hold out a random 20% for this purpose. Use this to choose between your top two models from your selection. Alternatively research and use 5-fold cross-validation.

* Check relevant assumptions for whatever final model(s) you settle on.

* Subject your best model to some bootstrapping to give empirical confidence intervals for the parameters, along with any parametric ones you generate for it.

*  Address practical significance as well as statistical significance.

*  Be critical of the study and your analyses - temper your conclusions in line with this.

As a group project, you should all do your fair share. Sometimes it is useful to divide tasks - for example:

1. Data checking, plotting, summarising
1. Report writing
1. Model selection
1. Bootstrapping
1. Prediction to a validation set or 5-fold cross-validation and the MSE

Although this is not comprehensive and you can do as you see fit.


# The report

*  Your group is a statistical consultancy contracted to provide an analysis report to address the specific questions above. Consider your target audience to be generally medically-trained people with only a passing familiarity with statistics. However also consider that medical statisticians might also read this to confirm the validity of your claims i.e. details are required, but should not interfere with the readability for a general audience.

*  The report should be no more than 4000 words and should contain relevant plots - however you can put extra output in an appendix at the end. 

*  Include an introductory section describing the purpose of your investigation and a discussion at the end summarising your findings.

*  Your report should contain an introduction, methods, results and discussion. Also include a short executive summary at the start in plain language (i.e. something understandable to those interested in the study but without statistical training).

*  Include references throughout the text as required (e.g. software used, source of the data), and include a bibliography. Your references should generally be from peer-reviewed sources (google scholar is your friend) - random websites are less compelling. Emulate the referencing style of an academic journal and use it consistently.

*  Analysis can be in any software you like. Do not include raw computer output in the body of the report - make sure any results you include are tidy (e.g. in a table) and are relevant. Include an appendix in your report with examples of the code used (or a markdown document). 

*  Submit the project by 5pm Thursday the 2nd of November. Submissions should uploaded to Moodle and only one required per group. The report should be in PDF format, but you can include supplementary files (code, markdown) in a zipped file.
