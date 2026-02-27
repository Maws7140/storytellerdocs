---
{"dg-publish":true,"permalink":"/storyteller-docs/features/templates/"}
---


# Templates

Templates let you populate a story with a set of pre-built entities — characters, locations, groups, and their relationships — in one step. Storyteller Suite includes several built-in templates and a full editor for creating your own.

## Built-in Templates

The template gallery includes the following templates out of the box:

- **Fantasy Kingdom** — a medieval fantasy world with royalty, noble houses, a capital city, surrounding regions, and court intrigue relationships
- **Cyberpunk Metropolis** — a near-future city with megacorporations, underground factions, districts, and characters across the social spectrum
- **Murder Mystery** — a closed-circle mystery with suspects, a victim, a detective, key locations, and a timeline of events leading to and following the crime
- Additional genre templates are included and can be browsed in the gallery

## Applying a Template

1. Open the template gallery: **Storyteller Suite: Open story template gallery**
2. Browse and filter templates by genre (Fantasy, Sci-Fi, Mystery, Horror, and so on) and category (Full World, Entity Set, Single Entity)
3. Click **Preview** on any template to see what entities it will create
4. Click **Use Template** to apply it to the active story
5. If the template defines variables (character names, city names, faction names), a prompt appears to fill them in before the entities are created

## Entity Templates

Separate from full story templates, entity templates define the default structure for individual entity types. When you create a new character, location, or other entity, any matching entity template is applied automatically.

**Command:** Storyteller Suite: Open entity template library

Entity templates define:
- Default field values
- Custom fields to include
- Markdown section structure in the generated note

## Creating Custom Templates

Open the template editor from the template library or by clicking **Create Custom Template** in the story template gallery footer.

### Template Editor Tabs

**Metadata** — name, description, genre, category, tags, and version information

**Entities** — define which entity types the template creates and the default field values for each. Click a type to add entities of that kind, then edit each entity's fields.

**Variables** — define placeholder values that users fill in when applying the template. Use `{{variableName}}` syntax in entity field values to reference variables. Variable types include text, number, date, select (dropdown), and multi-select.

**Preview** — shows a summary of how many entity types and variables the template defines, and a preview of the entities that will be created.

## Saving a Note as a Template

While viewing any entity note, run **Storyteller Suite: Save note as template** to capture the current note's structure and field values as a reusable template.

## Importing and Exporting Templates

Templates are stored as JSON files in your vault. The template library's **Import Template** option (coming soon) will allow importing templates shared by other users.
