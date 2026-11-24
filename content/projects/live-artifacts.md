---
weight: 30
title: "live-artifacts"
description: "Interactive HTML pages for Hermes agents, with persisted input the agent can read back"
tags: ["hermes", "python", "agents", "plugin"]
---

A [Hermes](https://hermes-agent.nousresearch.com/) plugin that lets an agent publish small interactive pages (forms, review lists, dashboards), open them by link on a phone or desktop over a tailnet, persist what you enter, and read it back or have it pushed into the chat that created the page.

Inspired by Claude artifacts, with a compatible page-side API, so many pages written for Claude work unchanged.

## How it looks

<video src="https://github.com/user-attachments/assets/14d957c4-7819-4bc9-8d4a-0bd5d97e4383" controls preload="metadata" style="width:100%;border-radius:8px"></video>

The agent builds a page for you to mark up, here a review of a phone agent's calls.

![Call review page: a caller/agent transcript with a highlighted mistake, a Wrong tag and a note](/live-artifacts/review-page.png)

Pressing Send notifies the chat that created the page. The agent reads your markup back and replies with what it will change.

![Hermes chat: the agent creates the page, is notified, reads the notes and summarises the changes](/live-artifacts/chat-send.png)

The Hermes dashboard tab lists every artifact with a live preview.

![Live Artifacts dashboard tab: list of artifacts beside a preview of the call review page](/live-artifacts/dashboard.png)

[Hermes plugin marketplace](https://hermes-agent.nousresearch.com/marketplace/live-artifacts) · [Source on GitHub](https://github.com/mindsocket/hermes-live-artifacts)

[![live-artifacts](https://github-readme-stats.vercel.app/api/pin/?username=mindsocket&repo=hermes-live-artifacts)](https://github.com/mindsocket/hermes-live-artifacts)
