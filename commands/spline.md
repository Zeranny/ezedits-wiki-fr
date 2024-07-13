# Spline

Toutes les sous-commandes sont sous `//ezspline`  (`//ezsp`) \
par exemple `//ezspline beads`

_Notez que chaque spline ne peut être exécutée qu'avec un type de sélection convexe (\`//sel convex\`)._

## `//ezspline ...`

### `beads`

<details>

<summary>Bead Spline</summary>

**`//ezsp beads <pattern> <radii> [-p <kb_parameters>] [-q <quality>]`** \
**`[-n <normalMode>] [-g] [-h]`**

Génère une spline en forme de perles le long de la région convexe sélectionnée.

* **Pattern**: spécifie le modèle de bloc.
* **Radii**:  l'épaisseur de la spline, définie par un maximum de trois valeurs séparées par des virgules.\
  _ Un rayon de 10 sera de 10 du début à la fin de la spline, 10,5,15 commenceront à 10, diminueront à 5 vers le milieu et augmenteront à 15 à la fin._
* **-p** (par défaut : "0:0:0"): définit les paramètres du flux de la spline, y compris la tension, la polarisation et la continuité, fournis dans un format séparé par deux points.
* **-q** (par défaut : 1.85):  ajuste la qualité de la génération de splines. Augmentez cette valeur pour réduire les espaces vides, en notant que des valeurs plus élevées augmentent le temps de traitement.
* **-n** (par défaut : "CONSISTENT"): détermine le mode de calcul normal de la spline.
* **-g**: Lorsqu'il est utilisé, calcule les rayons centraux en utilisant le centre géométrique pour trois rayons.
* **-h**: Affiche la page d'aide.
</details>

### `chainlink`

<details>

<summary>Chain Link Spline</summary>

**`//ezsp chainlink <pattern> <radii> [inner] [offset] [stretch] [spin] [-p <kb_parameters>] [-q <quality>] [-n <normalMode>] [-g] [-h]`**

Génère une spline en forme de maillon de chaîne le long de la région convexe sélectionnée.

* **Pattern**: spécifie le modèle de bloc.
* **Radii**: l'épaisseur de la spline, définie par un maximum de trois valeurs séparées par des virgules.\
  _Un rayon de 10 sera de 10 du début à la fin de la spline, 10,5,15 commenceront à 10, diminueront à 5 vers le milieu et augmenteront à 15 à la fin._
* **Inner** (par défaut : 1.0):  le rapport du rayon intérieur de chaque lien.
* **Offset** (par défaut : 0.0):  montant de décalage de chaque lien, ajustant l'alignement des liens de la chaîne.
* **Stretch** (par défaut : 1.0):  la quantité d'étirement des maillons individuels le long de la chaîne.
* **Spin** (par défaut : 0.0): ajoute une torsion à la spline.
* **-p** (par défaut : "0:0:0"):  définit les paramètres du flux de la spline, y compris la tension, la polarisation et la continuité, fournis dans un format séparé par deux points.
* **-q** (par défaut : 1.85): ajuste la qualité de la génération de splines. Augmentez cette valeur pour réduire les espaces vides, en notant que des valeurs plus élevées augmentent le temps de traitement.
* **-n** (par défaut : "CONSISTENT"): détermine le mode de calcul normal de la spline.
* **-g**: Lorsqu'il est utilisé, calcule les rayons centraux en utilisant le centre géométrique pour trois rayons.
* **-h**: Affiche la page d'aide.

</details>

### `cubes`

<details>

<summary>Cube Spline</summary>

**`//ezsp cubes <pattern> <radii> [gap] [-p <kb_parameters>] [-q <quality>] [-n <normalMode>] [-g] [-h]`**

Génère une spline à partir de cubes le long de la région convexe sélectionnée.

