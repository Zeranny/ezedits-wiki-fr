# Surface

Toutes les sous-commandes sont sous `//ezsurface`  (`//ezsu`) \
par exemple`//ezsurface rockify`

## `//ezsurface ...`

### `fuzzify`

<details>

<summary>Fuzzify Surface</summary>

**`//ezsu fuzzify <radius> [smooth_radius] [smooth_iterations] [-c] [-e] [-m] [-t]`**

Utilise du noise blanc pour rendre la surface plus floue.

* **Radius**: Valeur flottante déterminant la distance maximale de la surface à laquelle des modifications peuvent se produire.
* **Smooth Radius** (par défaut: 0): spécifie le rayon pour les opérations de lissage.
* **Smooth Iterations** (par défaut: 0): détermine le nombre de fois que l'opération de lissage est appliquée.
* **-c**: limite les modifications à la sculpture sur le terrain uniquement.
* **-e**: limite l'opération à l'extension uniquement à partir du terrain.
* **-m**:  applique un masque pour modifier uniquement les surfaces qui correspondent aux critères spécifiés. \
  Cette option peut ralentir considérablement le processus en raison de la complexité supplémentaire de la correspondance des surfaces.
* **-t**: Tente de conserver la topologie de la région..

</details>

### `rockify`

<details>

<summary>Rockify Surface</summary>

**`//ezsu rockify <radius> [size] [oct] [smooth_radius] [smooth_iterations] [-c] [-e] [-m] [-t]`**

Utilise le noise Perlin pour rendre une surface rocheuse.

* **Radius**: Valeur flottante déterminant la distance maximale de la surface à laquelle des modifications peuvent se produire.
* **Noise Size** (par défaut: 10): contrôle l’échelle du noise utilisé.
* **Noise Octaves** (par défaut: 1): définit le nombre de couches de noise appliquées.
* **Smooth Radius** (par défaut: 1): spécifie le rayon pour les opérations de lissage.
* **Smooth Iterations** (par défaut: 4): détermine le nombre de fois que l'opération de lissage est appliquée.
* **-c**:  limite les modifications à la sculpture sur le terrain uniquement.
* **-e**:  limite l'opération à l'extension uniquement à partir du terrain.
* **-m**: applique un masque pour modifier uniquement les surfaces qui correspondent aux critères spécifiés. \
  Cette option peut ralentir considérablement le processus en raison de la complexité supplémentaire de la correspondance des surfaces.
* **-t**: Tente de conserver la topologie de la région.

</details>

### `voronoify`

<details>

<summary>Voronoify Surface</summary>

**`//ezsu voronoify <radius> [cell_size] [smooth_radius] [smooth_iterations] [-c] [-e] [-m] [-t]`**

Utilise le noise de Voronoi pour déformer une surface.

* **Radius**: Valeur flottante déterminant la distance maximale de la surface à laquelle des modifications peuvent se produire.
* **Cell Size** (par défaut: 12): spécifie le rayon pour les opérations de lissage.
* **Smooth Radius** (par défaut: 0): Specifies the radius for smoothing operations.
* **Smooth Iterations** (par défaut: 0): détermine le nombre de fois que l'opération de lissage est appliquée.
* **-c**: limite les modifications à la sculpture sur le terrain uniquement.
* **-e**: limite l'opération à l'extension uniquement à partir du terrain.
* **-m**: applique un masque pour modifier uniquement les surfaces qui correspondent aux critères spécifiés. \
 Cette option peut ralentir considérablement le processus en raison de la complexité supplémentaire de la correspondance des surfaces.
* **-t**: Tente de conserver la topologie de la région.

</details>

### `noisify`

<details>

<summary>Noiseify Surface</summary>

**`//ezsu noisify <radius> <noise> [scale] [smooth_radius] [smooth_iterations] [-c] [-e] [-m] [-t]`**

Utilise un préréglage de noise pour déformer une surface.

* **Radius**: Valeur flottante déterminant la distance maximale de la surface à laquelle des modifications peuvent se produire.
* **Noise**:  Spécifie le noise à utiliser pour la modification.
* **Scale** (par défaut: 1):  ajuste l’échelle du noise.
* **Smooth Radius** (par défaut: 1): spécifie le rayon pour les opérations de lissage.
* **Smooth Iterations** (par défaut: 4): détermine le nombre de fois que l'opération de lissage est appliquée.
* **-c**:  limite les modifications à la sculpture sur le terrain uniquement.
* **-e**: limite l'opération à l'extension uniquement à partir du terrain.
* **-m**:applique un masque pour modifier uniquement les surfaces qui correspondent aux critères spécifiés. \
  Cette option peut ralentir considérablement le processus en raison de la complexité supplémentaire de la correspondance des surfaces.
* **-t**:  Tente de conserver la topologie de la région.

</details>
