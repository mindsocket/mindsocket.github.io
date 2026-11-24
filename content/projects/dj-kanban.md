---
weight: 45
title: "DJ Kanban"
description: "A Jira board that runs a live DJ set, from an Atlassian hackathon to a standalone web app"
tags: ["typescript", "audio", "react"]
---

A Jira Kanban board runs a live DJ set. Cards represent audio. Moving a card between columns applies loops, transitions and effects, kept in time with an audio engine.

## Origins

I built DJ Kanban for ShipIt 31, Atlassian's 24-hour hackathon in 2015. It was a web hook integration that turned a board into a mixer: the backlog held the available sounds, and dragging cards across the columns queued, played and retired them. 160 lines of Python backed by a project called SuperLooper

## Summit

DJ Kanban went from some in-house gigs to taking over stages at Atlassian Summit 2015. There, co-founders Mike Cannon-Brookes and Scott Farquhar played the board in full Daft Punk helmets, and DJ Kanban featured at the Summit Bash and presented at ShipIt Live. A rewritten version using Atlassian Connect and an all browser-based audio engine was also released on the Atlassian Marketplace, so other teams could try it on their own workflows. In 2016 DJ Kanban was a headline act at the Summit Bash party once again, mixing live mashups for thousands. 

## On the road

DJ Kanban kept getting booked: opening the AWS Summit Sydney partner event in 2017, warming up the crowd before the keynotes with Jira boards on the big screens, and a run of Atlassian events including Euro Summit in Barcelona.

## Mashups

The versatility of the DJ Kanban interface relative to traditional DJ systems made live mashups and discovery of potential mashups for full production very approachable.

## Now

While the gigs are few and far between, the project has been a creative outlet with improvements being added over the years. There are more effects, plus stem separation, automated mix transitions, scheduled actions (so you can DJ into the future), key-matching, midi controller integration, and more. The current version is a standalone web app.

## Gallery

<div style="display:grid;grid-template-columns:repeat(2,1fr);gap:8px">
  <a href="/dj-kanban/barcelona.jpg" target="_blank" style="grid-column:1/-1"><img src="/dj-kanban/barcelona.jpg" alt="DJ Kanban at Atlassian Summit Barcelona: hooded, goggles on, arms up behind the booth with the board on a screen" loading="lazy" style="margin:0;width:100%;aspect-ratio:16/9;object-fit:cover;object-position:50% 38%;border-radius:6px" /></a>
  <a href="/dj-kanban/board-set.jpg" target="_blank"><img src="/dj-kanban/board-set.jpg" alt="Dragging a track from the backlog into the play column mid-set" loading="lazy" style="margin:0;width:100%;aspect-ratio:16/10;object-fit:cover;border-radius:6px" /></a>
  <a href="/dj-kanban/keynote-stage.jpg" target="_blank"><img src="/dj-kanban/keynote-stage.jpg" alt="The board on the big screen at the keynote, with the DJs on stage" loading="lazy" style="margin:0;width:100%;aspect-ratio:16/10;object-fit:cover;border-radius:6px" /></a>
  <a href="/dj-kanban/board-bigscreen.jpg" target="_blank"><img src="/dj-kanban/board-bigscreen.jpg" alt="The kanban board on a big screen above the DJ Kanban slide" loading="lazy" style="margin:0;width:100%;aspect-ratio:16/10;object-fit:cover;border-radius:6px" /></a>
  <a href="/dj-kanban/aws-summit-stage.jpg" target="_blank"><img src="/dj-kanban/aws-summit-stage.jpg" alt="DJ Kanban on the main screens at AWS Summit Sydney" loading="lazy" style="margin:0;width:100%;aspect-ratio:16/10;object-fit:cover;border-radius:6px" /></a>
  <a href="/dj-kanban/aws-summit-video-hall.jpg" target="_blank"><img src="/dj-kanban/aws-summit-video-hall.jpg" alt="The AWS Summit Sydney hall, with the board on the side screen" loading="lazy" style="margin:0;width:100%;aspect-ratio:16/10;object-fit:cover;border-radius:6px" /></a>
  <a href="/dj-kanban/bash-bigscreen.jpg" target="_blank"><img src="/dj-kanban/bash-bigscreen.jpg" alt="The board projected over the party floor" loading="lazy" style="margin:0;width:100%;aspect-ratio:16/10;object-fit:cover;border-radius:6px" /></a>
  <a href="/dj-kanban/summit-booth.jpg" target="_blank"><img src="/dj-kanban/summit-booth.jpg" alt="The DJ booth with the board on two screens" loading="lazy" style="margin:0;width:100%;aspect-ratio:16/10;object-fit:cover;border-radius:6px" /></a>
  <a href="/dj-kanban/bash-booth.jpg" target="_blank"><img src="/dj-kanban/bash-booth.jpg" alt="The booth, with the board on a screen beside it" loading="lazy" style="margin:0;width:100%;aspect-ratio:16/10;object-fit:cover;border-radius:6px" /></a>
  <a href="/dj-kanban/barcelona-scott.jpg" target="_blank"><img src="/dj-kanban/barcelona-scott.jpg" alt="Two on the booth in Barcelona, goggles lit, with the DJ Kanban screen behind" loading="lazy" style="margin:0;width:100%;aspect-ratio:16/10;object-fit:cover;border-radius:6px;object-position:50% 55%" /></a>
  <a href="/dj-kanban/hoodie-selfie.jpg" target="_blank"><img src="/dj-kanban/hoodie-selfie.jpg" alt="Flashing hoodie and goggles" loading="lazy" style="margin:0;width:100%;aspect-ratio:16/10;object-fit:cover;border-radius:6px;object-position:50% 30%" /></a>
  <a href="/dj-kanban/photobooth.jpg" target="_blank"><img src="/dj-kanban/photobooth.jpg" alt="Photo booth" loading="lazy" style="margin:0;width:100%;aspect-ratio:16/10;object-fit:cover;border-radius:6px;object-position:50% 20%" /></a>
  <a href="/dj-kanban/aws-summit-hall.jpg" target="_blank"><img src="/dj-kanban/aws-summit-hall.jpg" alt="The board on the big screen in the hall" loading="lazy" style="margin:0;width:100%;aspect-ratio:16/10;object-fit:cover;border-radius:6px" /></a>
  <a href="/dj-kanban/crowd-screens.jpg" target="_blank"><img src="/dj-kanban/crowd-screens.jpg" alt="The crowd gathered around the screens" loading="lazy" style="margin:0;width:100%;aspect-ratio:16/10;object-fit:cover;border-radius:6px" /></a>
  <a href="/dj-kanban/crowd-hands-2.jpg" target="_blank"><img src="/dj-kanban/crowd-hands-2.jpg" alt="Hands up on the dance floor" loading="lazy" style="margin:0;width:100%;aspect-ratio:16/10;object-fit:cover;border-radius:6px" /></a>
</div>

## DJ Kanban in action

- [YouTube channel](https://www.youtube.com/channel/UCtelewFrl5MW-XZO7AKT4BA)
- [Gigs playlist](https://www.youtube.com/playlist?list=PLNnJdaRbV5DVAg0GlX18miVzevmmS6ViX)
- [Mashups playlist](https://www.youtube.com/playlist?list=PLNnJdaRbV5DWEW9BlQm2Ht4egPdIR7eut)
- [Twitter/X](https://x.com/DJKanban)
- [Mixcloud](https://www.mixcloud.com/mindsocket/)
