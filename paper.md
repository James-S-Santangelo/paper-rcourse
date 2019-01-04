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
- name: Ahmed R. Hasan
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

# Description and eligibility

<!-- this will not be part of the final paper -->

We present an open source learning module suitable for a semester long course
and designed to leverage participatory live-coding techniques to teach both
statistical and programming skills to primarily upper-year undergraduate biology
students. Our learning module has three primarily self-contained submodules spanning
sixteen lessons: 1) Programming in R, basic data wrangling, and visualizations; 2)
Exploratory data analysis, statistics and modelling; and 3) Reproducible
science. Our learning module includes eight assignments, distributed throughout
the term to assess students' learning and understanding of the material. All materials
were developed and taught using R Markdown [@rmarkdown], although no prior
knowledge of the R programming language [@R] is assumed or expected.
Our material is licensed under CC-BY 4.0 while the code is under an MIT License.
The open source and modular nature of our computational and statistical learning
module, as well as the focus on the need for greater programming training of
future researchers, makes our material an ideal resource for other instructors
and we believe it would be an excellent contribution to JOSE.

# Main Body

## Statement of Need

<!--
Describing why this material is beneficial to the community, why someone else would use it
-->

In traditional undergraduate biology education, students learn coding skills and
concepts in biology separately. Designed primarily for upper-year undergraduate
students, this learning module emphasizes gaining skills in R coding in the
context of learning statistics and ecology. Notably, the materials cover
statistical concepts that
are broadly useful in biological sciences: linear regression, mixed effects models,
randomization tests, principal component analyses, ANOVA and MANOVA, model
selection, and numerically solving differential equations. We delivered these
materials as a four-month course, but these concepts are presented in stand-alone
lessons designed by an interdisciplinary teaching team that could easily be
mixed and matched to suit any desired course outcome. The course is completely
interactive: all lessons are designed to be delivered in a participatory
live-coding format so that students learn experientially in real-time. The course
materials also include assignments matched to lesson materials that sharpen
students' understanding and allow them to critically apply their skills to new
problems. Reproducible research skills are emphasized throughout, and the course
culminates in an open-ended self-directed project that allows students to apply
their skills to real ecological data. The course repository is linked to an
auto-generated website that presents the syllabus and materials and is easily
modified by editing the course files on GitHub.

## Learning Objectives and Content

The overarching objective of the course is to teach reproducible and
collaborative quanititative research skills. The lessons are described in more
detail in Table 1 and are designed into three overall submodules:

1) Programming in R [@R], basic data wrangling, and visualizations (lessons 1-5).
2) Exploratory data analysis, statistics, and modelling (lessons 6-13).
3) Reproducible science (lessons 14-15). 


| **Module** | **Lesson** | **Description** | **Packages used** |
|:----------|:-------------|:-------------|:------------------|
| Programming in R, data wrangling, visualization | 1 | Introducing R, RStudio, and R Markdown | |
| | 2 | Vectors, data frames, basic operations, and functions  | `tidyverse` [@tidyverse] |
| | 3 | Introduction to exploratory data analysis | `tidyverse` |
| | 4 | Introduction to statistics and visualization | `tidyverse` |
| | 5 | Data transformation and visualization | `tidyverse` |
| Exploration and statistical analysis | 6 | Cleaning and preprocessing raw data | `tidyverse`; `mice` [@mice] |
| | 7 | Descriptive and inferential statistics | `tidyverse`; `car` [@car]; `psych` [@psych]; `multcomp` [@multcomp] |
| | 8 | Linear mixed-effects models | `tidyverse`; `plyr` [@plyr]; `lme4` [@lme4]; `lmerTest` [@lmerTest] |
| | 9 | Randomization tests and data simulation  | `tidyverse`; `reshape2` [@reshape2]; `EcoSimR` [@EcoSimR] |
| | 10 | Multivariate statistics (e.g. PCA) | `tidyverse`; `car`; `psych`; `multcomp`|
| | 11 | Model selection and averaging  | `tidyverse`; `lme4`; `lmerTest`; `MuMIn` [@MuMIn] |
| Numerical models | 12| Population modelling with differential equations  | `tidyverse`; `deSolve` [@deSolve] |
| | 13 | Time-series data and numerical models  | `tidyverse`; `deSolve` |
| Collaborative and reproducible science | 14 | Scientific methods | |
| | 15 | Collaborating through Git and GitHub | |
| | 16 | Git, metadata, and manuscript preparation in R Markdown | `knitr` [@knitr]; `rmarkdown` [@rmarkdown] |

Table: Overview of submodules, lessons, and packages used in the learning module.

## Instructional Design

Drawing from the authors' previous experiences teaching introductory
programming workshops, we designed each of our lessons to have the
following components:

1. *Lesson Outline*: A clearly defined outline of the lesson
objectives including expected time spent on each objective.
    - This makes clear to students not only what they can expect to
    learn from the lesson, but also provides a structured template
    for instructors to prioritize content and gauge how long they
    should be spending on each objective.
