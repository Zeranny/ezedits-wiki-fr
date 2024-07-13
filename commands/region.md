# Region

Une collection diverse de commandes qui fonctionnent dans la région sélectionnée.

### `//ezvines`

<details>

<summary>Vines</summary>

**`//ezvines <mask> <pattern> [percentage] [min_length] [max_length]`**

**`Alias: //vines`**

* **Mask**: Spécifie le masque correspondant aux blocs sur lesquels accrocher les « vignes ».&#x20;
* **Pattern**: Détermine le motif des blocs à placer.&#x20;
* **Percentage** (par défaut: 10%): définit le pourcentage de blocs sur lesquels suspendre les vignes.&#x20;
* **Min Length** (par défaut: 2): spécifie la longueur minimale de la vigne.&#x20;
* **Max Length** (par défaut: 5): définit la longueur maximale de la vigne.

<img src="../.gitbook/assets/ezvines_mask.gif" alt="" data-size="original"> **`<mask>`**

<img src="../.gitbook/assets/ezvines_percentage.gif" alt="" data-size="original"> **`[percentage]`**

<img src="../.gitbook/assets/ezvines_length.gif" alt="" data-size="original"> **`[min_length] [max_length]`**

</details>

### `//ezmoss`

<details>

<summary>Moss</summary>

**`//ezmoss <pattern> [amount] [smooth_radii] [smooth_iterations]`**

**`Alias: //moss`**

* **Pattern**:  Détermine le motif de bloc à utiliser pour la mousse.&#x20;
* **Amount** (par défaut: 2.0):indique la quantité de mousse à placer. Les valeurs décimales sont autorisées et les valeurs sont quelque peu arbitraires.&#x20;
* **Smooth Radii** (par défaut: 1):  définit les rayons de lissage pour le placement de la mousse. Il peut s'agir d'un rayon ou de trois rayons séparés par des virgules, dans l'ordre Est/Ouest, Haut/Bas, Nord/Sud.&#x20;
* **Smooth Iterations** (par défaut: 5): définit le nombre d'itérations de lissage à appliquer.

<img src="../.gitbook/assets/ezmoss_amount.gif" alt="" data-size="original"> **`[amount]`**

<img src="../.gitbook/assets/ezmoss_radius.gif" alt="" data-size="original"> **`[smooth_radii]`**

<img src="../.gitbook/assets/ezmoss_radii.gif" alt="" data-size="original"> **`[smooth_radii]`**

<img src="../.gitbook/assets/ezmoss_iterations.gif" alt="" data-size="original"> **`[smooth_iterations]`**

</details>

### `//ezslabmerge`

<details>

<summary>SlabMerge</summary>

**`//ezslabmerge <mask> [-b] [-t]`**

**`Alias: //slabmerge`**

* **Mask**: Spécifie le masque pour sélectionner les blocs à affecter dans la région.&#x20;
* **-b**: Lorsqu'il est utilisé, convertira également les dalles inférieures en blocs complets.&#x20;
* **-t**:  Lorsqu'il est utilisé, convertira également les dalles supérieures en blocs complets.&#x20;

</details>

### `//ezstatecyle`

<details>

<summary>StateCycle</summary>

**`//ezstatecycle <mask> <state>`**

**`Alias: //statecycle`**

* **Mask**: Spécifie le masque pour sélectionner les blocs à affecter dans la région.&#x20;
* **State**:  identifie la valeur d’état du bloc à parcourir pour chaque bloc de la sélection.

</details>