* **Pattern**: spécifie le modèle de bloc.
* **Radii**:  l'épaisseur de la spline, définie par un maximum de trois valeurs séparées par des virgules.\
  _ Un rayon de 10 sera de 10 du début à la fin de la spline, 10,5,15 commenceront à 10, diminueront à 5 vers le milieu et augmenteront à 15 à la fin._
* **Gap** (par défaut : 1.0): définit l’écart entre les cubes.
* **-p** (par défaut : "0:0:0"): définit les paramètres du flux de la spline, y compris la tension, la polarisation et la continuité, fournis dans un format séparé par deux points.
* **-q** (par défaut : 1.85): ajuste la qualité de la génération de splines. Augmentez cette valeur pour réduire les espaces vides, en notant que des valeurs plus élevées augmentent le temps de traitement.
* **-n** (par défaut : "CONSISTENT"): détermine le mode de calcul normal de la spline.
* **-g**: Lorsqu'il est utilisé, calcule les rayons centraux en utilisant le centre géométrique pour trois rayons.
* **-h**: Affiche la page d'aide.

</details>

### `expression`

<details>

<summary>Expression Spline</summary>

**`//ezsp expression <pattern> <radii> [spin] <expression> [-p <kb_parameters>] [-q <quality>] [-n <normalMode>] [-g] [-h]`**

Génère une spline façonnée par l'expression WorldEdit donnée le long de la région convexe sélectionnée.

* **Pattern**: spécifie le modèle de bloc.
* **Radii**:  l'épaisseur de la spline, définie par un maximum de trois valeurs séparées par des virgules.\
  _Un rayon de 10 sera de 10 du début à la fin de la spline, 10,5,15 commenceront à 10, diminueront à 5 vers le milieu et augmenteront à 15 à la fin._
* **Spin** (par défaut : 0): ajoute une torsion à la spline.
* **Expression**:  expression WorldEdit définissant la forme de la spline. Prend en charge « x », « y », « z » comme variables.
* **-p** (par défaut : "0:0:0"): définit les paramètres du flux de la spline, y compris la tension, la polarisation et la continuité, fournis dans un format séparé par deux points.
* **-q** (par défaut : 1.85): ajuste la qualité de la génération de splines. Augmentez cette valeur pour réduire les espaces vides, en notant que des valeurs plus élevées augmentent le temps de traitement.
* **-n** (par défaut : "CONSISTENT"): détermine le mode de calcul normal de la spline.
* **-g**:  Lorsqu'il est utilisé, calcule les rayons centraux en utilisant le centre géométrique pour trois rayons.
* **-h**: Affiche la page d'aide.

Exemple d'une spline d'expression :
`//ezsp expression red 20,5 0 -q 4 z^2+y^2<2-x%2`\
_Notez que l'expression doit venir en dernier_

</details>

### `fishnet`

<details>

<summary>Fishnet Spline</summary>

**`//ezsp fishnet <pattern> <radii> [spacing] [depth] [width] [-p <kb_parameters>] [-q <quality>] [-n <normalMode>] [-g] [-h]`**

Génère une spline en forme de filet de pêche le long de la région convexe sélectionnée.

* **Pattern**: spécifie le modèle de bloc.
* **Radii**:  l'épaisseur de la spline, définie par un maximum de trois valeurs séparées par des virgules.\
  _Un rayon de 10 sera de 10 du début à la fin de la spline, 10,5,15 commenceront à 10, diminueront à 5 vers le milieu et augmenteront à 15 à la fin._
* **Spacing** (par défaut : 10): l'espacement des mailles du filet.
* **Depth** (par défaut : 2): la profondeur de chaque corde dans le filet.
* **Width** (par défaut : 2):  la largeur de chaque chaîne.
* **-p** (par défaut : "0:0:0"): définit les paramètres du flux de la spline, y compris la tension, la polarisation et la continuité, fournis dans un format séparé par deux points.
* **-q** (par défaut : 1.85): ajuste la qualité de la génération de splines. Augmentez cette valeur pour réduire les espaces vides, en notant que des valeurs plus élevées augmentent le temps de traitement.
* **-n** (par défaut : "CONSISTENT"): détermine le mode de calcul normal de la spline.
* **-g**:  Lorsqu'il est utilisé, calcule les rayons centraux en utilisant le centre géométrique pour trois rayons.
* **-h**: Affiche la page d'aide.

