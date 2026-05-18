# Migration Notes

Source content repository: `pages-main (1).zip`  
Template repository: `WowPage-main (1).zip`

## Migration strategy

The migrated site uses WowPage as the base repository and keeps the visual direction of WowPage: single-page homepage, card-style sections, warm accent color, rounded cards, scrollable news, and project cards.

The old homepage's custom layout and CSS were not copied wholesale. Instead, the content was reorganized into data files and rendered with Liquid loops.

## Important files

- `_data/home.yml`: all editable homepage content
- `_data/grandmaster.yml`: all editable GrandMaster page content
- `_pages/about.md`: data-driven homepage renderer
- `_pages/grandmaster.md`: data-driven GrandMaster renderer
- `assets/css/home.css`: WowPage-coupled styling plus small helper classes
- `_config.yml`: updated site metadata and author profile
- `_data/navigation.yml`: updated menu

## Preserved from the original site

- Name: He Jipei / 何基培
- Email: `hejipei0228@ruc.edu.cn`
- GitHub: `UPwith-me`
- Institution: Renmin University of China
- Research interests and current focus
- Learning background
- GrandMaster project content
- Augur project content
- Cross-modal aggressive instruction filtering project content
- Avatar image

## Deliberately removed / replaced

- Old homepage-specific CSS structure
- WowPage sample / joke content
- WowPage sample comments data
- Hard-coded homepage content blocks

## Items left for future manual addition

- CV PDF under `files/`
- Formal publications under `_publications/`, if available later
- Real institutional/project logos, if you want to replace the neutral SVG placeholders

## Packaging note

Bundled local font binaries were not included in the downloadable package. Restore them from your own template source if you need the original icon-font rendering.
