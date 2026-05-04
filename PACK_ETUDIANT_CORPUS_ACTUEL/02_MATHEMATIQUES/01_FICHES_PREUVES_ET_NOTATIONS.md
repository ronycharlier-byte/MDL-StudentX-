# Fiches preuves et notations

## Regle de notation

Toujours definir:

- l'ensemble;
- les elements;
- l'application;
- la relation;
- le type de resultat.

Exemple:

```text
Theta: ensemble des configurations admissibles.
theta: element de Theta.
mu: application de Theta vers R.
d_mu: fonction de Theta x Theta vers R_+.
```

## Fiche 1 - Identite de marge

Enonce:

```text
mu = alpha - beta - kappa
```

Nature:

- definition locale;
- identite de comptabilite;
- non theorem universel.

Preuve:

La relation est vraie par definition de `mu` sur un snapshot fixe.

Erreur frequente:

Croire que la formule prouve une causalite. Elle ne prouve qu'une structure de calcul.

## Fiche 2 - Pseudometrique

Enonce:

```text
d_mu(theta_1, theta_2) = |mu(theta_1) - mu(theta_2)|
```

A verifier:

- `d_mu >= 0`;
- `d_mu(theta, theta) = 0`;
- symetrie;
- inegalite triangulaire;
- identite des indiscernables non exigee.

Conclusion:

Pseudometrique.

Erreur frequente:

Dire "metrique" sans verifier que `d_mu(theta_1, theta_2) = 0` implique `theta_1 = theta_2`.

## Fiche 3 - Quotient

Relation:

```text
theta_1 ~ theta_2 <=> mu(theta_1) = mu(theta_2)
```

Objectif:

Regrouper les configurations ayant la meme marge.

Preuve de bonne definition:

La distance entre classes ne depend pas du representant, car tous les representants d'une meme classe ont le meme `mu`.

Erreur frequente:

Croire que deux configurations de meme marge sont structurellement identiques. Elles sont seulement equivalentes pour la marge.

## Fiche 4 - Continuite de mu

Enonce:

`mu` est continue de `(Theta, T_mu)` vers `R`.

Nature:

- resultat de construction;
- pas une preuve empirique;
- pas une decouverte sur le monde externe.

Erreur frequente:

Surinterpreter une continuite definie par la topologie meme qui rend `mu` continue.

## Fiche 5 - Preuve locale vs preuve scientifique

Preuve locale:

- derivee de definitions;
- valide dans le cadre pose;
- peut etre mathematiquement correcte sans etre empiriquement utile.

Preuve scientifique:

- demande observables;
- demande methode;
- demande baseline;
- demande incertitude;
- demande replication.

Erreur frequente:

Utiliser une preuve locale comme preuve d'efficacite externe.

## Checklist avant d'ecrire "theoreme"

Avant le mot "theoreme", verifier:

- domaine fixe;
- hypotheses explicites;
- definitions non ambigues;
- conclusion precise;
- preuve complete;
- limites;
- contre-exemple impossible sous hypotheses;
- aucune confusion avec validation empirique.

Sinon, utiliser:

- definition;
- proposition;
- lemme;
- preuve sketch;
- hypothese;
- conjecture;
- resultat local.
