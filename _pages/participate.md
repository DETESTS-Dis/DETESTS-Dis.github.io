---
layout: page
permalink: /participate/
title: How to participate
description:
nav: true
nav_order: 4
---



## System Description Papers

Participants will be required to provide a technical report including a brief description of their
approach, an illustration of their experiments, in particular techniques and resources used, and an
analysis of their results for their publication in the Proceedings of the task.
{: style="text-align: justify;"}

Technical reports will be published in IberLEF 2024 Proceedings at [CEUR-WS.org](CEUR-WS.org).

All system description papers will be part of the official IberLEF Proceedings that will be published at
CEUR-WS.org ([http://ceur-ws.org/HOWTOSUBMIT.html](http://ceur-ws.org/HOWTOSUBMIT.html)).
{: style="text-align: justify;"}

For these papers please consider the following indications:

- System description papers should be formatted according to the uniform 1-column CEURART style. Latex and Word templates can be found in: [http://ceur-ws.org/HOWTOSUBMIT.html#PREPARE](http://ceur-ws.org/HOWTOSUBMIT.html#PREPARE)

- The minimum length of a regular paper should be 5 pages. There is no maximum page limit.

- Papers must be written in English.

- Each paper must include a copyright footnote on the first page of each paper:

 ```tex
{\let\thefootnote\relax\footnotetext{
Copyright \textcopyright\ 2024 for this paper by its authors.
Use permitted under Creative Commons License Attribution 4.0 International (CC BY 4.0). 
IberLEF 2024, September 2024, Valladolid, Spain.}}
```

- Eliminate the numbering in the pages of the paper, if there is one, and make sure that there are no headers or footnotes, except the mandatory copyright as a footnote on the first page.

- Authors should be described with their name and their full affiliation (university and country). Names must be complete (no initials), e.g.  “Soto Pérez” instead of “S. Pérez”.

- Titles of papers should be in emphatic capital English notation, i.e., "Filling an Author Agreement by Autocompletion" rather than "Filling an author agreement by autocompletion".

- At least one author of each paper must sign the CEUR copyright agreement. Instructions and templates can be found at [http://ceur-ws.org/HOWTOSUBMIT.html](http://ceur-ws.org/HOWTOSUBMIT.html). The signed form must be sent along with the paper to the task organizers. **Important: it must be physically signed with pencil on paper.**

- Please cite the overview paper of DETESTS-Dis in your respective work. The overviews will appear in the SEPLN journal (volumen 73, Septiembre 2024). The reference will be **announced soon.**

- Please, check the papers for text reuse/plagiarism. We would like to stress this point as CEUR is quite strict about it. Any paper found with plagiarized content will be rejected without further consideration.

## Submission format

Teams will be allowed (and encouraged) to submit multiple runs (max. 3) for each subtask and type of labels (total max. of 12 runs).
{: style="text-align: justify;"}

The submission format shall follow the examples provided in [data/sample](https://github.com/clic-ub/DETESTS-Dis/tree/main/data/sample).
[Examples.ipynb](https://github.com/clic-ub/DETESTS-Dis/blob/main/Examples.ipynb) shows how to transform the predictions to the appropiate format, as well as en example of the official evaluation metrics.
The participants should provide an output file in JSON format reporting:
- The name of the team
- The addressed subtask (t1 or t2)
- The use of _hard_ or _soft_ labels
- The ID of the run
{: style="text-align: justify;"}

For instance, if in the first run the team addresses the Subtask 1 with hard labels
the name of the file should be:
{: style="text-align: justify;"}

**TeamName_t1_hard_run1.json**

The ZIP file containing the relevant runs should be submitted till April 29th to the following email address:

**detests.iberlef@gmail.com**

## Google Group

We invite potential participants to subscribe to our
[Google Groups](https://groups.google.com/u/1/g/detests-dis) in order to be kept up to date with the
latest news related to the task. Please share comments and questions with the Google group. The
organizers will assist you for any potential issues that could be raised.
{: style="text-align: justify;"}
