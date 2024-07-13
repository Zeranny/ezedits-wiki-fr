# Formes

Toutes les sous-commandes sont sous `//ezshapes`  (`//ezsh`) \
par exemple `//ezshapes polydome`

## `//ezshapes ...`

### `cone`

<details>

<summary>Cone</summary>

**`//ezsh cone <pattern> <radii> <height> [rotation] [-dos]`**

* **Pattern**: spécifie le modèle de bloc.
* **Radii**: définit les rayons du cône. La première valeur correspond à la direction Nord/Sud et la seconde à la direction Est/Ouest. Ces directions peuvent changer si le cône est tourné.
* **Height**: Définit la hauteur du cône.
* **Rotation** (par défaut: 0): détermine l'angle de rotation autour de l'axe des Y, en degrés. Il peut être aligné avec la direction de visée du joueur si le `-o` commutateur est utilisé.
* **-d**:  Lorsqu'il est activé, génère le cône avec le côté pointu tourné vers le bas.
* **-o**: Lorsqu'il est utilisé, la direction de visée du joueur est prise en compte pour la rotation du cône.
* **-s**: Lorsqu'il est utilisé, la sélection des joueurs sera déplacée pour couvrir approximativement la forme

</details>

### `polydome`

<details>

<summary>Polydome</summary>

**`//ezsh polydome <pattern> <sides> <radius> <height> [-vs]`**

* **Pattern**: spécifie le modèle de bloc.&#x20;
* **Sides**: Définit le nombre de côtés du polydôme.&#x20;
* **Radius**:  définit le rayon du polydôme.&#x20;
* **Height** (par défaut: 1): détermine la hauteur du dôme.&#x20;
* **-v**: Spécifie un modèle de sommet, modifiant l'apparence des sommets du polydôme.
* **-s**:  Lorsqu'il est utilisé, la sélection des joueurs sera déplacée pour couvrir approximativement la forme

</details>

### `polygon`

<details>

<summary>Polygon</summary>

**`//ezsh polygon <pattern> <sides> <radius> <height> [direction] [-s]`** 

* **Pattern**: spécifie le modèle de bloc.&#x20;
* **Sides**: définit le nombre de côtés du polygone.&#x20;
* **Radius**: définit le rayon du polygone.&#x20;
* **Height** (par défaut: 1): détermine la hauteur du polygone.&#x20;
* **Direction** (par défaut: VISÉE du joueur): spécifie la direction du placement, qui peut inclure des diagonales.
* **-s**: Lorsqu'il est utilisé, la sélection des joueurs sera déplacée pour couvrir approximativement la forme

</details>

### `square`

<details>

<summary>Square</summary>

**`//ezsh square <pattern> <radius> <height> [-fws]`**

* **Pattern**: spécifie le modèle de bloc.&#x20;
* **Radius**: définit le rayon du carré.&#x20;
* **Height** (par défaut: 1): détermine la hauteur du carré.&#x20;
* **-f**: Lorsqu'il est activé, seules les faces du carré sont générées.&#x20;
* **-w**: Lorsqu'il est utilisé, seuls les murs du carré sont générés.
* **-s**: Lorsqu'il est utilisé, la sélection des joueurs sera déplacée pour couvrir approximativement la forme

</details>

### `tetrahedron`

<details>

<summary>Tetrahedron</summary>

**`//ezsh tetrahedron <pattern> <radius> [rotation] [-os]`**

* **Pattern**: spécifie le modèle de bloc.&#x20;
* **Radius**: définit la taille du tétraèdre.&#x20;
* **Rotation** (par défaut: 0): détermine l'angle de rotation autour de l'axe des Y, en degrés. Il peut être aligné avec la direction de visée du joueur si le commutateur -o est utilisé.&#x20;
* **-o**: Lorsqu'il est utilisé, la direction de visée du joueur est prise en compte pour la rotation du tétraèdre.
* **-s**: Lorsqu'il est utilisé, la sélection des joueurs sera déplacée pour couvrir approximativement la forme

</details>

### `torus`

<details>

<summary>Torus</summary>

**`//ezsh torus <pattern> <major_radius> <minor_radius> <cross_section> [-os]`**

* **Pattern**: spécifie le modèle de bloc.
* **Major Radius**: définit le rayon majeur du tore.
* **Minor Radius**: définit le rayon mineur du tore.
* **Cross Section**: Détermine la forme de la section transversale du tore :
  * `CIRCLE`
  * `DIAMOND`
  * `ROUNDED_SQUARE`
  * `SQUARE`

* **-o**: Lorsqu'il est utilisé, la rotation du tore s'aligne avec la direction de visée du joueur
* **-s**: Lorsqu'il est utilisé, la sélection des joueurs sera déplacée pour couvrir approximativement la forme

</details>
