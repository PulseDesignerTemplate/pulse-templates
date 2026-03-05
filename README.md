# block-valider

Repository de blocks normalises (1 fichier JSON par id/variant).

## Structure
- `manifest.json`: index global des categories + entrees.
- `blocks/<category>--<id>.json`: definition complete d'un variant.

## Schema d'un fichier variant
Chaque fichier `blocks/*.json` suit ce format:
- `schema_version` (number)
- `name` (string)
- `slug` (string)
- `category` (string)
- `id` (string)
- `label` (string)
- `description` (string)
- `height` (number)
- `created_at` (ISO-8601)
- `updated_at` (ISO-8601)
- `html` (string)

## Regenerer depuis library.php
```bash
php app/scripts/export-blocks-repository.php
```

## Chargement applicatif
`app/public/library.php` charge en priorite `block-valider/blocks/*.json`.
Si le repo est absent ou vide, le fallback historique dans `library.php` reste actif.
