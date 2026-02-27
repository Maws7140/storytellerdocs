---
{"dg-publish":true,"permalink":"/storyteller-docs/features/manuscript/"}
---


# Manuscript

The manuscript feature lets you organize your story's chapters and scenes, define a writing order, track word counts, and compile everything into a single document.

## Chapters

Chapters are containers for scenes. Create a chapter with **Storyteller Suite: Create new chapter** or from the **Scenes** tab of the dashboard.

Chapter fields:
- **Name** — the chapter title
- **Number** — used to sort chapters in the manuscript order
- **Summary** — a brief description of the chapter's events
- **Status** — outline, drafting, revising, complete
- **Word count goal** — an optional target for this chapter

## Scenes

Scenes are the individual writing units. Each scene is a regular Obsidian note with frontmatter tracking its metadata.

**Command:** Storyteller Suite: Create new scene

Scene fields:
- **Name** — the scene title
- **Chapter** — which chapter this scene belongs to
- **Status** — outline, drafting, revising, complete
- **POV character** — the point-of-view character for this scene
- **Location** — where the scene takes place
- **Summary** — a brief description
- **Priority** — used to sort scenes within a chapter
- **Include in compile** — whether this scene is included when compiling the manuscript

## Drafts

A draft is a specific ordering of scenes for compilation. One story can have multiple drafts — for example, Draft 1 might include all scenes in chronological order, while Draft 2 might exclude flashback scenes for a condensed version.

**Create a draft:** Storyteller Suite: Create draft
**Switch drafts:** Use the draft selector in the Scenes tab of the dashboard

Within a draft, scenes can be:
- Reordered by dragging
- Indented to create sub-scene hierarchy
- Included or excluded from compilation individually

## Navigating Between Scenes

While editing a scene note, use these commands to move between scenes in the current draft order:
- **Storyteller Suite: Go to next scene** — opens the next scene in draft order
- **Storyteller Suite: Go to previous scene** — opens the previous scene in draft order

## Compiling the Manuscript

**Command:** Storyteller Suite: Compile manuscript

This gathers all scenes in the active draft (those marked as included), concatenates their content in draft order, and creates a new note in your vault with the full compiled text. Chapters are used as section headings.

The compilation respects the scene order defined in your active draft, not the order of the scene notes themselves.

## Word Count Tracking

The Scenes tab in the dashboard shows word counts per scene and a total for the active draft. Word counts are calculated from the note content, excluding frontmatter.
