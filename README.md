> **NOTE**: If there is anything missing, incomplete, or which you'd simply like to know more about, [PLEASE open an issue](https://github.com/openscialliance/Aug-12-Faculty-Teaching-Workshop/issues)!

# Faculty Fellows Teaching Workshop

Materials for the Aug 12 Faculty Fellows teaching workshop. This is meant as a guide to help you determine what topics and/or practices around Open Science you might want to include in your course.

It's organized to include "Basics" (the fundamental Open Science topics that are relevant to any and all fields), "Intermediate" (some field-specific resources), and "Advanced" (if you want to completely overhaul how you teach your course).

## Basic

This is as course- and field-agnostic as possible and deals with the fundamentals of Open Science. Check out [Dr. Quinn's slides on Open Science](https://github.com/quinngroup/openscience-intro-oct2019) from multiple guest lectures on the topic in 2019.

### Code

Repositories (e.g., [GitHub](https://github.com/), [GitLab](https://gitlab.com/), [BitBucket](https://bitbucket.org/)) are a necessary step here. This is probably the most well-known and well-practiced of the pillars of Open Science.

Other ancillary elements that improve the quality, readability, and useability of code include adopting formal versioning processes like [GitLab Flow](https://docs.gitlab.com/ee/topics/gitlab_flow.html). This makes it easier for a community to form around and engage with your code.

### Data

Public data repositories
 - https://www.kaggle.com/datasets
 - https://registry.opendata.aws/
 - https://opendata.cern.ch/
 - https://datahub.io/
 - [CyVerse Data Commons](https://datacommons.cyverse.org/)
 - [Zenodo](https://zenodo.org/)

Very important to consider: how are the data collected? How are the data preprocessed? [Gender Shades](http://gendershades.org/) study looked at bias in both data collection and data modeling in the context of facial recognition. Dr. Timnit Gebru is one of the leading researchers in fairness and ethics in machine learning.

### Methods

Study preregistration:
 - https://www.cos.io/initiatives/prereg
 - https://help.osf.io/article/145-preregistration

Some publication venues are partnering with preregistration entities to guarantee publication of preregistered studies *regardless* of their outcome.

### Review

Open review (often on GitHub or similar).

[JOSS](https://joss.theoj.org/) or [OpenReview](https://openreview.net/).

### Access

Pre-publication or preprint servers.

![preprints](https://miro.medium.com/max/969/1*6xg-0fcUtAWU98eGdkPH4A.jpeg)

Open Access journals (beware predatory journals) or open access options through more traditional journals (beware large fees).

### Education

Making all course materials available through a GitHub repo (examples: https://github.com/eds-uga).

Setting up course websites with [Jupyter Book](https://github.com/executablebooks/cookiecutter-jupyter-book).

Submitting your course materials to [JOSE](https://jose.theoj.org/about).

Licensing is an important consideration when posting open materials, and especially when making use of other materials. [GitHub has a great overview of licenses](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository) (and a [flowchart](https://choosealicense.com/) for choosing a license!), but it's good to be familiar with the basics.

## Intermediate

### Jupyter notebook slides

Dr. Quinn [used these in the Open Science Fellowship kickoff event](https://github.com/openscialliance/July-18-2022-Fellowship-Kickoff) in July 2022. Jupyter notebooks can be exported as static HTML slides that are readable by web browsers. Additional plugins such as [RISE](https://rise.readthedocs.io/en/stable/) will make the code in your slides live as you are presenting, so you can modify and re-run the code in the slides while talking without having to re-export the slides. The notebook can also be exported in additional formats such as PDF and LaTeX.

### Educational resources

Non-profits like [2i2c](https://2i2c.org/) and [CyVerse](https://cyverse.org/) have recently been making concerted efforts in the educational and research space, making cloud environments specifically for academics and students, with an emphasis on open and reproducible work. Each of these have free services available to anyone with academic credentials.

(OSA is actually partnering with CyVerse on the offering of workshops down the road!)

## Advanced

If you want to completely overhaul how you teach your course to put Open Science front and center, you've come to the right place.

### JupyterHub (and similar) for live, hosted content

[JupyterHub](https://jupyterhub.readthedocs.io/en/stable/) is a centralized hub platform for multi-user Jupyter environments. Each user can log into a central authentication hub, and from there "spin up" their own in-browser Jupyter notebook that is isolated from all the other users. In this way, the administrators can precisely set the environments that all the users will use, and the users can operate fully-fledged Jupyter environments without installing anything other than a web browser.

![jupyterhub schematic](https://jupyterhub.readthedocs.io/en/stable/_images/jhub-fluxogram.jpeg)

Dr. Quinn has used JupyterHub to teach many classes so far:
 - CSCI 1360: [Summer 2016](https://eds-uga.github.io/csci1360e-su16/), [Fall 2016](https://eds-uga.github.io/csci1360-fa16/), [Summer 2017](https://eds-uga.github.io/csci1360e-su17/), [Summer 2018](https://eds-uga.github.io/csci1360e-su18/)
 - CBIO 4835/6835: [Spring 2017](https://eds-uga.github.io/cbio4835-sp17/), [Fall 2018](https://eds-uga.github.io/cbio4835-fa18/), [Spring 2020](https://eds-uga.github.io/cbio-x835-sp20/)

Full listing: https://github.com/eds-uga

JupyterHub has numerous plugins that can also help with education, including [nbgrader](https://nbgrader.readthedocs.io/en/stable/), an autograder plugin. Dr. Quinn has used this in all the above classes as well. It provides an entire interface for instructors to design assignments, include automated tests, and disseminate these assignments to students with due dates. The students can then run the tests against their assignments before submitting to gain valuable feedback, and the submitted assignments are automatically graded according to rubricks the instructors set up when the assignment is designed. Late penalties can also be automatically imposed.

With some [slight modifications](https://github.com/eds-uga/nbgrader-scripts), Dr. Quinn has also used nbgrader for timed remote exams. This is not a part of core nbgrader functionality, but requires only a tiny modification in how the assignments are released to students.

Articles and websites on Jupyter-based teaching:
 - https://lorenabarba.com/news/jupyter-based-courses-in-open-edx-authoring-and-grading-with-notebooks/
 - https://cooperrc.github.io/philosophy.html
 - https://tutorials.weshareresearch.com/

[mybinder](https://mybinder.org/) is a platform that can convert any (public) GitHub repository to an in-browser Jupyter notebook. This functions very similar to JupyterHub, except the environments are now public GitHub repos. Owners of the repos can specify the exact environment for mybinder to build, and anyone who executes this on mybinder is presented with their own isolated sandbox environment. Advanced students could potentially build their own environments using GitHub as well.

[AutoLab](https://autolabproject.com/) is an open source project out of Carnegie Mellon University that is a full replacement for eLC. It is not related to the Jupyter ecosystem, and it is substantially more complex than Jupyter-based teaching infrastructure, but consequently is infinitely more flexible.

Dr. Quinn has used AutoLab for his [CSCI 8360 courses](https://dsp-uga.github.io/). The key bit of AutoLab functionality is its robust autograder. Whereas nbgrader+Jupyter essentially uses "hidden cells" in the Jupyter notebook to execute unit tests against the code that is written by the students, AutoLab executes entire containerized testing environments against the submitted code. Hence, it can accept any program format as input, and run any kind of tests against it that can be programmed/scripted, in fully isolated environments with completely customized setup. This is exponentially more complicated, but is extremely useful when the submitted projects are complex machine learning models that have to be tested against hidden datasets ([a la Kaggle](https://www.kaggle.com/)).
