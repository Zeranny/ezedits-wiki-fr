# Masques

### `#near`

<details>

<summary>#near Mask</summary>

**`#near[mask][distance]`**\
**`#near[mask][minDistance][maxDistance]`**\
\
Masque tous les blocs dans une distance sphérique (euclidienne) donnée d'un masque. Ne modifie pas les blocs qui correspondent à la distance intérieure `mask`.\ également être défini pour exclure les blocs plus proches que la distance minimale.\


![](../.gitbook/assets/mask\_near\_mask.gif) **`[mask]`**

<img src="../.gitbook/assets/mask_near_max.gif" alt="" data-size="original"> **`[distance]`**

<img src="../.gitbook/assets/mask_near_min_max.gif" alt="" data-size="original"> **`[minDistance][maxDistance]`**

</details>

### `#aim`

<details>

<summary>#aim Mask</summary>

Prend le bloc que le joueur vise comme masque.

<img src="../.gitbook/assets/aimMask.gif" alt="" data-size="original">

</details>

### `#blocklight`

<details>

<summary>#blocklight Mask</summary>

**`#blocklight[lightLevel]` or `#blocklight[minLevel][maxLevel]`**

Masque les blocs d'un bloc lumineux donné (éclairage fourni par des sources lumineuses autres que la lumière du ciel). Prend éventuellement un niveau de lumière minimum et maximum, correspondant à n'importe quel niveau dans cette plage.

</details>

### `#truelight`

<details>

<summary>#truelight Mask</summary>

**`#truelight[lightLevel]` or `#truelight[minLevel][maxLevel]`**

Masque les blocs d'un niveau de lumière total donné (éclairage fourni par toutes les sources de lumière, y compris la lumière du ciel). Prend éventuellement un niveau de lumière minimum et maximum, correspondant à n'importe quel niveau dans cette plage.

</details>

### `#eznoise`

<details>

<summary>#eznoise Mask</summary>

**`#eznoisemask[noisePreset][<scale>][<threshold>][<seed>]`**\
**Alias: `#eznm`**

Utilise des valeurs de bruit prédéfinies `0.0-1.0` pour faire correspondre les blocs au-dessus d'un seuil de bruit donné.

</details>

### `#vectorgradient`

<details>

<summary>#vectorgradient Mask</summary>

**`#vectorgradientmask[vector][distance][<noisePreset>][<noiseScale>][noiseSeed]`**

Sténographie: `#vgradientm`

Masque les blocs le long d'un vecteur avec une longueur de distance donnée. Avec des blocs plus proches, il est plus probable de passer le test de masque. Compatible avec les préréglages de bruit.

</details>

### `#attached`

<details>

<summary>#attached mask</summary>

**`#attached[<vector,vector,vector ...>]`**

Masques pour blocs qui sont attachés à au moins 1 bloc non aérien adjacent.

Prend éventuellement une liste de vecteurs de direction à vérifier au lieu de chaque côté. \
par exemple`#attached[up,down,left,north]`

\
Dans les deux cas, attaché signifie que le bloc « touche » le bloc adjacent. Ainsi, une dalle inférieure ne passerait pas `#attached[up]` alors qu'une lanterne avec l'état  `[hanging=true]` le ferait.

</details>

### `#fullblock`

<details>

<summary>#fullblock mask</summary>

Masques pour blocs qui remplissent tout l'espace d'un cube.

Par exemple, 1 à 7 couches de neige ne passeront pas, mais 8 couches de neige, un bloc comme de la pierre ou un bloc transparent comme du verre passeront.

</details>

### `#palette`

<details>

<summary>#palette mask</summary>

**`#palette[palette][<strict>]`**

Masques de blocs qui correspondent à n'importe quel bloc de la palette.

Valeur facultative `<strict>` de True ou False pour déterminer si les données du bloc doivent également correspondre.\
par exemple, `oak_stairs[facing=east]` ne correspondra que  `oak_stairs[facing=west]` si strict est défini sur **False**.

</details>

### `#fuzzypalette`

<details>

<summary>#fuzzypalette mask</summary>

**`#fuzzypalette[palette]`**

Sténographie: **`#fpalette`**

Masques de blocs qui correspondent à n'importe quel bloc de la palette, quelles que soient les données du bloc. Équivalent à **`#palette[palette][False]`**

</details>
