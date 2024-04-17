---
layout: page
permalink: /evaluation/
title: Evaluation & Results
description:
nav: true
nav_order: 7
---

**Subtask 1** will be evaluated as in the Le.Wi.Di shared tasks at
SemEval 2021 and 2023 about learning with disagreement (Uma et al. 2021 and Leonardelli et al. 2023).
First, the models that output hard labels will be compared to the gold standard by using the standard
classification metric **F1**. The second evaluation metric will be the **cross-entropy** between the system
soft label values and the soft labels generated from the annotators average votes.
{: style="text-align: justify;"}

**Subtask 2** is a binary hierarchical classification problem. Since the appropriateness of evaluation
metrics for such task is still an open issue, we will consider three metrics:

- The **ICM metric** (Amigó and Delgado, 2022), an information theoretic based metric which
  considers both the hierarchical structure and the class specificity. It is applicable to both hard and
  soft labels. **The ICM metric will be the official metric considered for the ranking for both hard labels (ICM)
  and soft labels (ICM Soft).**
- **Hierarchical F measure** (Costa et al. 2007), which combines for each sample (sentence/post) the
  precision and recall between label sets and their ancestors, only applicable to hard labels.
- **Propensity F-measure** (Jain et al. 2016), which combines for each sample (sentence/post) the
  precision and recall of label sets (without considering ancestors) with an additional factor to
  consider the specificity of classes (frequency), only applicable to hard labels.
{: style="text-align: justify;"}

The implementation of the official metrics (F1, cross-entropy and ICM) will be based on [PyEvALL](https://github.com/UNEDLENAR/PyEvALL).
An example of the evaluation can be found in [Examples.ipynb](https://github.com/clic-ub/DETESTS-Dis/blob/main/Examples.ipynb).
{: style="text-align: justify;"}

For both subtasks 1 and 2, we will use non-informative baselines that classify all instances as either
the majority or the minority classes (all-ones and all-zeros). Furthermore, we also use a random
classifier, a Term Frequency-Inverse Document Frequency (TFIDF) with Support Vector Machine (SVM), and a
fine-tuned BERT model (Cañete et al. 2020).
The baselines and code to produce them can be found at [clic-ub/DETESTS-Dis](https://github.com/clic-ub/DETESTS-Dis)
{: style="text-align: justify;"}

## References

{: style="font-size: 12px; background-color: #9dd7d124; color: #336b85; padding: 10px; border-radius:
3px; font-family: monospace; text-align: justify"}

> Amigó, E., & Delgado, A. (2022, May). Evaluating extreme hierarchical multi-label classification. In
> Proceedings of the 60th Annual Meeting of the Association for Computational Linguistics (Volume 1: Long
> Papers) (pp. 5809-5819).
>
> Cañete, J., Chaperon, G., Fuentes, R., Ho, J. H., Kang, H., & Pérez, J. (2023). Spanish pre-trained
> bert model and evaluation data. In PML4DC at ICLR 2020.
>
> Costa, E. P., Lorena, A. C., Carvalho A. C. P. L. F. & Freitas A. (2007). A review of performance
> evaluation measures for hierarchical classifiers. AAAI Workshop - Technical Report
>
> Jain, H., Prabhu, Y. & Varma, M. (2016). ‘Extreme multi-label loss functions for recommendation,
> tagging, ranking & other missing label application. In Proceedings of the 22ndACM SIGKDD International
> Conference on Knowledge Discovery and Data Mining, KDD ’16, pp. 935–944, New York, NY, USA. Association
> for Computing Machinery.
>
> Leonardelli, E., Uma, A., Abercrombie, G., Almanea, D., Basile, V., Fornaciari, T., Plank, B., Rieser,
> V., Uma, A., & Poesio, M. (2023). SemEval-2023 Task 11: Learning With Disagreements (LeWiDi). In
> Proceedings of the 17th International Workshop on Semantic Evaluation (SemEval-2023), pages 2304–2318.
> Association for Computational Linguistics.
>
> Uma, A., Fornaciari, T., Dumitrache, A., Miller, T., Chamberlain, J., Plank, B., Simpson, E. & Poesio,
> M. (2021). ‘SemEval-2021 Task 12: Learning with Disagreements’. In Proceedings of the 15th
> International Workshop on Semantic Evaluation (SemEval-2021) (pp. 338-347). Association for
> Computational Linguistics. DOI:
> [https://doi.org/10.18653/v1/2021.semeval-1.41](https://doi.org/10.18653/v1/2021.semeval-1.41)
