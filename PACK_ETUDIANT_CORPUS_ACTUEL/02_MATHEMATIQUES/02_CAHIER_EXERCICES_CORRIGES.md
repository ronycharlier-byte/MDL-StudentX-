# Cahier d'exercices corriges

## Exercice 1 - Calcul de mu

Donnees:

```text
alpha = 0.72
beta = 0.18
kappa = 0.11
```

Calculer `mu`.

Correction:

```text
mu = alpha - beta - kappa
mu = 0.72 - 0.18 - 0.11
mu = 0.43
```

Interpretation:

La marge est positive. Cela ne prouve pas une efficacite externe; cela indique seulement un resultat local sous ces valeurs.

## Exercice 2 - Variation de mu

On passe de:

```text
alpha_1 = 0.60, beta_1 = 0.20, kappa_1 = 0.10
alpha_2 = 0.65, beta_2 = 0.24, kappa_2 = 0.09
```

Calculer `mu_1`, `mu_2`, puis `Delta_mu`.

Correction:

```text
mu_1 = 0.60 - 0.20 - 0.10 = 0.30
mu_2 = 0.65 - 0.24 - 0.09 = 0.32
Delta_mu = 0.32 - 0.30 = 0.02
```

Interpretation:

La marge progresse legerement. La hausse de `alpha` compense la hausse de `beta` et la baisse de `kappa` aide aussi.

## Exercice 3 - Pseudometrique

Soit:

```text
mu(theta_a) = 0.40
mu(theta_b) = 0.10
mu(theta_c) = 0.40
```

Calculer:

```text
d_mu(theta_a, theta_b)
d_mu(theta_a, theta_c)
```

Correction:

```text
d_mu(theta_a, theta_b) = |0.40 - 0.10| = 0.30
d_mu(theta_a, theta_c) = |0.40 - 0.40| = 0
```

Conclusion:

`theta_a` et `theta_c` peuvent etre distincts meme si leur distance de marge vaut 0. C'est pourquoi `d_mu` est une pseudometrique.

## Exercice 4 - Triangle

Montrer que:

```text
d_mu(theta_1, theta_3) <= d_mu(theta_1, theta_2) + d_mu(theta_2, theta_3)
```

Correction:

Par definition:

```text
d_mu(theta_1, theta_3) = |mu(theta_1) - mu(theta_3)|
```

Or, pour tous reels `a`, `b`, `c`:

```text
|a - c| <= |a - b| + |b - c|
```

En posant:

```text
a = mu(theta_1)
b = mu(theta_2)
c = mu(theta_3)
```

on obtient l'inegalite voulue.

## Exercice 5 - Quotient

On definit:

```text
theta_1 ~ theta_2 <=> mu(theta_1) = mu(theta_2)
```

Prouver que cette relation est une relation d'equivalence.

Correction:

Reflexivite:

```text
mu(theta) = mu(theta)
```

donc `theta ~ theta`.

Symetrie:

Si `theta_1 ~ theta_2`, alors `mu(theta_1) = mu(theta_2)`. Donc `mu(theta_2) = mu(theta_1)`, et `theta_2 ~ theta_1`.

Transitivite:

Si `theta_1 ~ theta_2` et `theta_2 ~ theta_3`, alors:

```text
mu(theta_1) = mu(theta_2)
mu(theta_2) = mu(theta_3)
```

donc `mu(theta_1) = mu(theta_3)`, et `theta_1 ~ theta_3`.

## Exercice 6 - Claim scientifique

Claim:

```text
Le modele reduit le risque de retrieval.
```

Transformer ce claim en claim testable.

Correction:

Formulation testable:

```text
Sur le snapshot S, avec la methode M, le taux d'erreur de retrieval mesure sur la fenetre W est inferieur au baseline B d'au moins delta, avec une incertitude compatible avec un effet positif. Echec si le gain observe est <= 0 ou si l'intervalle franchit le baseline.
```

Elements ajoutes:

- snapshot;
- methode;
- fenetre;
- baseline;
- seuil minimal;
- incertitude;
- condition d'echec.

## Exercice 7 - Critique de surclaim

Enonce:

```text
La topologie prouve que le systeme est stable.
```

Corriger.

Correction:

Formulation prudente:

```text
La topologie de marge decrit une stabilite locale relativement a `mu`. Elle ne prouve pas a elle seule la stabilite empirique du systeme complet, car des differences structurelles invisibles a `mu` peuvent subsister.
```

## Exercice 8 - Protocole minimal

Ecrire les 6 champs minimaux d'un protocole de validation.

Correction:

1. Claim.
2. Observable.
3. Methode.
4. Fenetre.
5. Baseline.
6. Condition d'echec.

Champs avances:

- incertitude;
- couverture;
- missingness;
- replication;
- preregistration.
