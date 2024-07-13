# Smoothing

### `//ezsmooth`

<details>

<summary>Smooth</summary>

**`//ezsmooth <radii> <iterations> <bias>`**

**`Alias: //ezsm`**

La `//ezsmooth` commande lisse les bords et les surfaces d'une région sélectionnée à l'aide d'un algorithme de lissage tridimensionnel.

* **Radii**: le ou les rayons de lissage, qui peuvent être une valeur unique ou trois valeurs séparées par des virgules pour les directions Est/Ouest, Haut/Bas et Nord/Sud, respectivement. Ce paramètre contrôle l'étendue de l'effet de lissage.
* **Iterations**: nombre de fois que l'opération de lissage est exécutée. Un nombre plus élevé d'itérations conduit à un résultat plus fluide mais augmente le temps de traitement.
* **Bias**:  valeur comprise entre -1,0 et 1,0 qui ajuste l'expansion ou la contraction de l'effet de lissage. Les valeurs positives élargissent la zone lissée, tandis que les valeurs négatives la contractent.

</details>

### `//ezinflate`

<details>

<summary>Inflate</summary>

**`//ezinflate <radius>`**

**`Alias: //inflate`**

La `//ezinflate` commande augmente le volume des blocs dans une région sélectionnée d'une quantité spécifiée, « gonflant » ainsi efficacement la construction.

* **Radius**: Spécifie la distance d'expansion en blocs. Cette valeur détermine à quelle distance des surfaces d'origine les nouvelles surfaces gonflées seront créées.

</details>

### `//ezdeflate`

<details>

<summary>Deflate</summary>

**`//ezdeflate <radius>`**

**`Alias: //deflate`**

La `//ezdeflate` commande contracte le volume des blocs dans une région sélectionnée d'une quantité spécifiée, « dégonflant » ainsi efficacement la construction.

* **Radius**: spécifie la distance d'expansion en blocs. Cette valeur détermine la distance à laquelle les blocs seront supprimés à partir des surfaces d'origine.

</details>

### `//ezsmoothblocks`

<details>

<summary>Smooth Blocks</summary>

**`//ezsmoothblocks <radius> <iterations> <bias> [-s] [-t] [-w]`**

**`Alias: //smoothblocks`**

La `//ezsmoothblocks` commande modifie une région sélectionnée en plaçant des dalles, des escaliers et des murs pour créer une surface nettement plus lisse.

* **Radius**: spécifie le rayon de lissage en blocs. Cette valeur détermine la zone autour de chaque bloc qui est prise en compte pendant le processus de lissage.
* **Iterations**:nombre de fois que l'opération de lissage est exécutée. Un nombre plus élevé d'itérations produit un résultat plus lisse, mais augmente le temps de traitement.
* **Bias**: valeur comprise entre -1,0 et 1,0 qui ajuste l'expansion ou la contraction de l'effet de lissage. Les valeurs positives tendent à élargir la zone lissée, tandis que les valeurs négatives la contractent, offrant ainsi un contrôle sur l'apparence finale.
* **-s**: limite le processus de lissage pour n'utiliser que des dalles.
* **-t**: exclut les murs du lissage.
* **-w**: utilise un ensemble alternatif de blocs.

</details>

