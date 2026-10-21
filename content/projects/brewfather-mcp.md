---
title: "brewfather-mcp"
description: "MCP server and CLI for Brewfather homebrewing software"
tags: ["homebrewing", "mcp", "python", "claude"]
---

An [MCP](https://modelcontextprotocol.io) server and command-line tool that give AI assistants (Claude, or any MCP client) access to a [Brewfather](https://brewfather.app) account: inventory, recipes, batches and live brewing readings.

This is my extended fork of [renanvieira/brewfather-mcp](https://github.com/renanvieira/brewfather-mcp), which provided the starting point (a read-only inventory server). The fork adds:

- Create, read and update coverage for batches, recipes and inventory (fermentables, hops, yeasts, miscellaneous), with much fuller field and type coverage.
- Brew tracking and device readings, with delta calculations between measurements and timing calculations for active brew steps.
- An HTTP/SSE runner alongside stdio, and `uvx` installation straight from the repository.
- A CLI for managing inventory and recipes without an MCP client, and a Claude skill that teaches the assistant how to brew with it.
- A much larger test suite.

[![brewfather-mcp](https://github-readme-stats.vercel.app/api/pin/?username=mindsocket&repo=brewfather-mcp)](https://github.com/mindsocket/brewfather-mcp)
