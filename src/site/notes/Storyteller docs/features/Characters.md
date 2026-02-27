---
{"dg-publish":true,"permalink":"/storyteller-docs/features/characters/"}
---


# Characters

Characters are the most feature-rich entity type in Storyteller Suite. Each character is stored as an Obsidian note with YAML frontmatter for structured fields and markdown sections for free-form content.

## Creating a Character

**Command palette:** Storyteller Suite: Create new character
**Dashboard:** Characters tab > Create character button

## Character Fields

### Basic Information
- **Name** — the character's display name, used as the note title
- **Status** — alive, deceased, unknown, or a custom status
- **Affiliation** — free-text field for organizational allegiances

### Physical Attributes
A dedicated section for demographic and physical details. All fields are free-text to accommodate any genre or style:

- **Gender** — gender identity or expression (e.g., Female, Non-binary, None)
- **Race / Ancestry** — species, lineage, or origin (e.g., Human, Half-Elf, Clone)
- **Age** — numerical or descriptive (e.g., 34, Ancient, Unknown)
- **Height** — measurement or descriptor (e.g., 5'10", Towering, Short)
- **Quirks & Mannerisms** — habits, ticks, and idiosyncrasies displayed as a freeform text block

Race and age are shown as small chips in the character's dashboard card alongside status and affiliation.

### Portrait
A character can have a portrait image linked from your vault or gallery. The image path is stored in frontmatter and displayed in the character modal and on generated character sheets.

### Traits
A comma-separated list of personality traits or descriptors. Displayed as tags on character sheets.

### Description and Backstory
Two free-form markdown sections. Description is for how the character presents themselves in the world; Backstory covers their history. Both support full markdown formatting.

### Relationships
Links to other characters with a relationship type (ally, rival, family member, mentor, and so on) and an optional label for more detail. Relationships are directional — adding a relationship from A to B does not automatically create a reverse link on B.

### Groups
Characters can belong to one or more groups (factions, guilds, families). Assign groups here; the character will then appear in the group's members list.

### Custom Fields
Any number of key-value pairs for fields beyond the built-in set — pronouns, weapon of choice, theme song, occupation, birth date, and so on.

## Editing an Existing Character

Click the character's name in the dashboard Characters tab, or open the character's note and use the **Open character modal** button that appears in the note header.

Changes made in the modal update the note's frontmatter and body sections. Changes made directly to the note are reflected the next time the modal opens.

## Character Sheet Export

Storyteller Suite can generate a formatted character sheet from any character. Run **Storyteller Suite: Generate character sheet** while the character's note is active.

Six visual themes are available: Classic, Manuscript, Minimal, Dossier, Neon, and D&D. You can switch between themes with a live preview before exporting.

Export options:
- **Save to note** — creates a new note with the rendered sheet in markdown
- **Export as HTML** — saves a standalone HTML file

See [[Storyteller docs/features/Character Sheets\|Character Sheets]] for full details on each theme.

## Viewing All Characters

**Dashboard:** Characters tab
**Command:** Storyteller Suite: View all characters

The character list shows name, race and age chips (if set), status, affiliation, balance, and a portrait thumbnail if one is set. Characters can be filtered by group membership or searched by name, description, and traits.
