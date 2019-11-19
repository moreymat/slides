
---

# Google Search et BERT

---
## L'annonce

Le 25 octobre 2018, Pandu Nayak (VP Google Search) annonce l'intégration de BERT à Google Search, qu'il qualifie de "changement le plus important dans les cinq dernières années".

L'utilisateur trouve plus facilement ce qu'il cherche lorsqu'il soumet :

* des requêtes longues

* des requêtes où les relations entre les mots sont importantes
  - prépositions ("pour", "vers")
  - négations ("non", "sans")

Ce changement affecterait les résultats d'1 requête sur 10, notamment sur les langues autres que l'anglais.

---
## Google Search avec ou sans BERT (1)

requête: "Parking on hill with no curb"

sans BERT: instructions pour stationner sur une colline **avec** une bordure de trottoir

avec BERT: lien qui conseille d'orienter les roues vers le trottoir

---
## Google Search avec ou sans BERT (2)

requête: "2019 brazil traveler to usa need a visa"

sans BERT: instructions pour les citoyens US voyageant au Brésil

avec BERT: page des formalités à remplir pour les citoyens brésiliens voyageant aux USA

---
## BERT, c'est quoi?

* Un modèle d'apprentissage profond de représentations contextualisées des mots
  - BERT pour *Bidirectional Encoder Representations from Transformers*
  - réponse à ELMo pour *Embeddings from Language Models* (Open AI et AI2)
* représentations **génériques** au départ mais **ajustables** (fine-tuning) à de nombreuses tâches
  - publi initiale: améliore l'état de l'art sur 12 tâches, dont la compréhension de texte
* développé par des chercheurs de *Google AI Language* et publié sur arXiv en octobre 2018.

["BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding", Devlin et al. 2018](https://arxiv.org/abs/1810.04805)

---
## Bert (et ELMo), comment ça marche?

Sur un gros corpus (1 milliard de mots) non-annoté:
* on cache 15% des mots
* on entraîne un modèle à prédire les mots cachés en fonction des mots du contexte
* on obtient un modèle de représentation contextualisée, générique, des mots

Sur un petit corpus annoté pour la tâche qui nous intéresse:
* on prend le modèle générique
* on ajoute une couche spécialisée au-dessus du modèle générique
* on entraîne cette couche sur la tâche choisie

---

## BERT, symbole d'une accélération de la recherche

* 2018/02/15 : [pre-print d'ELMo](https://arxiv.org/abs/1802.05365) par OpenAI et AI2
* ...
* 2018/10/11 : pre-print de BERT sur arXiv par Google AI Language
* 2018/10/31 : publication du code en open source sur github https://github.com/google-research/bert
* 2018/11/02 : annonce officielle de Google AI https://ai.googleblog.com/2018/11/open-sourcing-bert-state-of-art-pre.html
* 2018/11--... : explosion des réutilisations
* ...
* 2019/06/05 : présentation à la conférence NAACL (best paper) *après plusieurs réutilisations externes* https://www.aclweb.org/anthology/N19-1423/
* ...
* 2019/10/25 : annonce de l'intégration à Google Search
* 2019/11/18 : annonce de l'intégration à Bing Search https://azure.microsoft.com/en-us/blog/bing-delivers-its-largest-improvement-in-search-experience-using-azure-gpus/

À peine 12 mois se sont écoulés entre le pre-print et la mise en production au sein de l'un des produits les plus utilisés au monde.

---
## Pour aller plus loin

http://jalammar.github.io/illustrated-bert/

https://ruder.io/state-of-transfer-learning-in-nlp/

---
## Sources

https://www.wired.com/story/google-search-advancing-grade-reading/


---
## Comment Google mesure-t-il l'impact d'une modification?

* Tests de la qualité des résultats de recherche
* Tests comparatifs
* Tests du trafic en situation réelle
* Revue des données des tests et décision

https://www.google.com/search/howsearchworks/mission/users/

Consignes d'évaluation :
https://guidelines.raterhub.com/searchqualityevaluatorguidelines.pdf
