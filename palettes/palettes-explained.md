# Les palettes expliquées

Les palettes dans ezEdits représentent une liste de blocs qui peuvent être utilisés dans plusieurs commandes où l'ordre des blocs sera conservé.\

Les palettes peuvent être enregistrées et accessibles à l'aide du **`#`** préfixe des palettes enregistrées par l'utilisateur et **`##`** des palettes prédéfinies intégrées. \
par exemple, `##LegacyWool` représente la palette de laine intégrée commençant par la laine blanche, la laine orange jusqu'à la laine rouge et enfin la laine noire.&#x20;

Certaines des nombreuses fonctionnalités qui utilisent des palettes incluent :

* `//eztexture ...` - *Commandes de texturation*
* `#palette` - *Masques*
* `//ezbrush gradient ...` - *Brushes*



Palettes can be constructed as a simple list of blocks, or via several modifiers:

* &#x20;**`,`** - Concaténer : ajoute un bloc ou une palette à la fin du bloc ou de la palette précédente.\
  par exemple, `stone,dirt` il s'agit d'une palette de 2 blocs de pierre et de terre. `stone,##LegacyWool` est une palette composée de pierre et des blocs de la palette prédéfinie ##LegacyWool.
* &#x20;**`-`** - Inverser : inverse l'ordre d'une palette.\
  Par exemple, `-##LegacyWool`la palette prédéfinie de laine est-elle dans l'ordre inverse (commence par le noir au lieu du blanc)
* &#x20;**`(start:end)`** - Sous-palette : renvoie une partie d'une palette. \
  Par exemple, `##LegacyWool(1:8)` renverra les 8 premiers blocs de la palette prédéfinie ##LegacyWool.
* &#x20;**`*`** - Répéteur : répète le segment précédent un nombre donné de fois.\
  Par exemple, `gold_block*10,diamond_block` renverra une palette de 10 blocs d'or, suivis d'un seul bloc de diamant.
* &#x20;**`[]`** - Regroupement : regroupe les palettes pour permettre à un modificateur de les traiter comme une seule palette.\
  Par exemple, `-##LegacyWool,gold_block` renverra la palette prédéfinie ##LegacyWool dans l'ordre inverse, avec un bloc doré à la fin. le `-[##LegacyWool,gold_block]` renverra le bloc doré au début.
* &#x20;**`=`** - Résultat : Permet de compléter une palette par tabulation dans sa liste de blocs si nécessaire.



**##Palette prédéfinie LegacyWool**

<figure><img src="../.gitbook/assets/2024-02-04_19.31.54.png" alt=""><figcaption></figcaption></figure>

