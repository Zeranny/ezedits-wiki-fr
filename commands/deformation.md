# Déformation

Toutes les sous-commandes sont sous `//ezdeform`  (`//ezd`) \
par exemple `//ezdeform hexagonalize`

## `//ezdeform ...`

### `hexagonalize`

<details>

<summary>Hexagonalize</summary>

**`//ezdeform hexagonalize [size] [air_gap] [x_rotation] [z_rotation] [offset_angle]`**&#x20;

* **Taille** (par défaut: 12): définit la taille des hexagones.&#x20;
* **Espace d'air** (par défaut: 0.0): définit la largeur de l'espace d'air entre les colonnes.&#x20;
* **Rotation X** (par défaut: 0.0):définit l'angle de rotation de la colonne le long de l'axe X, en degrés.&#x20;
* **Rotation Z** (par défaut: 0.0):définit l'angle de rotation de la colonne le long de l'axe Z, en degrés.&#x20;
* **Angle de décalage** (par défaut: 60.0): ajuste l'angle de décalage, contrôlant la forme (plage : 0 à 90 degrés).

</details>

### `noise`

<details>

<summary>Noise</summary>

**`//ezdeform noise <noise> [strength] [-z <scale>] [-s <seed>]`**

* **Noise**: Spécifie le type de noise à utiliser pour la déformation.&#x20;
* **Force** (par défaut: 2.0): définit la force de l’effet de noise.&#x20;
* **échelle** (par défaut: 1): détermine l’échelle du noise.&#x20;
* **-s** (par défaut: -1): valeur de départ facultative pour le modèle de noise.&#x20;
* **-h**: Lorsqu'il est utilisé, déforme uniquement la région horizontalement.&#x20;
* **-v**: Lorsqu'il est utilisé, déforme uniquement la région verticalement.

</details>

### `rotate`

<details>

<summary>Rotate</summary>

**`//ezdeform rotate <angle> [-o]`**&#x20;

* **Angle**: définit l'angle de rotation, en degrés.&#x20;
* **-o**: Lorsqu'il est utilisé, utilise la position du joueur comme centre de rotation au lieu du centre de la sélection.

</details>

### `voronoialize`

<details>

<summary>Voronoialize</summary>

**`//ezdeform voronoialize [size] [air_gap] [-s <seed>]`**

* **Taille** (par défaut: 12): détermine la taille des cellules de Voronoï.&#x20;
* **espace d'air** (par défaut: 0.0): spécifie la largeur de l'espace d'air entre les cellules.&#x20;
* **-s** (par défaut: -1): graine facultative pour générer le motif.

</details>

### `voronoialize2`

<details>

<summary>nom de l'espace réservé</summary>

**`//ezdeform voronoialize2 <amount> [air_gap] [-s <seed>] [-r <seed_repulsion>] [-n <normalOffset>]`**

* **montant**: Spécifie le montant de la cellule dans le modèle Voronoi.&#x20;
* **espace d'air** (par défaut: 0.0): détermine la largeur de l'espace d'air entre les cellules.&#x20;
* **-s** (par défaut: -1): graine facultative pour générer le motif.&#x20;
* **-r** (par défaut: 15): définit le facteur de répulsion du point de départ de Voronoi.&#x20;
* **-n** (par défaut: 5): ajuste le facteur de décalage normal, qui peut être diminué pour les formes plus fines.

</details>

### `voxelize`

<details>

<summary>Voxelize</summary>

**`//ezdeform voxelize <scales> <gap> <distortion> [-i <primary>] [-j <secondary>] [-s <seed>] [-hv]`**

* **échelles** (par défaut: 3,3,3): définit l'échelle pour chaque dimension.&#x20;
* **Espace** (par défaut: 0.0): définit la largeur de l’espace d’air entre les voxels.
* **Distortion** (par défaut: 0.0): ajuste la force de la distorsion aléatoire de la grille (plage : 0-1).&#x20;
* **-i** (par défaut: y): spécifie l’axe principal pour la rotation de la grille.&#x20;
* **-j** (par défaut: -x):  spécifie l’axe secondaire pour la rotation de la grille.&#x20;
* **-s** (par défaut: -1):  graine facultative pour la distorsion aléatoire.&#x20;
* **-h**: Lorsqu'il est utilisé, voxélise uniquement horizontalement.&#x20;
* **-v**: Lorsqu'il est utilisé, voxélise uniquement verticalement.

</details>
