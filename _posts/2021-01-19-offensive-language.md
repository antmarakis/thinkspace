---
layout: post
title: Hate Speech Detection and Offensive Language
category: Paper Notes
---

The authors define hate speech as "language that is used to express hatred towards a targeted group or is intended to be derogatory, to humiliate, or to insult the members of the group". In some extreme cases, it can also include language that incites violence against a group, although limiting the definition to just these cases severely limits what constitutes hate speech.

A good chunk of pre-DL approaches include the development of vocabularies of offensive words. Classifying text as hate speech just when these words are included is not ideal, since a lot of times offensive words are used in everyday speech without negative connotations (for example, the use of the n-word by Afro-Americans). This type of language, even though offensive, does not constitute hate speech.

In this work they introduce a dataset where instead of a black-n-white labeling, more fine-grained labels are used: hate speech, offensive language, or neither. They try to push in a direction where context is taken into account when offensive language is used.

In a survey to combat anti-black hate speech on social media, researchers found that when speech was classified as hateful, in 86\% of the cases it is because an offensive word is used. Since social media posts contain offensive language and swear words, this is a challenging tasks.

Syntactic features help to identify the recipient of hate speech, and combinations of verbs and nouns are also indicative of hate speech (for example, 'kill' used in conjunction with 'Jews'). Some times features such as the identity/race of the author can be used to help with detection, but this information can often be unavailable or unreliable.

They created a dataset by querying Twitter using a set of offensive language words that have been marked as hate speech. The tweets were then annotated using crowd-sourcing. There was high inter-annotator agreement, although from the results we can see that some data may have been misclassified. For example, when a tweet quotes a slur, it may be classified as hate speech even though it is not. 

They tested some feature-based ML models such as Logistic Regression and Naive Bayes, achieving an F1-score of around 0.9. Around 40% of hate speech tweets were misclassified though. Seemingly, the model is biased towards classifying tweets as less offensive than humans.

Most tweets classified as actual hate speech contain multiple slurs. Interestingly, a lot of people *stand up* to hate speakers with more hate speech. Hate breeds hate and all that. Also, it seems that human coders treat misogynistic content as just offensive and not hate speech. On the other hand, a lot of offensive language was classified as hate speech because it contained multiple slurs. The models seem to be particularly susceptible to rap lyrics.

---
*Thomas Davidson et al. Automated Hate Speech Detection and the Problem of Offensive Language. 2017. arXiv: 1703.04009 [cs.CL]*
