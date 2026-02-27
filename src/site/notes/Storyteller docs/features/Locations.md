---
{"dg-publish":true,"permalink":"/storyteller-docs/features/locations/"}
---


# Locations

Locations represent places in your story world — cities, buildings, rooms, regions, planets. They support hierarchical nesting, sensory detail profiles, associated images, and placement on interactive maps.

## Creating a Location

**Command palette:** Storyteller Suite: Create new location
**Dashboard:** Locations tab > Create location button

## Location Fields

### Basic Information
- **Name** — the location's display name
- **Type** — city, building, region, dungeon, wilderness, and so on (customizable)
- **Description** — a free-form markdown field for the general description
- **Associated image** — a vault image path displayed in the location modal

### Hierarchy
Locations can be nested. Set a **Parent location** to place this location inside another — for example, a tavern inside a city, or a room inside a building. Child locations are listed on the parent's page.

### Sensory Profile
A detailed breakdown of the location's sensory atmosphere:
- **Sight** — visual details, lighting, colors
- **Sound** — ambient noise, echoes, silence
- **Smell** — scents and odors
- **Touch** — textures, temperature, physical sensations
- **Taste** — any flavors in the air or environment

### Entities at this Location
A list of characters, events, items, cultures, economies, magic systems, groups, and scenes associated with this location. Entities can be added from the location modal or by placing them on the map.

### Custom Fields
Additional key-value pairs for location-specific data — elevation, population, governing body, and so on.

## Map Integration

Locations can be placed on an interactive map as markers. Open a map from the **Maps** tab, enter placement mode, and click to drop a location pin. Clicking a location marker on the map opens a popup with the location's name, description, and a button to open its note.

Locations can also be linked to their own dedicated map — for example, a city location that has a city-level map. This creates a portal link: clicking the location marker on the parent map navigates to the child map.

See [[Storyteller docs/features/Maps\|Maps]] for more details.

## Viewing All Locations

**Dashboard:** Locations tab
**Command:** Storyteller Suite: View all locations

The list shows name, type, parent location, and entity count.
