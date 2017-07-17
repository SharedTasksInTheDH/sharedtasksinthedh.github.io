---
layout: post
title: A Shared Task for a Shared Goal — Systematic Annotation of Literary Texts
author:
- reiter
- gius
- strötgen
- willand
logo:
  url: /assets/generic/15383638574_240d9ff26e_m.jpg
  src:
    desc: "CC vickysandoval22"
    url: https://www.flickr.com/photos/115327016@N06/15383638574/
excerpt: The lack of systematic annotation for literary concepts is major roadblock for large-scale studies of literature. We propose to conduct a series of workshops inspired by *shared tasks* in NLP to foster the development of annotation guidelines for certain literary concepts. This in turn enables systematic annotation and development of automatisation options.
lang: en
---




## Preface
{:.no_toc}

This is the finally submitted version of the our abstract and will be published in the conference proceedings of DH 2017. It will also serve as the basis for our talk.

**We leave this page as it is, since it is identical to the abstract appearing in the Book of Abstract of DH 2017. However, some information on this page is no longer valid (e.g., the time plan).** 

## Contents
{:.no_toc}

* ToC
{:toc}

## Introduction

In this talk, we would like to outline a proposal for a *shared task* (ST) in and for the digital humanities. In general, shared tasks are highly productive frameworks for bringing together different researchers/research groups and, if done in a sensible way, foster interdisciplinary collaboration. They have a tradition in natural language processing (NLP) where organizers define research tasks and settings. In order to cope for the specialties of DH research, we propose a ST that works in two phases, with two distinct target audiences and possible participants.  

Generally, this setup allows both “sides” of the DH community to bring in what they can do best: Humanities scholars focus on conceptual issues, their description and definition. Computer science researchers focus on technical issues and work towards automatisation (cf. Kuhn & Reiter, 2015). The ideal situation, that  both “sides” of DH contribute to the work in both areas, this is challenging to achieve in practice. The shared task scenario takes this into account and encourages Humanities scholars without access to programming “resources” to contribute to the conceptual phase (Phase 1), while software engineers without interest in literature per se can contribute to the automatisation phase (Phase 2). We believe that this setup can actually lower the entry bar for DH research. Decoupling, however, does not imply strict, uncrossable boundaries: There needs to be interaction between the two phases, which is also ensured by our mixed organisation team. In particular, this setup does allow mixed teams  to participate in both phases (and it will be interesting to see how they fare).

In Phase 1 of a shared task, participants with a strong understanding of a specific literary phenomenon (literary studies scholars) work on the creation of annotation guidelines. This allows them to bring in their expertise without worrying about feasibility of automatisation endeavours or struggling with technical issues. We will compare the different annotation guidelines both *qualitatively*, by having an in-depth discussion during a workshop, and *quantitatively*, by measuring inter-annotator agreement, resulting in a community guided selection of annotation guidelines for a set of phenomena. The involvement of the research community in this process guarantees that heterogenous points of view are taken into account.

The guidelines will then enter Phase 2 to actually make annotations on a semi-large scale. These annotations then enter a “classical” shared task as it is established in the NLP community: Various teams competitively contribute systems, whose performances will be evaluated in a quantitative manner.

Given the complexity of many phenomena in literature, we expect the automatisation of such annotations to be an interesting challenge from an engineering perspective. On the other hand, it is an excellent opportunity to initiate the development of tools tailored to the detection of specific phenomena that are relevant for computational literary studies.

This talk has two purposes:
- To **discuss** these ideas and collect feedback and propositions. This is also an explicit invitation to contribute in the setup of this initiative. We are also welcoming a discussion about the phenomena that should be included.
- To **advertise** the idea of a shared task and to invite possible participants. The success of STs relies on a certain number of participants. Given that this has never been organized in den DH community before, we want to spread this idea into the community to gather estimates of potential participants.

## The Importance of Annotations
In computational literary studies, many phenomena cannot directly be detected from the text surface. To find and categorize such phenomena as, e.g., the "narrated time" in a novel, deep text understanding, knowledge about author or literary conventions, or historical  context knowledge are required. Therefore, instances of such phenomena need to be annotated either by human experts or software that is tailored to this task.

Unfortunately, many theories describing interesting phenomena are very difficult to apply to real texts. It has been shown numerous times (e.g., Reiter, 2015, Musi et al., 2016) that annotating theories or concepts directly can lead to very poor *inter-annotator agreement* (IAA): Different annotators interpret not only the text differently, but also descriptions of the theoretical concepts. While subjective annotations have their merit, studying annotations on large scale depends on their consistency, i.e., a high IAA. In addition, many theories are underspecified and examples for illustrations only. Creators of annotation guidelines often have to interpret what is meant by a certain statement and extend definitions to cover examples found in real texts.

