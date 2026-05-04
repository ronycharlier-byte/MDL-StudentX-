# Pack Etudiant Corpus Actuel

Statut: pack pedagogique dedie aux etudiants.
Date de generation: 2026-05-05.
Racine de reference du GPT etudiant: `PACK_ETUDIANT_CORPUS_ACTUEL`.
Source canonique avancee optionnelle: `BASE_DE_CONNAISSANCE`, seulement si elle est jointe et si la demande porte sur le corpus MDL Ynor.
Licence: voir `LICENSE.md`.
Licence commerciale: voir `COMMERCIAL_LICENSE.md`.

## Objet

Ce dossier recree un pack etudiant aligne sur le corpus actuel. Il transforme la base documentaire gouvernee en instrument de formation, d'analyse scientifique, de formalisation mathematique, de recherche et d'usage GPT au service de l'excellence etudiante.

Le pack n'est pas une nouvelle doctrine. C'est une couche pedagogique. Sa fonction n'est pas d'aider le corpus, mais d'aider les etudiants a exceller: comprendre mieux, raisonner plus juste, verifier plus fort, formaliser plus proprement et produire des travaux academiques de haut niveau.

## Finalite

Le corpus sert l'etudiant. L'etudiant ne sert pas le corpus.

Le GPT etudiant doit donc:

- partir du besoin de l'etudiant;
- utiliser le corpus comme support, laboratoire et bibliotheque;
- chercher sur Internet a chaque reponse si l'outil est disponible;
- transformer les notions en competences;
- produire exercices, methodes, critiques, plans et corrections;
- refuser de promouvoir le corpus a la place d'aider l'etudiant.

## Regle d'autorite

Ordre de lecture du pack etudiant:

1. `AAA_PRIORITE_GPT_CUSTOM.md`
2. `INSTRUCTIONS_GPT_COMPLETES_SANS_LIMITE.md`
3. `00_INDEX_PACK_ETUDIANT.md`
4. `README.md`
5. `07_GPT_UPLOAD/INDEX_MAITRE_ETUDIANT.md`
6. `07_GPT_UPLOAD/FICHE_UNE_PAGE.md`

Si un travail approfondi porte explicitement sur le corpus MDL Ynor et que `BASE_DE_CONNAISSANCE` est jointe, l'arbitrage interne avance suit ensuite:

1. `BASE_DE_CONNAISSANCE/README.md`
2. `BASE_DE_CONNAISSANCE/00_A_ROOT_INDEX_CORPUS_MDL_YNOR.md`
3. `BASE_DE_CONNAISSANCE/CANON/README.md`
4. `BASE_DE_CONNAISSANCE/CANON/22_CONTRAT_LECTURE_GOUVERNEE.md`
5. `BASE_DE_CONNAISSANCE/CANON/17_SCIENTIFIC_VALIDATION.md`
6. `BASE_DE_CONNAISSANCE/CANON/18_MATHEMATICAL_TOPOLOGY.md`
7. `BASE_DE_CONNAISSANCE/CANON/19_EMPIRICAL_MEASUREMENT.md`
8. `BASE_DE_CONNAISSANCE/CANON/23_PREUVE_REPLICATION_INCERTITUDE.md`
9. `BASE_DE_CONNAISSANCE/CANON/24_VALIDATION_EXTERNE.md`
10. `BASE_DE_CONNAISSANCE/CANON/41_PRODUCT_CLAIMS_BOUNDARY.md`

`RAG_SUPPORT` aide a lire. `AUDIT` encadre la preuve et la validation. Les zips, logs, caches, exports bruts et donnees quarantinees ne sont pas sources primaires.

Si `PACK_ETUDIANT_CORPUS_ACTUEL` est absent, ne pas faire comme si `BASE_DE_CONNAISSANCE` etait le pack etudiant. Signaler explicitement que le bon zip etudiant n'est pas charge.

## Architecture du pack

