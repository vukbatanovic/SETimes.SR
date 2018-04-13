# SETimes.SR: Southeast European Times corpus in Serbian
This repository contains the newest version of the SETimes.SR corpus, which has been annotated on the following levels:
* Document, sentence, and token segmentation
* Lemmas
* Parts of speech, morphosyntactic descriptors (MSDs), and morphosyntactic features, according to the MultextEast v5 (MTEv5) specification
* Syntactic dependency relations, parts of speech, and morphosyntactic features, according to the Universal Dependencies v2 (UDv2) specification
* Named entities, according to the IOB2 standard

## Annotation sources

Document segmentation was introduced in a previous version of this repository.
Sentence and token segmentation, lemmas, and MSD layers were taken from the [Regional Linguistic Data Initiative repository](https://github.com/uzh/reldi/tree/master/corpora).
UDv2 dependency relation layer was taken from the [UD Serbian repository](https://github.com/UniversalDependencies/UD_Serbian-SET).
Both the MTEv5 and the UD morphosyntactic features and POS tags were semi-automatically generated using the MTE - UD mapping and code available in this repository. The same mapping was also applied to the [hr500k corpus in Croatian](https://github.com/nljubesi/hr500k/).
The named entity annotation is newly added.

## Structure

The SETimes.SR corpus file is structured according to the CoNLL file format standard, with the following distribution of information across columns:
1. Token index in the sentence
2. Token
3. Lemma
4. MTE part-of-speech tag
5. MTE morphosyntactic descriptor
6. MTE morphosyntactic features
7. _ (left empty to preserve formatting equivalence with the hr500k corpus, which contains older, non-UD dependency relation tags in this position)
8. UD dependency relation (head:label)
9. UD specific features (used to encode the SpaceAfter attribute)
10. Named entity tag

## References
TBA