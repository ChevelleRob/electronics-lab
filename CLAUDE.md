# Notes for Claude

Electronics Lab is a set of single-file practice tools for a basic electronics
class, published with GitHub Pages from `main`. It matches PLC Lab
(github.com/ChevelleRob/plc-lab) in look and in how it's maintained, and the two
may be merged someday. The README is for students and visitors; maintenance
rules live here.

## How we work

- Before building a tool, propose the design and ask the instructor the few questions that matter, then build.
- Build each tool or change on its own branch. Test it in a real browser (Playwright) at 320 px, 375 px and desktop widths, in light and dark, with no sideways page scrolling. Send a private preview (an Artifact) before merging. Merge to `main` only when the instructor says "merge".
- If several changes are asked for before a merge, each round gets its own version and its own commit.
- Keep summaries short: what changed, what was tested, what to check, and the versions.

## Rules for every change

- Each tool lives in its own folder as a single self-contained `index.html` (inline CSS and JS, no build step, no frameworks), linked from the home page (`index.html`) and the README Tools table.
- Every change bumps the version of what changed (the tool, or the home page) and adds an entry to `CHANGELOG.md`. A tool's version appears in its header, on its home-page card, and in `CHANGELOG.md`; keep all three in sync. Home page changes bump the home page's version (in its header and `CHANGELOG.md`).
- Don't put changelogs in HTML comments.
- Track unconfirmed facts in `TO-VERIFY.md`. When a tool states something that came from memory rather than the instructor or a datasheet (values, part numbers, behaviors, rules of thumb), add an unticked item under that tool with where it appears. When the instructor confirms an item, move it to **Confirmed**; when they correct it, fix the tool (with a version bump) and then move it.

## Teaching choices

- The class uses **electron flow** (− to + outside the source). Any tool that shows flow defaults to electron flow, with a switch to show conventional current, and says that electron flow is the true flow of DC electricity. The choice is remembered in `localStorage` key `el-flow` (`e` or `c`).
- Ohm's law is taught with the **Ohm's law triangle**; the **power wheel** comes in when watts are introduced (its own Power tool).
- Voltage is written **E** (E = I × R), current **I**, resistance **R**. Units stay V, A, Ω.
- Resistors are **E12** values with **4 color bands**, gold (±5%) tolerance. Practice answers within **±5%** count as right.
- Bench supplies in the lab go to **30 V at 5 A**; most experiments use 6 V or 12 V. Power-supply sliders go the full 0–30 V so students can over-volt and burn out parts. A Replace/Fix button opens the switch, turns the supply back to 0 V and puts in a new part.
- Resistors in the examples are ¼ W. The Power tool may let students pick other wattages.

## Look

- Dark `header.top` bar: `<h1><a href="../">Electronics Lab</a></h1>` (a link back home, with the ‹ before it), a subtitle, the tool's version (`v1.0`) and the theme button.
- Barlow and JetBrains Mono fonts; light and dark color tokens on `:root` (copy the full set from `simple-circuit/index.html`).
- Theme button (Auto / Light / Dark): the early theme script right after the viewport meta, the `.themebtn` CSS and its narrow-screen rules, `<button class="themebtn" id="themeBtn">` after the version, and the theme script before `</body>`. It uses `localStorage` key `pl-theme`, the same key as PLC Lab, so one choice applies to both sites (same origin).
- Mobile first. No sideways page scrolling at 320 px. Wide tables scroll inside their own box with a sticky first column and a sticky header row.
- Controls students operate (switches, sliders, pushbuttons) go in the fixed `.bar` at the bottom of the screen; add `has-bar` to `body` so the page leaves room for it.
- Live, animated diagrams: current shown as moving dashes (`.flow`, speed follows the current), plain language, short "Try this" boxes (`.try`) and notes (`.note`), and checks or quizzes where they help.

## Icons and link previews

- `assets/` holds the site icon (`favicon.svg`, `favicon-32.png`, `apple-touch-icon.png`) and `social-preview.png` (1280 × 640), used as the link preview for every page and uploaded by hand as the repo's Social preview (Settings → General).
- Every page has the icon `<link>`s and the `og:` / `twitter:` meta tags right after `<title>`; tool pages point to `../assets/`. A new tool copies them from an existing tool and sets its own `og:title` (same as `<title>`) and `og:description` (same text as its home-page card).
- The social image is drawn in `assets/src/social-preview.html` (shared with the sister site; `#el` or `#plc` picks the version) and rendered with `node render.js` run from `assets/src/`. It writes `social-el.png` and `social-plc.png` there: copy this site's one to `assets/social-preview.png` and don't commit the copies left in `assets/src/`. `assets/src` is excluded from the published site.

## Adding a new tool

1. Make a new folder named for the tool, e.g. `ohms-law/`, with the tool in `ohms-law/index.html`. Keep it a single self-contained file.
2. Match the look (see above), starting from `simple-circuit/index.html`, including the icon and link-preview tags (see below).
3. Add a card for it in the `<ul class="tools">` list on the home page, with the same version number, and bump the home page version.
4. Add a row to the Tools table in `README.md`.
5. Add a section for the tool to `CHANGELOG.md`, plus a home page entry for the new card.
6. Add a section for the tool to `TO-VERIFY.md` for anything from memory.

## Planned tools (suggested order)

1. Simple Circuit (done)
2. Ohm's Law (done; triangle, E for voltage), then a separate Power tool (power wheel; maybe a choice of resistor wattage)
3. Resistor Color Code (both directions, 4 and 5 band)
4. Using a Multimeter (volts in parallel, amps in series, resistance with power off, common mistakes)
5. Series, Parallel and Combination circuits (with voltage dividers)
6. Batteries in series, parallel and combination
7. Kirchhoff's voltage and current laws
8. Capacitors (charging, RC time constant)
9. Diodes and LEDs (forward bias, current-limiting resistor)
10. Transistors as switches
11. AC: generators, motors and transformers (separate tools, one per chapter)
