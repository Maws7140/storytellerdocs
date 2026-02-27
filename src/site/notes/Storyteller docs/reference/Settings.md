---
{"dg-publish":true,"permalink":"/storyteller-docs/reference/settings/"}
---


# Settings

All settings are under **Settings > Storyteller Suite**.

## General

**Active story**
The currently selected story. All entity creation and listing commands operate on this story.

**Prevent auto-folder creation**
When enabled, the plugin does not create the StorytellerSuite folder hierarchy on startup. You must create the folders manually before using the plugin.

**Language**
The UI language. English and German are included. Contributions for additional languages are welcome.

## Folder Paths

Each entity type has a dedicated folder where its notes are stored. All paths are relative to your vault root.

| Setting | Default |
|---------|---------|
| Characters folder | StorytellerSuite/Characters |
| Locations folder | StorytellerSuite/Locations |
| Events folder | StorytellerSuite/Events |
| Groups folder | StorytellerSuite/Groups |
| Scenes folder | StorytellerSuite/Scenes |
| Chapters folder | StorytellerSuite/Chapters |
| Gallery folder | StorytellerSuite/Gallery |
| References folder | StorytellerSuite/References |
| Plot items folder | StorytellerSuite/PlotItems |
| Cultures folder | StorytellerSuite/Cultures |
| Economies folder | StorytellerSuite/Economies |
| Magic systems folder | StorytellerSuite/MagicSystems |
| Compendium folder | StorytellerSuite/Compendium |
| Templates folder | StorytellerSuite/Templates |
| Character sheets folder | StorytellerSuite/CharacterSheets |

## Maps

**Enable internal Leaflet processor**
Controls whether Storyteller Suite's built-in Leaflet map renderer is active. Disable this if you use the standalone Obsidian Leaflet community plugin to prevent conflicts.

**Location pins open associated map**
When enabled, clicking a location marker on a map that has an associated child map navigates directly to that child map instead of opening a popup.

## Timeline

**Default timeline grouping**
The grouping mode applied when first opening the timeline. Options: none, by character, by location, by tag. This setting persists between sessions.

## Character Sheets

**Default character sheet theme**
The theme pre-selected when the character sheet preview modal opens. Options: Classic, Manuscript, Minimal, Dossier, Neon, D&D, and any custom themes you have created.

**Custom character sheet templates**
A list of your custom HTML themes. Each can be added, edited, or deleted from this section. See [[Storyteller docs/features/Character Sheets\|Character Sheets]] for the full token reference.
