# Glossaire minimal

Ce glossaire sert aux etudiants. Il ne remplace pas `BASE_DE_CONNAISSANCE/CANON/05_GLOSSAIRE.md`.

## alpha

Role: capacite de stabilisation et densite utile.

Lecture etudiante:

- plus `alpha` est eleve, plus le systeme conserve de l'information utile;
- `alpha` doit rester lie a des observables;
- sans methode de mesure, `alpha` reste une notion descriptive.

## beta

Role: bruit documentaire, fuite, duplication, derive.

Lecture etudiante:

- `beta` represente ce qui degrade la clarte ou la fiabilite;
- une hausse de `beta` diminue `mu` si le reste est fixe;
- `beta` exige des proxys mesurables.

## kappa

Role: dette de maintenance et friction d'encodage.

Lecture etudiante:

- `kappa` capture le cout de maintien du support documentaire;
- exemples: erreurs de parsing, noms instables, cout de reparation;
- `kappa` n'est pas moral, c'est operationnel.

## mu

Definition locale:

```text
mu = alpha - beta - kappa
```

Role: marge nette interne.

Lecture etudiante:

- `mu` augmente si la densite utile augmente plus vite que le bruit et la dette;
- `mu` est une identite locale dans ce support documentaire, pas une loi universelle;
- un changement de signe de `mu` peut signaler une frontiere de regime.

## dot mu

Role: variation locale de `mu`.

Definition pratique:

```text
dot_mu ~= mu(t_2) - mu(t_1)
```

Lecture etudiante:

- utile pour suivre une trajectoire;
- fragile si les fenetres ou poids changent;
- doit etre mesure sur un snapshot et une methode fixes.

## epsilon

Role: residu apres calibration.

Lecture etudiante:

- indique ce que le modele n'explique pas encore;
- ne doit pas etre cache;
- peut guider une amelioration du modele.

## theta

Role: configuration ou regime admissible.

Lecture etudiante:

- `theta` appartient a un espace `Theta`;
- une configuration peut inclure un etat documentaire, une politique de mesure ou un regime.

## d_mu

Definition:

```text
d_mu(theta_1, theta_2) = |mu(theta_1) - mu(theta_2)|
```

Role: pseudometrique induite par la marge.

Important:

- deux configurations differentes peuvent avoir le meme `mu`;
- donc `d_mu` peut valoir 0 sans que les configurations soient identiques.

## T_mu

Role: topologie induite par `d_mu`.

Lecture etudiante:

- elle voit les differences de marge;
- elle ne voit pas forcement les differences structurelles cachees;
- sa continuite de `mu` est une propriete de construction.

## Gamma et Pi

Role: composants structurels symboliques.

Lecture etudiante:

- leurs observables doivent etre fixes pour devenir pleinement operatoires;
- ils rappellent qu'une configuration ne se reduit pas toujours a `mu`.

## D

Role: operateur correctif ou validation run controle.

Lecture etudiante:

- `D` represente l'action de correction;
- son effet doit etre mesure;
- une correction sans baseline ne prouve rien.

## Claim

Un claim est une affirmation a classer.

Question minimale:

```text
Quel observable, quelle methode, quelle fenetre, quel baseline, quelle incertitude, quelle condition d'echec ?
```

Sans reponse, le claim reste non etabli ou provisoire.
