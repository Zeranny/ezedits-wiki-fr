# Texture

Toutes les sous-commandes sont sous `//eztexture`  (`//ezt`) \
par exemple `//eztexture ambient`

## `//eztexture ...`

### `ambient`

<details>

<summary>Ambient Texture</summary>

**`//ezt ambient <mask> <palette> [radius] [brightness] [contrast]`**

Textures en rapprochant l'ambiance des blocs de la région.

* **Mask**: Blocs à remplacer.
* **Palette**: Spécifie la palette à utiliser.
* **Radius** (par défaut: 3):  le rayon dans lequel la commande évalue les différences ambiantes. Un rayon plus grand prend en compte une zone plus large pour chaque calcul, ce qui conduit à des transitions plus fluides.
* **Brightness** (par défaut: 0.0): ajuste la polarisation vers le début ou la fin de la palette. Des valeurs plus élevées renforcent le début de la palette, tandis que des valeurs plus faibles accentuent la fin.
* **Contrast** (par défaut: 0.0): amplifie ou réduit la différence entre le champ ambiant lissé et les variations locales, améliorant ou adoucissant l'impact de la texture.

</details>

### `axisgradient`

<details>

<summary>Axis Gradient Texture</summary>

**`//ezt axisgradient <mask> <palette> [axis] [-r]`**

Texture une région à l'aide d'un dégradé aligné sur un seul axe.

* **Mask**: Blocs à remplacer.
* **Palette**: Spécifie la palette à utiliser.
* **Axis** (par défaut: "y"): détermine l'axe le long duquel le dégradé est appliqué (« x », « y » ou « z »), guidant la direction du flux du dégradé.
* **-r**: Active le mode de dégradé relatif, étirant la palette sur des colonnes entières.

</details>

### `blend`

<details>

<summary>Blend Texture</summary>

**`//ezt blend <palette> [radius] [-v]`**

Mélange les blocs de palette dans une région.

* **Palette**:  spécifie la palette à utiliser pour le mélange.
* **Radius** (par défaut: "0.5"): détermine le rayon de fusion, affectant la largeur avec laquelle l'effet de fusion est appliqué autour de chaque bloc.
* **-v**: Active le mode de fusion complet, permettant le mélange de blocs non superficiels.

</details>

### `blocklight`

<details>

<summary>Blocklight Texture</summary>

**`//ezt blocklight <mask> <palette> [-v] [-s]`**

Texture une région en fonction des niveaux de lumière des blocs du jeu, à l'exclusion de la lucarne.

* **Mask**: Blocs à remplacer.
* **Palette**: Spécifie la palette à utiliser.
* **-v**:  Lorsqu'il est activé, ne prend en compte que le niveau de lumière directement au-dessus du bloc.
* **-s**:  Lorsqu'il est activé, prendra en compte les niveaux de lumière du ciel.

</details>

### `cells`

<details>

<summary>Cells Texture</summary>

**`//ezt cells <mask> <palette> <amount> [brightness] [contrast] [-s] [-r]`**

Texture une région avec un motif semblable à une cellule.

* **Mask**: Blocs à remplacer.
* **Palette**: Spécifie la palette à utiliser.
* **Amount**: Détermine la quantité de cellules dans la texture.
* **Brightness** (par défaut: 0.0): ajuste la polarisation vers le début ou la fin de la palette. Une valeur plus élevée renforce le début de la palette, une valeur plus faible renforce la fin.
* **Contrast** (par défaut: 0.0): modifie le contraste entre les cellules, améliorant la définition et la séparation du motif.
* **-s** (par défaut: -1): graine facultative pour générer le modèle de cellule.
* **-r** (par défaut: 5):  définit le facteur de répulsion pour les points de départ dans le diagramme de Voronoi, influençant la forme et la distribution des cellules.

</details>

### `curvature`

<details>

<summary>Curvature Texture</summary>

**`//ezt curvature <mask> <palette> [radius] [brightness] [contrast]`**

Texture une région en approchant la courbure.

* **Mask**: Blocs à remplacer.
* **Palette**: Spécifie la palette à utiliser.
* **Radius** (par défaut: 3): spécifie le rayon dans lequel la courbure est calculée, influençant la subtilité ou la proéminence de l'effet.
* **Brightness** (par défaut: 0.0): ajuste la polarisation vers le début ou la fin de la palette. Des valeurs plus élevées renforcent le début de la palette, tandis que des valeurs plus faibles accentuent la fin.
* **Contrast** (par défaut: 0.0): modifie le contraste entre les zones de courbure différente, améliorant ainsi la définition et la séparation du motif.

