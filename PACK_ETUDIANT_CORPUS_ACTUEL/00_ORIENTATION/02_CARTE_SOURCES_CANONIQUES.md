# Carte des sources canoniques

## Racine actuelle du GPT etudiant

La racine prioritaire pour le GPT etudiant est:

```text
PACK_ETUDIANT_CORPUS_ACTUEL/
```

`BASE_DE_CONNAISSANCE/` est une source canonique avancee optionnelle. Elle doit etre utilisee seulement si elle est jointe et si la demande porte explicitement sur le corpus MDL Ynor. Le travail etudiant general doit partir du pack etudiant pour eviter d'exposer inutilement la complexite du corpus.

## Sources de navigation

| Besoin | Source |
|---|---|
| Trouver le socle documentaire avance | `BASE_DE_CONNAISSANCE/README.md` |
| Lire l'ordre racine | `BASE_DE_CONNAISSANCE/00_A_ROOT_INDEX_CORPUS_MDL_YNOR.md` |
| Comprendre l'ordre canonique | `BASE_DE_CONNAISSANCE/CANON/README.md` |
| Orienter une requete | `BASE_DE_CONNAISSANCE/RAG_SUPPORT/02_CROSSWALK_CANON.md` |
| Lire le parcours de support | `BASE_DE_CONNAISSANCE/RAG_SUPPORT/16_INDEX_AND_READING_ORDER.md` |

## Sources mathematiques

| Notion | Source |
|---|---|
| Relation structurelle | `BASE_DE_CONNAISSANCE/CANON/03_THEORIE_STRUCTURELLE.md` |
| Variables et observables | `BASE_DE_CONNAISSANCE/CANON/19_EMPIRICAL_MEASUREMENT.md` |
| Topologie locale | `BASE_DE_CONNAISSANCE/CANON/18_MATHEMATICAL_TOPOLOGY.md` |
| Regimes de stabilite | `BASE_DE_CONNAISSANCE/CANON/13_REGIMES_STABILITE.md` |
| Definitions de base | `BASE_DE_CONNAISSANCE/CANON/05_GLOSSAIRE.md` |

## Sources scientifiques

| Besoin | Source |
|---|---|
| Discipline scientifique | `BASE_DE_CONNAISSANCE/CANON/17_SCIENTIFIC_VALIDATION.md` |
| Preuve, replication, incertitude | `BASE_DE_CONNAISSANCE/CANON/23_PREUVE_REPLICATION_INCERTITUDE.md` |
| Validation externe | `BASE_DE_CONNAISSANCE/CANON/24_VALIDATION_EXTERNE.md` |
| Curation de la base | `BASE_DE_CONNAISSANCE/CANON/25_KNOWLEDGE_BASE_CURATION_POLICY.md` |
| Frontiere des claims | `BASE_DE_CONNAISSANCE/CANON/41_PRODUCT_CLAIMS_BOUNDARY.md` |

## Sources de support

| Besoin | Source |
|---|---|
| Lecture rapide | `BASE_DE_CONNAISSANCE/RAG_SUPPORT/01_GUIDE_LECTURE.md` |
| Correspondance vers canon | `BASE_DE_CONNAISSANCE/RAG_SUPPORT/02_CROSSWALK_CANON.md` |
| Chunking et citation | `BASE_DE_CONNAISSANCE/RAG_SUPPORT/03_CHUNKING_AND_CITATION.md` |
| Role des sources support | `BASE_DE_CONNAISSANCE/RAG_SUPPORT/22_RAG_SUPPORT_ROLE_AND_UNSUPPORTED.md` |
| Guide d'enrichissement | `BASE_DE_CONNAISSANCE/RAG_SUPPORT/23_KB_ENRICHMENT_GUIDE.md` |

## Sources a traiter avec prudence

| Source | Statut |
|---|---|
| `MATH_complete.txt` | dataset brut quarantined / manifest-only selon registre racine |
| `MDL Ynor Archtecture_/` | bundle externe typoed / quarantined |
| logs runtime | deindexes |
| zips bruts | artefacts, non sources primaires |
| caches et node_modules | hors doctrine |

## Regle de citation au service de l'etudiant

Toute citation doit indiquer:

- chemin;
- couche: ROOT, CANON, RAG_SUPPORT, AUDIT, MONITORING, TECHNIQUE;
- statut: canonique, support, protocole, audit, non primaire;
- usage: definition, preuve, navigation, validation, limite.

Exemple:

```text
Source: BASE_DE_CONNAISSANCE/CANON/18_MATHEMATICAL_TOPOLOGY.md
Couche: CANON
Usage: definition de d_mu et de T_mu
Statut: formalisation locale, non theorie universelle
```
