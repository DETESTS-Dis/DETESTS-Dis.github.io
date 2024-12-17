---
layout: page
permalink: /corpus/
title: Corpus
description:
nav: true
nav_order: 6
related_publications: true
---

[README.md](https://github.com/clic-ub/DETESTS-Dis/blob/main/README.md)

[The corpus is now available on HuggingFace](https://huggingface.co/datasets/CLiC-UB/DETESTS-Dis)

The DETESTS-Dis dataset consists of two text genres: comments on news articles (DETESTS) and posts on
Twitter reacting to hoaxes (StereHoax-ES) about the integration of immigrants.

## DETESTS

<style>
  p {
    text-align: justify;
  }
</style>

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        <p>The <b>DETESTS dataset</b> was released for the
        <a href="https://detestsiberlef.wixsite.com/detests" target="_blank">DETESTS competition at IberLEF 2022</a>
        (Ariza-Casabona et al., 2022).
        It is made up of two parts: one part from the NewsCom-TOX corpus (Taulé et al., 2021) and another
        part from the StereoCom corpus, which was specially created for DETESTS following the same methodology as
        NewsCom-TOX. Both corpora consist of comments published in response to different articles extracted from
        Spanish online newspapers (ABC, elDiario.es, El Mundo, NIUS, etc.) and discussion forums (such as
        Menéame). In the case of NewsCom-TOX, the comments were extracted from news articles published from
        August 2017 to August 2020, while in the case of StereoCom they date from June 2020 to November 2021.</p>
        <p>NewsCom-TOX articles were manually selected considering their controversial subjects, their potential
        toxicity and the number of published comments (minimum 50 comments). A keyword-based approach was used to
        search for articles mainly related to racism and xenophobia. Since the NewsCom-TOX corpus was designed
        primarily to study toxicity and not stereotypes, we used only the part of the corpus with the highest
        percentage of stereotypes. In order to obtain a sufficient and balanced data volume in terms of the
        presence or absence of stereotypes, the StereoCom corpus was also collected with the same content (i.e.,
        comments in response to immigration-related news items in Spanish digital media), selected by subject on
        the basis of a keyword search.</p>
        <p>The comments were selected in the same order in which they appear in the temporal web thread, and in
        reference to the conversational thread. The author (pseudo-anonymized) and the timestamp of the comment
        were also retrieved. Each comment was segmented by punctuation into sentences, and the comment to which
        every sentence belongs and its position within the comment are indicated.</p>
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/image1.png" class="img-fluid rounded z-depth-1 mx-auto d-block" width="400"%}
    </div>
</div>

For each sentence, two features were annotated, namely the presence or absence of stereotypes, and the
implicitness of the message, i.e., whether the stereotype is expressed explicitly or implicitly. The
features "Stereotype" and "Implicitness" have binary values (0=absence of the feature and 1=presence of
the feature). Each comment was annotated in parallel by three annotators with a moderate inter-annotator
agreement of 0.57 on the presence of stereotypes and of 0.41 for the implicit forms. For the aggregated
form of this dataset, the cases of disagreements were discussed by the annotators and a senior annotator
until agreement was reached in its aggregated form. This dataset will also be released in its
disaggregated form to give the opportunity to participants to carry out their experiments, taking into
account the disagreement among annotators. The team of annotators involved in the task consisted of two
expert linguists and two trained annotators, who were students of linguistics. 
{: style="text-align: justify;"}

At present, the corpus consists of 3,306 sentences from NewsCom-TOX and 2,323 sentences from StereoCom,
for a total of 5,629 annotated sentences. On average, 40% of the sentences contain a stereotype. This
dataset will be increased with 1,100 additional sentences from new comments extracted from online news
articles collected in 2023 in order to balance the test set for textual genre. 
{: style="text-align: justify;"}

## StereoHoax-ES

The **StereHoax-ES dataset** contains tweets retrieved from Twitter in 2021 reacting to hoaxes published
online that aim to disseminate false news against immigrants in Spain. These tweets were collected also
taking into account their conversational thread. From 449 conversational heads, we retrieved a total of
5,349 tweets. 
{: style="text-align: justify;"}

This corpus was created within the framework of the
[STERHEOTYPES project](https://www.irit.fr/sterheotypes/) (Bourgeade et al., 2023), which brings together
international research units based in Italy, France, and Spain. The corpus used for the second edition of
DETESTS is the Spanish part of the StereHoax multilingual dataset. 
{: style="text-align: justify;"}

The collection of these tweets started with the manual identification of 72 anti-immigrant hoaxes on
debunking websites like maldita.es and newtral.es. Using the titles, keywords, and contents of the
hoaxes, we searched for them on Twitter using the Twitter APIs v2 for Academia, collecting conversations
related to them. The conversational thread is represented by a conversational head (the tweet starting
the conversation), direct replies and replies to replies. 
{: style="text-align: justify;"}

The annotation of these tweets focuses on the identification of the presence of stereotypes in the tweet,
also looking at the conversational context (represented by the conversational head and, if they exist,
the direct replies). The annotators have also labeled whether the stereotype expressed in the text is
implicit or explicit. The annotation process involved three annotators (two linguistics students trained
for this task and a researcher) with a substantial agreement on the presence of stereotypes (0.75) and a
slight agreement on implicitness (0.15). For the aggregated form of this dataset, the cases of
disagreements were discussed; however, this corpus will also be released in its disaggregated form like
the DETESTS dataset. 
{: style="text-align: justify;"}

## Provided data

We will provide participants with 82% of the DETESTS-Dis dataset to train their models, while the
remaining 18% will be used to test them. The training set will consist of the following columns: 
{: style="text-align: justify;"}

- _source_ = {"detests", "stereohoax"}
- _id_ = unique identifier
- _comment_id_ = comment identifier
- _text_ = sentence or tweet
- _level1_ = previous sentece, refers to "id" (only if source="detests")
- _level2_ = previous tweet or comment, refers to "comment_id"
- _level3_ = first tweet or comment, refers to "comment_id"
- _level4_ = news text or racial hoax, refers to "id" column in "level4.csv" table.
- _stereotype_a1_ = individual annotation
- _stereotype_a2_
- _stereotype_a3_
- _stereotype_ = majority voting (hard label)
- _stereotype_soft_ = softmax normalization (soft label)
- _implicit_a1_
- _implicit_a2_
- _implicit_a3_
- _implicit_
- _implicit_soft_

The test set will have: _source_, _id_, _comment_id_, _text_, _level1_, _level2_, _level3_, _level4_.

_level1_ to _level4_ columns can be used as wanted to provide the models with different kinds of context.

Given the restrictions posed by EU GDPR regulations and to avoid any conflict with the sources of the
comments regarding their intellectual property rights (IPR), both training and test data are made
available for academic purposes only, and participants therefore will access the data with a password by
filling in an online form published on the task website, and by accepting the
[task's terms and conditions](https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode), including the
commitment not to redistribute the dataset. It is important to note that user data is not disclosed,
since all data will be anonymized by removing all personal information such as @user and generating new
IDs for the texts coming from Twitter. 
{: style="text-align: justify;"}

## References

{: style="font-size: 12px; background-color: #9dd7d124; color: #336b85; padding: 10px; border-radius:
3px; font-family: monospace; text-align: justify"}

> Ariza-Casabona, A., Schmeisser-Nieto, W. S., Nofre, M., Taulé, M., Amigó, E., Chulvi, B., & Rosso, P.
> (2022). Overview of DETESTS at IberLEF 2022: DETEction and classification of racial STereotypes in
> Spanish. Procesamiento del lenguaje natural, 69, 217-228.
>
> Bourgeade, T., Cignarella, A. T., Frenda, S., Laurent, M., Schmeisser-Nieto, W., Benamara, F., Bosco,
> C., Moriceau, V., Patti, V., & Taulé, M. (2023). A Multilingual Dataset of Racial Stereotypes in Social
> Media Conversational Threads. In Findings of the Association for Computational Linguistics: EACL 2023
> (pp. 674-684).
>
> Taulé, Mariona, Alejandro Ariza, Montserrat Nofre, Enrique Amigó, Paolo Rosso (2021). ‘Overview of the
> DETOXIS Task at IberLEF-2021: DEtection of TOXicity in comments In Spanish’, Procesamiento del Lenguaje
> Natural, 67: 209-221.