```text
PACK_ETUDIANT_CORPUS_ACTUEL/
  README.md
  00_ORIENTATION/
  01_PARCOURS_ACADEMIQUES/
  02_MATHEMATIQUES/
  03_SCIENCES_VALIDATION/
  04_RECHERCHE/
  05_IA_TUTORAT_RAG/
  06_EVALUATION/
  07_GPT_UPLOAD/
  08_MANIFESTES/
```

## Usage rapide

Pour un etudiant:

1. Lire `00_ORIENTATION/00_MODE_D_EMPLOI_ETUDIANT.md`.
2. Lire `00_ORIENTATION/01_CONTRAT_PEDAGOGIQUE_SCIENTIFIQUE.md`.
3. Choisir un parcours dans `01_PARCOURS_ACADEMIQUES/00_PARCOURS_PAR_NIVEAU.md`.
4. Choisir ou declarer sa filiere avec `01_PARCOURS_ACADEMIQUES/03_CARTOGRAPHIE_ETUDES_UNIVERSITAIRES.md`.
5. Utiliser `01_PARCOURS_ACADEMIQUES/05_MODULES_DOMAINES_UNIVERSITAIRES_COMPLETS.md` pour adapter la reponse au domaine.
6. Pour la psychologie, utiliser `01_PARCOURS_ACADEMIQUES/04_MODULE_PSYCHOLOGIE_UNIVERSITAIRE.md`.
7. Travailler les bases mathematiques dans `02_MATHEMATIQUES/` si elles servent la filiere.
8. Passer a la validation dans `03_SCIENCES_VALIDATION/` si la demande implique un claim, une preuve ou une methode.
9. Utiliser Internet comme recherche externe citee avec `05_IA_TUTORAT_RAG/03_PROTOCOLE_RECHERCHE_WEB_ET_SOURCES_EXTERNES.md`.
10. Utiliser les prompts dans `05_IA_TUTORAT_RAG/`.
11. S'evaluer avec `06_EVALUATION/`.

Pour creer un GPT etudiant:

1. Coller seulement `07_GPT_UPLOAD/GRILLE_LECTURE_GPT_CUSTOM.md` dans le champ Instructions du GPT custom.
2. Ajouter le zip complet comme base de connaissances.
3. Verifier que `INSTRUCTIONS_GPT_COMPLETES_SANS_LIMITE.md` est dans le zip: c'est le fichier que le GPT doit lire avant les autres.
4. Ajouter ensuite les fichiers canoniques du corpus seulement si un travail approfondi sur le corpus interne est attendu.
5. Activer la recherche web/navigation Internet si disponible.
6. Imposer une ligne ou section `Recherche web` a chaque reponse du GPT.
7. Garder le corpus canonique comme source de verite interne, et Internet comme source externe citee, datee et qualifiee.

## Discipline academique

Le pack impose quatre distinctions:

- fait documentaire: present dans une source identifiee;
- inference: consequence raisonnable, mais non directement citee;
- hypothese: proposition a tester;
- non etabli: claim sans preuve, sans protocole ou sans validation suffisante;
- externe web: source Internet verifiable, a qualifier selon sa fiabilite.

Une phrase mathematique doit indiquer ses definitions, son domaine, ses hypotheses, sa preuve ou son statut. Une phrase scientifique doit indiquer son observable, sa methode, sa fenetre, son baseline, son incertitude et sa condition d'echec.

## Niveau vise

Le niveau cible va de licence avancee a master, avec extension doctorale. Les etudiants debutants peuvent l'utiliser par progression; les etudiants avances doivent l'utiliser comme protocole de rigueur, non comme texte a memoriser.

## Limite

Ce pack ne prouve pas les claims internes. Il fournit une architecture pedagogique pour transformer les sources en competences, exercices, recherches, analyses et travaux academiques reproductibles.

## Licence

Usage academique, educatif et recherche non commercial sous CC BY-NC-SA 4.0, sauf mention contraire. Les usages commerciaux ou integrations payantes demandent une autorisation ecrite prealable.

Contact commercial: ronycharlier@mdlstrategy.com
