# Formalisation MDL Ynor pour etudiants

## Sources

Sources canoniques principales:

- `BASE_DE_CONNAISSANCE/CANON/03_THEORIE_STRUCTURELLE.md`
- `BASE_DE_CONNAISSANCE/CANON/18_MATHEMATICAL_TOPOLOGY.md`
- `BASE_DE_CONNAISSANCE/CANON/19_EMPIRICAL_MEASUREMENT.md`

Ce document est une reformulation pedagogique au service de l'etudiant. En cas de conflit entre sources internes, le canon arbitre.

## Niveau 1 - Identite de marge

Definition locale:

```text
mu = alpha - beta - kappa
```

Interpretation:

- `alpha`: capacite de stabilisation et densite utile;
- `beta`: bruit, fuite, duplication, derive;
- `kappa`: dette de maintenance et friction;
- `mu`: marge nette interne.

Proposition:

Sur un snapshot fixe, si `mu` est defini comme `alpha - beta - kappa`, alors toute variation de `alpha`, `beta` ou `kappa` se propage lineairement a `mu`.

Preuve:

```text
mu_2 - mu_1
= (alpha_2 - beta_2 - kappa_2) - (alpha_1 - beta_1 - kappa_1)
= (alpha_2 - alpha_1) - (beta_2 - beta_1) - (kappa_2 - kappa_1)
```

Donc:

- si `alpha` augmente seul de `h`, alors `mu` augmente de `h`;
- si `beta` augmente seul de `h`, alors `mu` diminue de `h`;
- si `kappa` augmente seul de `h`, alors `mu` diminue de `h`.

Limite:

Cette relation est une identite locale de comptabilite, pas une loi universelle.

## Niveau 2 - Espace de configurations

Soit `Theta` l'ensemble des configurations admissibles. Une configuration `theta` peut representer:

- un snapshot documentaire;
- une politique de mesure;
- une fenetre temporelle;
- un regime d'organisation.

On suppose une application:

```text
mu : Theta -> R
```

Chaque configuration recoit une marge reelle.

## Niveau 3 - Pseudometrique de marge

Definition:

```text
d_mu(theta_1, theta_2) = |mu(theta_1) - mu(theta_2)|
```

Proposition:

`d_mu` est une pseudometrique sur `Theta`.

Preuve:

1. Non-negativite: une valeur absolue est toujours >= 0.
2. Symetrie: `|a - b| = |b - a|`.
3. Diagonale nulle: `d_mu(theta, theta) = |mu(theta) - mu(theta)| = 0`.
4. Inegalite triangulaire: `|a - c| <= |a - b| + |b - c|`.
5. Identite des indiscernables: elle peut echouer, car deux configurations distinctes peuvent avoir le meme `mu`.

Conclusion:

`d_mu` est une pseudometrique, pas necessairement une metrique.

## Niveau 4 - Topologie induite

Definition:

```text
B_mu(theta, eps) = { theta' in Theta : d_mu(theta, theta') < eps }
```

La topologie `T_mu` est induite par `d_mu`.

Theoreme local:

`mu` est continue de `(Theta, T_mu)` vers `R` muni de sa topologie usuelle.

Lecture critique:

Cette continuite vient de la construction de `T_mu`. Ce n'est pas une validation empirique du modele.

## Niveau 5 - Quotient par marge egale

Definition:

```text
theta_1 ~ theta_2  si et seulement si  mu(theta_1) = mu(theta_2)
Theta_mu = Theta / ~
```

Distance induite:

```text
bar_d([theta_1], [theta_2]) = |mu(theta_1) - mu(theta_2)|
```

Proposition:

`bar_d` est bien definie sur les classes d'equivalence.

Preuve:

Si `theta_1 ~ theta_1'` et `theta_2 ~ theta_2'`, alors:

```text
mu(theta_1) = mu(theta_1')
mu(theta_2) = mu(theta_2')
```

Donc la valeur `|mu(theta_1) - mu(theta_2)|` ne depend pas du representant choisi.

## Niveau 6 - Observables

Une variable n'est pas mathematiquement utile pour l'etudiant dans ce cadre si elle ne peut pas etre reliee a:

- un observable;
- une methode;
- un exemple;
- une condition d'echec.

Table minimale:

| Variable | Observable possible | Risque |
|---|---|---|
| `alpha` | retention des citations, densite utile | proxy trop subjectif |
| `beta` | duplication, fuite, derive | bruit mal defini |
| `kappa` | cout de correction, erreurs parsing | cout non mesure |
| `mu` | difference normalisee | poids arbitraires |
| `dot_mu` | delta de marge | fenetres non comparables |
| `epsilon` | residu | residu cache ou ignore |

## Conclusion etudiante

Le noyau mathematique utile est sobre:

1. une identite de marge;
2. une application `mu`;
3. une pseudometrique induite;
4. une topologie locale;
5. un quotient par marge egale;
6. une exigence d'observabilite.

Sa force pedagogique est de relier definition, preuve, mesure et limite.
