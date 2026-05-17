---
title: "Graph Algorithms Report"
generated: "2026-05-17"
model_version: "v4.0.1"
dataset: "react-router-7.15.1"
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
| ["TS","Local","Module"] | ./index.ts | 8.262529228011838 |
| ["TS","Local","Module"] | ./index-react-server.ts | 5.373070400029871 |
| ["TS","Local","Module"] | ./config/routes.ts | 4.53204662593712 |
| ["TS","Local","Module"] | ./routes.ts | 4.067520809655857 |
| ["TS","Local","Module"] | ./lib/router/utils.ts | 4.004872544431184 |
| ["TS","Local","Module"] | ./lib/rsc/server.rsc.ts | 2.164126016296791 |
| ["TS","Local","Module"] | ./lib/router/history.ts | 1.835730750311156 |
| ["TS","Local","Module"] | ./config/config.ts | 1.7959419151352183 |
| ["TS","Local","Module"] | ./lib/router/router.ts | 1.5401153791154225 |
| ["TS","Local","Module"] | ./config.ts | 1.3488623797991672 |

### 2.2 Top Nodes by ArticleRank

| nodeLabels | nodeName | articleRankScore |
| --- | --- | --- |
| ["TS","Local","Module"] | ./index.ts | 6.712583744338096 |
| ["TS","Local","Module"] | ./index-react-server.ts | 4.360708075186662 |
| ["TS","Local","Module"] | ./lib/router/utils.ts | 3.2916025977620755 |
| ["TS","Local","Module"] | ./config/routes.ts | 2.0962359876739987 |
| ["TS","Local","Module"] | ./routes.ts | 1.9950794335039266 |
| ["TS","Local","Module"] | ./lib/rsc/server.rsc.ts | 1.6824592040995334 |
| ["TS","Local","Module"] | ./lib/router/history.ts | 1.5216775946278132 |
| ["TS","Local","Module"] | ./lib/router/router.ts | 1.2786505055931878 |
| ["TS","Local","Module"] | ./utils.ts | 1.208695921682819 |
| ["TS","Local","Module"] | ./config/config.ts | 0.7506240445237004 |

### 2.3 Top Nodes by Betweenness Centrality

| nodeLabels | nodeName | betweennessScore |
| --- | --- | --- |
| ["TS","Local","Module"] | ./index.ts | 1209 |
| ["TS","Local","Module"] | ./lib/server-runtime/server.ts | 522 |
| ["TS","Local","Module"] | ./dom-export.ts | 394.5 |
| ["TS","Local","Module"] | ./index-react-server.ts | 370.5 |
| ["TS","Local","Module"] | ./lib/types/route-data.ts | 360.5 |
| ["TS","Local","Module"] | ./lib/dom/ssr/routeModules.ts | 351.5 |
| ["TS","Local","Module"] | ./lib/server-runtime/routes.ts | 203.5 |
| ["TS","Local","Module"] | ./lib/dom/ssr/entry.ts | 146 |
| ["TS","Local","Module"] | ./lib/router/instrumentation.ts | 142 |
| ["TS","Local","Module"] | ./lib/server-runtime/single-fetch.ts | 140 |

---

## 3. Community Detection

High community sizes may indicate monolithic modules; many small = well-modularised.

### 3.1 Leiden Communities Overview

| communityId | communitySize |
| --- | --- |
| 5 | 45 |
| 6 | 39 |
| 1 | 10 |
| 2 | 4 |
| 4 | 4 |
| 11 | 4 |
| 13 | 4 |
| 16 | 4 |
| 15 | 3 |
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
| ["TS","Local","Module"] | ./prompts-text.ts | ["TS","Local","Module"] | ./prompts-confirm.ts | 1 |
| ["TS","Local","Module"] | ./prompts-confirm.ts | ["TS","Local","Module"] | ./prompts-text.ts | 1 |
| ["TS","Local","Module"] | ./vite/ssr-externals.ts | ["TS","Local","Module"] | ./vite/vite.ts | 1 |
| ["TS","Local","Module"] | ./vite/vite.ts | ["TS","Local","Module"] | ./vite/ssr-externals.ts | 1 |
| ["TS","Local","Module"] | ./prompts-select.ts | ["TS","Local","Module"] | ./prompts-multi-select.ts | 0.956029011786038 |
| ["TS","Local","Module"] | ./prompts-multi-select.ts | ["TS","Local","Module"] | ./prompts-select.ts | 0.956029011786038 |
| ["TS","Local","Module"] | ./prompts-select.ts | ["TS","Local","Module"] | ./prompts-text.ts | 0.8705547652916074 |
| ["TS","Local","Module"] | ./prompts-text.ts | ["TS","Local","Module"] | ./prompts-select.ts | 0.8705547652916074 |
| ["TS","Local","Module"] | ./prompts-confirm.ts | ["TS","Local","Module"] | ./prompts-select.ts | 0.8705547652916074 |
| ["TS","Local","Module"] | ./prompts-select.ts | ["TS","Local","Module"] | ./prompts-confirm.ts | 0.8705547652916074 |
