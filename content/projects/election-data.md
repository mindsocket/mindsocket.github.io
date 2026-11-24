---
weight: 80
title: "election-data"
description: "Analysis pipeline and dashboard combining Australian election results with census data"
tags: ["python", "data", "politics", "geospatial"]
---

An analysis pipeline and interactive dashboard for Australian election data. It combines electoral commission results with ABS census statistics and boundary files to look at how votes move, where, and who is voting.

## Analysis

- **Preference flows.** How votes transfer between candidates across counting rounds, at electorate and polling-place level, shown as Sankey and alluvial charts.
- **Geographic mapping.** Census areas mapped to polling places, with several mapping methods compared, plus booth-level results and swings on interactive maps.
- **Census and polling correlation.** Demographic variables correlated with booth results, with the statistical caveats shown alongside the numbers.
- **Boundary changes.** Results projected across redistributions and overlapping electorates, with comparisons of weighting methods.

## How it's built

A Python pipeline (pandas, GeoPandas, SciPy) writes analysis outputs, and a Streamlit app with Plotly and Folium reads only those outputs. Coding agents work across the whole project, guided by per-module agent instructions, with a custom subagent that reruns analyses to refresh outputs after a change.

Soloware, source unavailable.
