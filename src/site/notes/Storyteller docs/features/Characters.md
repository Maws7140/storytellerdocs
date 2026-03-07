---
{"dg-publish":true,"permalink":"/storyteller-docs/features/characters/"}
---


# Characters

Characters are one of the core entity types in Storyteller Suite. Each character is stored as a normal Obsidian note with frontmatter for structured data and markdown sections for freeform writing.

## Creating a character

You can create a character from:
- **Command palette:** `Storyteller Suite: Create new character`
- **Dashboard:** Characters tab -> Create character

## Core character fields

### Identity and presentation
- **Name** - the note title and primary display label
- **Status** - alive, missing, retired, dead, or any custom label
- **Affiliation** - free-text allegiance or role
- **Traits** - short descriptors used for filtering and sheet output
- **Description** - who this character is in the story right now
- **Backstory** - what happened before the current story

### Physical details
Use these for either fiction or tabletop prep:
- **Gender**
- **Race / ancestry**
- **Age**
- **Height**
- **Quirks**

### Links and story context
Characters can link to:
- other characters through relationships
- groups
- current location and location history
- scenes and chapters
- items
- compendium entries
- economies, cultures, and magic systems

## Inventory and ownership

Two character fields matter for item tracking:

- **Owned items** - items this character currently carries or controls
- **Linked items** - items related to the character without implying direct ownership

Why this matters:
- the character note stays useful for writing and worldbuilding
- Campaign Play can seed party inventory from `ownedItems`
- plot item ownership can still be reassigned during a live session

Use `ownedItems` for things the character actually has in hand. Use `linkedItems` for things they are chasing, guarding, or associated with.

## D&D / RPG fields

Storyteller Suite now supports a lightweight D&D-style stat block directly on character notes.

### Class block
- `dndClass`
- `dndSubclass`
- `dndRace`
- `dndLevel`

### Ability scores
- `dndStr`
- `dndDex`
- `dndCon`
- `dndInt`
- `dndWis`
- `dndCha`

### Survival and combat
- `dndMaxHp`
- `dndCurrentHp`
- `dndTempHp`
- `dndAc`
- `dndSpeed`
- `dndProficiencyBonus`
- `dndHitDice`

### Status and proficiencies
- `dndConditions`
- `dndSkillProficiencies`
- `dndSavingThrowProficiencies`

You do not need to fill every D&D field. The useful minimum is:
- level
- six ability scores
- max HP
- current HP
- AC

## How character data is used elsewhere

Character notes are not isolated. The plugin reuses them across systems:

- **Character Sheets** use the same note data for export and themed presentation.
- **Timeline** can group or filter events around linked characters.
- **Groups** show character membership automatically.
- **Campaign Play** can use D&D stats for branch checks and HP tracking.
- **Inventory tracking** can pull starting party items from character ownership.

## Character sheet export

Run **Storyteller Suite: Generate character sheet** while a character note is active.

Built-in themes include:
- Classic
- Manuscript
- Minimal
- Dossier
- Neon
- D&D

The D&D theme is presentation only. It reads the same character note data you already entered.

See [[Storyteller docs/features/Character Sheets\|Character Sheets]].

## Good defaults for most users

If you do not know how much detail to enter, start with this set:
- Name
- Description
- Traits
- Status
- Affiliation
- Groups
- Current location

If you are running campaign play, add:
- D&D stats
- HP
- ownedItems

That is enough for the rest of the plugin to stay useful without turning the note into data entry busywork.
