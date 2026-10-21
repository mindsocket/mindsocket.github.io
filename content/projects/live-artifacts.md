---
title: "live-artifacts"
description: "Interactive HTML pages for Hermes agents, with persisted input the agent can read back"
tags: ["hermes", "python", "agents", "plugin"]
---

A [Hermes](https://hermes-agent.nousresearch.com/) plugin that lets an agent publish small interactive pages (forms, review lists, dashboards), open them by link on a phone or desktop over a tailnet, persist what you enter, and read it back or have it pushed into the chat that created the page.

Inspired by Claude artifacts. The page-side API follows Claude's artifact runtime (`window.claude.use("db")` and friends), cut down to one user, so a page written for Claude can move across when it sticks to the capabilities implemented.

- Eight agent tools, an aiohttp listener inside the Hermes gateway, SQLite persistence, and a dashboard tab.
- Pages run in a CSP sandbox with per-artifact API tokens; the threat model and known gaps are documented.
- Tested with pytest and Playwright end-to-end tests.

[Source on GitHub](https://github.com/mindsocket/hermes-live-artifacts)

[![live-artifacts](https://github-readme-stats.vercel.app/api/pin/?username=mindsocket&repo=hermes-live-artifacts)](https://github.com/mindsocket/hermes-live-artifacts)
