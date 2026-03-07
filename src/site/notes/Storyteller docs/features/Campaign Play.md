---
{"dg-publish":true,"permalink":"/storyteller-docs/features/campaign-play/"}
---


# Campaign Play

Campaign Play is the DM-facing mode for running scenes as playable encounters instead of just reading them as notes.

It is built for D&D-style play, but the structure also works for any RPG where you need:
- a current scene
- a party roster
- HP and conditions
- shared inventory
- flags / state changes
- gated choices
- simple dice checks

## How to open it

Campaign Play is currently opened from the **swords ribbon icon** in the left sidebar.

There is no dedicated command palette command for it yet.

## The mental model

Think of Campaign Play as a thin runtime layer on top of your existing notes:

- **Characters** provide stats, HP, conditions, and starting items.
- **Scenes** provide the text the DM reads plus the choices the players can take.
- **Plot items** provide inventory behavior and item-use effects.
- **Sessions** store the current scene, party, inventory, flags, HP changes, and session log.

You are not creating a separate game database. You are reusing the same notes you already write with.

## 5-minute setup

### 1. Prepare player characters

Open each player character and fill in the campaign-ready fields:

- `dndClass`, `dndSubclass`, `dndRace`, `dndLevel`
- `dndStr`, `dndDex`, `dndCon`, `dndInt`, `dndWis`, `dndCha`
- `dndMaxHp`, `dndCurrentHp`, `dndTempHp`
- `dndAc`, `dndSpeed`, `dndProficiencyBonus`
- `dndConditions`
- `dndSkillProficiencies`
- `dndSavingThrowProficiencies`
- `ownedItems`

Important: `ownedItems` matters. When you start a session, the party inventory is seeded from the selected characters' owned items.

### 2. Create plot items for anything you want to track

Use plot item notes for keys, quest items, consumables, magical artifacts, and tools.

Campaign-specific item fields include:
- `itemType`
- `itemRarity`
- `consumedOnUse`
- `campaignEffect`
- `grantsFlag`
- `navigatesToScene`
- `useRequiresLocation`
- `useRequiresFlag`

Practical examples:
- a key that sends the party to a vault scene
- a potion that disappears when used
- a relic that sets a `found-relic` flag
- a tool that only works in a specific location

### 3. Build a playable scene

Open a scene and use **Edit Branches & Encounter Table**.

Each branch can define:
- a label
- a target scene
- an optional fail scene
- a dice roll (`d4` to `d100`)
- a stat check (`str`, `dex`, `con`, `int`, `wis`, `cha`)
- a threshold
- requirements
- outcomes

### Requirements

You can gate a branch with:
- required item
- required character
- required flag
- passive minimum stat

### Outcomes

A branch can:
- grant an item
- remove an item
- add a character to the party
- remove a character from the party
- set a flag
- trigger an event
- navigate to another scene

If you want random content, add an encounter table to the same scene.

### 4. Start a session

Click the swords ribbon icon, then create a new session.

Pick:
- session name
- starting scene
- party members

The session note stores:
- current scene
- party members
- party HP state
- party inventory
- flags
- session log
- status (`active`, `paused`, `completed`)

### 5. Run the session

Inside Campaign Play you can:
- read the current scene body
- switch the active actor for stat-based choices
- roll branch checks
- follow scene-to-scene choices
- take items from the scene into party inventory
- assign inventory items to a specific party member or keep them shared
- use items
- adjust HP and conditions
- keep a running session log automatically

## What the sidebar is for

### Party

Use this to track:
- current HP / max HP
- temporary HP
- conditions

If a character does not have party state yet, you can initialize it from the sidebar.

### Inventory

This is the session's shared item state.

If a matching plot item note exists, you can also:
- assign an owner
- use the item
- trigger item behavior from its note fields

### Lore and log

The session view keeps quick-reference context near the scene and records what happened as you move through branches.

## Easy first demo setup

If you want a stable test story, build this:

1. Two characters with D&D stats.
2. One plot item called `Rust Key`.
3. A starting scene called `Locked Door`.
4. Branch A: `Pick the lock`
   - `dice: d20`
   - `stat: dex`
   - `threshold: 13`
   - success target: `Treasure Room`
   - fail mode: `loop`
5. Branch B: `Use the Rust Key`
   - `requiresItem: Rust Key`
   - success target: `Treasure Room`
6. A second scene called `Treasure Room`.

That one setup lets you test:
- stat checks
- inventory gates
- scene navigation
- session log updates

## Tips that save time

- Keep branch labels short. They become the player-facing choice text.
- Prefer linked target scenes where possible so scene renames do not break paths.
- Use flags for state you need to reference later, not for one-off flavor text.
- Use plot item notes for anything that should do something when used.
- Use location data when a place should apply ambient flags or encounter modifiers.

## Related pages

- [[Storyteller docs/features/Characters\|Characters]]
- [[Storyteller docs/features/Manuscript\|Manuscript]]
- [[Storyteller docs/features/Events and Timeline\|Events and Timeline]]

