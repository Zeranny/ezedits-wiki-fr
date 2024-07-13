# Commandes de bruit

Toutes les sous-commandes sont sous `//eznoise`  (`//ezn`) \
par exemple `//eznoise list`

## `//eznoise ...`

### `list [SET]`

* `ALL`\
 Répertorie tous les préréglages de bruit disponibles
* `DEFAULT`\
 Répertorie tous les préréglages de bruit de plug-in par défaut
* `MINE`\
 Répertorie tous les préréglages de bruit définis par l'utilisateur

### `save <presetName> <noise> [-f]`

Enregistre un préréglage de bruit défini par l'utilisateur avec un nom donné.\
`-f` pour remplacer un préréglage de bruit existant.

### `delete <presetName>`

Supprime un préréglage de bruit défini par l'utilisateur correspondant au nom donné.

### `print <noise>`

Imprime les paramètres d'un préréglage de bruit donné dans le chat.
