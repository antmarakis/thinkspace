---
layout: post
title: Lipstick on a Pig - Evaluation of Gender Debiasing Methods
category: Paper Notes
---

The authors evaluate gender debiasing methods on a series of proposed experiments, showing that gender bias is not removed but is instead still hidden in word embeddings. The two evaluated methods reduce the projection of words on a gender direction, either via post-processing or during training. These methods are shown to only reduce bias of certain words, while the biased relationships between words still remain.

First, the authors employ a clustering method to cluster together the top-500 most biased words as male and female. Clusters align with actual gender bias 99.9% of the time. After debiasing, this number is down to 92.5% with one method and down to 85.2% with the other. This shows that whereas bias for individual words is reduced, biased words are still neighbors of other biased words.

Finally, the authors train an SVM classifier to predict gender of words based only on representation. Before debiasing, accuracy is at 98%, after debiasing accuracy is at 88% and 96%.

Thus, the authors show that these pioneering methods in gender debiasing only work on a shallow level.

---
Hila Gonen and Yoav Goldberg. "Lipstick on a Pig: Debiasing Methods Cover up Systematic Gender Biases in Word Embeddings But do not Remove Them". In: Proceedings of the 2019 Conference of the North American Chapter of the Association for Computational Linguistics, url: https://aclanthology.org/N19-1061.
