# TOPO Solver

**Turn survey points into a reviewed TIN surface — then hand it over as LandXML or DXF.**

TOPO Solver is a free, single-file tool that runs entirely in your browser. Drop in a
points file, review and clean the triangulation, add breaklines, generate contours, and
export a surface that drops straight into Civil 3D or any CAD package. No install, no
account, no build step, and nothing is ever uploaded — the whole thing runs on your machine,
offline.

### ▶ Run it now

[Launch Topo Solver](https://howtocivilengineer.github.io/Topo-Solver/) (click open in new tab)

Open the link, drop a file on the page, and go. Works on desktop and mobile, (desktop is recommended).

---

## Video walkthrough

*A full video walkthrough is coming soon.*

<!-- Once the video is published, delete the line above and uncomment the block below,
     replacing VIDEO_ID with your YouTube video id (the part after v= or youtu.be/). -->
<!--
[![Watch the walkthrough](https://img.youtube.com/vi/VIDEO_ID/0.jpg)](https://youtu.be/VIDEO_ID)
-->

---

## What it does

TOPO Solver takes raw survey points and gives you a surface you can actually trust and edit
by hand, rather than a black-box triangulation. It sits alongside your main design software
as a fast cross-check and a zero-cost way to build, review and share a ground model.

- **Reads standard survey files** — `.txt`, `.csv`, `.pnt`, `.asc`, `.dat`, with common
  column orders (PNEZD, PENZD, NEZD, ENZD, PXYZD) and automatic separator detection.
- **Constrained Delaunay triangulation** built in the browser, with breaklines held as hard
  edges so ridges, kerbs and channels stay where you surveyed them.
- **Hands-on editing** — swap triangle diagonals, drop points out of the surface, draw and
  delete breaklines, and trim the long thin triangles that reach across the outside of a job.
- **Contours** at any interval, with heavy index lines every fifth contour and optional
  smoothing so the drawn and exported lines read like a real survey plan.
- **Full undo / redo** (Ctrl+Z / Ctrl+Y) across every edit.
- **Exports that carry your edits** — the LandXML surface holds the exact triangles on
  screen, so it imports into Civil 3D as *your* surface, not a fresh re-triangulation of the
  points.
- **Multilingual** — English, Português, Français and Español.

---

## The workflow

The panel is laid out in the order you actually work:

**1 · Import** — open a points file (or load the built-in sample), set the column order and
separator.

**2 · Edit Surface** — everything that shapes the surface, grouped together:
- **Codes** — chain every point sharing a code into a breakline, in the order they were shot.
- **Points** — filter, zoom to, and toggle individual points in or out of the surface.
- **Breaklines** — draw a string by clicking points in order; review and switch strings on/off.
- **Triangles** — trim triangles longer than a chosen length to pull the boundary back to
  where you surveyed.
- **Contours** — set the interval and toggle smoothing.

**3 · Exports** — name the surface and write out LandXML, DXF, or a working file you can
reopen later to carry on.

**Surface Info** — live counts and areas: points used, triangles, breakline segments held,
elevation range, plan area and surface area.

---

## Exports in detail

| Output | What it contains |
| --- | --- |
| **LandXML surface** | The exact triangulation on screen — every edge swap, every breakline, every point left out. Imports into Civil 3D as a finished surface. |
| **DXF** | Points, elevation and code text, TIN triangles (3D faces), breaklines and contours, each on its own named, coloured layer so you can sort out what you need in CAD. |
| **Working file (.json)** | Your full session — points, edits, breaklines and settings — to save and reopen and pick up exactly where you left off. |

---

## Privacy

Everything happens locally in your browser. No file you open is sent anywhere, and there is
no server, tracking or account. You can save the page and run it with no internet connection
at all.

---

## Run it locally / self-host

The whole tool is one HTML file with no dependencies and no build step.

- **Run offline:** download `index.html` and open it in any modern browser.
- **Self-host:** it's already served from this repository via GitHub Pages. Any static host
  works — just drop the file in and open it.

---

## Tech

Plain HTML, CSS and vanilla JavaScript in a single file. No frameworks, no bundler, no
package install. The triangulation, contouring, and LandXML / DXF writers are all
hand-rolled and run client-side.

---

## Feedback

Found a bug, or have a file that doesn't import cleanly? Open an
[issue](../../issues) — a sample of the points file that caused it is the fastest way to get
it fixed.

---

## License

<!-- Add your chosen license here (for example, MIT) and include a LICENSE file in the repo. -->

*License to be confirmed.*

---

*Built for surveyors and civil engineers who want a fast, free way to build, review and share
a ground model — without a seat of desktop software.*
