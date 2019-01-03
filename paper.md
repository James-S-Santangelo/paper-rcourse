---
title: "A graduate student-led participatory live-coding quantitative methods course in R: Experiences on initiating, developing, and teaching"
tags:
- R
- ecology
- statistics
- biology
- undergraduate
# Author order? Right now it is alphabetical
authors:
- name: Luke W. Johnston
  orcid: 0000-0003-4169-2616
  affiliation: "2,3"
- name: Madeleine Bonsma-Fisher
  orcid: 0000-0002-5813-4664
  affiliation: 1
- name: Lindsay Coome
  orcid:
  affiliation: 5
- name: Joel Ostblom
  orcid: 0000-0003-0051-3239
  affiliation: 4
- name: Elliott Sales de Andrade
  orcid: 0000-0001-7310-8942
  affiliation: 1
- name: Lina Tran
  orcid: 0000-0003-3504-4524
  affiliation: 8
- name: Ahmed Hasan
  orcid: 0000-0003-0002-8399
  affiliation: 6
- name: James S. Santangelo
  orcid: 0000-0002-5921-2548
  affiliation: 7
- name: Sara Mahallati
  orcid: 0000-0002-6765-0898
  affiliation: 4
affiliations:
- name: Department of Physics, University of Toronto
  index: 1
- name: Department of Nutritional Sciences, University of Toronto
  index: 2
- name: Department of Public Health, Aarhus University
  index: 3
- name: Institute of Biomaterials and Biomedical Engineering, University of Toronto
  index: 4
- name: Department of Psychology, University of Toronto
  index: 5
- name: Department of Cell and Systems Biology, University of Toronto
  index: 6
- name: Department of Ecology and Evolutionary Biology, University of Toronto
  index: 7
- name: Department of Physiology, University of Toronto
  index: 8
date: 18 December 2018
bibliography: paper.bib
---

# Summary

Possible outine:
- Background/History
- From idea to implementation, step by step
- Instructor experiences and undergraduate feedback
- Suggestions for other initiatives

Citations to entries in paper.bib should be in
[rMarkdown](http://rmarkdown.rstudio.com/authoring_bibliographies_and_citations.html)
format.

This is an example citation [@figshare_archive].

Figures can be included like this: ![Fidgit deposited in figshare.](figshare_article.png)

# Statement of Need

<!--
Describing why this material is beneficial to the community, why someone else would use it
-->

In traditional undergraduate biology education, students learn coding skills and biology concepts separately. This course, designed for third and fourth-year undergraduate students, fosters R coding skills in the context of learning statistics and ecology. Notably, the materials cover statistical concepts that are broadly useful in biology: linear regression, mixed effects models, randomization tests, principal component analyses, ANOVA and MANOVA, model selection, and numerically solving differential equations. We delivered these materials as a four month course, but these concepts are presented in stand-alone lectures designed by an interdisciplinary teaching team that could easily be mixed and matched to suit any desired course outcomes. The course is completely interactive: all lectures are designed to be delivered in a participatory live-coding format so that students learn experientally in real-time. The course materials also include assignments matched to lecture materials that sharpen students' understanding and allow them to critically apply their skills to new problems. Reproducible research skills are emphasized throughout, and the course culminates in an open-ended, self-directed project that allows students to apply their skills to real ecological data. The course repository is linked to an auto-generated website that presents the syllabus and materials and is easily modified by editing the course files on GitHub.

Bullet point version (can be removed after discussion):

* Students often learn coding skills and biology concepts separately, while this course fosters R coding skills in the context of learning statistics and ecology.
* Course contains stand-alone lectures that outline broadly useful statistical methods.
* Modular: lectures can be mixed and matched
* This course is completely interactive: all lectures are designed to be delivered in a participatory live-coding format so that students learn experientally in real-time.
* This course contains assignments that sharpen students' understanding and allow them to critically apply skills to new problems.  
* Students learn creativity and critical thinking through an open-ended, self-directed project that uses real ecological data.
* Students learn skills for reproducible research throughout the course.
* Course website - nice looking and easy to use
* We have taught this course twice and have refined the materials based on previous teaching experience

# Main Body

## Learning Objectives and Content
The overarching objective of the course is to teach quantitative research
methods that are reproducible and collaborative. The lectures are designed in
three main groups: Programming in R and basic data wrangling and visualizations
(lectures 1-5), exploratory data analysis, statistics and modelling (Lectures
6-12),  and reproducible science (Lectures 13-15).  The following is a brief
description of learning objectives of the lectures based on independent modules:  
- Introductory R:  
  - The first lecture starts with giving students an overview of
the capabilities of R such as more efficient quantitative analysis of data
compared to manual handling of spreadsheets, programming in R, and integrating
analyses with generating reports using R Notebook (markdown syntax).
  - Second lecture introduces fundamental elements in programming with R such as vectors,
data frames, basic operations and use of functions.
  - The third lecture introduces the concept of exploratory analysis of datasets
with a focus on using `dplyr` [@dplyr] package.
  - The objective for lecture four is to learn the advantage  of
using summary statistics and data visualization using `tidyverse` [@tidyverse]
packages.
  - Lecture five builds on tidy data topic to learn transforming datasets
to appropriate formats for different scientific questions and for reproducing
existing figures.  
- Exploratory data analysis and statistical models:
  - Lecture six focuses on approaches for cleaning up and preprocessing of raw data.  
  - Lecture seven introduces basic descriptive and inferential statistical techniques such
as linear models.
  - Lecture eight focuses on linear mixed effects models to
analyze the fixed and random effects in nested exploratory data.
  - Lecture nine
introduces randomization tests and teaches simulating datasets and applying such
tests on simulated and read data.
  - Lecture ten's objective is to learn multivariate statistics with a focus on
  principle component analysis and multivariate analysis of variance.  
- Numerical modeling:  
  - Lecture eleven introduces model selection approach, its benefits over traditional  
inferential statistics, and model selection criteria such as Akaike's  Information
Criterion.
  - Lecture twelve is to learn population models and using differential
equations to analyze system dynamics.  
- Reproducible science:
  - Lecture thirteen focuses on time series data and fitting numerical models to
such datasets.  
  - Lecture fourteen introduces the scientific method and integrating
scientific approaches with group dynamics and in assigning roles and tasks. In
this lecture students form groups for the final course project.
  - Lecture fifteen focuses on reproducible and
collaborative research tools such as Git version control and the Github platform.
Each group works within a GitHub repository and the team members learn the
basics of documenting the progress of the project and collaborating using these
tools.
  - Lecture sixteen finishes the course with the topic of reproducibility. We
learn the barriers, and the beneficial approaches such as the use of metadata
and generating comprehensive manuscript in R-markdown.

# References
