---
{"dg-publish":true,"permalink":"/storyteller-docs/help/faq/"}
---


# FAQ

## Can I use multiple stories in the same vault?

Yes. Create separate stories with **Storyteller Suite: Create new story**. Only one story is active at a time — switching the active story in settings changes which entities appear in all lists and commands. Entities from different stories are stored in the same folders, distinguished by their frontmatter `storyteller-story-id` field.

## My template disappeared from the list after restarting Obsidian

The template markdown file still exists in your Templates folder but is no longer showing in the plugin. Try running **Storyteller Suite: Reload custom templates** to force a rescan of the templates folder.

## Can an item be owned by multiple characters?

The item owner field currently accepts a single character. Multiple ownership is a known limitation being worked on. As a workaround, add additional owners as a custom field.

## Can I link groups to Obsidian's graph view?

Groups do not currently generate standalone notes, so they do not appear as nodes in Obsidian's native graph view. This is planned for a future update. For now, characters and locations linked to a group do exist as notes and appear in the graph.

## Images I drag into Obsidian aren't showing up in the gallery

Images dragged from your operating system into Obsidian land in the vault root, not the plugin's gallery folder. The gallery only searches its configured folder. Use the gallery's upload button to add images correctly, or manually move the image file into the gallery folder and then refresh.

## My scenes don't appear in the timeline

The timeline shows events, not scenes directly. To represent a scene on the timeline, create a linked event with the scene's in-world date and associate the relevant characters and location.

## Can I use a custom calendar system for dates?

The timeline accepts any date string. Sorting uses a best-effort parse of the date value. For fully custom fantasy calendars, use a consistent format and the timeline will display events in the order they were entered rather than by parsed date value. Full custom calendar support is planned for a future update.

## The plugin conflicts with the standalone Obsidian Leaflet plugin

Go to **Settings > Storyteller Suite > Maps** and disable **Enable internal Leaflet processor**. This turns off Storyteller Suite's built-in map renderer and prevents the two plugins from interfering.

## Can I edit entity notes directly without the modal?

Yes. All entity data is stored as YAML frontmatter and markdown body sections in regular Obsidian notes. You can edit these notes directly in the editor. The plugin reads from the note the next time it opens the modal. Do not change the `storyteller-id` or `storyteller-story-id` frontmatter fields, as these link the note to the plugin's data.

## How do I back up my story data?

Your story data lives in two places: the entity notes in your vault (the markdown files) and the plugin settings stored in `.obsidian/plugins/storyteller-suite/data.json`. Back up both. The `data.json` file contains story metadata, group definitions, draft orders, template data, and settings that are not stored in individual notes.
