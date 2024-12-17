---
layout: about
title: Home
permalink: /
subtitle: DETEction and classification of racial STereotypes in Spanish - Learning with Disagreement

profile:
  align: right
  image: # about.jpg
  image_circular: false # crops the image to make it circular
  more_info:

news: false # includes a list of news items
latest_posts: false # includes a list of the newest posts
selected_papers: false # includes a list of papers marked as "selected={true}"
social: false # includes social icons at the bottom of the page
---

{% include figure.html path="assets/img/wordcloud.png" class="img-fluid rounded z-depth-1 mx-auto d-block"%}

[📝 Read the Overview paper](http://journal.sepln.org/sepln/ojs/ojs/index.php/pln/article/view/6620)

The DETESTS-Dis task took place as part of
[IberLEF 2024](http://sepln2024.infor.uva.es/en/iberlef-en/), the 6th Workshop on Iberian Languages
Evaluation Forum at [SEPLN 2024 conference](http://sepln2024.infor.uva.es/en/front-page-english/),
held on September 24th, 2024 in Valladolid (Castilla y León, Spain).
{: style="text-align: justify;"}

One of the components that reinforce toxic and hateful speech are stereotypes. Understanding how they
emerge and spread is crucial for tackling this issue, since stereotypes are not always expressed
explicitly. The presence of stereotypes on social media and the need to identify and mitigate them is
leading to the development of systems for their automatic detection, especially in news comments. This
is, therefore, a new task that is attracting growing interest from the NLP community.
{: style="text-align: justify;"}

Here, we introduce the second edition of the [DETESTS task](https://detestsiberlef.wixsite.com/detests)
(Ariza-Casabona et al., 2022), which was first presented at IberLEF 2022. The aim of the new edition,
DETESTS-Dis, is to detect and classify **explicit and implicit stereotypes** in texts from social media
and comments on news articles, incorporating learning with disagreement techniques. Moreover,
participants will be given the gold standard or hard labels, as well as the **pre-aggregated labels**,
following the Learning with Disagreement paradigm (Uma et al., 2021; Leonardelli et al., 2023). The texts
consist of whole tweets (now known as X posts) published in response to verified racial hoaxes (a type of
fake news), and sentences extracted from comments on online news articles related to immigration, all in
Spanish.
{: style="text-align: justify;"}

## References

{: style="font-size: 12px; background-color: #9dd7d124; color: #336b85; padding: 10px; border-radius:
3px; font-family: monospace; text-align: justify"}

> Ariza-Casabona, A., Schmeisser-Nieto, W. S., Nofre, M., Taulé, M., Amigó, E., Chulvi, B., & Rosso, P.
> (2022). Overview of DETESTS at IberLEF 2022: DETEction and classification of racial STereotypes in
> Spanish. Procesamiento del lenguaje natural, 69, 217-228.
>
> Cabitza, F., Campagner, A., & Basile, V. (2023, June). Toward a perspectivist turn in ground truthing
> for predictive computing. In Proceedings of the AAAI Conference on Artificial Intelligence (Vol. 37,
> No. 6, pp. 6860-6868).
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
