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

**Subtask 2** is a binary hierarchical classification problem. We will use
  the **ICM metric** (Amigó and Delgado, 2022), an information theoretic based metric which
  considers both the hierarchical structure and the class specificity. It is applicable to both hard and
  soft labels. **The ICM metric will be the official metric considered for the ranking for both hard labels (ICM)
  and soft labels (ICM Soft).**
{: style="text-align: justify;"}

The implementation of the official metrics (F1, cross-entropy and ICM) will be based on [PyEvALL](https://github.com/UNEDLENAR/PyEvALL).
An example of the evaluation can be found in [Examples.ipynb](https://github.com/clic-ub/DETESTS-Dis/blob/main/Examples.ipynb).
{: style="text-align: justify;"}

For both subtasks 1 and 2, we will use non-informative baselines that classify all instances as either
the majority or the minority classes (all-ones and all-zeros). Furthermore, we also use a random
classifier, a Term Frequency-Inverse Document Frequency (TFIDF) with Support Vector Machine (SVM),
Fast Text embedding with SVM, and a fine-tuned BERT model (Cañete et al. 2020).
The baselines and code to produce them can be found at [clic-ub/DETESTS-Dis](https://github.com/clic-ub/DETESTS-Dis)
{: style="text-align: justify;"}

# Results

## Task 1 with Hard Labels

|   Rank |   | Run                        |   |    F1 |
|:-------|---|:---------------------------|---|------:|
|      0 |   | BASELINE_gold_standard     |   | 1.000 |
|      1 |   | Brigada Lenguaje_1         |   | 0.724 |
|      2 |   | I2C-Huelva_1               |   | 0.712 |
|      3 |   | I2C-Huelva_2               |   | 0.701 |
|      4 |   | EUA_2                      |   | 0.691 |
|      5 |   | EUA_3                      |   | 0.685 |
|      6 |   | BASELINE_beto              |   | 0.663 |
|      7 |   | EUA_1                      |   | 0.653 |
|      8 |   | UC3M-SAS_2                 |   | 0.641 |
|      9 |   | TaiDepZai999_UIT_AIC_1     |   | 0.630 |
|     10 |   | UC3M-SAS_1                 |   | 0.594 |
|     11 |   | BASELINE_all_ones          |   | 0.589 |
|     12 |   | BASELINE_beto_2_models     |   | 0.589 |
|     13 |   | VINE Bias Busters_1        |   | 0.581 |
|     14 |   | VINE Bias Busters_2        |   | 0.552 |
|     15 |   | VINE Bias Busters_3        |   | 0.545 |
|     16 |   | I2C-Huelva_3               |   | 0.375 |
|     17 |   | BASELINE_tfidf_svc         |   | 0.297 |
|     18 |   | BASELINE_random_classifier |   | 0.297 |
|     19 |   | BASELINE_fast_text_svc     |   | 0.297 |
|     20 |   | BASELINE_all_zeros         |   | 0.000 |

<br><br>

## Task 1 with Soft Labels

|   Rank |   | Run                    |   |   Cross Entropy |
|:-------|---|:-----------------------|---|----------------:|
|      0 |   | BASELINE_gold_standard |   |           0.255 |
|      1 |   | UC3M-SAS_1             |   |           0.841 |
|      2 |   | EUA_2                  |   |           0.850 |
|      3 |   | UC3M-SAS_2             |   |           0.865 |
|      4 |   | BASELINE_beto          |   |           0.893 |
|      5 |   | Brigada Lenguaje_1     |   |           0.938 |
|      6 |   | Brigada Lenguaje_2     |   |           0.979 |
|      7 |   | EUA_3                  |   |           1.081 |
|      8 |   | EUA_1                  |   |           1.409 |

<br><br>

## Task 2 with Hard Labels

|   Rank |   | Run                        |   |    ICM |   |   ICM Norm |
|:-------|---|:---------------------------|---|-------:|---|-----------:|
|      0 |   | BASELINE_gold_standard     |   |  1.380 |   |      1.000 |
|      1 |   | BASELINE_beto              |   |  0.126 |   |      0.546 |
|      2 |   | EUA_2                      |   |  0.065 |   |      0.524 |
|      3 |   | EUA_3                      |   |  0.061 |   |      0.522 |
|      4 |   | EUA_1                      |   |  0.045 |   |      0.516 |
|      5 |   | Brigada Lenguaje_1         |   | -0.240 |   |      0.413 |
|      6 |   | BASELINE_tfidf_svc         |   | -0.275 |   |      0.400 |
|      7 |   | I2C-Huelva_1               |   | -0.328 |   |      0.381 |
|      8 |   | BASELINE_fast_text_svc     |   | -0.412 |   |      0.351 |
|      9 |   | BASELINE_all_zeros         |   | -0.797 |   |      0.211 |
|     10 |   | BASELINE_random_classifier |   | -1.056 |   |      0.117 |
|     11 |   | BASELINE_all_ones          |   | -1.210 |   |      0.061 |
|     12 |   | I2C-Huelva_3               |   | -1.263 |   |      0.042 |
|     13 |   | I2C-Huelva_2               |   | -1.403 |   |      0.000 |
|     14 |   | UC3M-SAS_2                 |   | -2.103 |   |      0.000 |

<br><br>

## Task 2 with Soft Labels

|   Rank |   | Run                    |   |   ICM Soft |   |   ICM Soft Norm |
|:-------|---|:-----------------------|---|-----------:|---|----------------:|
|      0 |   | BASELINE_gold_standard |   |      4.651 |   |           1.000 |
|      1 |   | EUA_3                  |   |     -0.900 |   |           0.403 |
|      2 |   | EUA_1                  |   |     -0.917 |   |           0.401 |
|      3 |   | EUA_2                  |   |     -0.969 |   |           0.396 |
|      4 |   | BASELINE_beto          |   |     -1.124 |   |           0.379 |
|      5 |   | UC3M-SAS_2             |   |     -1.250 |   |           0.366 |
|      6 |   | Brigada Lenguaje_1     |   |     -1.684 |   |           0.319 |

<br><br>

## References

{: style="font-size: 12px; background-color: #9dd7d124; color: #336b85; padding: 10px; border-radius:
3px; font-family: monospace; text-align: justify"}

> Amigó, E., & Delgado, A. (2022, May). Evaluating extreme hierarchical multi-label classification. In
> Proceedings of the 60th Annual Meeting of the Association for Computational Linguistics (Volume 1: Long
> Papers) (pp. 5809-5819).
>
> Cañete, J., Chaperon, G., Fuentes, R., Ho, J. H., Kang, H., & Pérez, J. (2020). Spanish pre-trained
> bert model and evaluation data. In PML4DC at ICLR 2020.
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
