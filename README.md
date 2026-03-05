# block-valider

Repository de blocks normalises (1 fichier JSON par id/variant).

## Structure
- `manifest.json`: index global des categories + entrees.
- `blocks/<category>--<id>.json`: definition complete d'un variant.

## Schema d'un fichier variant
Chaque fichier `blocks/*.json` suit ce format:
- `type` (`"classique"` | `"pre-fait"` | `"perso"`)
- `category` (string)
- `id` (string)
- `label` (string)
- `icon` (string)
- `description` (string)
- `schema_version` (number)
- `name` (string)
- `slug` (string)
- `height` (number)
- `created_at` (ISO-8601)
- `updated_at` (ISO-8601)
- `html` (string)