2. *Participatory Live-Coding*: Coding snippets that form the
teaching content of each lesson objective, taught in-class using
live-coding, a hands-on method of teaching whereby
instructors share their screen while coding and students follow along. This
approach is frequently used by organizations that teach programming
(e.g. [Software Carpentry](https://software-carpentry.org/blog/2016/04/tips-tricks-live-coding.html)) [e.g. @carpentry].
   - These submodules cover all concepts necessary to understand
   the lesson content and complete the take-home assignments and
   in-class exercises. In lessons where the explicit goal was
   not to learn programming, but a topic such as "Statistical
   Modelling", we used the coding submodules to explain the concept
   while concurrently demonstrating how to use programming to
   create and apply statistical models to data.
3. *Interleaved Exercises*: Coding exercises or discussion points
during the lesson to assess and confirm that students are
following along.
   - These exercises serve to both challenge the students and slowly
   build confidence in the lesson material.
   - If many students struggle to successfully complete a given
   exercise, this is a way for instructors to identify which
   concepts to go over more thoroughly or clear up any misunderstandings.
4. *Summative Assignment*: A comprehensive assignment to test the
competency of students on the lesson material.
   - Assignments were designed to challenge the students to apply
   the techniques and concepts from the lesson to solve new problems,
   demonstrating their understanding of the material.
   - Each assignment covers two lessons worth of material.

Each of our lessons built on skills and concepts that would ultimately allow
students to work on a final open-ended analysis of real open ecological data.
We deliberately chose large and messy (e.g. missing values) datasets for use in the course,
reflecting the types of data that are being increasingly generated across
various disciplines. With this goal in mind, we designed lessons to provide the
building blocks to clean, manipulate, visualize, and analyze any datasets
students may come across, including those used for the final projects.

## Teaching Experience

For the first iteration of the course, our teaching team consisted of six
graduate students from several fields (Physiology, Biomedical
Engineering, Physics, Psychology, and Nutritional Science); we divided course
topics among each instructor to develop and deliver individual lessons and
assignments to the eight participating students. We reduced the number of
instructors to four graduate
students for the second iteration (Physics, Ecology and Evolutionary Biology,
Psychology, and Cell and Systems Biology) and the number of learners
increased to 26. We estimate that four instructors could effectively teach the
current iteration of the course to around 40 students.

To maximize the learning experience, we prioritized in-class participation,
engagement, and hands-on experience. The main teaching techniques we used to
achieve this were participatory live-coding
[@rubin_effectiveness_2013;@haaranen_programming_2017;@wilson_teaching_2018]
where students were asked to complete partial solutions as the class worked through
the material together, and project-based learning
[@sawyer_cambridge_2006;@strobel_when_2009;@markham_project_2011] where
students collaborated in teams on data analysis problems, similar to a real
world scenario.

To ensure that proper teaching assistance was available at all times, we
adopted a method used successfully in workshops developed by The Carpentries [@wilson-software-carpentry].
At least two instructors were present for each lesson, with one of these acting as
a "helper". Students would then signal their need for assistance by attaching
differently colored sticky notes to the back of their laptop monitor. This
method avoided interrupting the lesson flow when students needed assistance.

## Story of the project

While there are many excellent open source libraries for quantitative data
analysis, the use of less capable analysis tools (such as spreadsheet software)
is still prevalent among researchers although these drastically reduce
analysis reproducibility, power, and efficiency. Partly this happens because of
lack of awareness, and partly because students are often required to learn
about new tools in isolation and on top of their main research activities.
Those that do embark on this daunting journey often quit before they can
reap the rewards of their efforts. Like-minded peers could provide the needed
support structure to uphold motivation, but are often few and far between,
especially in fields without a strong quantitative culture. To remedy these
issues, we launched the student group [UofT
Coders](http://uoftcoders.github.io/) which teaches how to use code for
research through skill sharing, co-working and community building in a friendly
environment.

After receiving overwhelmingly positive feedback on our content and teaching style,
we sought to formally share our experiences through the university
curriculum. We designed a course on open, reproducible data analysis, which we
taught as a fourth-year undergraduate course in the Department of
Ecology and Evolutionary Biology with the title "Theoretical Ecology and
Reproducible Quantitative Methods in R." We modelled the structure and portions
of the course content after ["Reproducible Quantitative
Methods"](https://cbahlai.github.io/rqm-template/) a course created by Dr.
Christie Bahlai, modifying the lesson content to include additional theoretical
ecology topics but maintaining the focus on reproducibility and computational
skills.

Following a successful pilot term we modified our lesson material to include more generally applicable
statistical concepts and fewer theoretical ecology concepts, and renamed the
course "Quantitative Methods in R for
Biology" [@rcourse] to reflect this change. On
both occasions, the course received excellent feedback from the students and
the supervising professors.

# Contributions

LWJ, MB-F, LT, and LC initially conceptualized the course, while JO took
the initial lead on course development. 
JO, MB-F, LWJ, LC, ES, and LT designed and taught the first iteration of the course
JSS, LC, MB-F, and ARH taught the second iteration of the course, with
guest lectures from SM and LT. 
Lecture development for second iteration: JO and ARH (1-5), JSS (8, 9, 11), 
LC (6, 7, 10), MB-F (12, 13), LWJ (14), ARH and SM (15), LT (16). 
LWJ, MB-F, JO, SM, LT, ARH, and JSS wrote the paper.

# References
