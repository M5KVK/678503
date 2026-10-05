# [NODE NUMBER] Node Page — Starter Kit

*Starter Kit version 1.2 (September 19, 2026)*

Off-node reference site for an AllStarLink node, built with GitHub Pages
using Jekyll's `minima` theme. GitHub builds this automatically from the
Markdown files on push — there is no local build or deploy step.

## Before you push this anywhere

Open `_config.yml` and fill in two things near the top: `node_number` and
`callsign`. Every other page in the kit pulls those in automatically from
there — you only enter them once.

There are exactly two spots Jekyll can't fill in for you, because they sit
outside its templating system (front matter and `_config.yml` itself
aren't processed by Liquid). Fill these in by hand, the old-fashioned way:

- `_config.yml` — the `title` and `description` fields at the top
- `index.md` — the `title` field in its front matter (the three lines
  between the `---` markers)

Everywhere else — `about.md`, `changelog.md`, the body of `index.md`, and
the status indicator — reads `node_number` and `callsign` straight from
`_config.yml`. Change your node number once, in that one file, and it
updates everywhere except the two literal spots above.

`about.md`, `disclaimers.md`, and `changelog.md` also have italicized
instructional text describing what belongs in each section; replace that
with your own real content.

## Structure

- `_config.yml` — site settings, theme, and your node number/callsign
- `index.md` — home page
- `about.md`, `disclaimers.md`, `changelog.md` — content pages, linked
  from the home page and the site nav
- `_includes/node-status.html` — the live Online/Offline indicator shown
  on the home page

See the full how-to guide this kit accompanies for setup instructions.

## What's new in version 1.2

Your node number and callsign now live in one place: `node_number` and
`callsign` in `_config.yml`. Every page pulls them in automatically via
`{{ site.node_number }}` and `{{ site.callsign }}`, instead of a manual
find-and-replace across every file. Only two literal spots remain (see
above), and both are unavoidable — Jekyll doesn't run its templating
inside `_config.yml` or page front matter.

The status indicator got simpler too: `{% include node-status.html %}`
now works with no arguments and picks up your node number on its own.
Passing `node="123456"` still works if you ever want to show a different
node's status on a page.

## What's new in version 1.1

The home page shows a live Online / Offline / Status unavailable
indicator, with a "Check now" button. It reads AllStarLink's public
statistics for your node in the visitor's browser; it does not ping your
node. To remove it, open `index.md`, delete the comment block and the
`include` line under the intro paragraph, and delete the `_includes`
folder. The guide has a section that explains the indicator and how to
adjust it.
