---
layout: post
title: Racial Bias in Hate Speech
category: Paper Notes
---

It is known that bias exists in hate speech datasets across many axes. In this work, the authors are investigating staple Twitter hate speech datasets for bias against African American English. They find that classifiers predict AAE as hate speech more often than White American English. This corroborates previous findings and our intuition that AAE has been labeled as hate speech disproportionately more often.

To identify AAE tweets, they make use of the popular Blodgett classifier. The terminology used to denote the AAE and WAE tweets is "black-aligned" and "white-aligned". The examined null hypothesis that there is no racial bias is that the classifier will label examples independently of the author's race. If the probability of assigning a class to an example is higher when the race of the author is black/white than white/black, then we can reject the null hypothesis. In that case, racial bias does exist. The authors expect that white-aligned tweets are more likely to use racist language since white people are more likely to be racist against black people than black people themselves are. The authors are also expecting to see no difference on the axis of sexism for the two examined ethnicities.

The authors show that there is a racial bias in datasets, with tweets from black authors being more likely to be hateful, offensive, or sexist, while white authors are more likely to be racist.

In the discussions section an interesting point is made about the use of the "n-word" in AAE. Supported by Waseem et al. (2018), they claim that in this case the word shouldn't be considered offensive and we shouldn't penalize African-Americans for using the term. I believe this debate is at the core of hate speech research: it is so very heavily dependent on context and world knowledge that it is impossible to tackle with current methods. What happens if a white user uses the term? What if they are quoting the term? This is such a fine point that it has caused paralysis among researchers in the area (and unsurprisingly so, for this is a daunting task).

---
Thomas Davidson, Debasmita Bhattacharya, and Ingmar Weber. 2019. [Racial bias in hate speech and abusive language detection datasets.](https://aclanthology.org/W19-3504/) In Proceedings of the Third Workshop on Abusive Language Online, pages 25–35, Florence, Italy. Association for Computational Linguistics.
