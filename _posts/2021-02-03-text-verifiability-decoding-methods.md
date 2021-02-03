---
layout: post
title: How Decoding Methods Affect Generated Text Verifiability
category: Paper Notes
---

Work in the field of generated text analysis has focused on fluency and grammar. In this paper the accordance of generated text with real world knowledge is put to the test. It seems that the decoding method plays a major role in how verifiable text is. There is also a high correlation between repetitive text and verifiability. So, whereas top-k and nucleus sampling produce less repetitive text, that text is also less verifiable. The authors propose a decoding strategy that produces at the same time less repetitive and more verifiable text.

Text that is verifiable is text that can be either corroborated or refuted by a knowledge base (for example, Wikipedia).

Their decoding method is a hybrid of sampling and likelihood-maximization approaches. The first L tokens are generated with sampling and the rest with beam search. By tuning L they can hit a balance between the two approaches. Text is generated after given five tokens from a Wikipedia article.

Text can be verified (supported or refuted) or unverified. The authors measure both the number of supported sentences over all generated sentences, and the supported sentences out of all verified sentences. To counter duplication of text, only unique supports are counted. To measure repetitiveness, they employ two further metrics: distinct 4-grams and 4-gram overlap between human and machine-generated text. Human text is the first 256 tokens as found in the corresponding Wikipedia article.

To fact-check the statements, they make use of an off-the-shelf BERT-based model trained on FEVER. It is shown that likelihood approaches (like greedy or beam search) indeed produce more verifiable text (even though it is more repetitive). Their hybrid decoding approach achieves a good balance between repetitiveness and verifiability. Human evaluation was also carried out, and the results from the fact-checker model were corroborated.

---
*Luca Massarelli et al. "How Decoding Strategies Affect the Verifiability of Generated Text". In: Findings of the Association for Computational Linguistics: EMNLP 2020. Online: Association for Computational Linguistics, Nov. 2020, pp. 223{235. doi: 10.18653/v1/2020. findings - emnlp . 22. url: https://www.aclweb.org/anthology/2020.findings-emnlp.22*