</details>

### `noise`

<details>

<summary>Noise Spline</summary>

**`//ezsp noise <pattern> <radii> [strength] [stretch] [spin] <noise> [-p <kb_parameters>] [-q <quality>] [-n <normalMode>] [-g] [-h]`**

Crée une spline basée sur le noise le long de la région convexe sélectionnée.

* **Pattern**: spécifie le modèle de bloc.
* **Radii**:  l'épaisseur de la spline, définie par un maximum de trois valeurs séparées par des virgules.\
  _Un rayon de 10 sera de 10 du début à la fin de la spline, 10,5,15 commenceront à 10, diminueront à 5 vers le milieu et augmenteront à 15 à la fin._
* **Strength** (par défaut : 0.5): détermine la force du noise, affectant l'intensité du noise.
* **Stretch** (par défaut : 4.0): contrôle le facteur d’étirement du noise le long de la spline.
* **Spin** (par défaut : 0): ajoute une torsion à la spline.
* **Noise** (par défaut : `Perlin(Freq:3)`): spécifie le type de noise à utiliser pour la génération.
* **-p** (par défaut : "0:0:0"): définit les paramètres du flux de la spline, y compris la tension, la polarisation et la continuité, fournis dans un format séparé par deux points.
* **-q** (par défaut : 1.85): ajuste la qualité de la génération de splines. Augmentez cette valeur pour réduire les espaces vides, en notant que des valeurs plus élevées augmentent le temps de traitement.
* **-n** (par défaut : "CONSISTENT"): détermine le mode de calcul normal de la spline.
* **-g**:  Lorsqu'il est utilisé, calcule les rayons centraux en utilisant le centre géométrique pour trois rayons.
* **-h**: Affiche la page d'aide.

</details>

### `oscillate`

<details>

<summary>Oscillation Spline</summary>

**`//ezsp oscillate <pattern> <radii> [depth] [interval] [-p <kb_parameters>] [-q <quality>] [-n <normalMode>] [-g] [-h]`**

Génère une spline avec une épaisseur oscillante le long de la région convexe sélectionnée.

* **Pattern**: spécifie le modèle de bloc.
* **Radii**:  l'épaisseur de la spline, définie par un maximum de trois valeurs séparées par des virgules.\
  _Un rayon de 10 sera de 10 du début à la fin de la spline, 10,5,15 commenceront à 10, diminueront à 5 vers le milieu et augmenteront à 15 à la fin._
* **Depth** (par défaut : 2): détermine la profondeur de crête de l'oscillation, affectant l'amplitude des ondes.
* **Interval** (par défaut : 5): définit l'intervalle de crête, contrôlant la fréquence de l'oscillation le long de la spline.
* **-p** (par défaut : "0:0:0"): définit les paramètres du flux de la spline, y compris la tension, la polarisation et la continuité, fournis dans un format séparé par deux points.
* **-q** (par défaut : 1.85): ajuste la qualité de la génération de splines. Augmentez cette valeur pour réduire les espaces vides, en notant que des valeurs plus élevées augmentent le temps de traitement.
* **-n** (par défaut : "CONSISTENT"): détermine le mode de calcul normal de la spline.
* **-g**:  Lorsqu'il est utilisé, calcule les rayons centraux en utilisant le centre géométrique pour trois rayons.
* **-h**: Affiche la page d'aide.

</details>

### `polygon`

<details>

<summary>Polygonal Spline</summary>

**`//ezsp polygon <pattern> <radii> [sides] [spin] [-p <kb_parameters>] [-q <quality>] [-n <normalMode>] [-g] [-h]`**

Crée une spline régulière en forme de polygone le long de la région convexe sélectionnée.

