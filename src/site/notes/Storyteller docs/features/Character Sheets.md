---
{"dg-publish":true,"permalink":"/storyteller-docs/features/character-sheets/"}
---


# Character Sheets

Storyteller Suite can generate a formatted character sheet from any character's data. Sheets can be exported as a standalone HTML file or saved as an Obsidian note.

## Generating a Sheet

1. Open the character's note or select the character in the dashboard
2. Run **Storyteller Suite: Generate character sheet**
3. The preview modal opens, showing the sheet in the default theme
4. Use the theme dropdown to switch between visual styles
5. Click **Export as HTML** or **Save to note**

## Themes

Six built-in themes are included:

**Classic**
A dark glass aesthetic with a portrait panel, colored stat fields, and section cards on a dark background. The default theme.

**Manuscript**
A warm cream background with Georgia serif typography and brown ink tones. Styled after a typed manuscript or written character dossier.

**Minimal**
A white background with neutral greys and a clean table layout. Designed to print well and work in any context without strong stylistic opinions.

**Dossier**
A manila paper background with Courier New monospace type and dark red stamp accents. Styled as a classified investigative file.

**Neon**
A near-black background with cyan glow borders and scanline texture. Suited to cyberpunk and sci-fi stories.

**D&D**
An aged parchment background with dark red headers, decorative dividers, and a two-column stat-block layout. Designed for fantasy tabletop-adjacent stories.

## Custom Themes

Custom character sheet themes can be created in **Settings > Storyteller Suite > Character Sheet Templates**. A custom theme is an HTML document with `{{token}}` placeholders that are replaced with character data at generation time.

### Available Tokens

| Token | Content |
|-------|---------|
| `{{name}}` | Character name |
| `{{portrait_img}}` | Portrait image tag (HTML export) or wikilink (note export) |
| `{{status}}` | Character status |
| `{{affiliation}}` | Affiliations field |
| `{{gender}}` | Gender |
| `{{race}}` | Race / ancestry |
| `{{age}}` | Age |
| `{{height}}` | Height |
| `{{quirks}}` | Quirks and mannerisms |
| `{{occupation}}` | Occupation (custom field) |
| `{{born}}` | Birth date (custom field) |
| `{{traits}}` | Comma-separated traits |
| `{{description}}` | Description section |
| `{{backstory}}` | Backstory section |
| `{{relationships_html}}` | Pre-rendered relationship list |
| `{{groups_html}}` | Pre-rendered group membership list |
| `{{locations_html}}` | Pre-rendered associated locations list |
| `{{items_html}}` | Pre-rendered items list |
| `{{events_html}}` | Pre-rendered timeline entries |
| `{{custom_fields_html}}` | Pre-rendered custom fields table |
| `{{date_generated}}` | Date the sheet was generated |

## Setting a Default Theme

Go to **Settings > Storyteller Suite > Character Sheet Templates** and choose a default from the dropdown. This theme will be pre-selected each time the preview modal opens.
