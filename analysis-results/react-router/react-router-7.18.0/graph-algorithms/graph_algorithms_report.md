---
title: "Graph Algorithms Report"
generated: "2026-06-29"
model_version: "v4.0.1"
dataset: "react-router-7.18.0"
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
| ["TS","Local","Module"] | ./index.ts | 8.336356405659776 |
| ["TS","Local","Module"] | ./config/routes.ts | 4.510155154175984 |
| ["TS","Local","Module"] | ./routes.ts | 4.04872680184805 |
| ["TS","Local","Module"] | ./lib/router/utils.ts | 3.820419854786413 |
| ["TS","Local","Module"] | ./index-react-server.ts | 3.77616285807565 |
| ["TS","Local","Module"] | ./lib/router/history.ts | 2.664543740895719 |
| ["TS","Local","Module"] | ./config/config.ts | 1.89713732533955 |
| ["TS","Local","Module"] | ./lib/rsc/server.rsc.ts | 1.5464647882639382 |
| ["TS","Local","Module"] | ./config.ts | 1.4592375318539754 |
| ["TS","Local","Module"] | ./lib/router/router.ts | 1.417936566057811 |

### 2.2 Top Nodes by ArticleRank

| nodeLabels | nodeName | articleRankScore |
| --- | --- | --- |
| ["TS","Local","Module"] | ./index.ts | 6.258790861646853 |
| ["TS","Local","Module"] | ./lib/router/utils.ts | 2.908567371418786 |
| ["TS","Local","Module"] | ./index-react-server.ts | 2.8382492800362775 |
| ["TS","Local","Module"] | ./config/routes.ts | 2.102648888573224 |
| ["TS","Local","Module"] | ./lib/router/history.ts | 2.0378275567296873 |
| ["TS","Local","Module"] | ./routes.ts | 2.000946126575158 |
| ["TS","Local","Module"] | ./utils.ts | 1.2085808417745258 |
| ["TS","Local","Module"] | ./lib/rsc/server.rsc.ts | 1.1333320361507908 |
| ["TS","Local","Module"] | ./lib/router/router.ts | 1.1095850494695636 |
| ["TS","Local","Module"] | ./config/config.ts | 0.7691776373514998 |

### 2.3 Top Nodes by Betweenness Centrality

| nodeLabels | nodeName | betweennessScore |
| --- | --- | --- |
| ["TS","Local","Module"] | ./index.ts | 1238.6666666666667 |
| ["TS","Local","Module"] | ./lib/server-runtime/server.ts | 471.1666666666667 |
| ["TS","Local","Module"] | ./lib/dom/ssr/routeModules.ts | 408.1666666666667 |
| ["TS","Local","Module"] | ./lib/types/route-data.ts | 372.1666666666667 |
| ["TS","Local","Module"] | ./lib/dom/ssr/entry.ts | 343 |
| ["TS","Local","Module"] | ./dom-export.ts | 292.3333333333333 |
| ["TS","Local","Module"] | ./index-react-server.ts | 225.16666666666666 |
| ["TS","Local","Module"] | ./lib/router/instrumentation.ts | 144.66666666666666 |
| ["TS","Local","Module"] | ./lib/server-runtime/single-fetch.ts | 138 |
| ["TS","Local","Module"] | ./lib/server-runtime/cookies.ts | 115 |

---

## 3. Community Detection

High community sizes may indicate monolithic modules; many small = well-modularised.

### 3.1 Leiden Communities Overview

| communityId | communitySize |
| --- | --- |
| 9 | 43 |
| 5 | 26 |
| 4 | 19 |
| 2 | 10 |
| 3 | 4 |
| 15 | 4 |
| 16 | 4 |
| 6 | 3 |
| 8 | 3 |
| 7 | 2 |

### 3.2 Strongly Connected Components (SCC)

Components with more than one member = circular dependencies.

| componentId | componentSize |
| --- | --- |
| 64 | 35 |
| 60 | 2 |
| 85 | 2 |
| 16 | 2 |
| 41 | 2 |
| 18 | 2 |
| 58 | 2 |
| 6 | 1 |
| 5 | 1 |
| 2 | 1 |

### 3.3 Weakly Connected Components (WCC)

Weakly connected components identify isolated clusters of code units.

| componentId | componentSize |
| --- | --- |
| 8 | 52 |
| 4 | 45 |
| 2 | 10 |
| 3 | 4 |
| 11 | 4 |
| 5 | 3 |
| 7 | 3 |
| 6 | 2 |
| 0 | 1 |
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
| ["TS","Local","Module"] | ./vite/vite.ts | ["TS","Local","Module"] | ./vite/ssr-externals.ts | 1 |
| ["TS","Local","Module"] | ./prompts-confirm.ts | ["TS","Local","Module"] | ./prompts-text.ts | 1 |
| ["TS","Local","Module"] | ./prompts-text.ts | ["TS","Local","Module"] | ./prompts-confirm.ts | 1 |
| ["TS","Local","Module"] | ./vite/ssr-externals.ts | ["TS","Local","Module"] | ./vite/vite.ts | 1 |
| ["TS","Local","Module"] | ./prompts-select.ts | ["TS","Local","Module"] | ./prompts-multi-select.ts | 0.9537190082644628 |
| ["TS","Local","Module"] | ./prompts-multi-select.ts | ["TS","Local","Module"] | ./prompts-select.ts | 0.9537190082644628 |
| ["TS","Local","Module"] | ./prompts-confirm.ts | ["TS","Local","Module"] | ./prompts-select.ts | 0.8648180242634316 |
| ["TS","Local","Module"] | ./prompts-select.ts | ["TS","Local","Module"] | ./prompts-text.ts | 0.8648180242634316 |
| ["TS","Local","Module"] | ./prompts-select.ts | ["TS","Local","Module"] | ./prompts-confirm.ts | 0.8648180242634316 |
| ["TS","Local","Module"] | ./prompts-text.ts | ["TS","Local","Module"] | ./prompts-select.ts | 0.8648180242634316 |
