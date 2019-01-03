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
bibliography: bibliography.bib
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

## Instructional Design

Drawing from the authors' previous experiences teaching introductory programming
workshops, we designed each of our lectures to have the following components:

    1. *Lesson Outline*: A clearly defined outline of the lesson objectives including expected 
    length of time spent on each objective.
        - This makes clear to students not only what they can expect to learn from the lecture,
        but also provides a structured template for instructors to prioritize content and gauge
        how long they should be spending on each objective. This sets the expectations for both
        students and instructors.
    3. *Participatory Live-Coding*: Coding snippets that form the teaching content of each lesson 
    objective, taught in-class using live-coding.[^1]
       - These submodules go over all concepts necessary to understand the concepts, complete the
       in-class exercises, and summative assignment towards the goal of completing the lesson
       objectives. In lectures where the explicit goal was not to learn programming, but a topic
       such as `Statistical Modeling`, we used the coding submodules to explain the concept while
       concurrently demonstrating how to use programming to create, and apply statistical models to
       data.
    5. *Interleaved Exercises*: Coding exercises or discussion points during the lecture to assess
    and confirm that students are following along.
       - These exercises serve to both challenge the students and slowly build confidence in the
       lesson material.
       - Notably, if many students struggle to successfully complete the exercise, this is a way
       for instructors to identify which concepts to go over more thoroughly or clear up any
       misunderstandings made along the way.
    7. *Summative Assignment*: A comprehensive assignment to test the competency of students
    on the lesson material.
       - Assignments were designed to challenge the students to apply the techniques and concepts
       from the lesson to solve new problems, demonstrating their understanding of the material.

We have found that this combination of clear lesson outlines, coding submodules, interleaved
exercises and summative assignments allowed us to not only have a predictable structure to each
lecture, but also assure that lesson objectives were not only covered, but conveyed effectively
in order for students to complete both the exercises and assignments.

Each of our lectures built on skills and concepts that would ultimately allow students to work
on a final open-ended analysis of real open ecological data. With this goal in mind, we designed
lectures to provide the building blocks to manipulate, visualize and analyze any datasets
students may come across, including those used for the final projects.

[^1]: *A note on "live-coding".* Live-coding is a hands-on method of teaching coding where the
instructor shares their screen with the class and types all commands on their computer while
the group follows along. Live-coding has proven to be a very effective teaching technique as
it forces the instructor to go slowly and ensures that participants get to try out every
command being used. Furthermore, mistakes and errors are bound to happen.
It allows learners to experience common errors themselves and debug them in a supportive
environment, to explore variations on material as they go, and to immediately check their
understanding by trying things hands-on.



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
