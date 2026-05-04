# Source map du pack etudiant

## Origine

Ce pack a ete construit depuis le corpus local actuel:

```text
C:/Users/ronyc/Desktop/Corpus
```

Fichier zip source mentionne:

```text
C:/Users/ronyc/Downloads/GPT_UPLOAD_PACK_ETUDIANT.zip
```

Le zip source etait un point de depart minimal. Le present pack reconstruit une architecture plus complete, centree sur `PACK_ETUDIANT_CORPUS_ACTUEL`. `BASE_DE_CONNAISSANCE` reste une source canonique avancee optionnelle pour les demandes portant explicitement sur le corpus MDL Ynor.

## Anchors canoniques utilises

| Sujet | Chemin |
|---|---|
| Racine canonique avancee optionnelle | `BASE_DE_CONNAISSANCE/README.md` |
| Index racine | `BASE_DE_CONNAISSANCE/00_A_ROOT_INDEX_CORPUS_MDL_YNOR.md` |
| Racine canon | `BASE_DE_CONNAISSANCE/CANON/README.md` |
| Theorie | `BASE_DE_CONNAISSANCE/CANON/03_THEORIE_STRUCTURELLE.md` |
| Validation scientifique | `BASE_DE_CONNAISSANCE/CANON/17_SCIENTIFIC_VALIDATION.md` |
| Topologie mathematique | `BASE_DE_CONNAISSANCE/CANON/18_MATHEMATICAL_TOPOLOGY.md` |
| Mesure empirique | `BASE_DE_CONNAISSANCE/CANON/19_EMPIRICAL_MEASUREMENT.md` |
| Preuve et incertitude | `BASE_DE_CONNAISSANCE/CANON/23_PREUVE_REPLICATION_INCERTITUDE.md` |
| Validation externe | `BASE_DE_CONNAISSANCE/CANON/24_VALIDATION_EXTERNE.md` |
| Claims | `BASE_DE_CONNAISSANCE/CANON/41_PRODUCT_CLAIMS_BOUNDARY.md` |
| Guide lecture | `BASE_DE_CONNAISSANCE/RAG_SUPPORT/01_GUIDE_LECTURE.md` |
| Crosswalk | `BASE_DE_CONNAISSANCE/RAG_SUPPORT/02_CROSSWALK_CANON.md` |
| Ordre de lecture support | `BASE_DE_CONNAISSANCE/RAG_SUPPORT/16_INDEX_AND_READING_ORDER.md` |

## Decisions de transformation

| Decision | Raison |
|---|---|
| Pack dedie dans `PACK_ETUDIANT_CORPUS_ACTUEL` | rendre l'usage etudiant autonome et centre sur la progression |
| Finalite excellence etudiante | faire servir les sources a la progression des etudiants, et non l'inverse |
| Contenus sans surclaim | respecter les frontieres de preuve pour proteger la qualite du travail etudiant |
| Formalisation mathematique pedagogique | rendre `mu`, `d_mu`, `T_mu` et quotient enseignables |
| Protocoles scientifiques | transformer les claims en objets testables |
| Prompts GPT specialises | permettre un tuteur controle par la discipline epistemique |
| Recherche web externe | ouvrir le GPT aux sources scientifiques, institutionnelles et actuelles sans perdre la discipline de citation |
| Evaluation et rubriques | rendre le pack utilisable en formation |

## Non inclus comme source primaire

- `MATH_complete.txt`: dataset brut, utile eventuellement pour exercices generaux mais non canonique.
- zips bruts: artefacts de distribution.
- logs runtime: non doctrinaux.
- caches et dependencies: hors corpus documentaire.
