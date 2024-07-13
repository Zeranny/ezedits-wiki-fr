# Selections

## Commandes de sélection

### `//selload`

<details>

<summary>Selection Load</summary>

**`//selload [selection]`**\
_Alternate for \`//ezsel load\`_

La `//selload` commande récupère une sélection précédemment enregistrée dans la liste de sélection enregistrée du joueur.

* Sélection : une sélection précédemment enregistrée.

</details>

### `//next`

<details>

<summary>Selection Shift</summary>

**`//next <direction> <gap>`**

La `//next` commande décale votre zone de sélection actuelle de sa propre taille dans une direction spécifiée.

* **Direction** (par défaut: visé du joueurs): spécifie la direction vers laquelle déplacer la sélection. Si elle n'est pas fournie, la valeur par défaut est la direction vers laquelle le joueur vise.
* **Espace** (par défaut: 0): un paramètre facultatif permettant d'ajouter un espace supplémentaire entre la position de sélection actuelle et la position décalée.

</details>

### `//selhere`

<details>

<summary>Move Selection to Player</summary>

**`//selhere [selectionPosition]`**

**`Alias: //seltome`**

La `//selhere` commande déplace votre sélection actuelle vers votre emplacement.

* **SelectionPosition** (par défaut: POS1):  spécifie le point de la sélection à déplacer vers la position du joueur. Tous les autres points seront déplacés vers la position relative.
  * POS1 -  Le « Pos1 » de la sélection, ou premier point pour les sélections convexes/polygonales.
  * POS2 -  Le « Pos2 » de la sélection, ou les derniers points pour les sélections convexes/polygonales.
  * CENTER - Le point central de la sélection

</details>

### `//ezselinvert`

<details>

<summary>Selection Invert</summary>

**`//ezselinvert`**

**`Alias: //selinvert`**

La `//ezselinvert` commande inverse l'ordre des points dans votre sélection actuelle. \
Cela sera particulièrement visible avec les sélections convexes, car avec une sélection cuboïde, pos1 et pos2 échangeront simplement leurs places, alors qu'une sélection convexe inversera l'ordre de chaque point.

</details>

### `//delpos2`

<details>

<summary>Delete Last Position</summary>

**`//delpos2`**

**`Alias: //-2`**

La `//delpos2` commande supprime le dernier point de sélection secondaire pour les sélections convexes et poly.

</details>



## Selection Management Commands

Toutes les sous-commandes sont sous `//ezselection`  (`//ezsel`) \
par exemple `//ezsel list`

### `list [-g]`

Répertorie toutes les sélections enregistrées par l'utilisateur. Cliquez sur le nom d'une sélection pour la charger.\
`-g` pour regrouper les sélections par type.

### `load <selection>`

Récupère une sélection précédemment enregistrée dans la liste de sélection enregistrée du joueur.

### `save <selectionName> [-f]`

Enregistre la sélection actuelle de l'utilisateur avec un nom donné.\
`-f` pour remplacer une sélection enregistrée existante.

### `delete <selectionName>`

Supprime la sélection d'un utilisateur avec le nom donné.
