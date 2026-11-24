---
weight: 20
title: "Structured Context"
description: "Schemas, AI-judged rules and map views that keep strategy, playbooks and knowledge coherent in markdown"
tags: ["typescript", "markdown", "schemas", "agents", "claude-code", "obsidian"]
---

Keep your thinking clear and your content clean. structured-context gives a folder of markdown notes a schema, so people and AI agents can build up a body of thinking together and keep it coherent: a business strategy that ladders from vision and mission down to goals, opportunities and initiatives; a playbook that stays well documented and can be seen whole; or a knowledge wiki that an agent keeps growing.

![Claude Code with the structured-context mod: validation checks in the chat, a space status line, and a pane showing the space as a tree](/structured-context/claude-mod.png)

![Obsidian map view of a playbook: phases containing activities, each with the capabilities it needs](/structured-context/obsidian-map-view.png)

Structure catches the mechanical drift: missing fields, broken links, notes that connect to nothing. The more interesting part is judgement. Rules can ask a model whether the thinking holds together, so the tool points out inconsistencies and gaps in your reasoning, not just in your formatting.

## The core

A *space* is a folder of markdown files plus a schema. Notes carry typed frontmatter and wikilinks, and the `sctx` command line validates them:

- **Schema validation** of each note's fields, with JSON Schema.
- **Structure**: broken links, duplicates, hierarchy rules and orphaned nodes.
- **Rules** expressed against the graph, with error, warning and info severities, so best-practice advice doesn't fail a build.
- **AI-judged rules** for the questions an expression can't answer. Does this goal move its mission forward? Does this opportunity work against the vision above it? Is it a customer need, or a solution in disguise? Would this initiative actually address the need it sits under? Are two sibling goals really the same result, or steps in a sequence? Each rule gives a fixed set of verdicts with their own severities, and can send the surrounding nodes as context. An eval harness measures each model provider's agreement and stability on labelled cases.

Bundled schemas cover strategy (vision, mission, goals, opportunities, solutions, assumptions and experiments), opportunity solution trees and knowledge wikis, and you can write your own. It also renders spaces as Mermaid diagrams and syncs them to Miro.

## Map views

[Map views](https://github.com/mindsocket/structured-context-map-views) project a space into a visual form (a tree, nested containers or a network) from a short declarative definition, with validation results overlaid on the nodes, so a strategy or playbook can be seen whole and its weak spots found at a glance. The same space can be shown several ways, and a React library renders them in any host: a standalone navigator, a self-contained HTML export, or a Claude artifact.

## In Claude Code

A Claude Code plugin brings it all into an agent session:

- **Hooks** take a baseline of each space when a prompt starts, then validate when the agent finishes. New errors send the agent back to fix them before it stops, and new warnings are passed back as context. Validation runs on the whole turn, not each edit, because a space can be invalid partway through a multi-file change.
- **Skills** set up a space for an existing folder, help author schemas and rules, and publish a map view as a Claude artifact that others can view and comment on.
- **A UI mod** shows validation status beside the chat, with a space map pane that updates as the agent works, and gives the agent the schema for the spaces in play.

## In Obsidian

An [Obsidian plugin](https://github.com/mindsocket/obsidian-structured-context) validates as you edit, highlighting problems in a note's frontmatter and listing broken links and rule violations below it, and opens map views in a pane. It shares its configuration with the command line and Claude Code, so a space set up in one works in the others.

## Links

[Source on GitHub](https://github.com/mindsocket/structured-context) · [Documentation](/docs/structured-context/) · [npm](https://www.npmjs.com/package/structured-context)

[![structured-context](https://github-readme-stats.vercel.app/api/pin/?username=mindsocket&repo=structured-context)](https://github.com/mindsocket/structured-context)
