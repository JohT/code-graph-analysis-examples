---
title: "Graph Algorithms Report"
generated: "2026-05-16"
model_version: "v4.0.0"
dataset: "react-router-7.13.2"
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
| ["TS","Local","Module"] | ./index.ts | 8.281459225037262 |
| ["TS","Local","Module"] | ./index-react-server.ts | 5.353894601979948 |
| ["TS","Local","Module"] | ./config/routes.ts | 4.540557522169513 |
| ["TS","Local","Module"] | ./routes.ts | 4.075289078859909 |
| ["TS","Local","Module"] | ./lib/router/utils.ts | 3.9479101721866328 |
| ["TS","Local","Module"] | ./lib/rsc/server.rsc.ts | 2.163341295757832 |
| ["TS","Local","Module"] | ./lib/router/history.ts | 1.8359809278406294 |
| ["TS","Local","Module"] | ./config/config.ts | 1.8010494100340855 |
| ["TS","Local","Module"] | ./lib/router/router.ts | 1.5513700048750918 |
| ["TS","Local","Module"] | ./config.ts | 1.35226484417677 |

### 2.2 Top Nodes by ArticleRank

| nodeLabels | nodeName | articleRankScore |
| --- | --- | --- |
| ["TS","Local","Module"] | ./index.ts | 6.7248595690370205 |
| ["TS","Local","Module"] | ./index-react-server.ts | 4.3420568387618435 |
| ["TS","Local","Module"] | ./lib/router/utils.ts | 3.2376917896697637 |
| ["TS","Local","Module"] | ./config/routes.ts | 2.109351969978533 |
| ["TS","Local","Module"] | ./routes.ts | 2.006758909869065 |
| ["TS","Local","Module"] | ./lib/rsc/server.rsc.ts | 1.6818305823735573 |
| ["TS","Local","Module"] | ./lib/router/history.ts | 1.5207275635383555 |
| ["TS","Local","Module"] | ./lib/router/router.ts | 1.2877323536178449 |
| ["TS","Local","Module"] | ./utils.ts | 1.2088807577540683 |
| ["TS","Local","Module"] | ./config/config.ts | 0.7551488290955344 |

### 2.3 Top Nodes by Betweenness Centrality

| nodeLabels | nodeName | betweennessScore |
| --- | --- | --- |
| ["TS","Local","Module"] | ./index.ts | 1163.1666666666667 |
| ["TS","Local","Module"] | ./lib/server-runtime/server.ts | 554 |
| ["TS","Local","Module"] | ./dom-export.ts | 372.33333333333337 |
| ["TS","Local","Module"] | ./index-react-server.ts | 368.33333333333337 |
| ["TS","Local","Module"] | ./lib/types/route-data.ts | 289.1666666666667 |
| ["TS","Local","Module"] | ./lib/dom/ssr/routeModules.ts | 279.1666666666667 |
| ["TS","Local","Module"] | ./lib/server-runtime/routes.ts | 192 |
| ["TS","Local","Module"] | ./lib/router/instrumentation.ts | 189 |
| ["TS","Local","Module"] | ./lib/server-runtime/entry.ts | 174 |
| ["TS","Local","Module"] | ./lib/router/router.ts | 142 |

---

## 3. Community Detection

High community sizes may indicate monolithic modules; many small = well-modularised.

### 3.1 Leiden Communities Overview

| communityId | communitySize |
| --- | --- |
| 5 | 45 |
| 6 | 41 |
| 1 | 10 |
| 2 | 4 |
| 4 | 4 |
| 10 | 4 |
| 12 | 4 |
| 15 | 4 |
| 14 | 3 |
| 3 | 2 |

### 3.2 Strongly Connected Components (SCC)

Components with more than one member = circular dependencies.

| componentId | componentSize |
| --- | --- |
| 60 | 34 |
| 12 | 2 |
| 15 | 2 |
| 43 | 2 |
| 14 | 2 |
| 18 | 2 |
| 20 | 2 |
| 6 | 1 |
| 5 | 1 |
| 2 | 1 |

### 3.3 Weakly Connected Components (WCC)

Weakly connected components identify isolated clusters of code units.

| componentId | componentSize |
| --- | --- |
| 6 | 52 |
| 5 | 45 |
| 1 | 10 |
| 2 | 4 |
| 4 | 4 |
| 11 | 4 |
| 10 | 3 |
| 3 | 2 |
| 0 | 1 |
| 7 | 1 |

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
| ["TS","Local","Module"] | ./vite/ssr-externals.ts | ["TS","Local","Module"] | ./vite/vite.ts | 1 |
| ["TS","Local","Module"] | ./vite/vite.ts | ["TS","Local","Module"] | ./vite/ssr-externals.ts | 1 |
| ["TS","Local","Module"] | ./prompts-text.ts | ["TS","Local","Module"] | ./prompts-confirm.ts | 1 |
| ["TS","Local","Module"] | ./prompts-confirm.ts | ["TS","Local","Module"] | ./prompts-text.ts | 1 |
| ["TS","Local","Module"] | ./prompts-select.ts | ["TS","Local","Module"] | ./prompts-multi-select.ts | 0.956029011786038 |
| ["TS","Local","Module"] | ./prompts-multi-select.ts | ["TS","Local","Module"] | ./prompts-select.ts | 0.956029011786038 |
| ["TS","Local","Module"] | ./vendor/turbo-stream-v2/flatten.ts | ["TS","Local","Module"] | ./vendor/turbo-stream-v2/unflatten.ts | 0.92 |
| ["TS","Local","Module"] | ./vendor/turbo-stream-v2/unflatten.ts | ["TS","Local","Module"] | ./vendor/turbo-stream-v2/flatten.ts | 0.92 |
| ["TS","Local","Module"] | ./prompts-select.ts | ["TS","Local","Module"] | ./prompts-text.ts | 0.8705547652916074 |
| ["TS","Local","Module"] | ./prompts-select.ts | ["TS","Local","Module"] | ./prompts-confirm.ts | 0.8705547652916074 |
