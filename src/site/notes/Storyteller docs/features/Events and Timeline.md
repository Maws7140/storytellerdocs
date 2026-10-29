---
{"dg-publish":true,"permalink":"/storyteller-docs/features/events-and-timeline/"}
---


# Events and Timeline

The timeline is the visual history layer of Storyteller Suite. It can show your story as a traditional event timeline or as a Gantt-style schedule, depending on what you are trying to understand.

## Creating an event

Create events from:
- **Command palette:** `Storyteller Suite: Create new event`
- **Dashboard:** Events tab -> Create event

## Core event fields

- **Name** - the event title
- **Date / Time** - the main story date used for placement
- **End date** - optional duration for range-style events and Gantt bars
- **Status** - planned, active, complete, historical, or custom
- **Location** - main location reference
- **Characters involved** - linked characters
- **Items involved** - linked items
- **Groups involved** - linked groups
- **Description** - freeform markdown summary
- **Tags** - filtering and grouping labels
- **Milestone** - highlights the event as a major beat
- **Flashback / flashforward markers** - marks timeline relationship to the main narrative

## Views

> **Storyteller 2.0 (beta)** replaces the old timeline with a native canvas timeline. It stays fast on very large stories, follows your story's calendar, and draws everything below. Install the beta through BRAT from the `2.0.0-beta` prereleases. Your existing event notes are not changed or migrated.

Switch views with the segmented control at the left of the toolbar:

| View | Best for |
|---|---|
| **Chronology** | Events grouped into lanes, each with a marker on a baseline and a labelled chip below it. This is the default. |
| **Timeline** | One chronological spine with event cards alternating on either side. Choose **Horizontal** or **Vertical**. The vertical view reads like a calendar, with month and year dividers. |
| **Gantt** | Durations as bars, with dependency arrows. A bar too short for its label becomes a chip, with the real span shaded inside it. |
| **Calendar** | One month of the story's calendar, filling the pane. An event over several days is a tinted bar; a one-day event shows its icon (or a dot in its colour), its start time and its name. Taller panes show more events per week before the rest fold into *+N more*. Use **Today** and the arrows to change month. On narrow panes it becomes an agenda list. In edit mode, drag an event to another day. |

The same event data drives every view.

### Chronology view
Use this when you want to answer:
- What happened when?
- Which events overlap?
- Where are the major beats?
- How dense is the story in a given period?

### Gantt view
Use this when you want to answer:
- Which events have duration?
- What depends on what?
- How crowded is one arc compared to another?
- What stretches across multiple chapters or acts?

## The toolbar

The toolbar is grouped by what each control does:

- **What you are looking at:**
  - the view switch
  - **Group**: none, location, group, character, track, item, culture or magic system
  - **Track**
  - **Branch**: appears once you have alternate timelines
- **How much is on screen:** one zoom control that shows the visible span, with *Fit every event*, *Show a decade*, *Show a century* and *Jump to today*.
- **How it is drawn:**
  - **Theme** (see [[Storyteller docs/features/Timeline Themes\|Timeline Themes]])
  - **Edit**
  - **Show**: era backgrounds, presence bands, scenes, vault notes, stacking and narrative order, plus *Manage eras…*
- **On the right:**
  - the conflict badge
  - search with jump-to-event results
  - an overflow menu with *Export…* and *Refresh*

Each manager sits next to the list it manages: *Manage tracks…* at the end of the Track list, *Manage branches…* at the end of the Branch list, and *Edit theme…* and *Manage themes…* at the end of the Theme list.

## Navigating

- **Scroll:** a plain mouse wheel scrolls the lanes. When there are no lanes to scroll, it pans the time axis.
- **Zoom:** <kbd>Shift</kbd> + wheel, <kbd>Ctrl</kbd> + wheel, or a trackpad pinch zooms at the cursor. You can zoom from centuries down to minutes, depending on the calendar.
- **Touch:** drag to pan, and pinch to zoom.
- **Hover** over an event for its name, date, location, lane, description and any conflict messages.

## Editing dates on the timeline

Press **Edit** in the toolbar to turn on edit mode:

- Every place you can drop an event shows as a hollow **date slot**. Slots follow the active calendar's real days, weeks, months, years and decades.
- Draggable events get an accent ring around their marker. Drag the **marker** to a new date and release to save it. The notice shows the old date, because there is no undo.
- Scenes, vault notes and events with approximate dates ("around 1420") can't be dragged, so a vague date is never replaced with a precise one.

## What the timeline shows

