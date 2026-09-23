---
icon: material/music-note-eighth
tags:
  - R
  - Market Basket Analysis
  - Data Mining
---

# Spotify Pattern Mining Recommendations

> *Market basket analysis on 1M+ Spotify listening records to surface high-confidence music recommendation rules*

[:material-file-document-outline: Case Study](../assets/321-Lab-7.html){ .md-button .md-button--primary target="_blank" rel="noopener" }

:material-lock-outline: *Source private — academic coursework. [Available upon request](https://github.com/pdotpope/spotify-pattern-mining).*

![Case Study Preview](../assets/spotify-ss.jpg)

## Overview

- Frames each user's listening history as a "basket" and mines association rules to find artists and tracks that are reliably co-listened — the basis for a simple recommendation engine
- **Built three transaction sets** (artist, track, artist+track) from 742K cleaned Spotify records using user-level market basket framing
- **Benchmarked Apriori vs. ECLAT** across speed, memory, and rule quality — Apriori won both benchmarks
- **Surfaced top rules by lift** (e.g. Daft Punk catalog co-listens, hip-hop and pop trios) with an actionable recommendation pitch

## Tech Stack

| Layer | Tools |
|---|---|
| **Data Prep** | R, dplyr |
| **Mining** | arules (Apriori & ECLAT; support/confidence/lift tuning) |
| **Visualization** | arulesViz, ggplot2, plotly |
| **Profiling** | Rprofmem, proc.time |
| **Reporting** | Quarto |

## Skills Developed

- Association rule mining and parameter tuning
- Algorithm benchmarking (runtime and memory)
- Translating statistical output into business recommendations
