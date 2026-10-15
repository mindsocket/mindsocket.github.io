# Portfolio site plan

Goal: mini portfolio complementing LinkedIn. Examples of products and software built over the years, emphasis on recent AI work.

## Done (no Go needed)
- Deprecated `languageCode`/`languageName` replaced with `locale`/`label`
- CI: dropped submodule checkout, pinned Hugo 0.166.0, Go version from `go.mod`
- Home page and author block scaffolded (headline, bio, photo, LinkedIn URL are TODO)

- Go installed; Blowfish upgraded v2.98.0 -> v2.106.0 (`hugo mod get -u`, `hugo mod tidy`); clean build, no warnings

## Project inventory
| Page | Local repo | Public repo | Last commit | Notes |
|---|---|---|---|---|
| dj-kanban | ~/src/dj-kanban | yes | 2026-09-27 | 1052 commits, most mature; page says source private, repo has a GitHub remote: confirm visibility |
| me-next | ~/src/me.next | no remote | 2026-09-21 | private |
| chrome-open-tabs | ~/src/chrome-open-tabs | yes | 2026-09-20 | |
| podcast-addict-tools | ~/src/podcast-addict-tools | yes (remote) | 2026-09-20 | page says private: confirm |
| brewfather-mcp | ~/src/brewfather-mcp | yes | 2026-03-20 | |
| wfh-tax-calculator | ~/src/wfh_tax_calendar_calc | yes | 2026-09-20 | live app linked |
| election-data | ~/src/election_data | yes | 2026-02-10 | page is a placeholder, repo has no README |
| groceries | ~/src/groceries | no remote | 2026-05-04 | private |
| ost-tools | ~/src/ost-tools (no git) | ? | ? | possibly superseded by structured-context |
| shed-sensor-display | ~/src/esphome-temp (no git) | no | ? | work in progress |
| photo-tools | n/a | partial | n/a | Gradfilter Pro sold to Corel; pano scripts private |

Not on the site yet: **structured-context** (public, 191 commits, active 2026-09-27), claude-session-tools, snowmap, others in ~/src.

## Grilling sessions (one per project)
Questions: What problem, for whom? What did you build vs. what did AI build? What was hard or surprising? What's the current status and what does "finished" mean? What would you do differently? Is it OK to show publicly?

Order: structured-context, me-next, dj-kanban, brewfather-mcp, chrome-open-tabs, podcast-addict-tools, groceries, ost-tools, election-data, shed-sensor-display, then a career session for older products (Gradfilter Pro, pano scripts, etc.).

## Screenshots to capture
- dj-kanban: queue view mid-set, deck view
- me-next: main scoring view (redact personal data)
- brewfather-mcp / chrome-open-tabs: Claude Code session showing the tool in use
- podcast-addict-tools: pipeline output (transcript markdown)
- wfh-tax-calculator: results screen
- shed-sensor-display: photo of the device
- groceries / election-data / ost-tools: one representative chart or output each
Store in each project's page bundle (`content/projects/<name>/index.md` + images) so Hugo handles optimisation.

## Publish checklist
1. Go + module update, clean build
2. Fill author details, add LinkedIn link
3. Per-project status (finished / in progress / shelved) and screenshots
4. Remove or hold back anything not ready (`draft: true`)
5. Commit, push, set Pages source to GitHub Actions, verify live URL
