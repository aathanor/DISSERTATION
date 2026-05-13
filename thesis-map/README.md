---
title: "Thesis Map — Usage Notes"
author: Florin Cojocariu
status: working_tool
---

# What this is

A small static site that visualises the dissertation as an interactive argument map. The SVG on the left is generated at runtime from `argmap.canvas` (an open JSON-based canvas format). Content lives in `content/*.md` — one markdown file per node. The map can be edited visually in Obsidian; content can be edited in any markdown editor.

# Running it locally

```
cd thesis-map
python3 -m http.server 8000
```

Open `http://localhost:8000`. Stop with Ctrl-C.

# Editing the map visually (Obsidian)

Open `argmap.canvas` in Obsidian. Drag nodes, draw edges, change colors, save. Refresh the browser.

The Canvas feature is built into Obsidian's free desktop app — no plugin required for basic editing. Install Obsidian, open the `thesis-map` folder as a vault, then open `argmap.canvas`.

For better shape and style options (ellipses, dashed borders), install the **Advanced Canvas** community plugin (Settings → Community plugins → Browse → "Advanced Canvas"). The website will render whatever you set; the custom fields it expects (`kind`, `shape`, `dashed`, `role`) are preserved by Obsidian even if it doesn't use them itself.

## Node fields the website reads

Each text node in `argmap.canvas` may carry these custom fields (all optional):

- `kind`: one of `notation-primary`, `notation-secondary`, `framing`, `thesis`, `thinker`, `proposal`, `gap`, `support`, `explained`, `hub`, `mechanism`, `chapter`, `anchor`, `anchor-highlight`. Each maps to a fill/stroke style. Defined in `index.html` (`KIND_STYLES`).
- `shape`: `"ellipse"` to render as an ellipse. Default is rectangle.
- `dashed`: `true` for a dashed border.
- `role`: `"label"` for non-clickable zone labels (just text, no box).

The `id` of each node must match a markdown filename in `content/` (without the `.md` extension). The text inside the node may be plain or markdown — the website parses the first line as the title and the remaining lines as a subtitle.

## Adding a node

1. In Obsidian Canvas: create a text node, type a title and subtitle. Set color if you like.
2. Give it a meaningful id (Obsidian assigns UUIDs by default — to use a readable id, edit `argmap.canvas` in a text editor and change the `id` field).
3. Add custom fields (`kind`, `shape`, etc.) by editing the file in a text editor.
4. Create the matching `content/<id>.md` with title, kind, related, and body.
5. Add `"content/<id>.md"` to the `files` array in `nodes.json`.

# Editing content

Each node has one markdown file in `content/`. Open the file in Zettlr (or any editor), save, refresh the browser.

Front matter:

```
---
title: "Display title"
kind: "Short kind label, shown under the title in the content panel"
related: [other-node-id, another-node-id]
---

Body content in markdown. LaTeX in $...$ for inline, $$...$$ for display.
```

The `related` list controls the "See also" links at the bottom of the content panel and the dashed-amber highlights on the map when this node is active.

# URL bookmarks

The URL hash reflects the current node, e.g. `…#local-rigidity`. Bookmarkable. Shareable.

# Files

```
thesis-map/
  index.html        the shell — SVG renderer and loader script
  argmap.canvas     the map (JSON Canvas format; editable in Obsidian)
  nodes.json        manifest listing all content files
  README.md         this file
  assets/
    style.css       all styling
  content/
    *.md            one file per node
```

# Dependencies

Two CDN scripts, loaded from `index.html`:

- KaTeX 0.16.9 for LaTeX rendering
- marked.js 12.0.2 for markdown parsing

To make the site fully offline-portable, download both libraries and replace the CDN URLs with local paths under `assets/`.