- **Milestones** are gold stars. Pick a colour in the event modal to override the gold.
- **Conflicts:** an event involved in a conflict shows `!!` or `!` before its name, and its label takes the conflict colour.
- **Approximate dates** draw with a dashed outline.
- **Certainty:** an event marked reported, disputed or legendary draws faded, and its tooltip explains why.
- **Narrative order** (*Show → Narrative order*) adds `[n]` sequence numbers and draws narrative links between events.
- **Presence bands** (with *Group: character*) show where each character was between events, from their location history.

## Calendars

Each story can use its own **dating system**. Open Settings → Timeline → *Manage calendars*, or run `Manage custom calendars`. In the calendar designer you can set:

- any number of months
- leap rules
- day or minute precision
- seasonal cycles
- holidays

The axis, date slots and dragging all follow the active calendar. The bundled examples are Gregorian, Thirteen Moons and Japanese kō. Calendars can be shared as `.storycal.json` files or share codes.

## Alternate timelines (branches)

Create a branch with `Create timeline fork`, then pick it from the **Branch** field:

- A branch shows the history it grew from, up to its divergence point. Inherited events are faded, because editing one changes every branch.
- *Compare branches* stacks every branch under its parent. The curves leave at the real divergence point. A branch that is still being explored is dashed, an abandoned one is faint, and a merged one curves back into its parent.
- `View timeline forks` lists branches with their status, divergence, parent and event count.

Eras, tracks and branches are stored as **notes** in the story's folders. Sharing a story's folder shares its timeline structure too.

## Timeline blocks in notes

Embed a read-only, live timeline in any note with a fenced `timeline` block:

````markdown
```timeline
group: character
eras: true
characters: Mira, Tavin
from: 1420
to: 1430
height: 420
theme: Parchment
```
````

| Setting | Meaning |
|---|---|
| `group` | none, location, group, character, track, item, culture or magic |
| `gantt` | `true` for the Gantt view |
| `orientation` | `horizontal` or `vertical` |
| `height` | Height in pixels, 160–2000 (default 380) |
| `eras`, `presence`, `narrative`, `stack` | Turn layers on or off |
| `milestones` | `true` for milestones only |
| `characters`, `locations`, `groups`, `tags`, `era` | Comma-separated filters |
| `branch` | A branch id to show |
| `from`, `to` | Starting visible range. Set both or neither. |
| `theme` | A timeline theme's name or id |

Unknown settings are listed above the block instead of being silently ignored.

## Exporting

*Export…* in the overflow menu saves the timeline as PNG or JPG, either the current view or the **whole timeline** at high resolution. A theme's background image is included. CSV, JSON and Markdown exports list the visible events.

## Looks and themes

Colours, the lane palette, the label font, sizes and a background image all come from the story's timeline theme. See [[Storyteller docs/features/Timeline Themes\|Timeline Themes]] to pick, edit or share a theme, or to restyle the timeline with a CSS snippet.

## Tracks

Tracks are filtered timeline lanes.

A track can focus on:
- one character
- one location
- one group
- a custom filter set
- the whole story

Good uses for tracks:
- one protagonist plus a global track
- one city vs another city
- one faction's activity over time
- only milestone events

You can manage tracks manually or use **Auto-generate timeline tracks** to build starter tracks from your current entities.

## Eras and periods

Eras are named date ranges shown behind the events.

Use them for:
- acts
- wars
- reigns
- ages
- campaign arcs

They are useful when the story is long enough that isolated event dots stop being readable on their own.

## Milestones and alternate chronology

Milestones are just normal events with extra importance. Use them for:
- inciting incidents
- reveals
- deaths
- act breaks
- quest completions

Flashback and flashforward markers let you keep an event in the world timeline while still marking that it is told out of sequence.

## Putting normal notes on the timeline

The timeline is no longer limited to formal event notes.

You can also surface regular vault notes in two ways:

### Option 1: timeline watch property
Add a frontmatter property such as:

```yaml
timeline-date: 2025-01-15
```

Any note with the configured watch property appears on the timeline.

### Option 2: timeline watch tag
Tag a note with the configured timeline tag and add a normal `date` field:

```yaml
tags:
  - timeline
date: 2025-01-15
```

This is useful when you want journals, research notes, or lore notes to appear on the same timeline without converting them into formal event entities.

## Conflict detection

Use **Detect timeline conflicts** to scan for issues such as:
- impossible overlaps
- contradictory dates
- entities referenced in incompatible states
- circular chains of dependency

This is a review tool, not just a validator. It is best used after a big round of edits.

## Good defaults

If you are not sure how to structure events yet:
- use milestones sparingly
- keep tags short and consistent
- use groups when the story is faction-heavy
- switch to Gantt when duration matters more than single dates
- use tracks only after the main timeline starts feeling crowded
