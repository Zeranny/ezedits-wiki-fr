# Brushes

Tous les pinceaux sont contenus dans la commande `//ezbrush ...` (`//ezbr`) .



## `//ezbrush ...`

### `gradient`

<details>

<summary>Gradient Brush</summary>

**`//ezbr gradient <palette> [radius] [interpolation] [strength] [-av] [-n <noise>] [-z <scale>] [-d <distanceFunction>]`**

le `gradient` pinceau vous permet de définir d'abord un plan en sélectionnant 2 points, vous pouvez ensuite peindre avec votre dégradé avec des blocs choisis en fonction de la distance le long de ce plan.

**<u>Clic gauche pour démarrer un plan sur votre bloc cible.**\
**<u>Furtif + clic gauche</u> to start a plane at the player positionpour démarrer un plan à la position du joueur.**\
**<u>Clic droit </u>  pour définir la fin du plan sur votre bloc cible OU peindre des blocs de palette si le plan est défini.**\
**<u>Furtif + clic droit</u>  pour définir la fin du plan sur la position du joueur OU peindre des blocs de palette si le plan est défini.**\
**<u>Échanger les mains (touche F par défaut)</u> pour basculer entre les dégradés actifs GLOBAL et PER_ITEM**

* **Palette**:  spécifie la palette à utiliser pour le dégradé.
* **Rayon** (par défaut: 8):définit le rayon du pinceau.
* **Interpolation** (par défaut: NONE): détermine le type d’interpolation utilisé dans la transition de gradient.
* **Force** (par défaut: 0.5): ajuste la force de l'interpolation, avec une plage normale de 0 à 1.
* **-a**: Lorsqu'il est activé, permet au gradient de remplacer les blocs d'air.
* **-v**: Désactive l'intégration de WorldEditCUI.
* **-n \<noise>** (par défaut: `White()`): ajoute un champ de noise sous-jacent à l’effet de dégradé.
* **-z \<scale>** (par défaut: 1): modifie l'échelle du noise.
* **-d \<distanceFunction>** (par défaut: NONE): définit le mode de distance en modifiant le pinceau pour qu'il fonctionne en fonction de la distance par rapport au bloc initial avec la fonction de distance donnée.

</details>

### `gradientstroke`

<details>

<summary>Gradient Stroke Brush</summary>

**`//ezbr gradientstroke <palette> [radius] [interpolation] [strength] [-adv] [-n <noise>] [-z <scale>]`**

le `gradientstroke`pinceau permet d'appliquer un dégradé le long d'un tracé (trait) défini par la sélection de points.

**<u>Left Click</u> pour ajouter des points**\
**<u>Sneak + Left Click</u> pour supprimer le dernier point**\
**<u>Right Click</u> pour confirmer et placer le trait de dégradé**\
**<u>Sneak + Right Click</u>  pour effacer tous les points**\
**<u>Swap Hands (par défaut F key)</u>pour basculer entre les dégradés actifs GLOBAL et PER_ITEM**

* **Palette**: spécifie le motif de bloc pour le dégradé.
* **Radius** (par défaut: 8):  définit le rayon du pinceau.
* **Interpolation** (par défaut: LINÉAIRE): détermine le type d’interpolation utilisé dans la transition de gradient.
* **Force** (par défaut: 0.5): ajuste la force de l'interpolation, avec une plage normale de 0 à 1.
* **-a**:  Lorsqu'il est activé, permet au gradient de remplacer les blocs d'air.
* **-d**: Active le mode « distance au centre » qui applique le dégradé en fonction de la distance au milieu de la ligne de trait au lieu de la distance le long du trait.
* **-v**: Désactive l'intégration de WorldEditCUI.
* **-n \<noise>** (par défaut: `White()`): ajoute un champ de noise sous-jacent à l’effet de dégradé.
* **-z \<scale>** (par défaut: 1): modifie l'échelle du noise.

</details>

### `paletteshift`

<details>

<summary>Palette Shift Brush</summary>

**`//ezbr paletteshift <palette> [radius] [shift]`**

Remplace les blocs correspondant à la palette par des blocs de palette décalés de la valeur donnée.\
Par exemple, une valeur de décalage de 2 remplacera toutes les instances du premier bloc de palette par le troisième.

* **Palette**:  spécifie le motif de bloc pour le dégradé.
* **Radius** (par défaut: 8): définit le rayon du pinceau.
* **Shift** (par défaut: 1): la quantité selon laquelle les blocs doivent être décalés dans la palette

</details>
