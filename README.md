# PROJET POKÉMON — RÉFÉRENTIEL UNIVERSEL FR
## Prismora Solutions — v2.0 — Mai 2026

### OBJECTIF PRIORITAIRE
Base de données vivante FR des cartes TCG Pocket : noms FR/EN, effets, attaques, coûts énergie, talents, visuels par extension. Utilisée par l'IA pour construire les meilleurs decks compétitifs en saison classée.

### OBJECTIF SECONDAIRE
Référentiel universel de l'univers Pokémon : TCG physique + Pocket, jeux vidéo, artworks officiels, planches imprimables numérotées haute qualité.

### STRUCTURE
- config/sources.json → toutes les sources, switchable sans toucher au code
- data/raw/ → JSON bruts sources
- data/processed/ → CSV propres (pokemon_master, sets_master, cards_pocket_fr, cards_fr_en)
- data/exports/print/ → planches imprimables
- assets/images/pocket/ → visuels Pocket par extension
- assets/images/tcg/ → visuels JCC physique
- assets/images/pokemon/ → artworks officiels

### TABLES PRINCIPALES
- pokemon_master.csv → ID interne PKM-XXXX + noms FR/EN + Pokédex
- sets_master.csv → toutes extensions (Pocket + physique) + ID SET-PKT-XX
- cards_pocket_fr.csv → TABLE PRIORITAIRE — cartes Pocket complètes FR
- cards_fr_en.csv → correspondance universelle FR/EN

### SOURCES
1. TCGdex API FR (api.tcgdex.net/v2/fr) — noms FR natifs
2. flibustier/pokemon-tcg-pocket-database — données techniques Pocket + images
3. chase-manning/pokemon-tcg-pocket-cards — complément Pocket
4. PokéAPI (pokeapi.co) — Pokédex complet
5. LimitlessTCG — fallback compétitif

### STOCKAGE
- Local I:\Drive Prismora → CSV, notebooks, config (léger)
- Google Drive 5To → images haute qualité, archives JSON, planches imprimables

### NOTEBOOK
TCG_BDD.ipynb — scripts de récupération et construction pas à pas