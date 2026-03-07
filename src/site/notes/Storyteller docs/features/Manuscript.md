---
{"dg-publish":true,"permalink":"/storyteller-docs/features/manuscript/"}
---


# Manuscript

The manuscript system is where Storyteller Suite stops being just a worldbuilding tool and becomes a drafting workflow.

It combines:
- chapters and scenes
- draft-specific ordering
- writing board views
- compile workflows
- campaign-ready scene notes

## Chapters

Chapters are containers for scenes.

Typical chapter fields:
- **Name**
- **Number**
- **Summary**
- **Status**
- **Linked entities**

Use chapters when you want reader-facing structure. If you only need short playable beats, scenes can still stand on their own.

## Scenes

Scenes are the main writing unit.

Useful scene fields include:
- **Name**
- **Chapter**
- **Status**
- **POV character**
- **Date**
- **Priority**
- **Synopsis**
- **Emotional tone**
- **Intensity**
- **Linked characters, locations, items, groups, and events**
- **Setup / payoff scene links**

A scene note can work in three modes at once:
- drafting
- structural planning
- campaign play

## Writing board views

The writing workspace now includes multiple views for the same scene data:
- **Board** - scene order and structure
- **Arc** - emotional or intensity trends
- **Heatmap** - character presence / coverage
- **Plot hole detector** - structural review panel

These are best used after you already have a rough scene list.

## Drafts

A draft is a named scene order for one version of the manuscript.

Each draft can keep its own:
- scene order
- nesting / indentation
- include-in-compile choices
- compile workflow

This is important. You do not need one global compile setup anymore.

You can keep one draft for:
- chronological order
- reader-facing order
- trimmed export
- campaign recap version

## Compile workflows

The compile tab now works more like a workflow builder than a one-button export.

### What a workflow is
A compile workflow is an ordered list of steps such as:
- strip frontmatter
- prepend scene or chapter titles
- clean wiki links
- join scenes by chapter
- export markdown
- export HTML

### Preset vs custom workflows
You can:
- start from a preset workflow
- customize it into your own saved workflow
- assign a workflow to a specific draft
- set a default workflow for new drafts

### Custom compile steps
You can also define your own JavaScript compile steps.

Use this when you need custom behavior such as:
- inserting a house style block
- rewriting markers or placeholders
- transforming scene text before export
- creating a special output format for editors or players

This is powerful, but it is still just part of the compile pipeline. Your source notes stay unchanged unless you edit them directly.

## Campaign-ready scenes

Scenes can also drive the new Campaign Play mode.

If a scene should be playable, use **Edit Branches & Encounter Table**.

That lets a scene define:
- player-facing choices
- dice checks
- requirements like items or flags
- outcomes like adding items, setting flags, or jumping to another scene
- encounter tables for random or manual use

This is the bridge between writing notes and live session-running.

See [[Storyteller docs/features/Campaign Play\|Campaign Play]].

## Good workflow for most people

If you are writing a novel:
1. Create scenes first.
2. Assign chapters later.
3. Build one draft for structure.
4. Build a second draft for clean export.
5. Customize compile only after the scene order feels stable.

If you are running a campaign:
1. Use scenes as encounter or situation nodes.
2. Add branch logic only where player choice matters.
3. Keep one draft for the story path you expect.
4. Keep compile workflows for recap / export use, not session logic.
