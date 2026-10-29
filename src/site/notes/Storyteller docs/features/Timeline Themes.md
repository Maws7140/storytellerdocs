---
{"dg-publish":true,"permalink":"/storyteller-docs/features/timeline-themes/"}
---


# Timeline Themes

> **Storyteller 2.0 (beta).** Timeline themes are part of the native timeline that ships with the 2.0 beta.

A timeline theme controls how the timeline looks for one story:

- every colour on the canvas
- the lane palette
- the label font
- chip, lane and connector sizes
- an optional background image

Each story uses one theme, and you can switch at any time. Your events and notes are never touched.

You can restyle the timeline three ways. All three set the same `--sts-timeline-*` CSS variables, so they combine predictably:

1. **Pick or edit a theme** in the theme editor. This is the easiest option and needs no CSS.
2. **Share a theme** as a share code or a `.storytl.json` file.
3. **Write a CSS snippet** that overrides the variables directly.

When more than one sets the same variable, the **theme wins over a snippet**, and **a snippet wins over the Obsidian theme**. The *Obsidian native* theme sets nothing, so with it selected your snippet and your Obsidian colours decide everything.

## Picking a theme

- **From the timeline:** use the **Theme** field in the timeline toolbar, next to *Edit*. It lists every theme. *Edit theme…* opens the editor on the current theme, and *Manage themes…* opens the theme list.
- **From settings:** go to Settings → Storyteller Suite → Timeline → **Timeline theme**. Use *Manage themes* or the pencil button there.
- **From the command palette:** run `Storyteller Suite: Edit timeline theme` or `Storyteller Suite: Manage timeline themes`.

A new theme takes effect on every open timeline of the story straight away. You don't need to reopen anything.

### Bundled themes

| Theme | What it looks like |
|---|---|
| **Obsidian native** | Follows your Obsidian theme and any CSS snippet. This is the default. |
| **High contrast** | Black canvas, white text and saturated lane colours. Good for projection and readability. |
| **Parchment** | Warm paper, ink text, serif labels and dashed dependency arrows. Suits chronicles and histories. |
| **Minimal** | Your Obsidian colours with a quiet palette, flat chips and thin lines. |

Bundled themes can't be changed in place. If you edit one, the editor works on a copy, and saving switches the story to that copy.

## The theme editor

The editor shows a **live preview of your active story's timeline** at the top. The preview stays in view while you scroll the form and redraws as you change things. Your open timelines only change when you press **Save theme**.

| Section | What it controls |
|---|---|
| **Identity** | Name and description. |
| **Canvas colours** | Background, surface (chips, cards, axis header), lane sidebar, grid and period lines. |
| **Text colours** | Text, muted text (axis dates), accent text (period labels) and text on coloured Gantt bars. |
| **Accent colours** | Accent (selection and edit handles), connectors, the today line, era and holiday bands with no colour of their own, the milestone star and its rim, and edit-mode date slots. |
| **Signal colours** | Conflict and conflict-warning labels, and the flashback and flash-forward badges. |
| **Lane palette** | The colours handed out to lanes, characters, locations and calendar cycles in turn. Turn on *Custom palette* to edit it. You can use 1 to 24 colours. |
| **Background image** | See the next section. |
| **Typography** | A CSS font family for every label, for example `Georgia, serif`. Leave it blank to use the Obsidian interface font. |
| **Events** | Corner radius, chip height and opacity. |
| **Lanes** | Label column width, minimum lane height and the gap below each lane. |
| **Axis** | Label density, and whether calendar cycles and holidays show under the axis. |
| **Connectors** | Line width, and the dependency arrow style. *Use the setting* follows the dependency arrow style in Timeline settings. |
| **Share** | Copy the theme as a share code or as JSON. |

Every colour row has a ↺ button. It removes the theme's colour so that role goes back to following Obsidian. A colour picker always opens on the colour currently in use, even when that colour is inherited.

Colours, lane and chip sizes, and the background image all come from the theme. Your own per-item colours still win over the theme: an event's colour, a coloured track, group, era or branch, and calendar cycle and holiday colours.

## Background images

A theme can draw an image behind the timeline, such as a world map, a parchment texture or a starfield.

