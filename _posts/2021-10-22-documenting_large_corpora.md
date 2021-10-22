---
layout: post
title: Documenting Large Webtext Corpora
category: Paper Notes
---

The Colossal Clean Crawled Corpus (C4) is a corpus curated for pretraining large language models. It is clean in that a set of filters was applied, from banning a list of offensive words to applying language detection (only keeping English examples). The authors here provide an extensive analysis of this corpus.

One of the main findings is that a lot of machine-generated text was found, for example through translations of patents. Also, a lot of content comes from patent websites themselves (the top website by far is patents.google.com, while patents.com is in the top 10), as well as US government websites (.gov and .mil, for the military). Other NLP datasets (including their test sets) were found in the corpus as well, mostly because the datasets were extracted from Wikipedia/IMDB/etc. or because they were uploaded on, for example, Github. Worryingly, since a lot of filters were keyword-based to remove text containing keywords from a list of banned words, text about and from African Americans and the LGBT+ community, among other communities, was filtered out.

In an analysis of metadata, the authors found that while 92\% of the documents were from the last decade (2010-2019), some of the documents date back to 1996. Also, around 50\% of the documents come from the US, followed by Germany and the United Kingdom.

As for demographic biases, it was found that in the corpus positive mentions of Hebrews were at 73\% while for Arabs it was 65\%. Further, mentions of sexual orientation were filtered out (both heterosexual and LGBT+), with approximately only 30\% of these mentions being actually offensive (after a manual inspection). Also, African and Hispanic English is filtered out at a disproportionate degree too (around 4 times more likely to be removed than White American English).

The authors also found that data from patents was not only the most prevalent, not only was it quite often translated from another language, but that originally some of this data came from OCR systems that could have potentially added further noise.

Finally, to increase transparency, the authors propose that data excluded via filtering should also be available for completion and to allow for further analysis.

---
Jesse Dodge, Maarten Sap, Ana Marasović, William Agnew, Gabriel Ilharco, Dirk Groeneveld, Margaret Mitchell, and Matt Gardner. 2021. [Documenting Large Webtext Corpora: A Case Study on the Colossal Clean Crawled Corpus](https://arxiv.org/abs/2104.08758), EMNLP 2021.
