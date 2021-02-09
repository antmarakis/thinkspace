---
layout: post
title: Words Are Windows to the Soul (Of News Spreaders)
category: Paper Notes
---

Alongside fake news text representation, the representations of users who spread these fake news can also be utilized in detection. It has been shown that users who share fake news also share some common characteristics. In this paper user representations are generated from the text these users produce and combined with the representation of news, providing an increase in detection accuracy. They also analyze language used by fake news spreaders and find that not only do they have a distinct focus of topics and emotions, but also typographic variations (eg. abnormal use of punctuation) to normal users. Their analysis takes place over the FakeNewsNet datasets (PolitiFact and GossipCop).

For user representations, both their tweets and descriptions are used. The model has two CNN-based modules, one for users and one for news. These two resulting representations are given to a one-layer feedforward network.

The authors experiment with providing the model only with news, only with user information and both. When providing both, performance is the best for CNNs. When provided only with user information, the model performance drops although not by that much.

An analysis of linguistic features is also presented. N-grams are categorized into multiple features, such as punctuation, pronouns, topics, proper names, etc. For topics, Negative Emotion and Death appear often in fake news, whereas for real news the most prominent topics are Government and Politics. For news spreaders, there seems to be little overlap between fake and real news spreaders. Fake news spreaders make use of similar vocabulary across both datasets, whereas real news spreaders do not. As with previous studies, fake news sharers use more punctuation marks, emotive language and first-person pronouns. Real news spreaders use more domain specific words. Finally, similarity between fake news and its spreaders is low, whereas it is higher for real news.

As an ablation study, they investigate whether echo chambers exist within spreader circles. They conjecture that the similarity between user representations drops the further away two users are in the social graph. This indeed seems to be the case, both for fake and real news spreaders.

---
*Marco Del Tredici and Raquel Fern´andez. \Words are the Window to the Soul: Languagebased User Representations for Fake News Detection". In: Proceedings of the 28th International Conference on Computational Linguistics. Barcelona, Spain (Online): International Committee on Computational Linguistics, Dec. 2020, pp. 5467{5479. url: https://www.aclweb.org/anthology/2020.coling-main.477.*
