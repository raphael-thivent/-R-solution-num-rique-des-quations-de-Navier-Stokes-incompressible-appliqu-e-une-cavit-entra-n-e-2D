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
- Appliquer ces équations au problème de la cavité entrainée en 2D et aux instabilités;
- Développer un code fortran permettant de résoudre numériquement les équations équations de Navier-Stokes dans une cavité entraînée bidimensionnelle;
- Observer les champs de **vitesse, de pression et de température** résultants;
- Analyser l’influence des paramètres physiques, notamment du **nombre de Reynolds**, sur la structure de l’écoulement;
- Appliquer ces équations aux instabilités de Rayleigh-Bénard;
- Implémenter sa résolution numérique en fortran;
- Observer l'apparition de cellules convectives;
- Analyser l'influence du  **nombre de Rayleigh**, notamment trouver un Ra critique à partir duquel les cellules convectives apparaissent.

## Implementation 

L’implémentation en Fortran repose d’abord sur une discrétisation spatiale et temporelle des équations de Navier-Stokes. Plusieurs schémas sont utilisés pour les termes convectifs : centré d’ordre 2, centré d’ordre 4 et upwind. L’avancement temporel est réalisé avec un schéma d’Euler explicite. La pression est obtenue en résolvant une équation de Poisson grâce à une méthode itérative de Jacobi, puis les vitesses sont corrigées à partir du gradient de pression. Pour Rayleigh-Bénard, le code est ensuite adapté avec l’équation de la température, le terme de Boussinesq, des conditions périodiques en x et une perturbation initiale de température.

## Principaux résultats

### Cavité entrainée
Les résultats montrent un écoulement principalement organisé autour d’un vortex central, entraîné par le mouvement du couvercle supérieur. La vitesse horizontale \(u\) est maximale au niveau du couvercle, tandis que la vitesse verticale \(v\) traduit la circulation du fluide dans la cavité. Le champ de pression reste globalement faible, avec des variations principalement localisées près des zones où l’écoulement est fortement accéléré. Enfin, la norme de la vitesse met clairement en évidence la structure tourbillonnaire principale et les zones de plus forte vitesse près de la paroi supérieure.  

En faisant une étude en variant le nombre de Reynolds, nous observons qu'en augmentant le Re le centre de vortex se décale dans la direction de la vitesse. Cela est cohérent et souligne que les forces d’inertie prennent le dessus par rapport aux forces visqueuses.

### Instabilités de Rayleigh-Bénard
Dans un premier temps, une étude à Ra = 10 a été effectuée. Nous observons une évolution linéaire de la température, ainsi qu’une vitesse résultante nulle. Dans ces conditions, notre système peut être considéré comme conductif, sans mouvement convectif assimilable à un solide.

Enfin, une étude en fonction du nombre de Rayleigh montre l’apparition de cellules convectives pour des valeurs élevées de Ra. Ces cellules apparaissent à partir d’un nombre de Rayleigh critique d’environ 1400. Ce nombre critique n’est cependant pas universel : il dépend du système étudié et des conditions aux limites considérées.

## Documents

### Rapport

[Consulter le rapport complet](report/Rapport_Proj-scientifique_2026.pdf)

Le rapport présente l'ensemble de la démarche, de l'étude des équations de Navier-Stokes jusqu'à la résolution numérique des problèmes de cavité entraînée ainsi que des instabilités de Rayleigh-Bénard, avec l'analyse des résultats obtenus.


## Équipe

Projet réalisé à l'INSA Rouen Normandie dans le cadre du projet scientifique EP3.

- Raphaël Thivent
- Etienne Oblin

Enseignant-responsable : **Pierre Bénard**

