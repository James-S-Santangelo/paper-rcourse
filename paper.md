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

# Description and eligibility

We present a stand-alone module designed for simultaneously teaching statistical
skills and programming skills in a participatory live-coding format to upper year
undergraduate biology students. Our module has 16 primarily self-contained
lectures with topics ranging from data cleaning, manipulation, and visualization,
to the statistical analysis of biological data and reproducibility through GitHub.
Our module additionally includes eight assignments that were distributed to
students throughout the term to assess learning and understanding of course
material. All materials were developed and taught using R Markdown, although no
prior knowledge of the R programming language is assumed prior to taking the
course. Course content is licensed under the CC-BY 4.0 licence while code is
licensed under MIT. The open-source and stand-alone nature of our computational
and statistical learning module makes this material ideally suited to adoption
by other instructors and an excellent contribution to JOSE.


# Statement of Need

<!--
Describing why this material is beneficial to the community, why someone else would use it
-->

In traditional undergraduate biology education, students learn coding skills and
biology concepts separately. This course, designed for third and fourth-year
undergraduate students, fosters R coding skills in the context of learning
statistics and ecology. Notably, the materials cover statistical concepts that
are broadly useful in biology: linear regression, mixed effects models,
randomization tests, principal component analyses, ANOVA and MANOVA, model
selection, and numerically solving differential equations. We delivered these
materials as a four month course, but these concepts are presented in stand-alone
lectures designed by an interdisciplinary teaching team that could easily be
mixed and matched to suit any desired course outcomes. The course is completely
interactive: all lectures are designed to be delivered in a participatory
live-coding format so that students learn experientally in real-time. The course
materials also include assignments matched to lecture materials that sharpen
students' understanding and allow them to critically apply their skills to new
problems. Reproducible research skills are emphasized throughout, and the course
culminates in an open-ended, self-directed project that allows students to apply
their skills to real ecological data. The course repository is linked to an
auto-generated website that presents the syllabus and materials and is easily
modified by editing the course files on GitHub.

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
  - **Lecture 1** starts with giving students an overview of
the capabilities of R such as more efficient quantitative analysis of data
compared to manual handling of spreadsheets, programming in R, and integrating
analyses with generating reports using R Notebook (markdown syntax).
  - **Lecture 2** introduces fundamental elements in programming with R such as vectors,
data frames, basic operations and use of functions.
  - **Lecture 3** introduces the concept of exploratory analysis of datasets
with a focus on using `dplyr` [@dplyr] package.
  - **Lecture 4** objective is to learn the advantage  of
using summary statistics and data visualization using `tidyverse` [@tidyverse]
packages.
  - **Lecture 5** builds on tidy data topic to learn transforming datasets
to appropriate formats for different scientific questions and for reproducing
existing figures.  
- Exploratory data analysis and statistical models:
  - **Lecture 6** focuses on approaches for cleaning up and preprocessing of raw data.  
  - **Lecture 7** introduces basic descriptive and inferential statistical techniques such
as linear models.
  - **Lecture 8** focuses on linear mixed effects models to
analyze the fixed and random effects in nested exploratory data.
  - **Lecture 9** introduces randomization tests and teaches simulating datasets
  and applying such tests on simulated and read data.
  - **Lecture 10** objective is to learn multivariate statistics with a focus on
  principle component analysis and multivariate analysis of variance.  
- Numerical modeling:  
  - **Lecture 11** introduces model selection approach, its benefits over traditional  
inferential statistics, and model selection criteria such as Akaike's  Information
Criterion.
  - **Lecture 12** objective is to learn population models and using differential
equations to analyze system dynamics.  
- Reproducible science:
  - **Lecture 13** focuses on time series data and fitting numerical models to
such datasets.  
  - **Lecture 14** introduces the scientific method and integrating
scientific approaches with group dynamics and in assigning roles and tasks. In
this lecture students form groups for the final course project.
  - **Lecture 15** focuses on reproducible and
collaborative research tools such as Git version control and the Github platform.
Each group works within a GitHub repository and the team members learn the
basics of documenting the progress of the project and collaborating using these
tools.
  - **Lecture 16** finishes the course with the topic of reproducibility. We
learn the barriers, and the beneficial approaches such as the use of metadata
and generating comprehensive manuscript in R-markdown.

## Instructional Design

Drawing from the authors' previous experiences teaching introductory
programming workshops, we designed each of our lectures to have the
following components:

1. *Lesson Outline*: A clearly defined outline of the lesson
objectives including expected length of time spent on each objective.
    - This makes clear to students not only what they can expect to
    learn from the lecture, but also provides a structured template
    for instructors to prioritize content and gauge how long they
    should be spending on each objective. This sets the expectations
    for both students and instructors.
2. *Participatory Live-Coding*: Coding snippets that form the
teaching content of each lesson objective, taught in-class using
live-coding.[^1]
   - These submodules cover all concepts necessary to understand
   the lesson content and complete the take-home assigments and
   in-class exercises. In lectures where the explicit goal was
   not to learn programming, but a topic such as `Statistical
   Modeling`, we used the coding submodules to explain the concept
   while concurrently demonstrating how to use programming to
   create and apply statistical models to data.
3. *Interleaved Exercises*: Coding exercises or discussion points
during the lecture to assess and confirm that students are
following along.
   - These exercises serve to both challenge the students and slowly
   build confidence in the lesson material.
   - Notably, if many students struggle to successfully complete the
   exercise, this is a way for instructors to identify which
   concepts to go over more thoroughly or clear up any misunderstandings
   made along the way.