</details>

### `flow`

<details>

<summary>Flow Texture</summary>

**`//ezt flow <mask> <palette> [exposure] [iterations] [velocity] [paletteScalar] [noise] [-m] [-g] [-f]`**

Génère un effet de champ d'écoulement sur toutes les surfaces de la sélection.

* **Mask**: Blocs à remplacer.
* **Palette**: Spécifie la palette à utiliser.
* **Exposure** (par défaut: 0.6):  contrôle la densité globale des lignes de flux, affectant la quantité de la palette utilisée.
* **Iterations per Line** (par défaut: 32):  le nombre d'étapes nécessaires pour dessiner chaque ligne, avec davantage d'itérations produisant des lignes plus longues.
* **Point Velocity** (par défaut: 0.5): la vitesse à laquelle les points se déplacent sur la surface.
* **Palette Index Scalar** (par défaut: 1.0): met à l'échelle la valeur utilisée pour sélectionner un bloc de palette.
* **Noise** (par défaut: \[Type:Perlin]): le type de noise utilisé pour générer le champ de flux.
* **-m**: Pondération de l'élan du point, mélange des directions de mouvement précédentes.
* **-g**: Applique la gravité aux points, les tirant dans la direction spécifiée.
* **-f**: Remplit les espaces avec le bloc de palette le plus bas.

</details>

### `noise`

<details>

<summary>Noise Texture</summary>

**`//ezt noise <mask> <palette> <noise> [-z] [-s]`**

Texture une région en utilisant un noise donné.

* **Mask**: Blocs à remplacer.
* **Palette**: Spécifie la palette à utiliser.
* **Noise** (par défaut: `Perlin(Freq:0.05)`): définit le noise à utiliser.
* **-z** (par défaut: 1): ajuste l’échelle du noise.
* **-s** (par défaut: -1): valeur de départ facultative pour générer le modèle de noise.

</details>

### `pointlight`

<details>

<summary>Pointlight Texture</summary>

**`//ezt pointlight <mask> <palette> [falloffRange] [radius] [interval] [-l] [-o] [-r][-f]`**

Texture une région en fonction de l'orientation des surfaces par rapport à une source lumineuse.

* **Mask**: Blocs à remplacer.
* **Palette**: Spécifie la palette à utiliser.
* **Falloff Range** (par défaut: 0):  définit la plage de décroissance, qui correspond à la luminosité du point lumineux. Si elle est définie sur 0, la distance entre le joueur et le centre de la région est utilisée.
* **Radius** (par défaut: 1): spécifie le rayon d'approximation normal, affectant la douceur du bord de la lumière.
* **Interval** (par défaut: "0,90"): définit l'intervalle d'orientation de la surface en degrés, où 0 correspond à une orientation directe vers la lumière et 180 à une orientation opposée. Les surfaces situées dans cet intervalle sont texturées et toutes celles situées en dessous ou au-dessus seront texturées avec le premier ou le dernier bloc de palette.
* **-f**: Désactive la diminution de la lumière, en appliquant une intensité lumineuse uniforme sur toute la région, quelle que soit la distance par rapport à la source lumineuse.
* **-l**:Modifie la position de la source lumineuse selon les coordonnées données, sinon utilise la position du joueur.
* **-o** (par défaut: 0.0): détermine la force de l'occlusion. Une valeur plus élevée produit des ombres plus « sombres ». Plage attendue de 0 à 1.
* **-r** (par défaut: 1): détermine le rayon de lissage pour l’occlusion (ombres).

</details>

### `shift`

<details>

<summary>Shift Texture</summary>

**`//ezt shift <palette> [shift]`**

Modifie la texture d'une région en décalant la palette d'une quantité définie.

* **Palette**: Spécifie la palette à utiliser.
* **Shift** (par défaut: 1): détermine le nombre de blocs à décaler dans la palette.
</details>

### `sunlight`

<details>

<summary>Sunlight Texture</summary>

**`//ezt sunlight <mask> <palette> [radius] [interval] [-l] [-o] [-r]`**

Texture une région en utilisant une direction de source lumineuse globale pour contrôler l'application de la palette.

