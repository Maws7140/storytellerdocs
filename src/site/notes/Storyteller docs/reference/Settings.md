---
{"dg-publish":true,"permalink":"/storyteller-docs/reference/settings/"}
---


# Settings

All settings live under **Settings > Storyteller Suite**.

This page focuses on the settings that most users actually need to understand.

## General

### Active story
The currently selected story. Most commands and dashboard lists operate on this story.

### Prevent auto-folder creation
If enabled, Storyteller Suite will not create its folder structure for you.

Use this only if you want strict manual control over folder creation.

### Language
Changes the plugin UI language.

## Folder paths

Each entity type can use its own folder path. Paths are relative to the vault root.

| Setting | Default idea |
|---------|--------------|
| Characters folder | Character notes |
| Locations folder | Location notes |
| Events folder | Event notes |
| Groups folder | Group notes |
| Scenes folder | Scene notes |
| Chapters folder | Chapter notes |
| Sessions folder | Campaign session notes |
| Gallery folder | Image storage |
| References folder | Reference notes |
| Plot items folder | Item notes |
| Cultures folder | Culture notes |
| Economies folder | Economy notes |
| Magic systems folder | Magic system notes |
| Compendium folder | Compendium notes |
| Templates folder | Template files |
| Character sheets folder | Generated sheet output |

The important addition for the new RPG flow is **Sessions folder**. That is where Campaign Play stores session notes and logs.

## Timeline and parsing

### Custom fields serialization
This controls how custom fields are written into note frontmatter.

- **Flatten** - custom fields are written at the top level. Best for Dataview and direct querying.
- **Nested** - custom fields are grouped under one key. Best if you want cleaner frontmatter namespaces.

### Custom today
Overrides what the plugin treats as `today` for relative date parsing.

Useful for:
- long-running fictional timelines
- campaign prep where you want a fixed in-world date
- reproducible timeline review

## Timeline defaults

### Default timeline grouping
The first grouping mode when you open the timeline.

Current grouping modes:
- none
- by location
- by group
- by character

### Default zoom preset
Controls the first zoom state when the timeline opens.

### Default stacking
If enabled, overlapping items stack by default instead of fighting for the same space.

### Default density
Controls how compressed or spread out the initial timeline render feels.

### Show legend by default
Toggles whether the legend starts open.

## Gantt settings

These affect the Gantt-style timeline mode.

### Show progress bars in Gantt
Shows progress overlays on duration-based items.

### Default Gantt duration
Used when an event has a start date but no end date.

### Dependency arrow style
Controls whether dependency arrows are solid, dashed, or dotted.

## Vault note timeline inclusion

These two settings let regular notes appear on the timeline even when they are not formal event notes.

### Timeline watch property
Any note with this frontmatter property is included on the timeline using the property's value as the date.

Example:

```yaml
timeline-date: 2025-01-15
```

### Timeline watch tag
Any note with this tag and a normal `date` field is included on the timeline.

Example:

```yaml
tags:
  - timeline
date: 2025-01-15
```

## Maps

### Enable internal Leaflet processor
Turns the built-in map renderer on or off.

Disable this if you want to rely on another Leaflet plugin instead.

### Location pins open associated map
If enabled, clicking a location marker with a linked child map jumps straight into that child map.

## Character sheets

### Default character sheet theme
The theme preselected when the character sheet preview opens.

Built-in themes currently include:
- Classic
- Manuscript
- Minimal
- Dossier
- Neon
- D&D

### Custom character sheet templates
This is where your custom HTML-based character sheet themes are managed.

## Important note about compile workflows

Compile workflows are **not** managed from Settings.

They live in the **Compile** tab of the dashboard, where you can:
- choose a workflow per draft
- customize presets
- save custom workflows
- add custom JavaScript compile steps