Annotation guidelines serve as a mediator between a theory (that uses specialised vocabulary) and the annotators. Those guidelines often also contain re-appearing instance patterns and how they are to be annotated, or exceptions and typically a lot of examples from real texts (see below).

We see the **creation of annotation guidelines** as one of the cornerstones of large scale text analysis in computational literary studies. Additionally, it supports systematically disciplinary discussions about concepts and thus may lead to additional findings relevant for the theoretical discourse (e.g., Meister, 1995; Gius and Jacke, forthcoming). Experts from literary studies are predestined for working on annotation guidelines, as annotation of literary phenomena in literary texts can be seen as a special form of close reading.

## Phase One: Annotation Guidelines

### The Shared Task
In theory, any phenomenon can be addressed in this fashion, given that it can be defined inter-subjectively at all, is reasonably frequent and of interest in computational literary studies. As a starting point, we propose to address the issue of **narrative levels** (Pier, 2014). Narrative levels are a core concept in narrative theory (Genette, 1980; Bal, 1997) which in turn has shown to be a promising foundation for automatisation in literary theory (Bögel et al. 2015). The first reason for choosing narrative levels  is its ubiquity: every narrative text necessarily consists at least one, most texts contain many narrative levels; each element of a text can be assigned to a specific level. The second reason is our intuition that a definition of "level" in guidelines is as achievable as the automated detection of levels by computers.

Concretely, participating teams are asked to create guidelines for the detection and annotation of a) narrative levels and b) the relation of the narrator(s) to the narrated world (i.e., is the narrator part of the narrated world or not?). Participants are not bound to adhere to a specific narratological theory. The *result* of this phase, however, will be a fixation on a set of guidelines (that instantiate a theory).

We will select a number of literary narrative texts and provide copyright-free digitized corpora. All “official” texts (development and test sets) will be English literary texts. Extending this framework to other languages and/or phenomena is a natural thing to do as a second step.

### Evaluation

In NLP shared tasks, the predictions of the systems are compared against a fixed test set, the gold standard. Since there is no gold standard in Phase 1, we will evaluate the guidelines using an unseen data set. Each participating team annotates this set using their own guidelines, before submitting them. Submitted guidelines will be anonymized and re-distributed among the participants. Each participant is asked to annotate the evaluation data set using two other annotation guidelines. In addition, we will be collecting annotations from students.

The evaluation data set will thus be annotated according to each participant’s guidelines four times (1 x self, 1 x student,  2 x other participants).

This setup allows direct calculation of inter-annotator agreement. However, IAA should be only one aspect in evaluating the guidelines, but not the only one. Therefore, we will submit a workshop at DH 2018 to discuss the submissions and select final ones. This setup also allows merging different annotation guidelines as well as adaptations according to the discussion during the workshop. Soon after the workshop, Phase 2 will commence.

## Phase Two: Automatic Prediction
In Phase 2 of this endeavour, the selected guidelines of Phase 1 will be annotated on a large scale by student assistants. Since we currently do not know how long, complex and involved the guidelines will be, there should be a close communication between the organizers and the team responsible for the selected guidelines.

As soon as texts have been annotated, they will be made accessible to participants. For the deadline in Phase 2, participants will be asked to process a new data set -- one that has not been released before -- and return the predicted annotations to the organizers, who will then make evaluations using standard measures (e.g., accuracy). Finally, there will be a workshop in which each participating team presents its system. This workshop is projected to be coordinated with the LaTeCH workshop series, which has taken place at ACL conferences in the past years (one of the authors of this paper has been workshop organiser in the past years).

There will be no fixation on computational approaches, statistical models, programming languages or environments to tackle this problem. The main benefit of shared tasks towards automatisation is that different approaches can be compared directly. Restricting this possibility space would directly harm the goal.

## Technical Details and timeline
This proposal is innovative in a number of ways: Shared tasks are a new kind of framework in the DH/H community, duration and focalisation have not been investigated in this way before and last but not least, a shared task with the goal of creating annotation guidelines has not been organized before (to our knowledge). We believe it is more important to do this right than to do this fast and that is why we are looking at a rather lengthy timeline.

| Date | Event |
| ----- | ----- |
| August 2017 | Announcement talks at DH and LaTeCH-CLfL 2017 |
| November 2017 | Finalisation of Phase 1 details, submission for DH 2018, Call for participation (Phase 1) |
| April 2018 | Submission deadline for guidelines |
| June 2018 | Phase 1 workshop (DH) |
| August 2018 | Announcement talk for Phase 2 (LaTeCH 2018) |
| October 2018 | Finalisation of Phase 2 details, submission for ACL 2019, Call for participation (Phase 2) |
| May 2019 | Submission deadline for systems for Phase 2 |
| August 2019 | Phase 2 workshop (ACL/LaTeCH) |

