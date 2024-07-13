# Noisegen

All sub-commands are under `//eznoisegen`  (`//noisegen`, `//ng`) \
e.g `//ng heightmap`

## `//eznoisegen ...`

### heightmap

<details>



<summary>Heightmap (2D)</summary>

**`//eznoisegen heightmap <palette> <noise> [height] [-z <zoom>] [-s <seed>] [-o <offset>] [-ct]`**

* **Palette**:  Spécifie la palette de blocs à utiliser.&#x20;
* **Noise**: définit le préréglage de noise à utiliser.&#x20;
* **Height** (par défaut: 0): contrôle la hauteur à partir du bas de votre sélection. Une valeur de 0 correspond à la hauteur de la sélection.
  _Vous pouvez placer des blocs au-dessus de la sélection si la hauteur est suffisamment grande._&#x20;&#x20;
* **-z** (par défaut: 1): ajuste le niveau de zoom du noise.&#x20;
* **-s** (par défaut: -1): définit la valeur de départ du noise.&#x20;
* **-o** (par défaut: (0,0,0)): décale les coordonnées de génération de noise par un vecteur donné (X,Y,Z).&#x20;
* **-c**:  Lorsqu'il est utilisé, centre la génération de noise sur les coordonnées mondiales de la sélection.&#x20;
* **-t**:  Active le mode lisse, spécifiquement pour les blocs de neige, d'eau et de lave dans la palette \[Applicable uniquement en mode carte de hauteur].

</details>

### terrain

<details>



<summary>Terrain (3D)</summary>

**`//eznoisegen terrain <palette> <noise> [height] [strength] [-z <scale>] [-s <seed>] [-l <smear>] [-o <offset>] [-chnt]`**

* **Palette**:  Spécifie la palette de blocs à utiliser.&#x20;
* **Noise**: définit le préréglage de noise à utiliser.&#x20;
* **Height** (par défaut: 0): contrôle la hauteur à partir du bas de votre sélection. Une valeur de 0 correspond à la hauteur de la sélection.
  _Vous pouvez placer des blocs au-dessus de la sélection si la hauteur est suffisamment grande_&#x20;
* **Strength** (par défaut: 1,0.5,0): prend jusqu'à 3 valeurs séparées par des virgules qui contrôlent l'intensité du noise à différentes hauteurs :
  - *`0.5` il y aurait 50 % de force partout*
  - *`0.7,0` il y aurait 70 % de force tout en bas et 0 % en haut, avec tout ce qui se trouve entre les deux étant une transition en douceur*
  - *`0,1,0` il y aurait 0 % de force en bas, 100 % au milieu et 0 % en haut&#x20;*
* **-z** (par défaut: 1): ajuste le niveau de zoom du noise.&#x20;
* **-s** (par défaut: -1): définit la valeur de départ du noise.&#x20;
* **-l** (par défaut: 0): applique un frottis vertical au noise 3D.&#x20;
* **-o** (par défaut: (0,0,0)): décale les coordonnées de génération de noise par un vecteur donné (X,Y,Z).&#x20;
* **-c**:  Lorsqu'il est utilisé, centre la génération de noise sur les coordonnées mondiales de la sélection.

</details>

### advanced

<details>


<summary>Advanced</summary>

**`//eznoisegen <palette> <noise> [lowerThreshold] [upperThreshold] [-z <scale>] [-s <seed>] [-l <smear>] [-o <offset>] [-chnt]`**

* **Palette**:  Spécifie la palette de blocs à utiliser.&#x20;
* **Noise**: définit le préréglage de noise à utiliser.&#x20;
* **Lower Threshold** (par défaut: 0):  définit le seuil inférieur pour la génération de noise, avec prise en charge des expressions WorldEdit (plage : 0-1,0).&#x20;
* **Upper Threshold** (par défaut: 0.5): définit le seuil supérieur pour la génération de noise, avec prise en charge des expressions WorldEdit (plage : 0-1,0).&#x20;
* **-z** (par défaut: 1):  ajuste le niveau de zoom du noise.&#x20;
* **-s** (par défaut: -1): définit la valeur de départ du noise.&#x20;
* **-l** (par défaut: 0): applique un frottis vertical au noise 3D.&#x20;
* **-o** (par défaut: (0,0,0)): décale les coordonnées de génération de noise par un vecteur donné (X,Y,Z).&#x20;
* **-c**: Lorsqu'il est utilisé, centre la génération de noise sur les coordonnées mondiales de la sélection.&#x20;
* **-h**: active le mode Heightmap à l'aide du noise 2D. \
  _Le mode Heightmap est uniquement compatible avec les types de régions Cuboid, Cylinder ou Polygon._
* **-n**: utilise des coordonnées normalisées (-1 à 1) centrées sur la sélection pour la génération de noise.
* **-t**: Active le mode lisse, spécifiquement pour les blocs de neige, d'eau et de lave dans la palette \[Applicable uniquement en mode carte de hauteur].

</details>