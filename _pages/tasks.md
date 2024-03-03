---
layout: page
permalink: /tasks/
title: Tasks
description:
nav: true
nav_order: 5
---

This task is designed in a hierarchical fashion by chaining two subtasks and allowing participants to
either model the simple binary scenario or complete the entire pipeline by identifying a second binary
classification problem. That is, firstly, to detect whether a text contains a stereotype, and secondly,
whether the stereotype is expressed explicitly or implicitly:
{: style="text-align: justify;"}


This task is designed in a hierarchical fashion by chaining two subtasks and allowing participants to
either model the simple binary scenario or complete the entire pipeline by identifying a second binary
classification problem. That is, firstly, to detect whether a text contains a stereotype, and secondly,
whether the stereotype is expressed explicitly or implicitly:
{: style="text-align: justify;"}

- **Subtask 1, stereotype Identification**: This is a binary classification task the aim of which is to
  determine whether a comment or sentence contains at least one stereotype or none, considering the full
  distribution of labels provided by the annotators. This subtask follows the SemEval 2021 Task 12 (Uma
  et al., 2021) proposal about learning with disagreement, in which the authors state that there does not
  necessarily exist a single gold label for every sample in the dataset. This fact is particularly
  evident when multiple contradictory annotations arise at the data labeling stage due to “debatable,
  subjective, or linguistic ambiguity”. The actual gold label of this subtask is left as a proxy to
  determine the subset of comments that will be evaluated in the posterior subtask. Examples of instances
  with and without stereotype:
  {: style="text-align: justify;"}

  Stereotype: _Immigrants have more rights than us._

  No Stereotype: _The new government will reform the immigration law._

- **Subtask 2 (Optional), Implicitness Identification**: This subtask introduces a novel binary
  classification problem to determine whether the stereotype is manifested or latent within the text,
  that is, whether the stereotype is implicit or explicit. The added difficulty in this case is that
  implicit stereotypes are not directly expressed in the text, and a process of inference must be applied
  by the annotators. Moreover, there are different strategies in which an implicit stereotype can be
  coded, such as metaphors, irony and other figures of speech, evaluations of the in-group, and the
  overgeneralization of a social group from features of some of its members. For instance, an example of
  an implicit stereotype taken from our dataset is the sentence “We will end up being a minority in our
  own country”, in which the stereotype is expressed through an evaluation of the in-group. This subtask
  will be presented as a hierarchical binary classification problem. Examples of instances of explicit
  and implicit stereotypes:
  {: style="text-align: justify;"}

  Explicit: _Immigrants have more rights than us._

  Implicit: _We will end up being a minority in our own country._


## References

{: style="font-size: 12px; background-color: #9dd7d124; color: #336b85; padding: 10px; border-radius:
3px; font-family: monospace; text-align: justify"}

> Uma, A., Fornaciari, T., Dumitrache, A., Miller, T., Chamberlain, J., Plank, B., Simpson, E. & Poesio,
> M. (2021). ‘SemEval-2021 Task 12: Learning with Disagreements’. In Proceedings of the 15th
> International Workshop on Semantic Evaluation (SemEval-2021) (pp. 338-347). Association for
> Computational Linguistics. DOI:
> [https://doi.org/10.18653/v1/2021.semeval-1.41](https://doi.org/10.18653/v1/2021.semeval-1.41)