Attracting enough participants is the main challenge from the organiser's perspective. The main incentive we envision for contributors are excellent publication opportunities: All submitted and generated materials will be published online (open access) under the umbrella of the shared task. Each individual work will be citable. This includes the submitted annotation guidelines, the produced consensus guidelines, and explanation and commentary documents.
In addition to the publication incentive, we believe that our approach is an important contribution towards systematic text analysis in the DH realm and count on the playfulness and curiosity (in a good way!) of the DH community to take part in this experiment.

## References

Mieke Bal. Narratology: Introduction to the Theory of Narrative. University of Toronto Press, 2 edition, 1997.

Thomas Bögel, Michael Gertz, Evelyn Gius, Janina Jacke, Jan Christoph Meister, Marco Petris and Jannik Strötgen. Collaborative Text Annotation Meets Machine Learning: heureCLÉA, a Digital Heuristic of Narrative. In DHCommons Journal, 2015. URL http://dhcommons.org/journal/issue-1/collaborative-text-annotation-meets-machine-learning-heurecl%C3%A9-digital-heuristic.

Gérard Genette. Narrative Discourse. An Essay in Method. Ithaca, N.Y: Cornell University Press, 1980.

Evelyn Gius and Janina Jacke. The Hermeneutic Profit of Annotation. On preventing and fostering disagreement in literary text analysis. International Journal of Humanities and Arts Computing, forthcoming.

Eduard Hovy and Julia Lavid. Towards a ‘science’ of corpus annotation: A new methodological challenge for corpus linguistics. International Journal of Translation Studies, 22(1), January 2010.

Jonas Kuhn and Nils Reiter. A Plea for a Method-Driven Agenda in the Digital Humanities. In Proceedings of Digital Humanities 2015, Sydney, Australia, June 2015.

Jan Christoph Meister. Consensus ex Machina? Consensus qua Machina! Literary and Linguistic Computing, 10(4), pages 263–270, 1995.

Elena Musi, Debanjan Ghosh, and Smaranda Muresan. Towards feasible guidelines for the annotation of argument schemes. In Proceedings of the Third Workshop on Argument Mining (ArgMining2016), pages 82–93, Berlin, Germany, August 2016. Association for Computational Linguistics. URL http://www.aclweb.org/anthology/W16-2810.

John Pier. Narrative Levels (revised version; uploaded 23 April 2014). In Peter Hühn et al., editors, the living handbook of narratology. Hamburg: Hamburg University. URL http://www.lhn.uni-hamburg.de/article/narrative-levels-revised-version-uploaded-23-april-2014

Nils Reiter. Towards annotating narrative segments. In Kalliopi Zervanou, Marieke van Erp, and Beatrice Alex, editors, Proceedings of the 9th SIGHUM Workshop on Language Technology for Cultural Heritage, Social Sciences, and Humanities (LaTeCH), pages 34–38, Beijing, China, July 2015. Association for Computational Linguistics, Association for Computational Linguistics. URL http://www.aclweb.org/anthology/W15-3705.

### Annotation Guidelines
Lynn Carlson and Daniel Marcu. Discourse tagging reference manual. Annotation Manual, University of Southern California, 2001. URL https://www.isi.edu/ marcu/discourse/tagging-ref-manual.pdf.

Lisa Ferro, Laurie Gerber, Inderjeet Mani, Beth Sundheim, and George Wilson. TIDES 2005
Standard for the Annotation of Temporal Expressions. Technical report, The MITRE
Corporation, 2005.

Evelyn Gius and Janina Jacke. Zur Annotation narratologischer Kategorien der
Zeit. Annotation Manual 2.0, Hamburg University, November 2016. URL http://heureclea.de/guidelines

Beatrice Santorini. Penn treebank: Part-of-speech tagging. Annotation Manual 3, University of Pennsylvania, 1992. URL ftp://ftp.cis.upenn.edu/pub/treebank/doc/tagguide.ps.gz.

Roser Sauri, Jessica Littman, Bob Knippen, Robert Gaizauskas, Andrea Setzer, and James Pustejovsky. TimeML Annotation Guidelines, Version 1.2.1. http://timeml.org/publications/timeMLdocs/annguide_1.2.1.pdf

William Styler, Guergana Savova, Martha Palmer, James Pustejovsky, Tim O’Gorman, and
Piet C. de Groen. THYME Annotation Guidelines. Technical report, 2014. http://clear.colorado.edu/compsem/documents/THYME_guidelines.pdf
