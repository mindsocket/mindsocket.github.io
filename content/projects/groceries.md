---
weight: 50
title: "groceries"
description: "An agent that tracks Woolworths prices and sends a weekly summary of discounts worth acting on"
tags: ["python", "data", "agents"]
---

An agent that keeps track of grocery prices at Woolworths (Australia) and tells me, each week, which discounts on things I actually buy are worth paying attention to.

- **Price history.** My purchase history comes from e-receipts and past orders, extended with longer-term price data, so each product has a picture of its normal price and how often it goes on special.
- **Current deals.** Each week the agent drives a browser session to fetch current specials for my regular items, and scores them against that history to separate real discounts from routine ones.
- **Weekly summary.** A scheduled run produces a short list of what's worth buying now, delivered to chat without me asking.

Built with the Claude Agent SDK, agent skills for fetching, discount analysis and list updates, Playwright, and Python analysis scripts.

Soloware, source unavailable.
