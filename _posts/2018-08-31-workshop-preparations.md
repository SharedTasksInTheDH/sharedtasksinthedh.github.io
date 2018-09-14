---
layout: post
title: "Workshop Preparations"
mtitle: "Workshop Preparations"
author:
- reiter
lang: en
phase: 1
add_to_menu: true
index: 141
indent: 1
excerpt: "This post outlines our plans for the upcoming workshop. It includes a first look at (not yet finalized) agenda and describes what material we generate beforehand, and how."
logo: 
  url: /assets/generic/hamburg-1593827_1920.jpg
---

On September 17 to 19, most of the participating teams in the shared task will be in Hamburg for a three-day workshop to discuss their guidelines and evaluate them in a collaborative way. This is the first time (to our knowledge) that annotation guidelines for the same phenomenon are evaluated in a (mild) competitive way.

## Agenda

While we are still finalizing the details of the agenda, the overall structure is as follows: We take the Monday afternoon to **familiarize us with the guidelines**. This includes a very brief presentation of the guideline authors covering the main ideas of their guidelines (e.g., what theoretical basis they follow, or what the most important issues/ideas are in the making of the guidelines). We will then form small working groups to identify similarities, discrepancies and general issues with each guideline.

On Tuesday, we will have a **structured look at each guideline** individually. To this end, we first discuss evaluation criteria in the three dimensions coverage (of theoretical claims), applicability (on new texts), and usefulness (for either subsequent text analysis steps or literary analysis). We have outlined our ideas on the evaluation in [this post]({% post_url 2018-05-23-evaluation-of-guidelines %}). Although the questionnaire outlined in the post needs to be approved by the participants, each guideline will receive points for each question. We will also discuss the achieved inter-annotator agreement on Tuesday.

Wednesday is reserved for **determining one or more winner guidelines**, and possibly to identify guidelines that are to be merged (for use in Phase 2). Finally, we will determine the next steps and reflect on the workshop itself.

## Material

We also have prepared a lot of material to allow the groups to prepare for the workshop. First of all, all annotations of the evaluation data have been made accessible to all teams. Each guidelines has been used three times (during the summer): By the guideline authors themselves (own), by one other participating team (foreign) and by one (paid) research assistant from the Digital Humanities or Computational Linguistics master's programs at Stuttgart University (student). This means that each team is now able to inspect what other annotators, with different levels of familiarity with the subject annotated.

Next to the annotations, we provide tables showing the inter annotator agreement for each text between all three annotations and every pair. As metric, we opted for γ (gamma), as proposed by Mathet et al. (2015). The main reason for this is that the metric makes very little assumptions on the annotations, and includes both unitizing and categorizing. Luckily, we were able to use [an implementation](https://gamma.greyc.fr) provided by the [GREYC lab](https://www.greyc.fr). There is a newer version that can be used on the command line. These tables provide interesting insights, but we will not share them publicly (yet), because the IAA is only of the dimensions we are interested in.


## Participants

All in all, there will be 15 participants at the workshop, and all but one guideline submissions are represented. We are looking forward to meeting the participants and to having an exciting workshop!

## Acknowledgements

The workshop is generously supported by the [Volkswagen foundation](https://www.volkswagenstiftung.de) as [part of the "Mixed Methods in the Humanities?"-initiative](https://portal.volkswagenstiftung.de/search/projectDetails.do?ref=94642). The Stuttgart annotators have been paid by the [Center for Reflected Text Analytics (CRETA)](https://www.creta.uni-stuttgart.de).

## Appendix

### Formatting

It was not a trivial thing to decide on a format to represent the annotations. The way we encode them has to cope with small or long spans, should allow for overlapping, but not including annotations, and should be extensible with attributes. In addition, we want to be able to render the annotations easily in markdown, LaTeX and HTML. In the end, we are using the format showing in the following example:

> [<sup>0</sup> [<sup>2</sup> ”Alas,” ]<sup>2</sup> said the mouse, [<sup>1</sup> ”the world gets smaller every day. At first it was so wide that I ran along and was happy to see walls appearing to my right and left, but these high walls converged so quickly that I’m already in the last room, and there in the corner is the trap into which I must run.”     ”But you’ve only got to run the other way,” ]<sup>1</sup> said the cat, and ate it. ]<sup>0</sup>

Each span is enclosed in square brackets, with a number shown both on the opening and closing bracket. If necessary, there is a footnote showing the attribute value assignments.

### Code to calculate IAA

The code to calculate the IAA got a bit more complex than anticipated, but it will be made available soon. In general, the workflow is as following: 

0. Annotations have been done in [CATMA](http://catma.de). We first export all annotations as TEI/XML files ("export annotations with text"). This is done manually.
1. Convert TEI/XML into two other formats: (this is done in Java, which is called by a bash script)
   - CSV: One line per span, with their token boundary and attributes. This is later used in the Gamma software.
   - LaTeX: Generate LaTeX source code to produce a PDF with the annotations for humans to read
2. Calculate inter annotator agreement: This is done by combining the annotations (own, foreign, and student) and then passing them to the Gamma software. This software produces a plain text file. Gamma is implemented in Java, and is called by a bash script.
3. Collect the IAA values from the plain text file and put them into tables. This step is implemented in Perl and writes markdown into a pipe, which is read by [pandoc](https://pandoc.org).
4. Run `xelatex` on the LaTeX files.

## References

Yann Mathet, Antoine Widlöcher, and Jean-Philippe Métivier. The unified and holistic method gamma (γ) for inter-annotator agreement measure and alignment. Computational Linguistics, 41(3):437–479, 2015.