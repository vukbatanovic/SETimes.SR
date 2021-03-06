# SETimes.SR: A reference training corpus of Serbian
This repository contains the SETimes.SR reference training corpus of Serbian, which has been annotated on the following levels:
* Document, sentence, and token segmentation
* Lemmas
* Parts of speech, morphosyntactic descriptors (MSDs), and morphosyntactic features, according to the MultextEast v5 (MTEv5) specification
* Syntactic dependency relations, parts of speech, and morphosyntactic features, according to the Universal Dependencies v2 (UDv2) specification
* Named entities, according to the IOB2 standard

## Annotation sources

The texts within SETimes.SR were taken from the [SETimes parallel corpus](http://opus.nlpl.eu/SETIMES.php), a multilingual parallel collection of news stories from the now defunct Southeast European Times news portal.
Document segmentation was introduced in a previous version of the SETimes.SR repository.
Sentence and token segmentation, lemmas, and MSD layers were taken from the [Regional Linguistic Data Initiative repository](https://github.com/uzh/reldi/tree/master/corpora).
UDv2 dependency relation layer was taken from the [UD Serbian repository](https://github.com/UniversalDependencies/UD_Serbian-SET).
Both the MTEv5 and the UD morphosyntactic features and POS tags were semi-automatically generated using the MTE - UD mapping and code available in this repository. The same mapping was also applied to the [hr500k corpus in Croatian](https://github.com/nljubesi/hr500k/).
The named entity annotation is newly added.

## Structure

The [SETimes.SR corpus file](https://raw.githubusercontent.com/vukbatanovic/SETimes.SR/master/set.sr.conll) is structured according to the CoNLL file format standard, with the following distribution of information across columns:
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

## Other formats
The SETimes.SR corpus is also available in several different formats on the Slovenian Research Infrastructure [CLARIN.SI repository](http://hdl.handle.net/11356/1200):
* TEI format
* Vertical format
* [NoSketch Engine interface](https://www.clarin.si/noske/run.cgi/corp_info?corpname=setimes_sr)
* [KonText interface](https://www.clarin.si/kontext/first_form?corpname=setimes_sr)

## References
If you wish to use the SETimes.SR corpus in your paper or project, please cite the following paper and resource references:

* **[SETimes.SR – A Reference Training Corpus of Serbian](http://www.sdjt.si/wp/wp-content/uploads/2018/09/JTDH-2018_Batanovic-et-al_SETimesSR-A-Reference-Training-Corpus-of-Serbian.pdf)**, Vuk Batanović, Nikola Ljubešić, Tanja Samardžić, in Proceedings of the Conference on Language Technologies & Digital Humanities 2018 (JT-DH 2018), pp. 11-17, Ljubljana, Slovenia (2018).

* Batanović, Vuk; Ljubešić, Nikola; Samardžić, Tanja and Erjavec, Tomaž, 2018, *Training corpus SETimes.SR 1.0*, Slovenian language resource repository CLARIN.SI, [http://hdl.handle.net/11356/1200](http://hdl.handle.net/11356/1200).

## Acknowledgement
Work on the SETimes.SR corpus was supported by the [Regional Linguistic Data Initiative](http://reldi.spur.uzh.ch/) (ReLDI) via the Swiss National Science Foundation grant no. 160501, and the Slovenian Research Infrastructure [CLARIN.SI](http://www.clarin.si/).

## License
[Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)](http://creativecommons.org/licenses/by-sa/4.0/)
