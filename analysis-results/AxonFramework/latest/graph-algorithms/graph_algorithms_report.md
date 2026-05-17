---
title: "Graph Algorithms Report"
generated: "2026-05-17"
model_version: "v4.0.1"
dataset: "AxonFramework-5.0.3"
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
| ["Type","Java","GenericDeclaration","Class"] | org.axonframework.common.TypeReference | 55.72396354031647 |
| ["Type","Java","Class"] | org.axonframework.common.TypeReference$1 | 23.830790162613184 |
| ["Type","Java","Class"] | org.axonframework.common.TypeReference$2 | 23.830790162613184 |
| ["Type","Java","GenericDeclaration","Class"] | org.axonframework.messaging.core.Context$ResourceKey | 21.535011791887158 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.Message | 18.990384377853424 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.unitofwork.ProcessingContext | 16.836430298013376 |
| ["Type","Java","Interface"] | org.axonframework.common.infra.ComponentDescriptor | 11.385080188798016 |
| ["Type","Java","Interface"] | org.axonframework.common.infra.DescribableComponent | 11.313026504022579 |
| ["Package","Java"] | org.axonframework.common | 11.293971497104378 |
| ["Type","Java","Interface"] | org.axonframework.conversion.Converter | 10.722356401285493 |

[Full data](./Java_Package/centrality/Package_Centrality_Page_Rank.csv)

### 2.2 Top Nodes by ArticleRank

| nodeLabels | nodeName | articleRankScore |
| --- | --- | --- |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.Message | 8.978342928599854 |
| ["Type","Java","GenericDeclaration","Class"] | org.axonframework.messaging.core.Context$ResourceKey | 7.403874973133302 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.unitofwork.ProcessingContext | 7.180607352629666 |
| ["Type","Java","GenericDeclaration","Class"] | org.axonframework.common.TypeReference | 6.230648582059334 |
| ["Package","Java"] | org.axonframework.common | 5.912804370951201 |
| ["Type","Java","Interface"] | org.axonframework.conversion.Converter | 4.536010027941138 |
| ["Package","Java"] | org.axonframework.messaging.core | 4.317171793992321 |
| ["Type","Java","Interface","GenericDeclaration"] | org.axonframework.messaging.core.MessageStream | 3.419016665191459 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.Context | 3.263625625372985 |
| ["Type","Java","Interface"] | org.axonframework.messaging.eventhandling.EventMessage | 2.8155684917134627 |

[Full data](./Java_Package/centrality/Package_Centrality_Article_Rank.csv)

### 2.3 Top Nodes by Betweenness Centrality

| nodeLabels | nodeName | betweennessScore |
| --- | --- | --- |
| ["Type","Java","Interface","GenericDeclaration"] | org.axonframework.messaging.core.MessageStream | 10120.975559734383 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.Message | 9922.418001443004 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.unitofwork.ProcessingContext | 6810.244227994231 |
| ["Type","Java","Record"] | org.axonframework.messaging.core.QualifiedName | 4806.01433664375 |
| ["Type","Java","Class"] | org.axonframework.common.ReflectionUtils | 4449.550000000002 |
| ["Type","Java","Record"] | org.axonframework.messaging.core.MessageType | 4213.667697988286 |
| ["Type","Java","GenericDeclaration","Class"] | org.axonframework.modelling.entity.annotation.AnnotatedEntityMetamodel | 3160.1476190476183 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.unitofwork.ProcessingLifecycle | 2507.9396825396825 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.Context | 2039.7333333333336 |
| ["Type","Java","Class"] | org.axonframework.common.TypeReflectionUtils | 2024 |

[Full data](./Java_Package/centrality/Package_Centrality_Betweeness.csv)

---

## 3. Community Detection

High community sizes may indicate monolithic modules; many small = well-modularised.

### 3.1 Leiden Communities Overview

| communityId | communitySize |
| --- | --- |
| 8 | 158 |
| 4 | 136 |
| 2 | 108 |
| 3 | 106 |
| 1 | 105 |
| 0 | 99 |
| 9 | 88 |
| 5 | 83 |
| 11 | 79 |
| 13 | 78 |

[Full data](./Java_Package/communities/Package_Communities_Leiden.csv)

### 3.2 Strongly Connected Components (SCC)

Components with more than one member = circular dependencies.

| componentId | componentSize |
| --- | --- |
| 65 | 29 |
| 9 | 19 |
| 0 | 14 |
| 834 | 14 |
| 3 | 12 |
| 627 | 12 |
| 874 | 9 |
| 269 | 9 |
| 791 | 8 |
| 77 | 8 |

[Full data](./Java_Package/communities/Package_Communities_Strongly_Connected_Components.csv)

### 3.3 Weakly Connected Components (WCC)

Weakly connected components identify isolated clusters of code units.

| componentId | componentSize |
| --- | --- |
| 0 | 1323 |
| 2 | 5 |
| 1 | 4 |
| 4 | 3 |
| 3 | 2 |

[Full data](./Java_Package/communities/Package_Communities_Weakly_Connected_Components.csv)

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
| ["Type","Java","GenericDeclaration","Class"] | org.axonframework.test.matchers.SequenceMatcher | ["Type","Java","GenericDeclaration","Class"] | org.axonframework.test.matchers.ListWithAllOfMatcher | 1 |
| ["Type","Java","GenericDeclaration","Class"] | org.axonframework.test.matchers.ExactSequenceMatcher | ["Type","Java","GenericDeclaration","Class"] | org.axonframework.test.matchers.SequenceMatcher | 1 |
| ["Type","Java","Class"] | org.axonframework.test.matchers.AllFieldsFilter | ["Type","Java","Class"] | org.axonframework.test.matchers.NonStaticFieldsFilter | 1 |
| ["Type","Java","GenericDeclaration","Class"] | org.axonframework.test.matchers.SequenceMatcher | ["Type","Java","GenericDeclaration","Class"] | org.axonframework.test.matchers.ExactSequenceMatcher | 1 |
| ["Type","Java","Class"] | org.axonframework.test.matchers.NonStaticFieldsFilter | ["Type","Java","Class"] | org.axonframework.test.matchers.AllFieldsFilter | 1 |
| ["Type","Java","GenericDeclaration","Class"] | org.axonframework.test.matchers.SequenceMatcher | ["Type","Java","GenericDeclaration","Class"] | org.axonframework.test.matchers.ListWithAnyOfMatcher | 1 |
| ["Type","Java","Record"] | org.axonframework.test.util.MessageMonitorReport$Report$Success | ["Type","Java","Record"] | org.axonframework.test.util.MessageMonitorReport$Report$Ignored | 1 |
| ["Package","Java"] | org.axonframework.conversion.jackson2 | ["Package","Java"] | org.axonframework.conversion.jackson | 1 |
| ["Type","Java","Record"] | org.axonframework.test.util.MessageMonitorReport$Report$Failure | ["Type","Java","Record"] | org.axonframework.test.util.MessageMonitorReport$Report$Ignored | 1 |
| ["Type","Java","Class"] | org.axonframework.test.matchers.PayloadsMatcher | ["Type","Java","GenericDeclaration","Class"] | org.axonframework.test.matchers.PayloadMatcher | 1 |

[Full data](./Java_Package/similarity/Package_Similarity.csv)
