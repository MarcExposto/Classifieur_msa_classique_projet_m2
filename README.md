# Classifieur_msa_classique_projet_m2
Classifieur arabe classique / arabe standard moderne (MSA) sur le corpus OpenITI : comparaison d’un modèle à n-grammes et de CAMeLBERT, avec contrôle des biais d’auteur et de thème. Projet de TAL M2 pour les langues peu dotées.


## Question idées

Peut-on distinguer automatiquement l'arabe classique de la MSA, sans que le modèle
apprenne le thème ou l'auteur à la place ?

- **Q1.** Un modèle simple (n-grammes de caractères + SVM) suffit-il ?
- **Q2.** Un modèle pré-entraîné (CAMeLBERT, version MSA et version CA) fait-il mieux, surtout avec peu de données ?
- **Q3.** Le classifieur repose-t-il sur la variété de langue, ou sur le thème, l'auteur et les voyelles ?

## Données Corpus

Le dépôt **ne contient pas les textes** (pas le droit avec les licences ):

| Source | Rôle | Lien |
|---|---|---|
| OpenITI, versions principales | Entraînement et test (CA et MSA) | https://doi.org/10.5281/zenodo.7764025 |
| KSUCCA | Test externe CA | https://sourceforge.net/projects/ksucca-corpus |
| OSIAN | Test externe MSA | https://aclanthology.org/W19-4619/ |

**Étiquetage.** L'etiquetage des donnée ( aconfirmer) La classe vient de l'année de mort de l'auteur, en hégire, lue dans
l'identifiant OpenITI (`0310Tabari` = mort en 310 H) :

- CA : auteur mort avant 1200 H ;
- MSA : auteur mort après 1350 H ;
- auteurs morts entre 1200 et 1350 H : exclus (période de transition).(possible dans inclure si pas assez de donnée dans une partie ou l'autre)

## Utilisation

```bash
python nom_script.py
python 
```

## Références
(article déja dans la presentation)
- Alkhazi & Teahan (2017). *Classifying and Segmenting Classical and Modern Standard Arabic using Minimum Cross-Entropy.* IJACSA 8(4).
- Belinkov et al. (2019). *Studying the History of the Arabic Language: Language Technology and a Large-Scale Historical Corpus.* Language Resources and Evaluation.
- Inoue et al. (2021). *The Interplay of Variant, Size, and Task Type in Arabic Pre-trained Language Models.* WANLP.
- Alhathloul & Ahmad (2026). *Automatic Classification of Arabic Literature into Historical Eras.* arXiv:2601.16138.
(Autre article et reference)
-
-

## Licences

- **Code** : MIT (voir `LICENSE`).
- **Données utilisé** : non incluses, chaque source garde sa licence.
  - OpenITI : CC BY-NC-SA 4.0
  - KSUCCA : CC BY-NC 2.0
  - OSIAN : CC BY-NC 4.0
- **Fichiers dérivés** (identifiants des passages, annotations de genre) : CC BY-NC-SA 4.0, comme OpenITI.

