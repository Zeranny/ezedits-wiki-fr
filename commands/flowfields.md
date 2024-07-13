# Flowfields

Commandes basées sur le concept de « champs de flux », souvent observés dans l'art génératif.

Conceptuellement, ils utilisent une fonction (du bruit dans notre cas) pour générer un ensemble de vecteurs le long d'une grille, ou d'un champ, qui dictera la manière dont les particules circulent à travers ce champ.

### `//ezflowfield`

<details>

<summary>Flow Field</summary>

**`//ezflowfield <palette> <lines> <iterations> <velocity> <paletteScalar> <noise> [-m <source>] [-h <distributionMode>] [-i <inertia>] [-g <gravity>] [-j <jitter>] [-b <boundary>] [-x <xMod>] [-y <yMod>] [-z <zMod>] [-p <progression>] [-s <seed>] [-c] [-f] [-t]`**

**`Alias: //flow`**

Génère un champ de flux dans une sélection, créant un motif dynamique basé sur les nombreux paramètres disponibles.

* **Palette**:  Spécifie la palette de blocs à utiliser pour générer le champ de flux.
* **ligne**: définit le nombre de lignes ou une distribution en pourcentage pour déterminer la densité de remplissage du champ de flux dans la sélection.\
  Par exemple, `100` générera 100 lignes, `100%` générera 1 ligne pour chaque bloc de la région.
* **Iterations** (par défaut: 32): le nombre d'itérations ou d'étapes par ligne contrôlant leur durée.
* **Velocity** (par défaut: 1): la vitesse à laquelle les points se déplacent sur la surface.
* **PaletteScalar** (par défaut: 1.0): met à l'échelle la valeur utilisée pour sélectionner un bloc de palette.
* **Noise** (par défaut: `Perlin()`): le type de noise utilisé pour générer le champ de flux.
* **-m**: Applique un masque pour limiter les points de départ du flux, en concentrant l'effet sur des zones spécifiques.
* **-h**: Active le mode heightmap pour créer des champs de flux 2D, avec des modes de distribution de blocs facultatifs.
* **-i** (par défaut: 0.0): définit la pondération d'inertie du flux, contrôlant dans quelle mesure les directions de mouvement précédentes influencent la suivante.
* **-g** (par défaut: (0,0,0) ): applique la gravité aux points, les tirant dans la direction spécifiée.
* **-j** (par défaut: (0,0,0) ): ajoute de la gigue aux points de départ des lignes. Utile avec `-m` l'indicateur.
* **-b** (par défaut: 0): étend la limite de calcul sans placer de blocs en dehors de la sélection d'origine. Ne place pas de blocs en dehors de la sélection.
* **-x, -y, -z**: modifie les coordonnées du flux, permettant des transformations telles que la mise à l'échelle ou la rotation. Prend une expression WorldEdit, Par exemple, `-x *10`pour multiplier l'axe des x par 10.
* **-p** (par défaut: 1:1):  ajuste la force de la ligne au fur et à mesure de sa progression, accepte des valeurs négatives pour démarrer ou terminer sur une force de point qui se soustrait au champ de flux.
* **-s** (par défaut: -1): remplace la valeur de noise par défaut.
* **-c**: Renvoie la boucle du champ.
* **-f**: Remplit les espaces avec le bloc le plus bas de la palette.
* **-t**: génère un champ d'écoulement 3D à la place. La génération peut nécessiter beaucoup de temps.

</details>

### `//ezflowline`

<details>

<summary>Flow Line</summary>

**`/ezflowline <pattern> <length> <gravity> <noise> [-i <inertia>] [-c <convexSelPoints>] [-s]`**

**`Alias: //flowline`**

Génère une seule ligne de flux en fonction de la position de l'acteur et de la direction de visualisation. Le même principe fondamental qu'un champ de flux, mais en ne générant qu'une seule ligne.

* **Pattern**: Détermine le motif des blocs à placer.&#x20;
* **Length**: définit la longueur de la ligne d'écoulement en blocs. Cela définit la distance à laquelle la ligne d'écoulement s'étendra à partir du point de départ.
* **Gravity** (par défaut: -1): applique la gravité aux points, les tirant dans la direction spécifiée.
* **Noise** (par défaut: `Perlin()`): le type de noise utilisé pour générer le champ d'écoulement.flowfield.
* **-i** (par défaut: 0.0): ajuste la pondération de l'inertie du point, en contrôlant l'influence des directions de mouvement précédentes sur les directions futures. Une valeur comprise entre 0,0 et 1,0.
* **-c** (par défaut: 0): si la valeur est supérieure à 0, crée une sélection convexe à partir de la ligne de flux, en utilisant le nombre de points spécifié pour définir la forme de la sélection.
* **-s**: Permet d'accrocher la ligne d'écoulement aux surfaces, faisant adhérer la ligne aux contours du paysage ou des structures qu'elle croise.

</details>
