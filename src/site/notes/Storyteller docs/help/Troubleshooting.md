---
{"dg-publish":true,"permalink":"/storyteller-docs/help/troubleshooting/"}
---


# Troubleshooting

## Plugin fails to load ("Failed to load plugin" error)

This usually means the plugin files are missing or incomplete.

1. Go to your vault's `.obsidian/plugins/storyteller-suite/` folder
2. Confirm that `main.js`, `styles.css`, and `manifest.json` are all present
3. If any are missing, reinstall the plugin by downloading the latest release and copying the files again
4. Restart Obsidian

## Entity notes aren't being picked up by the plugin

The plugin discovers entity notes by reading their frontmatter. A note must have a `storyteller-id` and `storyteller-story-id` field to be associated with a story. If you moved or renamed notes outside the plugin, these fields may be missing or incorrect.

Check the note's frontmatter and ensure these fields are present and match a valid story ID. You can find your story's ID in the plugin's `data.json` file under `.obsidian/plugins/storyteller-suite/`.

## Changes to entity fields aren't saving

If changes made in the modal are not persisting:

1. Confirm you are clicking **Save** at the bottom of the modal (not just closing it)
2. Check that the entity note is not open in another application that might have a file lock on it
3. Check the Obsidian developer console (`Ctrl/Cmd + Shift + I`) for any error messages
4. If the body text fields specifically are not updating, this is a known issue on some systems. As a workaround, edit the note content directly in the editor.

## The dashboard tabs are cut off or not scrolling

This can happen if the Obsidian sidebar is very narrow. Widen the sidebar by dragging its edge. The dashboard tabs will reflow to fit.

## Map markers are not showing after adding them

If you placed a marker but it is not visible:

1. Reload the map view by closing and reopening it
2. Check that the location is assigned to the correct story
3. If the map image is very large or slow to load, wait for it to fully render before checking for markers

## Conflict with the Obsidian Leaflet plugin

See the FAQ entry: [[Storyteller docs/help/FAQ#The plugin conflicts with the standalone Obsidian Leaflet plugin\|FAQ#The plugin conflicts with the standalone Obsidian Leaflet plugin]]

## CSS from Storyteller Suite is affecting other parts of Obsidian

Storyteller Suite uses scoped CSS classes. If you notice layout issues in areas unrelated to the plugin (such as the file explorer), it may be an interaction with another plugin's CSS. Check if disabling Storyteller Suite resolves the issue. If it does, report the conflict at the [GitHub issues page](https://github.com/Maws7140/obsidian-storyteller-suite/issues) with details about the conflicting plugin.

## Reporting a Bug

If you encounter a bug not covered here:

1. Open the Obsidian developer console (`Ctrl/Cmd + Shift + I`) and check for error messages
2. Note the steps to reproduce the problem
3. Open an issue at [github.com/Maws7140/obsidian-storyteller-suite/issues](https://github.com/Maws7140/obsidian-storyteller-suite/issues) with the error message, reproduction steps, your Obsidian version, and your operating system
