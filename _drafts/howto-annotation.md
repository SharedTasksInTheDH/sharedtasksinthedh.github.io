---
layout: post
title: "How to Develop Annotation Guidelines"
author:
- reiter
lang: en
excerpt: ""
logo: 
  url: /assets/generic/IMG_1693.jpg
phase: 1
excerpt: "This article describes where to start and how to proceed when developing annotation guidelines. It focuses on the scenario when you're creating new guidelines for a phenomenon that has been described mostly theoretically."
---

*This article describes where to start and how to proceed when developing annotation guidelines. It focuses on the scenario when you're creating new guidelines for a phenomenon that has been described mostly theoretically.*



Developing annotation guidelines is an iterative process: Once a first version is established, its shortcomings are to be identified and fixed, leading to a second version, which has shortcomings that need to be identified and fixed, etc. This process is displayed schematically in Figure 1. We will describe how to get create a first version, and how to come from one version to the next. The most important idea is that in each round, **a text is annotated by multiple annotators independently**. This is the main device that allows to identify these shortcomings.

<div><img src="{{ site.url }}/assets/generic/annotation-workflow.png" style="width:70%" alt="Flowchart depicting the general annotation workflow"/><p class="caption">Figure 1: General annotation workflow</p></div>

Please note that we don't make assumptions on whether the annotations are done on paper or digitally. Digital annotation tools make it easier to compare annotations, but are not better from a conceptual point of view. Paper-based annotations, however, make it easy (too easy) to skip over details, for instance the exact boundaries of annotations. It is important to pay attention to every detail even on paper.

## Making Pilot Annotations

The first round of annotations is best done by annotators who are familiar with the theory that is to be annotated. As with the following annotation rounds, please annotate in parallel and discuss afterwards. It is not necessary to spend a lot of time  on preparation. Specifying a list of references or theoretical works should be sufficient as a starting point. 

Your time is best spent on discussing annotation disagreements. In particular in the very first round, many parameters are still undecided and likely to cause disagreement. At the beginning, you need to focus on the big questions: 

- What is to be annotated? Every paragraph/sentence/word? Only paragraphs that fulfill a set of conditions?
- What exactly are the annotation categories? Are they related somehow? It sometimes helps to organize them in a hierarchy, as some categories subsume others (e.g., every *finite verb* is a *verb*).
- If you're using a digital annotation tool: Make sure annotators have the possibility to attach comments to annotations. It helps a lot in the discussions later.

Annotation guidelines typically also contain *a lot* of examples. So you best start collecting interesting/difficult/explanatory examples right away. Examples you find in real texts (possibly with some context) are usually advantageous over made-up ones.


## Improving Guidelines
To improve guidelines in this manner, we first need to analyze annotations of the previous "round", before we reformulate/refine the guidelines. This can be done by inspecting the *annotation disagreements*: These are cases in which different annotators made different decisions. Practically, there are two ways of analyzing these disagreements: By discussing them with the annotators, and by counting and inspecting them. 

A discussion with the annotators is fruitful in particular in the first few rounds of the process. Once the annotators are trained and annotation guidelines are maturing, a quantitative view might be sufficient. For the latter, a number of metrics have been established (see [Wikipedia: Inter-rater reliability](https://en.wikipedia.org/wiki/Inter-rater_reliability) for an overview; or Artstein, 2017). Analyzing the inter-annotator-agreement quantitatively gives you a number and allows comparison if you're actually improving your annotation guidelines, but it does not distinguish different kinds of disagreement, although there are reasons for wanting that.

Some of the disagreements will be caused by annotators not paying annotation, or by overlooking something -- annotators are human beings after all. These can be fixed easily, without the need to refine the guidelines. It is good practice to let the annotators fix these mistakes by themselves. 

Other kinds of disagreement can be expected to have impact on the guidelines: If two annotators made different decisions which are both covered by the annotation guidelines, it is likely that the annotation guidelines are contradictory in this aspect. The source of the contradiction should be identified and resolved. 

Many disagreements will be caused when the annotators encounter cases that are not mentioned in the guidelines. In this case, either an existing annotation definition can be applied (perhaps with minor changes), or a new one needs to be defined. 

While going through this iterative process, two process are likely to be intertwined: The annotation guidelines get better and the annotators get trained. Both are expected and, in principle, welcomed. But: In the end, the annotation guidelines are supposed to be self-contained and also applicable by untrained (or less trained) annotators. It is therefore important to pay attention not to develop rules within a project that are never written down. It will be much harder to integrate new annotators (even if someone drops out has to be replaced) unwritten rules exist.

## List of Annotation Guidelines

- Brunner
- TimeML

## References

Artstein, Ron. Inter-annotator Agreement. In: Ide Nancy & Pustejovsky James (eds.) *Handbook of Linguistic Annotation*. Springer, Dordrecht, 2017.
