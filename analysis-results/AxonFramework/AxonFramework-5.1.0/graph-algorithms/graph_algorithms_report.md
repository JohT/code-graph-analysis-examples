---
title: "Graph Algorithms Report"
generated: "2026-05-18"
model_version: "v4.0.1"
dataset: "AxonFramework-5.1.0"
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
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.common.TypeReference | 54.03456777430063 |
| ["Type","Java","Class"] | org.axonframework.common.TypeReference$2 | 23.112846134866174 |
| ["Type","Java","Class"] | org.axonframework.common.TypeReference$1 | 23.112846134866174 |
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.messaging.core.Context$ResourceKey | 22.0759814258775 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.Message | 18.661931768508047 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.unitofwork.ProcessingContext | 16.847849876355898 |
| ["Package","Java"] | org.axonframework.common | 11.616163415031838 |
| ["Type","Java","Interface"] | org.axonframework.common.infra.ComponentDescriptor | 11.221498809618774 |
| ["Type","Java","Interface"] | org.axonframework.common.infra.DescribableComponent | 11.121318393371578 |
| ["Type","Java","Interface"] | org.axonframework.conversion.Converter | 10.61064350264295 |

[Full data](./Java_Package/centrality/Package_Centrality_Page_Rank.csv)

### 2.2 Top Nodes by ArticleRank

| nodeLabels | nodeName | articleRankScore |
| --- | --- | --- |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.Message | 8.800980929431146 |
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.messaging.core.Context$ResourceKey | 7.428954365967199 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.unitofwork.ProcessingContext | 7.147402431627966 |
| ["Package","Java"] | org.axonframework.common | 6.048292360657327 |
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.common.TypeReference | 5.974516648629894 |
| ["Type","Java","Interface"] | org.axonframework.conversion.Converter | 4.565699645399374 |
| ["Package","Java"] | org.axonframework.messaging.core | 4.492794267420532 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.Context | 3.2879979381782856 |
| ["Type","Java","GenericDeclaration","Interface"] | org.axonframework.messaging.core.MessageStream | 3.2311646685365227 |
| ["Type","Java","Interface"] | org.axonframework.messaging.eventhandling.EventMessage | 2.788936676329492 |

[Full data](./Java_Package/centrality/Package_Centrality_Article_Rank.csv)

### 2.3 Top Nodes by Betweenness Centrality

| nodeLabels | nodeName | betweennessScore |
| --- | --- | --- |
| ["Type","Java","GenericDeclaration","Interface"] | org.axonframework.messaging.core.MessageStream | 11442.45983853312 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.Message | 9856.609527541425 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.unitofwork.ProcessingContext | 6626.2426108374375 |
| ["Type","Java","Record"] | org.axonframework.messaging.core.QualifiedName | 4588.6106569900685 |
| ["Type","Java","Class"] | org.axonframework.common.ReflectionUtils | 4459.95 |
| ["Type","Java","Record"] | org.axonframework.messaging.core.MessageType | 4158.158174178763 |
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.modelling.entity.annotation.AnnotatedEntityMetamodel | 3528.50101010101 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.unitofwork.ProcessingLifecycle | 2515.47619047619 |
| ["Type","Java","Class"] | org.axonframework.common.TypeReflectionUtils | 2042 |
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.eventsourcing.configuration.SimpleEventSourcedEntityModule | 1930.0353174603174 |

[Full data](./Java_Package/centrality/Package_Centrality_Betweeness.csv)

---

## 3. Community Detection

High community sizes may indicate monolithic modules; many small = well-modularised.

### 3.1 Leiden Communities Overview

| communityId | communitySize |
| --- | --- |
| 1 | 169 |
| 4 | 161 |
| 3 | 126 |
| 2 | 123 |
| 5 | 121 |
| 7 | 86 |
| 15 | 74 |
| 0 | 61 |
| 12 | 60 |
| 6 | 58 |

[Full data](./Java_Package/communities/Package_Communities_Leiden.csv)

### 3.2 Strongly Connected Components (SCC)

Components with more than one member = circular dependencies.

| componentId | componentSize |
| --- | --- |
| 277 | 33 |
| 36 | 20 |
| 161 | 14 |
| 70 | 13 |
| 214 | 12 |
| 167 | 12 |
| 217 | 10 |
| 499 | 9 |
| 194 | 9 |
| 872 | 8 |

[Full data](./Java_Package/communities/Package_Communities_Strongly_Connected_Components.csv)

### 3.3 Weakly Connected Components (WCC)

Weakly connected components identify isolated clusters of code units.

| componentId | componentSize |
| --- | --- |
| 0 | 1296 |
| 1 | 5 |
| 3 | 3 |
| 2 | 2 |

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
| ["Type","Java","Class"] | org.axonframework.conversion.jackson.JsonNodeToObjectNodeConverter | ["Type","Java","Class"] | org.axonframework.conversion.jackson.ByteArrayToJsonNodeConverter | 1 |
| ["Type","Java","Class"] | org.axonframework.conversion.jackson.ByteArrayToJsonNodeConverter | ["Type","Java","Class"] | org.axonframework.conversion.jackson.JsonNodeToObjectNodeConverter | 1 |
| ["Type","Java","Class"] | org.axonframework.conversion.jackson.ObjectNodeToJsonNodeConverter | ["Type","Java","Class"] | org.axonframework.conversion.converter.StringToByteArrayConverter | 1 |
| ["Type","Java","Class"] | org.axonframework.conversion.jackson.ObjectNodeToJsonNodeConverter | ["Type","Java","Class"] | org.axonframework.conversion.converter.ByteArrayToInputStreamConverter | 1 |
| ["Type","Java","Class"] | org.axonframework.conversion.jackson.JsonNodeToObjectNodeConverter | ["Type","Java","Class"] | org.axonframework.conversion.converter.InputStreamToByteArrayConverter | 1 |
| ["Type","Java","Class"] | org.axonframework.conversion.jackson.ByteArrayToJsonNodeConverter | ["Type","Java","Class"] | org.axonframework.conversion.jackson.JsonNodeToByteArrayConverter | 1 |
| ["Type","Java","Class"] | org.axonframework.eventsourcing.eventstore.EventStoreException | ["Type","Java","Class","Throwable"] | org.axonframework.test.matchers.MatcherExecutionException | 1 |
| ["Type","Java","Class"] | org.axonframework.conversion.jackson.JsonNodeToByteArrayConverter | ["Type","Java","Class"] | org.axonframework.conversion.jackson.ByteArrayToJsonNodeConverter | 1 |
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.eventsourcing.eventstore.StreamSpliterator | ["Type","Java","Class"] | org.axonframework.update.common.DelayedTask | 1 |
| ["Type","Java","Class"] | org.axonframework.conversion.jackson.ObjectNodeToJsonNodeConverter | ["Type","Java","Class"] | org.axonframework.conversion.converter.ByteArrayToStringConverter | 1 |

[Full data](./Java_Package/similarity/Package_Similarity.csv)
