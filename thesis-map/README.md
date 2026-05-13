---
title: "Thesis Map — Usage Notes"
author: Florin Cojocariu
status: working_tool
---

# What this is

A small static site that visualises the dissertation as an interactive argument map. The SVG on the left is the navigation; clicking a node loads the corresponding content panel on the right. Content lives in `content/*.md` — one markdown file per node — so editing a node means opening one file in Zettlr, not touching the HTML.

# Running it locally

The page fetches markdown files at runtime, which means opening `index.html` directly with `file://` will fail with a CORS error. Serve the folder with any static server:

```
cd thesis-map
python3 -m http.server 8000
```

Then visit `http://localhost:8000` in any browser. To stop, hit Ctrl-C in the terminal.

If you prefer, `npx serve` or VS Code's "Live Server" extension work too.

# Editing content

Each node has one markdown file in `content/`. The filename without `.md` is the node id used by the map. To edit a node, open the file in Zettlr, save, refresh the browser.

File structure:

```
---
title: "Display title"
kind: "Short kind label, shown under the title"
related: [other-node-id, another-node-id]
---

Body content in markdown. LaTeX in $...$ for inline, $$...$$ for display.

H1 headings if you want sub-sections inside the body (rare — most entries are short).
```

The `related` list controls both the "See also" links at the bottom of the panel and the dashed-amber highlights on the map when this node is active.

# Adding a node

Three steps:

1. Create `content/your-node-id.md` with the front matter shown above.
2. Add `"content/your-node-id.md"` to the `files` array in `nodes.json`.
3. Open `index.html` and add a `<g class="node" data-id="your-node-id">` element to the SVG with a `<rect>` (or `<ellipse>`) and `<text>` labels. Pick coordinates that don't collide with existing nodes; extend the `viewBox` height if needed.

The node id must be the filename stem and must match the `data-id` attribute in the SVG.

# Removing or renaming a node

Delete or rename the md file, remove the corresponding entry from `nodes.json`, and remove or rename the SVG element. Check that no other md file's `related` list references the deleted id.

# Updating the visual map

The map is hand-drawn SVG in `index.html`. To rearrange, just edit the SVG. Common operations:

- Change a node's position: edit `x`, `y` (or `cx`, `cy`) on the `<rect>` / `<ellipse>` and the corresponding `<text>` elements.
- Change a node's colour: edit `fill` and `stroke`.
- Add a connecting line: insert `<line class="edge" x1="..." y1="..." x2="..." y2="..."/>` between two nodes.
- Extend the canvas: increase the `height` value in `viewBox="0 0 440 1180"`.

# URL bookmarks

The URL hash reflects the current node, e.g. `…#local-rigidity`. You can bookmark any view or share a link to a specific node.

# Files

```
thesis-map/
  index.html        the shell — SVG map and loader script
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

Both work offline once cached. To make the site fully offline-portable, download both libraries and replace the CDN URLs with local paths under `assets/`.

# Known limitations

The SVG labels use Unicode superscripts (`xᵒ`, `xᶜ`, `𝓡`) rather than KaTeX, because KaTeX doesn't render inside SVG `<text>` elements. If you need cleaner formula display in the map labels, the workaround is to use `<foreignObject>` instead of `<text>`, or to switch the labels to HTML overlays positioned over the SVG. Neither is necessary for current use.