4. *Summative Assignment*: A comprehensive assignment to test the
competency of students on the lesson material.
   - Assignments were designed to challenge the students to apply
   the techniques and concepts from the lesson to solve new problems,
   demonstrating their understanding of the material.
   - Each assignment covers two lectures worth of course material.

We have found that this combination of clear lesson outlines, coding submodules,
interleaved exercises, and summative assignments gave each lecture a
predictable structure. It also assures that lesson objectives
were both covered and conveyed effectively in order for students to
complete both the exercises and assignments.

Each of our lectures built on skills and concepts that would ultimately allow
students to work on a final open-ended analysis of real open ecological data.
Of note, the datasets we chose for the course were large and messy (e.g. missing
values), reflecting the type of data that is being increasingly generated across
various disciplines. With this goal in mind, we designed lectures to provide the
building blocks to clean, manipulate, visualize and analyze any datasets
students may come across, including those used for the final projects.

[^1]: *A note on "live-coding".* Live-coding is a hands-on method of teaching
coding where the instructor shares their screen with the class and types all
commands on their computer while the group follows along. Live-coding has proven
to be a very effective teaching technique as it forces the instructor to go
slowly and ensures that participants get to try out every command being used.
Furthermore, mistakes and errors are bound to happen. We used two colors of
sticky notes, distributed to students each class, one color to signal
whether they are ready to move on, the other to signal that they are
stuck/have a question, whereby another instructor in the class can follow
up with the student as the class continues. It allows learners to
experience common errors themselves and debug them in a supportive
environment, to explore variations on material as they go, and to
immediately check their understanding by trying things hands-on.
See [Teaching Experience](#teaching-experience) for more details.
This teaching format is heavily influenced by [Software Carpentry](https://software-carpentry.org/blog/2016/04/tips-tricks-live-coding.html)
which uses live-coding as a key practice in their introductory programming
workshops.

## Teaching Experience

For the first iteration of the course, our teaching team consisted of six
graduate students from several different fields (Physiology, Biomedical
Engineering, Physics, Psychology, and Nutritional Science); we divided course
topics among each instructor to develop and deliver individual lessons and
assignments to the eight participating students. After the core material had
been developed, we could reduce the number of instructors to four graduate
students for the second iteration (Physics, Ecology and Evolutionary Biology,
Psychology, and Cell and Systems Biology) although the number of students
increased to 26. We estimate that four instructors could effectively teach the
current iteration of the course to around 40 students.

To maximize the learning experience, we prioritized in-class participation,
engagement, and hands-on experience. The main teaching techniques we used to
achieve this were participatory live coding
[@rubin_effectiveness_2013;@haaranen_programming_2017;@wilson_teaching_2018]
where students were asked to complete partial solutions as we worked through
the material together, and project-based learning
[@sawyer_cambridge_2006;@strobel_when_2009;@markham_project_2011] where
students collaborated in teams on data analysis problems, similar to a real
world scenario.

To ensure that proper teaching assistance was available at all times, at least
two instructors were present for each lecture. One of these would act as
a "helper" and students signal their need for assistance by attaching
differently colored sticky notes to the back of their laptop monitor. This
method avoided interrupting the lecture flow when students needed assistance and it
has been used successfully in workshops developed by The Carpentries
[@wilson-software-carpentry].

## Story of the project

While there are many excellent open source libraries for quantitative data
analysis, the use of less capable analysis tools (such as spreadsheet software)
is still prevalent among graduate students although these drastically reduce
analysis reproducibility, power and efficiency. Part of this issue stems from
lack of awareness, and part from that students are often required to learn
about new tools in isolation and on top of their main research activities. As
such, those that do embark on this daunting journey often quit before they can
reap the rewards of their efforts. Like-minded peers could provide the needed
support structure to uphold motivation, but are often few and far between,
especially in fields without a strong quantitative culture. To remedy these
issues, we launched the student group [UofT
Coders](http://uoftcoders.github.io/) which teaches how to use code for
research through skill sharing, co-working and community building in a friendly
environment.

After receiving overwhelmingly positive feedback on content and teaching style,
we sought to formally share our experiences through the university
curriculum. We designed a course on open, reproducible data analysis, which we
created and taught as a fourth-year undergraduate course in the department of
Ecology and Evolutionary Biology under the title "Theoretical Ecology and
Reproducible Quantitative Methods in R." We modelled the structure and portions
of the course content after ["Reproducible Quantitative
Methods"](https://cbahlai.github.io/rqm-template/) a course created by Dr.
Christie Bahlai, modifying the lesson content to include additional theoretical
ecology topics but maintaining the focus on reproducibility and computational
skills. Our teaching team consisted of six graduate students from several
different fields (Physiology, Biomedical Engineering, Physics, Psychology, and
Nutritional Science); we divided course topics among each instructor to develop
and deliver individual lessons and assignments.

Following a successful pilot term with a class of eight students, the course
was incorporated into the long-term curriculum and delivered a second time to a
class of twenty-six students with a teaching team of four graduate students
(Physics, Ecology and Evolutionary Biology, Psychology, and Cell and Systems
Biology). We modified our lecture material to include more generally applicable
statistical concepts and fewer theoretical ecology concepts, and renamed the
course ["Quantitative Methods in R for
Biology."](https://uoftcoders.github.io/rcourse/) to reflect this change. On
both occasions, the course received excellent feedback from the students and
the supervising professors.


# References
