---
layout: post
title: Stolen Probabilities
category: Paper Notes
---

In this paper, the inability of NNLMs to assign high probabilities to rare words in high-probability sentences (for example, to "America" in "United States of America") is examined. Here AWD-LSTMs are studied.

Words with larger embedding norm (that is, more frequent words) will be assigned higher probabilities relative to a less frequent word, even when the two words appear in similar contexts. The authors show that words on the convex hull of a group of words in the embedding space can achieve high probabilities, whereas words on the inside of the convex hull are bound by the probability of words *on* the convex hull.

The authors develop an approximation algorithm to find interior and non-interior words, with high precision and low recall. They extract the top 500 words for each set, according to their probability. On those 500-word sets, trigram probabilities are extracted. These trigram probabilities do not showcase the stolen probability effect.

In general, the difference between non-interior and interior words is much starker for NNLMs, showing that the average probability of interior words is on average lower in that setup. The authors show that ensembling the NNLM probabilities with models that do not exhibit the stolen probability effect improves performance substantially. The more the dimensions, the smaller this effect is (ie. higher probabilities in the interior).

---
*David Demeter, Gregory Kimmel, and Doug Downey. Stolen Probability: A Structural Weakness of Neural Language Models. 2020. arXiv: 2005.02433 [cs.LG].*
