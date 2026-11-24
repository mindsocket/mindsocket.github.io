---
weight: 40
title: "podcast-addict-tools"
description: "Podcast transcription feeding an agent-maintained knowledge wiki"
tags: ["python", "whisper", "audio", "agents"]
---

Tools that turn the podcasts I listen to into searchable, linked knowledge. Episodes I favourite or queue in [Podcast Addict](https://podcastaddict.com) are transcribed, then ingested by an agent into a knowledge wiki.

- **Automated ingestion.** Scheduled jobs pick up tagged episodes from Podcast Addict backups, transcribe them locally with whisper.cpp on the Mac's GPU, and write markdown transcripts with episode metadata and bookmarks.
- **Knowledge wiki.** An agent classifies each new transcript and writes source, concept and entity pages into a wiki, cross-linked with existing notes. Every page is validated against the wiki's schema with [structured-context](/projects/structured-context/), so the agent's output stays consistent as the wiki grows.
- **On demand.** Agent skills summarise an episode from a shared link, or ingest one into the wiki, from a chat message.
- **Listening analysis.** Reports on bookmarks, engagement by podcast, and recommendations for what to listen to next.

Soloware, source unavailable.