* **Pattern**: spécifie le modèle de bloc.
* **Radii**:  l'épaisseur de la spline, définie par un maximum de trois valeurs séparées par des virgules.\
  _Un rayon de 10 sera de 10 du début à la fin de la spline, 10,5,15 commenceront à 10, diminueront à 5 vers le milieu et augmenteront à 15 à la fin._
* **Sides** (par défaut : 6): détermine le nombre de côtés du polygone.
* **Spin** (par défaut : 0.0): ajoute une torsion à la spline.
* **-p** (par défaut : "0:0:0"): définit les paramètres du flux de la spline, y compris la tension, la polarisation et la continuité, fournis dans un format séparé par deux points.
* **-q** (par défaut : 1.85): ajuste la qualité de la génération de splines. Augmentez cette valeur pour réduire les espaces vides, en notant que des valeurs plus élevées augmentent le temps de traitement.
* **-n** (par défaut : "CONSISTENT"): détermine le mode de calcul normal de la spline.
* **-g**:  Lorsqu'il est utilisé, calcule les rayons centraux en utilisant le centre géométrique pour trois rayons.
* **-h**: Affiche la page d'aide.

</details>

### `rope`

<details>

<summary>Rope Spline</summary>

**`//ezsp rope <pattern> <radii> [ropeCount] [spin] [-p <kb_parameters>] [-q <quality>] [-n <normalMode>] [-g] [-h]`**

Crée une spline en forme de corde le long de la région convexe sélectionnée.

* **Pattern**: spécifie le modèle de bloc.
* **Radii**:  l'épaisseur de la spline, définie par un maximum de trois valeurs séparées par des virgules.\
  _Un rayon de 10 sera de 10 du début à la fin de la spline, 10,5,15 commenceront à 10, diminueront à 5 vers le milieu et augmenteront à 15 à la fin._
* **RopeCount** (par défaut : 3): détermine le nombre de cordes entrelacées.
* **Spin** (par défaut : 2.0): ajoute une torsion à la spline.
* **-p** (par défaut : "0:0:0"): définit les paramètres du flux de la spline, y compris la tension, la polarisation et la continuité, fournis dans un format séparé par deux points.
* **-q** (par défaut : 1.85): ajuste la qualité de la génération de splines. Augmentez cette valeur pour réduire les espaces vides, en notant que des valeurs plus élevées augmentent le temps de traitement.
* **-n** (par défaut : "CONSISTENT"): détermine le mode de calcul normal de la spline.
* **-g**:  Lorsqu'il est utilisé, calcule les rayons centraux en utilisant le centre géométrique pour trois rayons.
* **-h**: Affiche la page d'aide.

</details>

### `simple`

<details>

<summary>Simple Spline</summary>

**`//ezsp simple <pattern> <radii> [-p <kb_parameters>] [-q <quality>]`** \
**`[-n <normalMode>] [-g] [-h]`**

Crée une spline cylindrique simple le long de la région convexe sélectionnée.

* **Pattern**: spécifie le modèle de bloc.
* **Radii**:  l'épaisseur de la spline, définie par un maximum de trois valeurs séparées par des virgules.\
  _Un rayon de 10 sera de 10 du début à la fin de la spline, 10,5,15 commenceront à 10, diminueront à 5 vers le milieu et augmenteront à 15 à la fin._
* **-p** (par défaut : "0:0:0"): définit les paramètres du flux de la spline, y compris la tension, la polarisation et la continuité, fournis dans un format séparé par deux points.
* **-q** (par défaut : 1.85): ajuste la qualité de la génération de splines. Augmentez cette valeur pour réduire les espaces vides, en notant que des valeurs plus élevées augmentent le temps de traitement.
* **-n** (par défaut : "CONSISTENT"): détermine le mode de calcul normal de la spline.
* **-g**:  Lorsqu'il est utilisé, calcule les rayons centraux en utilisant le centre géométrique pour trois rayons.
* **-h**: Affiche la page d'aide.

</details>
