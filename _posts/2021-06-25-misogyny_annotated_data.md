---
layout: post
title: Expert-Annotated Misogyny Dataset
category: Paper Notes
---

In this paper, a Reddit dataset annotated by trained experts is presented, alongside a hierarchical taxonomy of misogyny found online. The entries in the dataset take context into account, following conversation threads. They also annotate the specific span of the text that includes misogynistic content.

Targeted sampling was used, with the authors picking some known misogynistic subreddits. To balance the data bias towards specific terms being associated with misogynistic content, the authors also sampled text from random subreddits. Thus, certain keywords will appear in a general context as well as in a misogynistic one.

Labeling took place on three levels. First is a binary class (misogynistic and non-misogynistic), then granularity is added within each class, while finally labels such as "threatening language" are applied. For misogynistic content, the following labels are presented:

* Misogynistic Pejoratives: derogatory language terms against women
* Misogynistic Treatment: comments that advocate for dangerous or disrespectful actions against women
* Misogynistic Derogation: comments that imply that women are inferior
* Gendered Personal Attacks: attacks that are about the recipient's gender

For non-misogynistic content, the authors capture non-misogynistic personal attacks and counter speech (replies that counter abusive language) as well as neutral content.

Annotators were involved in the development of the definitions' hierarchy, and during the annotation phase, weekly meetings were held where annotation disagreements were hashed out with an expert PhD researcher as the intermediary. These meetings took place until a consensus was reached. For the binary task (first level), inter-annotator agreement was 0.48 both for Fleiss' Kappa and Krippendorf's Alpha, which is higher or at least on par with the other mentioned work. Kappa values for the granular misogynistic labels (level two) can be seen in the following table (as seen on the paper).

<img src="https://i.imgur.com/v1bhp22.png" width="50%">

As for the distribution of classes, 10\% are misogynistic, with the most prevalent subclasses being pejoratives and derogation (both at 4\%).

In their experiments, model performance was overall quite low. The best examined model is BERT with class weighting (to account for the low percentage of positive examples). This model scores a precision score of 0.38, while recall is at 0.5, F1 at 0.43 and accuracy at 89\%. In their error analysis, the authors found a lot of false positives. Mentions of women, even if they are not misogynistic, get classified as misogynistic.

---
Ella Guest, Bertie Vidgen, Alexandros Mittos, Nishanth Sastry, Gareth Tyson, and Helen Margetts. 2021. [An expert annotated dataset for the detection of online misogyny](https://www.aclweb.org/anthology/2021.eacl-main.114/). In Proceedings of the 16th Conference of the European Chapter of the Association for Computational Linguistics: Main Volume, pages 1336–1350, Online. Association for Computational Linguistics.