- **Image:** a vault image (use **Choose** to pick one), or an `https://` link.
- **Fit:**
  - **Cover** fills the timeline and crops the overflow.
  - **Contain** shows the whole image.
  - **Stretch** distorts the image to fill the timeline.
  - **Tile** repeats the image at its natural size.
- **Position:** the edge the image is anchored to when it doesn't fit exactly: center, top, bottom, left or right.
- **Image opacity:** how strongly the image shows through the background colour. It starts at 35%, so labels stay readable.
- **Blur:** softens a busy image, from 0 to 24 pixels.

The lane sidebar and the axis header keep their solid colours on top of the image, so lane names and dates stay legible. Image exports from the timeline include the background.

> **Sharing:** a vault image only exists in your vault. A share code that names a vault path shows no image for anyone else. To share a theme with its background, use an `https://` link. A small image can also be embedded as a `data:image/...;base64,` URI in the theme file.

## Sharing themes

- **Share code:** in the theme editor or the theme list, choose *Copy share code*. Anyone can paste it into Settings → Timeline → **Import dating system or timeline theme**.
- **File:** choose *Copy as JSON* and save the text as `my-theme.storytl.json`. The same import box accepts the file's contents.

Imported themes are checked field by field. A malformed colour, number or image source is dropped, and the rest of the theme still imports. Background images must be vault paths, `https://` links or inline `data:image` URIs. Anything else is ignored.

## A theme for one timeline block

A fenced `timeline` block can draw with a different theme from the story's:

````markdown
```timeline
group: character
theme: Parchment
height: 420
```
````

`theme:` takes a theme's name or id. If no theme matches, the block says so above the timeline and uses the story's theme.

## CSS variables

You can restyle the timeline from a CSS snippet: Settings → Appearance → CSS snippets. Target `.sts-native-timeline`:

```css
.sts-native-timeline {
  --sts-timeline-background: #10141c;
  --sts-timeline-accent: #ff8a3d;
  --sts-timeline-font: "Iowan Old Style", Georgia, serif;

  /* a four-colour lane palette */
  --sts-timeline-lane-count: 4;
  --sts-timeline-lane-1: #ff8a3d;
  --sts-timeline-lane-2: #3dd6ff;
  --sts-timeline-lane-3: #b48cff;
  --sts-timeline-lane-4: #7bd88f;
}

/* different values in light mode */
.theme-light .sts-native-timeline {
  --sts-timeline-background: #fbf8f2;
}
```

Snippets apply while the story uses the **Obsidian native** theme, or a theme that leaves that colour unset. The timeline repaints as soon as you save the snippet or switch between light and dark mode.

### Variable reference

| Variable | Theme file key | Default | Used for |
|---|---|---|---|
| `--sts-timeline-background` | `colors.background` | `--background-primary` | Canvas behind everything |
| `--sts-timeline-surface` | `colors.surface` | `--background-secondary` | Event chips, cards, axis header |
| `--sts-timeline-sidebar` | `colors.sidebar` | `--background-secondary-alt` | Lane name sidebar |
| `--sts-timeline-grid` | `colors.grid` | `--background-modifier-border` | Gridlines, borders, axis line |
| `--sts-timeline-grid-strong` | `colors.gridStrong` | `--background-modifier-border-hover` | Month and year dividers (vertical view) |
| `--sts-timeline-text` | `colors.text` | `--text-normal` | Event names and labels |
| `--sts-timeline-text-muted` | `colors.mutedText` | `--text-muted` | Axis dates, secondary details |
| `--sts-timeline-text-accent` | `colors.accentText` | `--text-accent` | Period labels, uncoloured era names |
| `--sts-timeline-text-on-accent` | `colors.onAccent` | `--text-on-accent` | Labels on coloured Gantt bars |
| `--sts-timeline-accent` | `colors.accent` | `--interactive-accent` | Selection, edit handles, main lane |
| `--sts-timeline-connector` | `colors.connector` | `--interactive-accent` | Dependency arrows, narrative links |
| `--sts-timeline-now` | `colors.now` | `--color-red` | Today line |
| `--sts-timeline-conflict-error` | `colors.conflictError` | `--color-red` | Labels of events with a conflict |
| `--sts-timeline-conflict-warning` | `colors.conflictWarning` | `--color-yellow` | Labels of events with a possible conflict |
| `--sts-timeline-flashback` | `colors.flashback` | `--color-purple` | Flashback badge |
| `--sts-timeline-flashforward` | `colors.flashforward` | `--color-orange` | Flash-forward badge |
| `--sts-timeline-era` | `colors.era` | `#8b5cf6` | Eras without their own colour |
| `--sts-timeline-holiday` | `colors.holiday` | `#f59e0b` | Holidays without their own colour |
| `--sts-timeline-milestone` | `colors.milestone` | `#d9a520` | Milestone star |
| `--sts-timeline-milestone-edge` | `colors.milestoneEdge` | `#8a6410` | Milestone star rim |
| `--sts-timeline-slot` | `colors.slot` | `#0b0f16` (`#9aa4b2` in light mode) | Edit-mode date slots |
| `--sts-timeline-font` | `font` | `--font-interface` | Every label |
| `--sts-timeline-lane-count` | length of `palette` | `10` | How many lane colours are used (1–24) |
| `--sts-timeline-lane-1` … `-24` | `palette[0]` … `palette[23]` | a 10-colour palette | Lane, character, location and cycle colours |

