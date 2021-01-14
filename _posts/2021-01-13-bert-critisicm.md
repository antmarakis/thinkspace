---
layout: post
title: BERT Critisicm - Comprehension of Natural Language Arguments
category: Paper Notes
---

A bit of an "old" one, but important in order to keep us grounded in our collective research direction.

BERT had suspiciously high accuracy on the Argument Reasoning Comprehension Task. It reached 77\%, while untrained human accuracy was at around 80\%. In the task, each item has a Claim, a Reason and two Warrants. The two warrants are conflicting and either support or disagree with the claim. The task is to identify the warrant that supports the claim, given the reason.

The rest of the models struggled to surpass a 60\% accuracy, while BERT got 77\%. The authors of the paper found this suspicious and investigated the results. In short, they found that BERT's impressive performance was based on specific statistical artefacts, like the presence of 'not' in a sentence, instead of actually inferring something useful from the text.

The authors investigated this further by augmenting the available dataset. Each item in the original dataset had the following properties: Reason, Claim, 2 Warrants, Correct Warrant. For each item, they added another one with the Claim negated and the Correct Warrant reversed. In that way, all text in Reason and the Warrants remains the same, but the Claim is the opposite. This nullifies statistical cues like `not', since text appears in both for and against examples.

In the new dataset, BERT performed much worse. From 77\%, it dropped down to 53\%. This means the new dataset is a more robust way of evaluating what the model is understanding.

The authors finally provided a method to identify statistical cues. In general, these include high-frequency words, like 'is' and 'do'.

---
*Timothy Niven and Hung-Yu Kao. \Probing Neural Network Comprehension of Natural Language Arguments". In: CoRR abs/1907.07355 (2019). arXiv: 1907.07355. url: http://arxiv.org/abs/1907.07355.*
