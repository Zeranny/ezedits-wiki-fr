# Le bruit expliqué

Le bruit peut être un sujet complexe pour quiconque ne l'a jamais étudié auparavant, mais dans ses termes les plus simples, le bruit est un moyen d'obtenir une valeur à partir d'une entrée (généralement des coordonnées X, Y, Z).

L'endroit où vous serez probablement le plus familier avec le bruit est dans la génération de terrain de Minecraft. À chaque point du monde, plusieurs fonctions de bruit sont combinées pour déterminer si un bloc doit être placé, et si oui, quel bloc.

C'est à peu près ce que nous faisons dans ezEdits, en utilisant le bruit pour générer des formes, du terrain et des textures.



Dans le plugin, vous trouverez plusieurs types de bruit, chacun ayant des caractéristiques différentes, et Cellular est spécifiquement livré avec de nombreux paramètres supplémentaires que vous pouvez personnaliser.

Certaines des nombreuses fonctionnalités qui utilisent le bruit incluent :

* `//eznoisegen ...` - *Commandes Noisegen*
* `#eznoisemask` - *Masques*
* `//ezbrush gradient ...` - *Brushes*



_Le bruit dans ezEdits est basé sur une version modifiée de FastNoiseLite, nous recommandons donc fortement ce site Web pour expérimenter les paramètres de bruit :_ [_http://auburn.github.io/FastNoiseLite/_ ](http://auburn.github.io/FastNoiseLite/)

## Paramètres de bruit

Chaque paramètre et de nombreuses valeurs disposent également d'un raccourci, tel que « Fractal » au lieu de « FractalType » ou « Simplex » au lieu de « OpenSimplex2 ». Dans la mesure du possible, le raccourci sera indiqué entre parenthèses.\
<mark style="color:red;">`Red = Parameter`</mark>    <mark style="color:purple;">`Purple = Value`</mark>

&#x20;

### Type de bruit

<details>

<summary>Réglage du type de bruit<br><mark style="color:red;"></summary>

Définit le type de bruit à utiliser. Il s'agit du début de tout bruit et sera au format `Noise()`,  par exemple  `Perlin()`, où tous les autres paramètres seront placés entre parenthèses.

* <mark style="color:purple;">`Perlin (per)`</mark>
* <mark style="color:purple;">`OpenSimplex2 (simplex)`</mark>
* <mark style="color:purple;">`OpenSimplex2S (smooth)`</mark>
* <mark style="color:purple;">`Value (val)`</mark>
* <mark style="color:purple;">`ValueCubic (cubic)`</mark>
* <mark style="color:purple;">`White`</mark>
* <mark style="color:purple;">`Cellular (vor)`</mark>
* <mark style="color:purple;">`Shard`</mark>

</details>

### Paramètres de bruit de base

<details>

<summary>Paramètres de bruit de base</summary>

* <mark style="color:red;">`Seed`</mark>\
  Définit la valeur de départ pour le bruit. -1 ou aucune valeur entraînera une valeur de départ de bruit aléatoire.
* <mark style="color:red;">`Frequency (Freq)`</mark>\
  Définit la fréquence du bruit. Une fréquence plus élevée entraînera un bruit plus prononcé, une valeur plus basse entraînera un bruit plus doux.
* <mark style="color:red;">`Inverted (Invert)`</mark>\
  Inverser ou non la valeur du bruit. La valeur par défaut est false.
  * <mark style="color:purple;">`True`</mark>
  * <mark style="color:purple;">`False`</mark>
* <mark style="color:red;">`ValueMapping (Map)`</mark>\
  Indique s'il faut ignorer ou remplacer le mappage de valeurs. Par défaut, le bruit est échantillonné pour correspondre à une valeur comprise entre 0 et 1.
  * <mark style="color:purple;">`Default (Def)`</mark>
  * <mark style="color:purple;">`None (No)`</mark>
  * <mark style="color:purple;">`Override (OR)`</mark>\
    **Si annulé :**
    * <mark style="color:red;">`LowerBound (Min)`</mark>
    * <mark style="color:red;">`UpperBound (Max)`</mark>
* <mark style="color:red;">`YScaling (Y)`</mark>\
 Lors de l'utilisation de bruits 3D, cela peut être utilisé pour étirer ou écraser l'axe Y.

</details>

### Paramètres du bruit cellulaire

<details>

<summary><strong>Paramètres du bruit cellulaire</strong></summary>

* <mark style="color:red;">`CellularJitterModifier (Jitter)`</mark>\
 Contrôle généralement `0..1.0`\
  la gigue aléatoire ou la distribution des nœuds de bruit cellulaire, 0 étant une grille parfaite et 1 étant au maximum « aléatoire », sans chevauchement. Les valeurs supérieures à 1 commenceront à chevaucher leurs voisins.
* <mark style="color:red;">`CellularDistanceFunction (Distance)`</mark>\
 Contrôle la méthode mathématique utilisée pour déterminer la valeur de distance de chaque point à son nœud.
  * <mark style="color:purple;">`Euclidean`</mark>
  * <mark style="color:purple;">`EuclideanSq (sq)`</mark>
  * <mark style="color:purple;">`Manhattan (man)`</mark>
  * <mark style="color:purple;">`Hybrid`</mark>
  * <mark style="color:purple;">`Minkovski1 (m1)`</mark>
  * <mark style="color:purple;">`Minkowvki4 (m4)`</mark>
  * <mark style="color:purple;">`Minkowski99 (m99)`</mark>
  * <mark style="color:purple;">`Rounded (round)`</mark>
* <mark style="color:red;">`CellularReturnType (DistReturn)`</mark>\
  Contrôle la manière dont la valeur de distance est modifiée avant d'être renvoyée. Toutes les valeurs Distance2* font référence au deuxième nœud le plus proche au lieu du plus proche.
  * <mark style="color:purple;">`CellValue (cell)`</mark>
  * <mark style="color:purple;">`Distance (1)`</mark>
  * <mark style="color:purple;">`DistanceSquared (sq)`</mark>
  * <mark style="color:purple;">`DistanceInverse (inv)`</mark>
  * <mark style="color:purple;">`DistanceLog (log)`</mark>
  * <mark style="color:purple;">`DistanceExp (exp)`</mark>
  * <mark style="color:purple;">`Distance2 (2)`</mark>
  * <mark style="color:purple;">`Distance2Add (2add)`</mark>
  * <mark style="color:purple;">`Distance2Add (2sub)`</mark>
  * <mark style="color:purple;">`Distance2Add (2mul)`</mark>
  * <mark style="color:purple;">`Distance2Add (2div)`</mark>
  * <mark style="color:purple;">`Distance2Sq (2sq)`</mark>
  * <mark style="color:purple;">`Distance2Inv (2inv)`</mark>
  * <mark style="color:purple;">`Distance2Log (2log)`</mark>
  * <mark style="color:purple;">`Distance2Exp (2exp)`</mark>
  * <mark style="color:purple;">`Edge`</mark>
  * <mark style="color:purple;">`Rounded (round)`</mark>
  * <mark style="color:purple;">`NoiseLookup (noise)`</mark>\
    **Paramètres de recherche de bruit supplémentaires :**
    * <mark style="color:red;">`CellularNoiseLookup (Lookup)`</mark>\
      Lorsque vous utilisez le type de retour NoiseLookup, cela contrôle le bruit sous-jacent sur lequel superposer le bruit cellulaire.
      * <mark style="color:purple;">`Perlin (per)`</mark>
      * <mark style="color:purple;">`OpenSimplex2 (simplex)`</mark>
      * <mark style="color:purple;">`OpenSimplex2S (smooth)`</mark>
      * <mark style="color:purple;">`Value (val)`</mark>
      * <mark style="color:purple;">`ValueCubic (cubic)`</mark>
      * <mark style="color:purple;">`White`</mark>
      * <mark style="color:purple;">`Cellular (vor)`</mark>
    * <mark style="color:red;">`CellularNoiseLookupFrequency (DistReturn)`</mark>\
      Contrôle la fréquence du bruit sous-jacent.

</details>

### Paramètres du bruit des éclats

<details>

<summary>Paramètres du bruit des éclats</summary>

* <mark style="color:red;">`Sharpness (Sharp)`</mark>\
  Contrôle généralement `0..1.0`\
  la netteté du motif pour le bruit des éclats. Les valeurs élevées ont des bords plus définis dans le motif, tandis que les valeurs faibles apparaîtront plus floues.

</details>

### Paramètres du bruit fractal

<details>

<summary>Paramètres du bruit fractal</summary>

* <mark style="color:red;">`FractalType (Fractal)`</mark>\
 Définit le type de bruit fractal à utiliser.
  * <mark style="color:purple;">`None (No)`</mark>
  * <mark style="color:purple;">`FBm`</mark>
  * <mark style="color:purple;">`Ridged`</mark>
  * <mark style="color:purple;">`PingPong (PP)`</mark>\
    **Paramètre fractal PingPong supplémentaire :**
    * <mark style="color:red;">`PingPongStrength (PPStr)`</mark>

**Si le type fractal est autre que 
celui sélectionné :**

* <mark style="color:red;">`Octaves (Oct)`</mark>\
 Définit le nombre de couches de bruit fractal à utiliser.
* <mark style="color:red;">`Lacunarity (Lac)`</mark>\
  Définit l'échelle de chaque couche fractale. Les valeurs > 1 augmenteront effectivement la fréquence de chaque couche, les valeurs < 1 réduiront effectivement la fréquence de chaque couche.
* <mark style="color:red;">`Gain`</mark>\
  Définit la force relative de chaque couche fractale. Les valeurs < 1 diminueront la force de chaque couche, les valeurs > 1 augmenteront.
* <mark style="color:red;">`WeightedStrength (Weighted)`</mark>\
 Définit la réactivité de la force de chaque couche à la valeur du bruit.

</details>

### Paramètres de déformation de domaine

<details>

<summary>Paramètres de déformation de domaine</summary>

* <mark style="color:red;">`DomainWarpType (Warp)`</mark>\
  Définit le type de déformation de domaine à utiliser.
  * <mark style="color:purple;">`None (No)`</mark>
  * <mark style="color:purple;">`BasicGrid (Grid)`</mark>
  * <mark style="color:purple;">`OpenSimplex2 (Simplex)`</mark>
  * <mark style="color:purple;">`OpenSimplex2Reduced (Reduced)`</mark>
  * <mark style="color:purple;">`Flow`</mark>
  * <mark style="color:purple;">`Turbulence (Turb)`</mark>

**Si le type de déformation de domaine est autre que celui sélectionné :**

* <mark style="color:red;">`DomainWarpFreq (WarpFreq)`</mark>\
 Définit la fréquence de la déformation du domaine.
* <mark style="color:red;">`DomainWarpOct (WarpOct)`</mark>\
 Définit le nombre de couches pour la déformation de domaine.
* <mark style="color:red;">`DomainWarpGain (WarpGain)`</mark>\
  Définit la force relative de chaque couche de déformation de domaine.
* <mark style="color:red;">`DomainWarpAmp (WarpAmp)`</mark>\
  Définit l'amplitude globale (force) de la déformation du domaine.
* <mark style="color:red;">`DomainWarpFrac (WarpFrac)`</mark>\
  Définit le type fractal spécifique de déformation de domaine à utiliser.
  * <mark style="color:purple;">`None (No)`</mark>
  * <mark style="color:purple;">`DomainWarpIndependent (ind)`</mark>
  * <mark style="color:purple;">`DomainWarpProgressive (prog)`</mark>
* <mark style="color:red;">`DomainWarpLacunarity (WarpLac)`</mark>\
  Définit l'échelle de chaque couche de déformation de domaine.

</details>



## Exemples

**`Value(Seed:123,Freq:0.04)`**

<figure><img src="../.gitbook/assets/2024-01-10_20.38.35.png" alt=""><figcaption></figcaption></figure>

**`Cellular(Distance:Euclidean,DistReturn:NoiseLookup,Lookup:Perlin,LookupFreq:0.2,Freq:0.1)`**

<figure><img src="../.gitbook/assets/2024-01-10_20.41.26.png" alt=""><figcaption></figcaption></figure>
