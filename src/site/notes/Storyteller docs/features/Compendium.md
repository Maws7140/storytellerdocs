---
{"dg-publish":true,"permalink":"/storyteller-docs/features/compendium/"}
---


# Compendium

The Compendium is a world-knowledge database for entities that are neither characters nor items — creatures, plants, materials, potions, phenomena, and anything else that populates your world. Think bestiaries, herbalism guides, alchemical references, or field notes from a monster hunter.

## Creating a Compendium Entry

**Command palette:** Storyteller Suite: Create new compendium entry
**Dashboard:** Compendium tab > New Entry button

## Entry Types

Each entry is assigned one of six types:

| Type | Use for |
|------|---------|
| **Creature** | Animals, monsters, sentient beasts, undead, spirits |
| **Plant** | Flora, fungi, supernatural vegetation |
| **Material** | Metals, minerals, alchemical reagents, rare fabrics |
| **Potion** | Brews, elixirs, tinctures, consumables |
| **Phenomenon** | Weather events, magical anomalies, natural wonders |
| **Other** | Anything that doesn't fit the above |

## Fields

### Core
- **Name** — required
- **Entry Type** — one of the six types above
- **Rarity** — Common, Uncommon, Rare, Legendary, or Mythical
- **Danger Rating** — None, Low, Medium, High, or Deadly
- **Profile Image** — an image from your vault or gallery

### Narrative Sections
| Section | Purpose |
|---------|---------|
| **Description** | Physical appearance and overview |
| **Behavior & Ecology** | Habits, habitat, diet, growth conditions |
| **Properties** | Physical, magical, or alchemical properties |
| **History & Lore** | World mythology, historical significance |
| **Dimorphism** | Male/female or juvenile/adult differences (creatures) |
| **Hunting Notes** | Tactics, vulnerabilities, and harvest methods |

### Linked Entities
Compendium entries support circular links to all major entity types:

| Link | Direction | Notes |
|------|-----------|-------|
| **Locations** | One-way → Location | Where it can be found |
| **Characters** | Bidirectional ↔ Character | Hunters, researchers, those who use or encounter it |
| **Items** | Bidirectional ↔ Plot Item | Items derived from or related to this entry |
| **Magic Systems** | Bidirectional ↔ Magic System | Systems that involve or draw from this entry |
| **Cultures** | Bidirectional ↔ Culture | Cultures that use, worship, or fear it |
| **Events** | Bidirectional ↔ Event | Events involving this entry |

When you link a Compendium entry to a character, that character's note is automatically updated with a back-link — and vice versa.

## Dashboard Card

Each entry in the Compendium tab shows:
- Profile image (or initials placeholder)
- Name with a colored **entry-type badge** (creature, plant, material, etc.)
- **Rarity badge** (color-coded from common grey to mythical purple)
- **Danger badge** for deadly or high-danger entries
- Description preview
- Count of linked locations and characters

## Filtering

The search bar at the top of the Compendium tab filters by name, entry type, and description.

## Viewing All Entries

**Dashboard:** Compendium tab
**Command:** Storyteller Suite: View compendium
