---
{"dg-publish":true,"permalink":"/storyteller-docs/features/maps/"}
---


# Maps

Maps are the spatial layer of Storyteller Suite. They can be simple image maps for fictional settings or real-world maps backed by tile layers.

## Two map modes

### Image maps
Use image maps for:
- world maps
- city plans
- dungeon layouts
- battle maps
- floor plans

You provide an image and place markers on top of it.

### Real-world maps
Use real-world maps when you want latitude / longitude navigation with tile servers or OpenStreetMap style behavior.

## Opening the map system

- **Command palette:** `Storyteller Suite: Open map view`
- **Dashboard:** Maps tab

## Creating a map

A map note can define:
- display name
- map type (`image` or `real`)
- base image or tile layer
- default zoom / bounds / center
- parent map
- linked location
- custom fields

## Marker sources

Storyteller Suite supports more than one way to get markers onto a map.

### 1. Manual placement
Place locations and other entities directly from the map UI.

Best for:
- quick setup
- one-off markers
- maps you edit mostly by hand

### 2. Frontmatter-based markers
Notes with marker-compatible frontmatter can be scanned into a map.

Best for:
- keeping map placement attached to the entity note
- reusing the same location on multiple maps
- syncing map state with location notes

### 3. Marker files / marker folders
A map can scan specific files or folders for marker data.

Best for:
- large map projects
- splitting marker data across regions
- map maintenance by folder conventions

### 4. Code block markers
A map note can also include marker definitions inside a code block.

Important: code block markers are useful for authored layouts, but they are effectively note-driven content. If you want to change them, edit the source note rather than expecting full in-map editing.

## Linked child maps and portals

Maps and locations can form a hierarchy.

Typical pattern:
- world map -> region location -> region map
- region map -> city location -> city map
- city map -> building location -> interior map

When a location is linked to another map, that marker acts like a portal and can jump to the child map.

## Linked entities on maps

Maps are not limited to locations. They can also reference:
- characters
- events
- items
- groups
- cultures
- economies
- magic systems
- scenes
- references

Use this when a map is more than just geography and needs to reflect story state.

## When to use which approach

Use manual placement when the map is still changing quickly.

Use frontmatter markers when:
- the entity note should stay the source of truth
- you want properties-pane visibility
- you want the same entity to appear on multiple maps cleanly

Use code block markers when:
- you want the map note itself to define a static layout
- you are documenting a reference map rather than interactively editing it

## Related settings

Map behavior is also affected by settings such as:
- internal Leaflet processor
- frontmatter marker support
- marker scanning
- child-map navigation from location pins

See [[Storyteller docs/reference/Settings\|Settings]].
