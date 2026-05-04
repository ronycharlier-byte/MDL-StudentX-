# Mesure experimentale et baselines

## But

Une mesure academique n'est pas seulement un nombre. C'est un nombre rattache a une methode, une fenetre, un baseline et une incertitude.

## Construction d'une mesure

1. Definir l'objet.
2. Choisir l'observable.
3. Choisir le proxy.
4. Normaliser.
5. Mesurer sur un snapshot.
6. Comparer a un baseline.
7. Rapporter incertitude et limite.

## Exemple pour alpha

Objet:

```text
capacite de stabilisation documentaire
```

Proxy possible:

```text
taux de citations correctement conservees apres transformation
```

Attention:

- un proxy n'est pas la notion;
- un proxy peut etre biaise;
- plusieurs proxys peuvent etre necessaires.

## Exemple pour beta

Objet:

```text
pression de bruit documentaire
```

Proxy possible:

```text
taux de duplication, contradictions, leakage, derives non resolues
```

Attention:

- le bruit doit etre defini;
- un doublon utile n'est pas forcement du bruit;
- un conflit peut etre informatif.

## Exemple pour kappa

Objet:

```text
dette de maintenance
```

Proxy possible:

```text
temps moyen de correction, erreurs de parsing, cout de renommage, instabilite des chemins
```

Attention:

- le cout doit etre mesure ou estime selon une regle stable;
- un cout ponctuel ne prouve pas une dette durable.

## Baselines acceptables

| Baseline | Usage |
|---|---|
| null drift | comparer a absence de changement |
| prior window | comparer a fenetre precedente |
| naive policy | comparer a methode simple |
| delayed action | comparer a absence de correction immediate |
| random sampling | verifier si la methode depasse le hasard |

## Mauvais baselines

- baseline choisi apres resultat;
- baseline trop faible;
- baseline non documente;
- baseline qui utilise les donnees de test;
- baseline impossible a rejouer.

## Table experimentale minimale

| Champ | Valeur |
|---|---|
| Snapshot | a remplir |
| Fenetre | a remplir |
| Variable | alpha / beta / kappa / mu |
| Proxy | a remplir |
| Methode | a remplir |
| Baseline | a remplir |
| Resultat | a remplir |
| Incertitude | a remplir |
| Failure case | a remplir |

## Conclusion

Le meilleur resultat n'est pas celui qui parait le plus spectaculaire. C'est celui qui reste interpretable quand on change legerement les seuils, qu'on verifie le baseline et qu'on rend les donnees manquantes visibles.
