# 🌪️ Résolution numérique des équations de Navier-Stokes incompressible appliquée à une cavité entraînée 2D et aux instabilités de Rayleigh-Bénard

Projet scientifique — INSA Rouen Normandie - Energétique et propulsion 3 — 2025-2026

## Présentation

Les équations de **Navier-Stokes** permettent de décrire le mouvement des fluides en prenant en compte les effets de la pression, de la viscosité et des forces volumiques. Elles sont obtenues à partir des principes de conservation de la **masse** et de la **quantité de mouvement**.

Dans le cas d’un fluide incompressible, elles s’écrivent notamment sous la forme :

```math
\nabla \cdot \vec{u} = 0
```

```math
\frac{\partial \vec{u}}{\partial t}
+ (\vec{u}\cdot\nabla)\vec{u}
= -\frac{1}{\rho}\nabla p
+ \nu\nabla^2\vec{u}
```
### Variables utilisées

<div align="center">

| Symbole | Description |
|:---:|:---|
| $\vec{u}$ | Champ de vitesse |
| $p$ | Pression |
| $\rho$ | Masse volumique |
| $\nu$ | Viscosité cinématique |

</div>

Dans cette étude, nous nous intéressons dans un premier temps à la **résolution numérique des équations de Navier-Stokes dans une cavité entraînée bidimensionnelle**. Le domaine est constitué d’une cavité fermée dont la paroi supérieure se déplace horizontalement à vitesse constante, tandis que les autres parois restent immobiles. Le mouvement de la paroi supérieure entraîne progressivement le fluide et génère un écoulement caractérisé notamment par la formation de **tourbillons**. Dans la réalité, une telle cavitée peut s’apparenter à un renfoncement de forme carrée présent le long d’une conduite de fluide.

Puis dans un second temps, l'étude portera sur la **résolution numérique des équations de Navier-Stokes appliquées aux instabilités de Rayleigh-Bénard**. Le domaine étudié est constitué d’une cavité fermée contenant un fluide, dont la paroi inférieure est maintenue à une température élevée tandis que la paroiz supérieure est maintenue à une température plus faible. Cette différence de température crée un **gradient thermique** vertical au sein du fluide.  
Ainsi ce gradient engendre des variations de masse volumique et donc des **forces de flottabilité**, à l’origine de la mise en mouvement du fluide.
Les équations de Navier-Stokes sont alors couplées à une **équation de transport de la température**. Dans l’approximation de Boussinesq, la variation de masse volumique est prise en compte uniquement dans le terme de poussée d’Archimède.

## Objectifs

- Étudier et comprendre les équations de Navier-Stokes;
- Appliquer ces équations au problème de la cavité entrainée en 2D;
- Développer un code fortran permettant de résoudre numériquement les équations équations de Navier-Stokes dans une cavité entraînée bidimensionnelle ;
- Observer les champs de **vitesse, de pression et de température** résultants ;
- Analyser l’influence des paramètres physiques, notamment du **nombre de Reynolds**, sur la structure de l’écoulement.

## Principaux résultats


### Cavité entrainée

### Instabilités de Rayleigh-Bénard


## Équipe

Projet réalisé à l'INSA Rouen Normandie dans le cadre du projet scientifique EP3.

- Raphaël Thivent
- Etienne Oblin

Enseignant-responsable : **Pierre Bénard**

