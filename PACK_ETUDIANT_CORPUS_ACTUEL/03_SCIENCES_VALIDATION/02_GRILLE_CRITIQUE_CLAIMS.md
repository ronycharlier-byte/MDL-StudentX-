# Grille critique des claims

## Usage

Cette grille sert a evaluer une affirmation avant de la publier, l'enseigner ou l'utiliser dans une note academique.

## Grille courte

| Question | Oui | Non | Note |
|---|---:|---:|---|
| Le claim a-t-il une source ? |  |  |  |
| Le niveau documentaire est-il clair ? |  |  |  |
| Le domaine est-il defini ? |  |  |  |
| Les variables sont-elles observables ? |  |  |  |
| La methode est-elle rejouable ? |  |  |  |
| Le baseline est-il declare ? |  |  |  |
| L'incertitude est-elle mentionnee ? |  |  |  |
| La condition d'echec est-elle explicite ? |  |  |  |
| La validation est-elle interne ou externe ? |  |  |  |
| Le claim evite-t-il la surpromesse ? |  |  |  |

## Verdict

| Score | Verdict |
|---:|---|
| 0-3 | non etabli |
| 4-6 | hypothese ou support interne |
| 7-8 | candidat prudent |
| 9-10 | claim robuste localement |

Le score ne suffit pas. Une absence de baseline ou d'incertitude bloque la promotion forte.

## Corrections typiques

Claim trop fort:

```text
Le systeme prouve sa robustesse.
```

Version academique:

```text
Les sources internes proposent un protocole de robustesse interne. La robustesse externe reste a valider sur materiel independant avec baseline et incertitude.
```

Claim trop vague:

```text
Le modele ameliore la qualite.
```

Version testable:

```text
Sur le snapshot S, la methode M augmente le taux de citations correctement resolues de delta par rapport au baseline B, avec condition d'echec E.
```

Claim mathematique surinterprete:

```text
La pseudometrique garantit l'identite des configurations.
```

Correction:

```text
La pseudometrique identifie les configurations par marge. Elle ne garantit pas leur identite structurelle.
```

## Phrase de prudence

```text
Cette formulation est acceptable comme hypothese pedagogique, mais elle ne doit pas etre presentee comme validation externe tant que le protocole preregistre, le baseline, l'incertitude et la replication ne sont pas executes.
```
