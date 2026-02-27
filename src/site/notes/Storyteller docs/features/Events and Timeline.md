---
{"dg-publish":true,"permalink":"/storyteller-docs/features/events-and-timeline/"}
---


# Events and Timeline

The timeline gives you a scrollable, filterable view of your story's events. It supports multiple tracks, era overlays, custom date systems, and conflict detection.
![](https://i.ibb.co/rKDqXv92/yh2WJ9r.png)

## Creating an Event

**Command palette:** Storyteller Suite: Create new event
**Dashboard:** Events tab > Create event button

## Event Fields

- **Name** — the event's title
- **Date/Time** — the in-world date. The timeline sorts and positions events by this value. Any date format is accepted; the timeline will attempt to parse it.
- **End date** — for events with duration, displays as a range on the timeline
- **Status** — planned, in progress, completed, historical, or custom
- **Location** — links the event to a location
- **Characters involved** — links characters to this event
- **Description** — a free-form markdown field
- **Tags** — for filtering and grouping
- **Is milestone** — marks the event as a significant story beat, highlighted on the timeline
- **Is flashback / flashforward** — marks the event's temporal relationship to the main narrative

## The Timeline View

Open the full timeline panel with **Storyteller Suite: Open timeline panel** or from the **View Timeline** button on the dashboard.

### Tracks

The timeline supports multiple tracks displayed in parallel horizontal lanes. Each track can be filtered to show only events matching certain criteria — by character, location, group, or custom tags. This lets you view, for example, one track showing all events involving a specific character alongside a global track.

Manage tracks with **Storyteller Suite: Manage timeline tracks**. Tracks can be reordered by dragging, toggled visible or hidden, and color-coded.

### Eras

Eras are named date ranges displayed as colored bands behind the timeline. They are useful for marking historical periods, story acts, or in-world ages. Manage eras with **Storyteller Suite: Manage timeline eras**.

### Timeline Forks

A timeline fork represents an alternate history or branching narrative. Create forks with **Storyteller Suite: Create timeline fork**. Events in a fork are displayed separately and can be compared to the main timeline.

### Conflict Detection

**Storyteller Suite: Detect timeline conflicts** analyzes your events for logical inconsistencies — characters in two places at once, events referencing entities that do not exist, circular causal chains, and similar problems. Conflicts are displayed in a list with descriptions and suggested resolutions.

### Filtering

The timeline toolbar includes filters for:
- Date range
- Character
- Location
- Tags
- Event status
- Milestones only
- Flashbacks / flashforwards

### Generating Events from Tags

**Storyteller Suite: Generate events from scene tags** scans your scene and chapter notes for date-tagged content and creates timeline events automatically, linking them to the relevant scenes.

## Viewing All Events

**Dashboard:** Events tab
**Command:** Storyteller Suite: View timeline (modal view)
