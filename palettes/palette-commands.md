# Commandes de la palette

Toutes les sous-commandes sont sous `//ezpalette` (`//ezp`)\
par exemple `//ezpalette list`

## `//ezpalette ...`

### `fetch <fetchMode> <paletteName> [length] [-d <direction>] [-f]`

<details>

<summary>Récupérer la palette</summary>

Enregistre une palette définie par l'utilisateur avec un nom donné.

* **Mode de récupération**: d'où récupérer les blocs de palette :
  * **`WORLD`**
    * Prend les blocs de la position du joueur
  * **`SELECTION`**
    * Prend les blocs de la sélection du joueur
    * La sélection doit avoir une taille de 1x1xN, où N est la longueur de palette souhaitée
  * **`HOTBAR`**
    * Prend des blocs de la barre de raccourcis du joueur
    * Ignore les éléments et utilise les propriétés de bloc par défaut
* **Longueur** (par défaut: 0): nombre de blocs à récupérer. Une longueur de 0 (par défaut) récupérera des blocs jusqu'à ce que l'air soit atteint.
* **-d** (par défaut: moi): la direction à laquelle effectuer la recherche. La valeur par défaut est la direction vers laquelle l'utilisateur fait face.
* **-f**: Lorsqu'il est activé, écrase la palette existante portant le même nom.

<img src="../.gitbook/assets/ezp_fetch.gif" alt="" data-size="original">

</details>

### `save <paletteName> <palette> [-f]`

Enregistre une palette définie par l'utilisateur avec un nom donné.

* **-f**: Lorsqu'il est activé, écrase la palette existante portant le même nom.

### `delete <paletteName>`

Supprime une palette définie par l'utilisateur correspondant au nom donné.

### `list [SET]`

* `ALL`\
  Répertorie toutes les palettes disponibles
* `par défaut`\
  Répertorie toutes les palettes de plugins par défaut
* `MINE`\
  Répertorie toutes les palettes définies par l'utilisateur

### `place <palette> [direction]`

Place une palette dans le monde sous forme d'une rangée de blocs dans la direction donnée. La direction par défaut est celle vers laquelle l'utilisateur fait face.

### `swap <sourcePalette> <targetPalette> [-a] [-f]`

Opération de région qui échange les blocs de la palette source avec ceux de la palette cible.

* **-a**: Activer pour inclure les blocs d'air (si la palette source contient de l'air).
* **-f**: Activer pour étirer la palette cible pour qu'elle corresponde à la taille de la palette source.

### `print <palette> [-v]`

Imprime les blocs d'une palette donnée dans le chat. La liste des blocs peut être cliquée pour être copiée.

**-v**: mode détaillé. Imprime le nom complet du bloc et les états des blocs.

### `encode <palette>`

Imprime une chaîne codée représentant une palette donnée. Cliquez sur la chaîne pour la copier.\ _Ne prend en charge que les blocs Minecraft classiques._

### `decode <string>`

Imprime les blocs d'une chaîne de palette codée donnée. La liste des blocs peut être cliquée pour être copiée.
