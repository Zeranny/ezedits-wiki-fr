---
description: Diffuseur de forme de surface
---

# Scatter

la commande `//ezscatter` (`//ezsc`)  disperse une forme sur la surface des blocs dans votre sélection.

Il est livré avec un certain nombre de formes prédéfinies ainsi que la possibilité d'utiliser des expressions WorldEdit pour définir votre propre forme.

{% code overflow="wrap" %}
```
//ezscatter [-s <dimensions>] [-o <sizeMultiplier>] [-n <density>] [-c <angleDeg>] [-k <rotationAxis>] [-i <primaryAxis>] [-j <secondaryAxis>] [-d <filterDirections>] [-e <filterThreshold>] [-m <maskFilter>] [-p <palette>] <shape> [-a] [-b] [-r] [-u] [-w]
```
{% endcode %}

<details>

<summary><mark style="color:red;"><strong>&#x3C;shape></strong></mark></summary>

**Formes actuelles**

_Des paramètres supplémentaires sont indiqués entre parenthèses après une forme._

* bean
* cube
* curl
* cylinder
* ellipsoid
* fur
* leaf
* lemon
* onion
* polygon(*cotés*)
* pyramid(*cotés*)
* spike
* supersphere(*exposant*)
* tetrahedron
* torus(*épaisseur*)

En plus de cela, vous pouvez également définir votre propre forme avec une expression WorldEdit

**`Expression;<expression>`**
or
**`Expr;<expression>`**

Par exemple, cette expression créera des spirales :\
`//ezsc expr;x+=sin(2*pi*y)/2;z+=cos(2*pi*y)/2;x*x+z*z<0.3^2`



</details>

* **Shape**:  Spécifie le type de forme à disperser.
* **-s** (par défaut: "20"): définit la taille des formes à disperser. Vous pouvez spécifier une taille pour les formes uniformes ou trois pour (X, Y, Z).
* **-o** (par défaut: "0.8"): contrôle la différence de taille entre les ensembles de formes. Définissez la valeur sur 1 pour un dimensionnement constant.
* **-n** (par défaut: "2.0%"):  contrôle la densité de dispersion des formes dans la région, en pourcentage.
* **-c** (par défaut: "0"):  spécifie l’angle de rotation des formes.
* **-k** (par défaut: "up"): détermine l'axe autour duquel la forme pivote.\
  Si **CONSTANT**:
  * **-i** (par défaut: "y"): définit l’axe principal pour l’orientation de la forme.
  * **-j** (par défaut: "x"): définit l’axe secondaire pour l’orientation de la forme.
* **-d**:  Limite le placement à des directions spécifiques.
  * **-e** (par défaut: "0.5"): renforce ou affaiblit l’effet du filtre directionnel.
* **-m**:  limite le placement de la forme aux blocs de surface correspondant au masque spécifié.
* **-p**:  choisit la palette de blocs à utiliser pour les formes dispersées. Si elle n'est pas définie, utilise les blocs existants.
* **-a**:Ne placera pas d'air si cette option est activée.
* **-b**: ignore le placement des formes qui tombent partiellement en dehors de la région.
* **-r**: Aligne les formes avec la normale de la surface.
* **-u**: désactive la distribution uniforme des points de départ, permettant des placements de formes plus aléatoires.
* **-w**: Supprime la forme d'origine, ne laissant que les formes dispersées.
