---
title: "Graph Algorithms Report"
generated: "2026-08-03"
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
| ["TS","Local","Module"] | ./index.ts | 8.150240394925964 |
| ["TS","Local","Module"] | ./config/routes.ts | 4.510155154175984 |
| ["TS","Local","Module"] | ./index-react-server.ts | 4.3577885425688185 |
| ["TS","Local","Module"] | ./routes.ts | 4.04872680184805 |
| ["TS","Local","Module"] | ./lib/router/utils.ts | 3.822423393062565 |
| ["TS","Local","Module"] | ./lib/router/history.ts | 2.273652054730552 |
| ["TS","Local","Module"] | ./config/config.ts | 1.89713732533955 |
| ["TS","Local","Module"] | ./lib/rsc/server.rsc.ts | 1.7583672785631015 |
| ["TS","Local","Module"] | ./config.ts | 1.4592375318539754 |
| ["TS","Local","Module"] | ./lib/router/router.ts | 1.4529576338219823 |

### 2.2 Top Nodes by ArticleRank

| nodeLabels | nodeName | articleRankScore |
| --- | --- | --- |
| ["TS","Local","Module"] | ./index.ts | 6.42005057488811 |
| ["TS","Local","Module"] | ./index-react-server.ts | 3.427271390597128 |
| ["TS","Local","Module"] | ./lib/router/utils.ts | 3.0464250822470027 |
| ["TS","Local","Module"] | ./config/routes.ts | 2.09966846225266 |
| ["TS","Local","Module"] | ./routes.ts | 1.9984080297655733 |
| ["TS","Local","Module"] | ./lib/router/history.ts | 1.8227651558157882 |
| ["TS","Local","Module"] | ./lib/rsc/server.rsc.ts | 1.3352644334167072 |
| ["TS","Local","Module"] | ./utils.ts | 1.2077187931793871 |
| ["TS","Local","Module"] | ./lib/router/router.ts | 1.179058257514483 |
| ["TS","Local","Module"] | ./config/config.ts | 0.7685189472305033 |

### 2.3 Top Nodes by Betweenness Centrality

| nodeLabels | nodeName | betweennessScore |
| --- | --- | --- |
| ["TS","Local","Module"] | ./index.ts | 1195.3333333333335 |
| ["TS","Local","Module"] | ./lib/server-runtime/server.ts | 517.5 |
| ["TS","Local","Module"] | ./lib/dom/ssr/routeModules.ts | 346 |
| ["TS","Local","Module"] | ./lib/types/route-data.ts | 344 |
| ["TS","Local","Module"] | ./dom-export.ts | 335 |
| ["TS","Local","Module"] | ./index-react-server.ts | 298.5 |
| ["TS","Local","Module"] | ./lib/dom/ssr/entry.ts | 257 |
| ["TS","Local","Module"] | ./lib/server-runtime/routes.ts | 159.83333333333334 |
| ["TS","Local","Module"] | ./lib/router/instrumentation.ts | 142.5 |
| ["TS","Local","Module"] | ./lib/server-runtime/single-fetch.ts | 138 |

---

## 3. Community Detection

High community sizes may indicate monolithic modules; many small = well-modularised.

### 3.1 Leiden Communities Overview

| communityId | communitySize |
| --- | --- |
| 8 | 43 |
| 5 | 27 |
| 4 | 18 |
| 2 | 10 |
| 0 | 4 |
| 6 | 4 |
| 7 | 4 |
| 14 | 4 |
| 15 | 3 |
| 17 | 3 |

### 3.2 Strongly Connected Components (SCC)

Components with more than one member = circular dependencies.

| componentId | componentSize |
| --- | --- |
| 64 | 35 |
| 15 | 2 |
| 84 | 2 |
| 14 | 2 |
| 0 | 2 |
| 58 | 2 |
| 40 | 2 |
| 17 | 2 |
| 6 | 1 |
| 11 | 1 |

### 3.3 Weakly Connected Components (WCC)

Weakly connected components identify isolated clusters of code units.

| componentId | componentSize |
| --- | --- |
| 7 | 52 |
| 4 | 45 |
| 2 | 10 |
| 0 | 4 |
| 5 | 4 |
| 6 | 4 |
| 10 | 3 |
| 12 | 3 |
| 3 | 2 |
| 1 | 1 |

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
| ["TS","Local","Module"] | ./prompts-text.ts | ["TS","Local","Module"] | ./prompts-confirm.ts | 1 |
| ["TS","Local","Module"] | ./prompts-confirm.ts | ["TS","Local","Module"] | ./prompts-text.ts | 1 |
| ["TS","Local","Module"] | ./vite/vite.ts | ["TS","Local","Module"] | ./vite/ssr-externals.ts | 1 |
| ["TS","Local","Module"] | ./prompts-multi-select.ts | ["TS","Local","Module"] | ./prompts-select.ts | 0.9488054607508533 |
| ["TS","Local","Module"] | ./prompts-select.ts | ["TS","Local","Module"] | ./prompts-multi-select.ts | 0.9488054607508533 |
| ["TS","Local","Module"] | ./prompts-text.ts | ["TS","Local","Module"] | ./prompts-select.ts | 0.8516187050359713 |
| ["TS","Local","Module"] | ./prompts-select.ts | ["TS","Local","Module"] | ./prompts-confirm.ts | 0.8516187050359713 |
| ["TS","Local","Module"] | ./prompts-select.ts | ["TS","Local","Module"] | ./prompts-text.ts | 0.8516187050359713 |
| ["TS","Local","Module"] | ./prompts-confirm.ts | ["TS","Local","Module"] | ./prompts-select.ts | 0.8516187050359713 |