* **Mask**: Blocs à remplacer.
* **Palette**: Spécifie la palette à utiliser.
* **Radius** (par défaut: 1): définit le rayon d'approximation normal, affectant le calcul de l'orientation des surfaces par rapport à la lumière du soleil.
* **Interval** (par défaut: "0,180"): définit l'intervalle d'orientation de la surface en degrés, où 0 correspond à une orientation directe vers la lumière et 180 à une orientation opposée. Les surfaces situées dans cet intervalle sont texturées et toutes celles situées en dessous ou au-dessus seront texturées avec le premier ou le dernier bloc de palette.
* **-l** (par défaut: down): direction globale dans laquelle la lumière brille.
* **-o** (par défaut: 0.0): détermine la force de l'occlusion. Une valeur plus élevée produit des ombres plus « sombres ». Plage attendue de 0 à 1.
* **-r** (par défaut: 1): détermine le rayon de lissage pour l’occlusion (ombres).

</details>

### `advanced`

<details>

<summary>Advanced Texturing</summary>

**`//ezt advanced <mask> <palette> <texture>`**

Interface plus puissante pour utiliser eztexture. Elle a accès à toutes les autres commandes eztexture et peut également les mélanger/combiner. Cela signifie que vous pouvez par exemple faire des textures ambiantes et solaires simultanément.

- **Mask**: Blocs à remplacer.
- **Palette**: Spécifie la palette à utiliser.
- **Texture**: une spécification de texturation.

#### Comment définir un `<texture>`?

la `<texture>` suit la méthode courante suivante pour spécifier des objets complexes : ```<type (<parameter1>:<value1>,<parameter2>:<value2>)```
Chaque type de texture possède son propre ensemble de paramètres. Vous pouvez définir autant de paramètres que vous le souhaitez. Si un paramètre n'est pas défini, une valeur par défaut sera utilisée à la place. Chaque paramètre peut avoir différentes entrées qu'il accepte. Certains paramètres acceptent des nombres, d'autres un vecteur 3D, d'autres un argument de noise et certains acceptent même les objets Texture eux-mêmes.
La `<texture>` peut être l'un des modes de texture existants. Quelques exemples simples :
- `Ambient`
- `Ambient()`
- `Ambient(Radius:2)`
- `Ambient(Radius:2,Brightness:0.2,Contrast:0.3)`
- `Flow(Noise:@@ridged(Freq:0.12))`

Pour clarifier : les deux commandes suivantes feront la même chose.
- `//eztexture ambient #existing ##grayscale 2 0.2 0.3`
- `//eztexture advanced #existing ##grayscale Ambient(Radius:2,Brightness:0.2,Contrast:0.3)`

#### Combinaison de textures

Les textures suivantes ont des paramètres  `Texture1`(`T1`)/`Texture2`(`T2`) acceptant `<texture>` eux-mêmes des arguments vous permettant de combiner les modes de texture :
- `Add(T1:...,T2:...)`
- `Subtract(T1:...,T2:...)`
- `Multiply(T1:...,T2:...)`
- `Divide(T1:...,T2:...)`
- `WeightedAverage(T1:...,T2:...)`
- `Darken(T1:...,T2:...)`
- `Lighten(T1:...,T2:...)`
- `Difference(T1:...,T2:...)`
- `Screen(T1:...,T2:...)`

Les textures suivantes ont des paramètres `Texture`(`T`) acceptant `<texture>` eux-mêmes des arguments vous permettant d'ajuster/post-traiter les textures :
- `Adjust(T:...,Brightness:...,Contrast:...)`
- `Invert(T:...)`
- `Blend(T:...,Radius:...)`

Exemples:
- `WeightedAverage(T1:Sun(),T2:Ambient())`
- `Blend(T:Flow(Noise:@@ridged(Freq:0.12)),Radius:0.7)`
- `Darken(T1:Noise(Noise:@@smoothcells(freq:0.5)),T2:Flow)`
- `Adjust(T:Pointlight,Contrast:0.5)`

Veuillez noter que les `Texture`/`Texture1`/`Texture2` (`T`/`T1`/`T2`) ne sont pas facultatifs. Vous devez les définir pour utiliser ces textures de combinaison/ajustement. (Si vous ne les définissez pas, vous recevrez une erreur indiquant `cannot be null`).

</details>
