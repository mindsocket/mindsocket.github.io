---
weight: 20
title: "Structured Context"
description: "Schemas, validation and map views for markdown knowledge, built for humans and AI agents to share"
tags: ["typescript", "markdown", "schemas", "agents", "claude-code", "obsidian"]
---

Keep your content clean and your thinking clear. structured-context gives a folder of markdown notes a schema, so people and AI agents can work on the same body of knowledge and keep it consistent: knowledge wikis, product and strategy frameworks such as opportunity solution trees and strategy cascades, or any kind of knowledge graph.

AI agents write a lot of markdown quickly. Without structure, a knowledge base drifts: missing fields, broken links, notes that don't connect to anything. structured-context catches that drift as it happens, and shows the shape of the whole.

## The core

A *space* is a folder of markdown files plus a schema. Notes carry typed frontmatter and wikilinks, and the `sctx` command line validates them:

- **Schema validation** of each note's fields, with JSON Schema.
- **Structure**: broken links, duplicates, hierarchy rules and orphaned nodes.
- **Rules** expressed against the graph, with error, warning and info severities, so best-practice advice doesn't fail a build.
- **Semantic rules** for tests an expression can't do, such as "is this opportunity a customer need, or a solution in disguise?", judged by a model. An eval harness measures each model provider's agreement and stability on labelled cases.

Bundled schemas cover knowledge wikis, opportunity solution trees and general strategy. It also renders spaces as Mermaid diagrams and syncs them to Miro.

## Map views

[Map views](https://github.com/mindsocket/structured-context-map-views) project a space into a visual form (a tree, nested containers or a network) from a short declarative definition, with validation results overlaid on the nodes. The same space can be shown several ways, and a React library renders them in any host: a standalone navigator, a self-contained HTML export, or a Claude artifact.

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
