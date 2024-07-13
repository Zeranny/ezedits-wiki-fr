# Motifs

### `#aim`

<details>

<summary>#aim Pattern</summary>

Prend le bloc que le joueur vise comme motif.

<img src="../.gitbook/assets/aimPattern.gif" alt="" data-size="original">

</details>

### `#eznoise`

<details>

<summary>#eznoise Pattern</summary>

**`#eznoisepattern[palette][noisePreset][<scale>][<seed>]`**\
**Alias: `#eznp`**

Utilise des valeurs prédéfinies de bruit pour renvoyer des blocs de palette.\
**Qui possède également les préréglages intégrés suivants :**

* **`#ridged[palette][<scale>][<seed>]`**
* **`#smoothcells[palette][<scale>][<seed>]`**&#x20;
* **`#voronoiedge[palette][<scale>][<seed>]`**

</details>

### `#vectorgradient`

<details>

<summary>#vectorgradient Pattern</summary>

**`#vectorgradientpattern[palette][vector][distance][<noisePreset>][<noiseScale>][<noiseSeed>]`**\
**Alias: `#vgradientp`**

Définit des blocs de palette le long d'un vecteur avec une longueur de distance donnée, le bloc étant choisi en fonction de la distance plus un facteur de fusion. Peut également utiliser des préréglages de bruit.

</details>

### `#selection`

<details>

<summary>#selection Pattern</summary>

**`#selection[selection][<offset>]`**

Sténographie: **`#sel[selection][<offset>]`**

SDéfinit des blocs en utilisant les blocs actuellement présents dans le monde à l'emplacement de la sélection enregistrée. Agit comme si la sélection était en mosaïque/empilée.

Variable facultative `<offset>` pour décaler le motif par un vecteur donné.

</details>



### `#palette`

<details>

<summary>#palette Pattern</summary>

**`#palette[palette]`**

Prend la palette donnée et renvoie une liste de blocs de palette. Peut être utilisé comme modèle de bloc aléatoire.

par exemple `//set #palette[##ice]` est le même que `//set [blue_ice,packed_ice,ice]`

</details>
