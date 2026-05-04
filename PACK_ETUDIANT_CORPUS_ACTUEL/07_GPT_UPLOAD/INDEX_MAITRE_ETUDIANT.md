# Index maitre etudiant

## Sources prioritaires du GPT etudiant

Le dossier prioritaire est toujours `PACK_ETUDIANT_CORPUS_ACTUEL`.

Si le GPT ne trouve pas `PACK_ETUDIANT_CORPUS_ACTUEL`, `INSTRUCTIONS_GPT_COMPLETES_SANS_LIMITE.md`, `00_INDEX_PACK_ETUDIANT.md` ou `07_GPT_UPLOAD/FICHE_UNE_PAGE.md`, il doit ecrire:

```text
Sources internes: dossier PACK_ETUDIANT_CORPUS_ACTUEL indisponible.
```

Dans ce cas, il ne doit pas remplacer automatiquement le pack etudiant par `BASE_DE_CONNAISSANCE`. Il peut repondre avec prudence a partir du web et de connaissances generales, mais il doit signaler que le bon zip etudiant n'est pas charge.

`BASE_DE_CONNAISSANCE` est une source avancee optionnelle uniquement si elle est aussi jointe et si la demande porte explicitement sur le corpus MDL Ynor. Elle ne doit jamais masquer l'absence du pack etudiant.

## Fichiers du pack a charger dans un GPT

Noyau minimal:

1. `../AAA_PRIORITE_GPT_CUSTOM.md`
2. `GRILLE_LECTURE_GPT_CUSTOM.md` a coller dans le champ Instructions du GPT custom
3. `../INSTRUCTIONS_GPT_COMPLETES_SANS_LIMITE.md` a joindre dans le zip et a lire comme instruction complete
4. `07_GPT_UPLOAD/FICHE_UNE_PAGE.md`
5. `EXECUTIVE_DIGEST_ETUDIANT.md`
6. `INDEX_MAITRE_ETUDIANT.md`
7. `WEB_RESEARCH_POLICY.md`

Noyau pedagogique:

1. `../00_ORIENTATION/01_CONTRAT_PEDAGOGIQUE_SCIENTIFIQUE.md`
2. `../00_ORIENTATION/02_CARTE_SOURCES_CANONIQUES.md`
3. `../00_ORIENTATION/04_FINALITE_EXCELLENCE_ETUDIANTE.md`
4. `../01_PARCOURS_ACADEMIQUES/03_CARTOGRAPHIE_ETUDES_UNIVERSITAIRES.md`
5. `../01_PARCOURS_ACADEMIQUES/04_MODULE_PSYCHOLOGIE_UNIVERSITAIRE.md`
6. `../01_PARCOURS_ACADEMIQUES/05_MODULES_DOMAINES_UNIVERSITAIRES_COMPLETS.md`
7. `../02_MATHEMATIQUES/00_FORMALISATION_MDL_YNOR_ETUDIANTS.md`
8. `../03_SCIENCES_VALIDATION/00_PROTOCOLE_PREUVE_REPLICATION_INCERTITUDE.md`
9. `../05_IA_TUTORAT_RAG/02_PROTOCOLE_ANTI_HALLUCINATION_CITATIONS.md`
10. `../05_IA_TUTORAT_RAG/03_PROTOCOLE_RECHERCHE_WEB_ET_SOURCES_EXTERNES.md`

## Requetes types

- "Explique cette notion en intuition, definition, limite."
- "Formalise ce claim avec objets, hypotheses et preuve locale."
- "Transforme ce claim en protocole testable."
- "Detecte les surclaims et propose une formulation academique."
- "Prepare un oral de master avec questions difficiles."
- "Cherche sur Internet les sources scientifiques recentes et compare-les aux sources internes."
- "Verifie ce claim avec sources web citees, datees et qualifiees."
- "Utilise le corpus pour m'aider a exceller sur cette competence precise."
- "Adapte ton aide a ma filiere universitaire et au livrable demande."
- "Aide-moi en psychologie sans diagnostic, avec methode, sources, ethique et exercice."

## Verdict attendu du GPT

Le GPT doit produire une aide exigeante centree sur la progression de l'etudiant, pas une validation automatique ni une defense d'une architecture documentaire.
