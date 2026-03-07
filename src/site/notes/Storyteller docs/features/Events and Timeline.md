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

## Timeline view vs Gantt view

### Timeline view
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

The same event data drives both views.

## Useful toolbar features

The current timeline UI supports:
- search with jump-to-event results
- timeline / Gantt toggle
- milestone-only filtering
- grouping by character, location, or group
- date range and zoom controls
- track and era management

If you work with a large story, the search box is the fastest way to jump to a specific event instead of scrolling for it.

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
