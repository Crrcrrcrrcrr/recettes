# Recettes — format fiches indépendantes

Structure proposée :

```
recettes_index.json              # index léger global
recettes_master_split.json       # métadonnées globales sans les recettes complètes
recettes/00001_....json          # une fiche indépendante par recette
```

## Ajouter une nouvelle recette

1. Créer une nouvelle fiche JSON dans `recettes/`, par exemple `00256_nom-recette.json`.
2. Garder le format `schema: recette_fiche` avec la recette dans la clé `recipe`.
3. Ajouter une entrée courte dans `recettes_index.json` uniquement quand tu veux qu’elle apparaisse dans le HTML.

Avantage : tu peux nettoyer une recette au fur et à mesure, l’envoyer sur GitHub comme fichier indépendant, puis l’indexer plus tard.

## Compatibilité

L’ancien `recettes_master.json` n’est pas écrasé. Le fichier `recettes_master_split.json` conserve les métadonnées globales et pointe vers l’index.
