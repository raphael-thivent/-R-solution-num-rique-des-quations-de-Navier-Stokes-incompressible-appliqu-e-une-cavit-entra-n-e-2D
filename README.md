# Introduction

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

Dans cette étude, nous nous intéressons à la **résolution numérique des équations de Navier-Stokes dans une cavité entraînée bidimensionnelle**. Le domaine est constitué d’une cavité fermée dont la paroi supérieure se déplace horizontalement à vitesse constante, tandis que les autres parois restent immobiles. Le mouvement de la paroi supérieure entraîne progressivement le fluide et génère un écoulement caractérisé notamment par la formation de **tourbillons**. Dans la réalité, une telle cavitée peut s’apparenter à un renfoncement de forme carrée présent le long d’une conduite de fluide.

L’objectif est de résoudre numériquement les équations gouvernant cet écoulement afin d’obtenir les champs de **vitesse, de pression et de température**, puis d’analyser l’influence des paramètres physiques, notamment du **nombre de Reynolds**, sur la structure de l’écoulement.
