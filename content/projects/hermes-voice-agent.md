---
weight: 10
title: "Hermes Voice Agent and E-ink Satellite"
description: "Talk to a personal agent by phone or from a desk display, to check on and steer other agent sessions"
tags: ["hermes", "voice", "livekit", "pipecat", "esphome", "agents"]
---

I can ring my own AI agent from a phone, or talk to a small e-ink display on my desk, to check in on my agent sessions in [Hermes](https://hermes-agent.nousresearch.com/) and Claude Code, and to start new tasks. It's a handy way to keep sessions moving, and to work through decisions and questions conversationally rather than reading a wall of text.

The voice agent is a facilitator rather than a worker. It's tuned to understand the conversational context it operates in: it reads the real state of other sessions, delegates work to them and relays what comes back, so a conversation moves between agent sessions and a voice call without losing the thread. Everything runs on one laptop over Tailscale: no public ports, no phone number, no custom phone app.

## The system at a glance

A phone call goes over SIP into LiveKit, then to a Pipecat bot that handles turn-taking, local speech-to-text and text-to-speech. The satellite is an ESP32 device with an e-ink screen and a microphone, bridged to the same agent. Both talk to one Hermes voice profile, whose only tools are for working with other sessions.

{{< mermaid >}}
flowchart TB
  Phone["Phone<br/>(SIP app)"] <-->|"SIP + audio"| LK["LiveKit<br/>+ SIP bridge"]
  LK <-->|"room audio"| Bot["Voice bot (Pipecat)<br/>turn-taking · cues"]
  Bot <-->|"speech ⇄ text"| Speech["Whisper (local)<br/>edge-tts / Piper"]
  Bot <-->|"turns, steering"| Voice["Hermes<br/>voice profile"]
  Sat["E-ink satellite<br/>(ESPHome)"] <-->|"push-to-talk, text"| Voice
  Voice <-->|"list · read · send<br/>start · watch"| MCP["Session tools<br/>(MCP server)"]
  MCP <--> Work["Hermes and<br/>Claude Code sessions"]
  MCP -->|"job update"| Voice
{{< /mermaid >}}

## Turn-taking

People pause mid-thought and talk while the agent is still working. The bot holds briefly after each stretch of speech, longer if it trails off, while a small judgment model (TypeSafe's Jev) decides whether the speaker has finished. Reframing that question as "is this actionable?", with the prior turns as context, cut false holds from 35% to 25% and false releases from 42% to 26% on 132 labelled turns. Speech that arrives while the agent is mid-task steers it rather than waiting for the next turn.

<iframe src="/voice-agent/turn-timeline.html" title="Animated timeline of one spoken turn" loading="lazy" style="width:100%;height:520px;border:1px solid rgba(128,128,128,.3);border-radius:8px"></iframe>

## Audio as the interface

With no screen, the agent shows what it's doing through sound rather than spoken filler. Short tones mark the moments of a turn: heard you, still working, done, and a job update has arrived. Some tool calls are announced with a single word, such as "list", "read" or "prompt", so you can follow what the agent is doing without waiting for it to explain.

## Background jobs

The voice agent starts jobs, sends prompts to existing sessions, or watches busy ones. It keeps track of those background jobs and relays updates when they finish or need input, at a natural pause, or stays quiet if an update isn't worth the interruption. Hanging up loses nothing: anything unsent or still owed carries on in the job's own session.

## The satellite

A reTerminal Sticky (ESP32-S3, e-ink, microphone) running ESPHome. Hold the button to talk; replies are written to be read at a glance. Both clients share the same voice sessions, so a conversation can start on the phone and continue at the desk.

<iframe src="/voice-agent/satellite-screen.html" title="Mock of the satellite screen" loading="lazy" style="width:100%;height:470px;border:1px solid rgba(128,128,128,.3);border-radius:8px"></iframe>

## Built with

LiveKit and livekit-sip · Pipecat · whisper.cpp · Silero VAD · edge-tts and Piper · Hermes (profiles, Sessions API, MCP) · ESPHome · Home Assistant · Tailscale

Soloware, source unavailable.
