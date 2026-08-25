---
title: "Graph Algorithms Report"
generated: "2026-08-25"
model_version: "v4.0.2"
dataset: "react-router-7.18.1"
authors: ["JohT/code-graph-analysis-pipeline"]
---

# 📊 Graph Algorithms Report

## 1. Overview

Graph algorithm results from the code graph: centrality, community detection, and node similarity.

- **Centrality** — which nodes (packages, types, artifacts) are most influential
- **Community Detection** — how code units cluster based on dependencies
- **Similarity** — which code units share the most common dependencies (Jaccard)

> **Reading the tables**: Rows are sorted by algorithm score — the **first rows are the most significant**.

## 📚 Table of Contents

1. [Overview](#1-overview)
1. [Centrality](#2-centrality)
1. [Community Detection](#3-community-detection)
1. [Similarity](#4-similarity)

---

## 2. Centrality

High PageRank = depended on by many important nodes. High betweenness = bridge between graph parts.

### 2.1 Top Nodes by PageRank

| nodeLabels | nodeName | pageRankScore |
| --- | --- | --- |
| ["TS","Local","Module"] | ./index.ts | 7.74454794932003 |
| ["TS","Local","Module"] | ./index-react-server.ts | 5.966840687252372 |
| ["TS","Local","Module"] | ./config/routes.ts | 4.590541454489806 |
| ["TS","Local","Module"] | ./routes.ts | 4.117128388905979 |
| ["TS","Local","Module"] | ./lib/router/utils.ts | 3.652890036891216 |
| ["TS","Local","Module"] | ./lib/rsc/server.rsc.ts | 2.7327267995487743 |
| ["TS","Local","Module"] | ./lib/router/router.ts | 1.578272736463822 |
| ["TS","Local","Module"] | ./config/config.ts | 1.3778280655650803 |
| ["TS","Local","Module"] | ./utils.ts | 1.2457147505432433 |
| ["TS","Local","Module"] | ./lib/router/history.ts | 1.1792603401652801 |

### 2.2 Top Nodes by ArticleRank

| nodeLabels | nodeName | articleRankScore |
| --- | --- | --- |
| ["TS","Local","Module"] | ./index.ts | 6.507195149774777 |
| ["TS","Local","Module"] | ./index-react-server.ts | 5.0197129649466605 |
| ["TS","Local","Module"] | ./lib/router/utils.ts | 3.1209469274703516 |
| ["TS","Local","Module"] | ./lib/rsc/server.rsc.ts | 2.191923980014328 |
| ["TS","Local","Module"] | ./config/routes.ts | 2.0100407303457413 |
| ["TS","Local","Module"] | ./routes.ts | 1.915839353763857 |
| ["TS","Local","Module"] | ./lib/router/router.ts | 1.3455643427733597 |
| ["TS","Local","Module"] | ./utils.ts | 1.1885559037142113 |
| ["TS","Local","Module"] | ./lib/router/history.ts | 1.0202570724041595 |
| ["TS","Local","Module"] | ./vite/vite.ts | 0.6963890072958532 |

### 2.3 Top Nodes by Betweenness Centrality

| nodeLabels | nodeName | betweennessScore |
| --- | --- | --- |
| ["TS","Local","Module"] | ./index.ts | 1250.5 |
| ["TS","Local","Module"] | ./lib/server-runtime/server.ts | 553.5 |
| ["TS","Local","Module"] | ./dom-export.ts | 463.5 |
| ["TS","Local","Module"] | ./index-react-server.ts | 413.5 |
| ["TS","Local","Module"] | ./lib/types/route-data.ts | 366.5 |
| ["TS","Local","Module"] | ./lib/dom/ssr/routeModules.ts | 353.5 |
| ["TS","Local","Module"] | ./lib/server-runtime/routes.ts | 231.5 |
| ["TS","Local","Module"] | ./lib/router/instrumentation.ts | 139 |
| ["TS","Local","Module"] | ./lib/server-runtime/single-fetch.ts | 138 |
| ["TS","Local","Module"] | ./lib/dom/ssr/entry.ts | 138 |

---

## 3. Community Detection

High community sizes may indicate monolithic modules; many small = well-modularised.

### 3.1 Leiden Communities Overview

| communityId | communitySize |
| --- | --- |
| 16 | 45 |
| 2 | 21 |
| 15 | 10 |
| 1 | 7 |
| 6 | 7 |
| 7 | 6 |
| 0 | 4 |
| 9 | 4 |
| 13 | 4 |
| 17 | 4 |

### 3.2 Strongly Connected Components (SCC)

Components with more than one member = circular dependencies.

| componentId | componentSize |
| --- | --- |
| 0 | 35 |
| 85 | 2 |
| 42 | 2 |
| 40 | 2 |
| 65 | 2 |
| 83 | 2 |
| 24 | 2 |
| 6 | 1 |
| 5 | 1 |
| 2 | 1 |

### 3.3 Weakly Connected Components (WCC)

Weakly connected components identify isolated clusters of code units.

| componentId | componentSize |
| --- | --- |
| 0 | 52 |
| 9 | 45 |
| 8 | 10 |
| 6 | 4 |
| 10 | 4 |
| 3 | 3 |
| 11 | 3 |
| 5 | 2 |
| 1 | 1 |
| 2 | 1 |

### 3.4 Local Clustering Coefficient

How tightly interconnected a node's neighbours are. High = dependencies are also mutually dependent.

> No graph algorithm data available.
> Run `centralityCsv.sh`, `communityCsv.sh`, and `similarityCsv.sh` first to generate the required data.

---

## 4. Similarity

Jaccard similarity: code units sharing common dependencies. High = potential duplication or related functionality.

### 4.1 Top Jaccard Similarity Pairs

| sourceNodeLabels | sourceNodeName | targetNodeLabels | targetNodeName | similarityScore |
| --- | --- | --- | --- | --- |
| ["TS","Local","Module"] | ./vite/vite.ts | ["TS","Local","Module"] | ./vite/ssr-externals.ts | 1 |
| ["TS","Local","Module"] | ./vite/ssr-externals.ts | ["TS","Local","Module"] | ./vite/vite.ts | 1 |
| ["TS","Local","Module"] | ./prompts-confirm.ts | ["TS","Local","Module"] | ./prompts-text.ts | 1 |
| ["TS","Local","Module"] | ./prompts-text.ts | ["TS","Local","Module"] | ./prompts-confirm.ts | 1 |
| ["TS","Local","Module"] | ./prompts-multi-select.ts | ["TS","Local","Module"] | ./prompts-select.ts | 0.9314516129032258 |
| ["TS","Local","Module"] | ./prompts-select.ts | ["TS","Local","Module"] | ./prompts-multi-select.ts | 0.9314516129032258 |
| ["TS","Local","Module"] | ./vendor/turbo-stream-v2/flatten.ts | ["TS","Local","Module"] | ./vendor/turbo-stream-v2/unflatten.ts | 0.8702928870292888 |
| ["TS","Local","Module"] | ./vendor/turbo-stream-v2/unflatten.ts | ["TS","Local","Module"] | ./vendor/turbo-stream-v2/flatten.ts | 0.8702928870292888 |
| ["TS","Local","Module"] | ./copy-template.ts | ["TS","Local","Module"] | ./prompts-prompt-base.ts | 0.8333333333333334 |
| ["TS","Local","Module"] | ./prompts-prompt-base.ts | ["TS","Local","Module"] | ./copy-template.ts | 0.8333333333333334 |
