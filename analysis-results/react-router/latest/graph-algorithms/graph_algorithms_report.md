---
title: "Graph Algorithms Report"
generated: "2026-11-01"
model_version: "v5.0.0"
dataset: "react-router-7.18.4"
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
| ["TS","Local","Module"] | ./config/routes.ts | 4.521835360658178 |
| ["TS","Local","Module"] | ./routes.ts | 4.058809050094733 |
| ["TS","Local","Module"] | ./lib/router/url.ts | 2.189948927363485 |
| ["TS","Local","Module"] | ./lib/router/history.ts | 2.1726310617196747 |
| ["TS","Local","Module"] | ./lib/router/utils.ts | 2.0545285811791114 |
| ["TS","Local","Module"] | ./utils.ts | 1.2310670442525808 |
| ["TS","Local","Module"] | ./config/is-react-router-repo.ts | 1.1421281906923575 |
| ["TS","Local","Module"] | ./index.ts | 0.9997042353362876 |
| ["TS","Local","Module"] | ./server.ts | 0.9997042353362876 |
| ["TS","Local","Module"] | ./vite/vite.ts | 0.9487072964079414 |

### 2.2 Top Nodes by ArticleRank

| nodeLabels | nodeName | articleRankScore |
| --- | --- | --- |
| ["TS","Local","Module"] | ./config/routes.ts | 1.8809882288177266 |
| ["TS","Local","Module"] | ./routes.ts | 1.7767260866669135 |
| ["TS","Local","Module"] | ./lib/router/history.ts | 1.4102754234583277 |
| ["TS","Local","Module"] | ./lib/router/utils.ts | 1.3389968349317953 |
| ["TS","Local","Module"] | ./utils.ts | 1.2111837353332375 |
| ["TS","Local","Module"] | ./vite/vite.ts | 0.6634183538942674 |
| ["TS","Local","Module"] | ./lib/router/url.ts | 0.633573298779074 |
| ["Package","Json","NPM","NpmNonDevPackage"] | /home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.4/./source/react-router-7.18.4/packages/react-router/package.json | 0.6210063135297951 |
| ["TS","Local","Module"] | ./lib/router/router.ts | 0.5119785467651081 |
| ["TS","Local","Module"] | ./vendor/turbo-stream-v2/utils.ts | 0.49217418688088044 |

### 2.3 Top Nodes by Betweenness Centrality

| nodeLabels | nodeName | betweennessScore |
| --- | --- | --- |
| ["TS","Local","Module"] | ./lib/router/instrumentation.ts | 444.5 |
| ["TS","Local","Module"] | ./lib/router/router.ts | 424 |
| ["TS","Local","Module"] | ./lib/server-runtime/server.ts | 411 |
| ["TS","Local","Module"] | ./lib/dom/ssr/entry.ts | 385 |
| ["TS","Local","Module"] | ./lib/server-runtime/data.ts | 166 |
| ["TS","Local","Module"] | ./lib/dom/ssr/routeModules.ts | 130.5 |
| ["TS","Local","Module"] | ./lib/types/route-data.ts | 108.5 |
| ["TS","Local","Module"] | ./vite/plugin.ts | 97.5 |
| ["TS","Local","Module"] | ./lib/server-runtime/single-fetch.ts | 96 |
| ["TS","Local","Module"] | ./lib/server-runtime/routes.ts | 79 |

---

## 3. Community Detection

High community sizes may indicate monolithic modules; many small = well-modularised.

### 3.1 Leiden Communities Overview

| communityId | communitySize |
| --- | --- |
| 9 | 45 |
| 10 | 43 |
| 3 | 10 |
| 1 | 4 |
| 4 | 4 |
| 7 | 4 |
| 17 | 4 |
| 0 | 3 |
| 8 | 3 |
| 5 | 2 |

### 3.2 Strongly Connected Components (SCC)

Components with more than one member = circular dependencies.

| componentId | componentSize |
| --- | --- |
| 76 | 18 |
| 20 | 2 |
| 22 | 2 |
| 53 | 2 |
| 3 | 2 |
| 0 | 2 |
| 30 | 2 |
| 28 | 2 |
| 6 | 1 |
| 11 | 1 |

### 3.3 Weakly Connected Components (WCC)

Weakly connected components identify isolated clusters of code units.

| componentId | componentSize |
| --- | --- |
| 10 | 51 |
| 9 | 45 |
| 3 | 10 |
| 1 | 4 |
| 4 | 4 |
| 7 | 4 |
| 0 | 3 |
| 8 | 3 |
| 5 | 2 |
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
| ["TS","Local","Module"] | ./lib/dom/ssr/routeModules.ts | ["TS","Local","Module"] | ./lib/server-runtime/routeMatching.ts | 1 |
| ["TS","Local","Module"] | ./prompts-confirm.ts | ["TS","Local","Module"] | ./prompts-text.ts | 1 |
| ["TS","Local","Module"] | ./index-react-server-client.ts | ["TS","Local","Module"] | ./lib/router/navigation.ts | 1 |
| ["TS","Local","Module"] | ./vite/vite.ts | ["TS","Local","Module"] | ./vite/ssr-externals.ts | 1 |
| ["TS","Local","Module"] | ./prompts-text.ts | ["TS","Local","Module"] | ./prompts-confirm.ts | 1 |
| ["TS","Local","Module"] | ./lib/server-runtime/routeMatching.ts | ["TS","Local","Module"] | ./lib/dom/ssr/routeModules.ts | 1 |
| ["TS","Local","Module"] | ./lib/router/navigation.ts | ["TS","Local","Module"] | ./index-react-server-client.ts | 1 |
| ["TS","Local","Module"] | ./vite/ssr-externals.ts | ["TS","Local","Module"] | ./vite/vite.ts | 1 |
| ["TS","Local","Module"] | ./prompts-select.ts | ["TS","Local","Module"] | ./prompts-multi-select.ts | 0.9488054607508533 |
| ["TS","Local","Module"] | ./prompts-multi-select.ts | ["TS","Local","Module"] | ./prompts-select.ts | 0.9488054607508533 |