Shapes and the background image are set in the theme file only, not in CSS. That covers event size, lane size, axis density, connectors and the image.

## Theme file format

A `.storytl.json` file looks like this. Every field except `id` and `name` is optional. Anything you leave out keeps its default.

```json
{
  "kind": "storyteller-timeline-theme",
  "schemaVersion": 1,
  "metadata": { "author": "Your name", "description": "Dusk over the harbour" },
  "theme": {
    "id": "harbour-dusk",
    "name": "Harbour dusk",
    "description": "Deep blue canvas with warm lanes.",
    "font": "Georgia, serif",
    "colors": {
      "background": "#0f1726",
      "surface": "#17223a",
      "sidebar": "#121b2e",
      "grid": "#2a3a5c",
      "text": "#e8ecf5",
      "mutedText": "#9aa6c2",
      "accent": "#ffb454",
      "connector": "#ffb454",
      "milestone": "#ffd166"
    },
    "palette": ["#ffb454", "#5ec8ff", "#c792ea", "#7ee787", "#ff7b72"],
    "background": {
      "image": "https://example.com/harbour-map.jpg",
      "fit": "cover",
      "position": "center",
      "opacity": 0.3,
      "blur": 2
    },
    "event": { "radius": 4, "height": 26, "opacity": 1 },
    "lane": { "labelWidth": 200, "height": 40, "gap": 10 },
    "axis": { "density": 50, "showCycles": true, "showHolidays": true },
    "connectors": { "width": 2, "dependencyStyle": "dashed" }
  }
}
```

| Field | Range | Meaning |
|---|---|---|
| `colors.*` | Any CSS colour: `#rgb`, `#rrggbb`, `#rrggbbaa`, `rgb()`, `hsl()` or a colour name | See the variable reference above |
| `palette` | 1–24 colours | Lane colours, in order |
| `font` | A CSS font family | Label font |
| `background.image` | Vault path, `[[wikilink]]`, `https://` link or `data:image/...;base64,` URI | Background image |
| `background.fit` | `cover`, `contain`, `stretch`, `tile` | How the image fills the timeline |
| `background.position` | `center`, `top`, `bottom`, `left`, `right` | Anchor edge |
| `background.opacity` | 0–1 (default 0.35) | Image strength |
| `background.blur` | 0–24 px | Image blur |
| `event.radius` | 0–16 px (default 3) | Chip corner radius |
| `event.height` | 16–48 px (default 24) | Chip height at the default row density |
| `event.opacity` | 0.2–1 (default 1) | Chip opacity, before certainty fading |
| `lane.labelWidth` | 80–400 px (default 174) | Lane name column |
| `lane.height` | 20–200 px (default 36) | Minimum lane height |
| `lane.gap` | 0–40 px (default 8) | Space below each lane's last row |
| `axis.density` | 0–100 (default 50) | Date label packing. Higher fits more labels. |
| `axis.showCycles` / `axis.showHolidays` | `true` / `false` | Calendar bands under the axis |
| `connectors.width` | 0.5–6 px (default 2) | Arrow line width |
| `connectors.dependencyStyle` | `solid`, `dashed`, `dotted` | Arrow style. Leave it out to follow the setting. |

The *row density* toolbar control and the *Default density* setting still loosen or tighten rows around the theme's chip height.
