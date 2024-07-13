# Stained Glass

Commandes liées à l'utilisation du vitrail pour la couleur.

### `//ezstainedglassgradient`

<details>

<summary>Glass Gradient</summary>

**`//ezstainedglassgradient <startColor> [endColor] <layers> [length] [quality] [direction] [-c <backgroundColor>] [-bs]`**

**`Aliases: //stainedglassgradient, //glassgradient`**

* **StartColor**:  Spécifie la couleur de départ (sous forme de code hexadécimal) pour le dégradé.
* **EndColor** (par defaut: None): spécifie la couleur de fin (sous forme de code hexadécimal) du dégradé. Si aucune valeur n'est fournie, la couleur de départ sera utilisée pour l'ensemble du dégradé.
* **Layers**: Combien de couches de verre utiliser pour créer le dégradé.
* **Length** (Default: 1):  la longueur en nombre de blocs que doit avoir le dégradé.
* **Quality** (Default: 7): quelle doit être la précision du dégradé. Une valeur plus élevée peut prendre plus de temps à s'exécuter.
* **-c** (Default: #000000): spécifie la couleur d'arrière-plan (sous forme de code hexadécimal) sur laquelle se trouve le dégradé si l'indicateu **-b** n'est pas utilisé.
* **-b**:  recherche le bloc solide le plus proche à placer derrière la vitre pour augmenter la précision des couleurs. Cette opération nécessite beaucoup plus de ressources.
* **-s**:  ignorer les combinaisons de calques en double.

</details>
