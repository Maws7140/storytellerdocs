---
{"dg-publish":true,"permalink":"/storyteller-docs/features/maps/"}
---


# Maps

The map view is an interactive Leaflet-based viewer that lets you place entity markers on images — world maps, city plans, dungeon layouts, or any image file in your vault.

## Opening the Map View

**Command palette:** Storyteller Suite: Open map view
**Dashboard:** Maps tab

## Creating a Map

In the Maps tab of the dashboard, click **Create map**. Give the map a name and select an image from your vault as the base layer. The image can be any format Obsidian supports — PNG, JPG, WebP, and so on.

## Placing Markers

### Location Markers
Switch the map to placement mode using the placement button in the toolbar. Click anywhere on the map to drop a location marker. A prompt appears to select which location from your story to attach to that point.

Location markers are displayed with a pin icon. Clicking a marker opens a popup with the location's name and description, plus buttons to open the location's note or navigate to a linked child map.

### Entity Markers
Entities other than locations (characters, events, items, groups) can also be placed on the map. Each entity type uses a distinct icon. Clicking an entity marker opens a popup with the entity's name and a button to open its note.

## Portal Links

A location can be linked to another map — for example, a city on a world map linked to a detailed city map. This creates a portal: the location marker shows a map icon in its popup, and clicking it navigates to the linked map. Portals allow drilling down through map hierarchy.

## Map Hierarchy

Maps and locations form a tree. A world map can contain region locations, each linked to a region map, which contains city locations linked to city maps, and so on. The map view maintains context as you navigate between levels.

## Editing Maps

Click the edit button in the map toolbar to open the map settings. You can:
- Rename the map
- Replace the base image
- Set a parent map for this map
- Link this map to a location (so it appears as a portal on the parent map)
- Add custom fields

## Multiple Maps

You can have any number of maps in a story. Switch between them using the map selector dropdown at the top of the map view.
