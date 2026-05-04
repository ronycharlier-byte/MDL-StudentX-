# Protocole preuve, replication et incertitude

## Sources

- `BASE_DE_CONNAISSANCE/CANON/17_SCIENTIFIC_VALIDATION.md`
- `BASE_DE_CONNAISSANCE/CANON/23_PREUVE_REPLICATION_INCERTITUDE.md`
- `BASE_DE_CONNAISSANCE/CANON/24_VALIDATION_EXTERNE.md`

## Objectif

Transformer un claim en objet testable.

## Template de claim

```text
Claim:
Observable:
Methode:
Snapshot ou fenetre:
Baseline:
Condition d'echec:
Incertitude:
Couverture:
Donnees manquantes:
Statut attendu:
```

## Hypothese nulle et verification de manipulation

Pour `H0`, eviter la formulation vague `pas de difference significative`. Preferer:

```text
H0: il n'y aura pas de difference detectable selon le test statistique prevu.
```

Quand une manipulation est supposee produire un effet intermediaire, cet effet doit entrer dans la condition d'echec. Exemple: si un support dense est suppose augmenter la charge cognitive, l'hypothese n'est pas correctement soutenue si la charge cognitive percue n'augmente pas dans le groupe dense.

## Echelle de preuve

| Niveau | Description | Verdict |
|---|---|---|
| Mock | test double ou placeholder | pas preuve |
| Simulation | comportement genere par modele | utile mais limite |
| Benchmark interne | test controle sur sources proches | evidence interne |
| Validation interne | invariants internes | support local |
| Benchmark externe | materiel independant | candidat externe |
| Validation externe | criteres preregistres sur unseen material | candidat solide |
| Replication independante | autre run, sampler ou annotateur | evidence forte |
| Resultat fort | validation + replication + incertitude + echec explicite | preuve scientifique forte |

## Regle preregistration

Avant execution:

- figer le claim;
- figer la methode;
- figer le seuil;
- figer le baseline;
- figer la fenetre;
- declarer les echecs possibles.

Apres execution, on ne change pas le seuil pour sauver le resultat.

## Regle de replication

Une replication valable doit:

- utiliser les memes criteres;
- ne pas reutiliser les donnees de calibration comme test final;
- indiquer l'independance;
- produire ou non le meme verdict dans une tolerance declaree.

## Regle d'incertitude

Tout resultat numerique doit donner:

- point estimate;
- spread;
- intervalle ou borne;
- sensibilite aux seuils;
- couverture;
- missingness.

Si un petit changement de seuil renverse la conclusion, le resultat est fragile.

## Verdicts

`ACCEPT`:

- endpoints primaires passent;
- baseline battu;
- incertitude compatible avec le signe du claim;
- pas de fuite majeure;
- protocole respecte.

`REJECT`:

- endpoint primaire echoue;
- leakage;
- baseline non battu;
- protocole modifie post-hoc.

`INDETERMINATE`:

- donnees insuffisantes;
- incertitude trop large;
- independence non demontree;
- conflit non resolu.

## Phrase modele

```text
Ce resultat est [statut] sur [fenetre], selon [methode], compare a [baseline]. Il reste limite par [incertitude], [coverage] et [condition d'echec].
```
