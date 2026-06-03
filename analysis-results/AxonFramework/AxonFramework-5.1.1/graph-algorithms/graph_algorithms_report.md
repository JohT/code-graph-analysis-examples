---
title: "Graph Algorithms Report"
generated: "2026-06-03"
model_version: "v4.0.1"
dataset: "AxonFramework-5.1.1"
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
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.common.TypeReference | 53.85181024069588 |
| ["Type","Java","Class"] | org.axonframework.common.TypeReference$2 | 23.035178974074586 |
| ["Type","Java","Class"] | org.axonframework.common.TypeReference$1 | 23.035178974074586 |
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.messaging.core.Context$ResourceKey | 22.397207902024846 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.Message | 18.59835757595238 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.unitofwork.ProcessingContext | 16.88815291462526 |
| ["Package","Java"] | org.axonframework.common | 11.589884268040368 |
| ["Type","Java","Interface"] | org.axonframework.common.infra.ComponentDescriptor | 11.167066256391257 |
| ["Type","Java","Interface"] | org.axonframework.common.infra.DescribableComponent | 11.042516110452677 |
| ["Type","Java","Interface"] | org.axonframework.conversion.Converter | 10.529095461653233 |

[Full data](./Java_Package/centrality/Package_Centrality_Page_Rank.csv)

### 2.2 Top Nodes by ArticleRank

| nodeLabels | nodeName | articleRankScore |
| --- | --- | --- |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.Message | 8.763706821588157 |
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.messaging.core.Context$ResourceKey | 7.660000237075169 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.unitofwork.ProcessingContext | 7.158231123206262 |
| ["Package","Java"] | org.axonframework.common | 6.025806393235335 |
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.common.TypeReference | 5.9377535621985436 |
| ["Type","Java","Interface"] | org.axonframework.conversion.Converter | 4.5306879116318015 |
| ["Package","Java"] | org.axonframework.messaging.core | 4.520227917997469 |
| ["Type","Java","Interface","GenericDeclaration"] | org.axonframework.messaging.core.MessageStream | 3.2305715436278715 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.Context | 3.2264670883334436 |
| ["Type","Java","Interface"] | org.axonframework.messaging.eventhandling.EventMessage | 2.7521053621907936 |

[Full data](./Java_Package/centrality/Package_Centrality_Article_Rank.csv)

### 2.3 Top Nodes by Betweenness Centrality

| nodeLabels | nodeName | betweennessScore |
| --- | --- | --- |
| ["Type","Java","Interface","GenericDeclaration"] | org.axonframework.messaging.core.MessageStream | 11349.729365079374 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.Message | 9817.588167388172 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.unitofwork.ProcessingContext | 6610.471428571433 |
| ["Type","Java","Record"] | org.axonframework.messaging.core.QualifiedName | 4627.043990323405 |
| ["Type","Java","Class"] | org.axonframework.common.ReflectionUtils | 4484.96666666667 |
| ["Type","Java","Record"] | org.axonframework.messaging.core.MessageType | 4151.324840845429 |
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.modelling.entity.annotation.AnnotatedEntityMetamodel | 3527.6537878787876 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.unitofwork.ProcessingLifecycle | 2523.4428571428566 |
| ["Type","Java","Class"] | org.axonframework.common.TypeReflectionUtils | 2051 |
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.eventsourcing.configuration.SimpleEventSourcedEntityModule | 2006.2623015873014 |

[Full data](./Java_Package/centrality/Package_Centrality_Betweeness.csv)

---

## 3. Community Detection

High community sizes may indicate monolithic modules; many small = well-modularised.

### 3.1 Leiden Communities Overview

| communityId | communitySize |
| --- | --- |
| 3 | 183 |
| 5 | 173 |
| 0 | 150 |
| 4 | 120 |
| 7 | 84 |
| 2 | 83 |
| 1 | 81 |
| 11 | 81 |
| 10 | 74 |
| 8 | 72 |

[Full data](./Java_Package/communities/Package_Communities_Leiden.csv)

### 3.2 Strongly Connected Components (SCC)

Components with more than one member = circular dependencies.

| componentId | componentSize |
| --- | --- |
| 6 | 35 |
| 0 | 21 |
| 817 | 14 |
| 759 | 12 |
| 818 | 12 |
| 787 | 12 |
| 788 | 10 |
| 854 | 9 |
| 193 | 9 |
| 657 | 8 |

[Full data](./Java_Package/communities/Package_Communities_Strongly_Connected_Components.csv)

### 3.3 Weakly Connected Components (WCC)

Weakly connected components identify isolated clusters of code units.

| componentId | componentSize |
| --- | --- |
| 0 | 1302 |
| 2 | 5 |
| 3 | 3 |
| 1 | 2 |

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
| ["Type","Java","Interface"] | org.axonframework.messaging.commandhandling.CommandPriorityCalculator | ["Type","Java","Class"] | org.axonframework.modelling.entity.EntityMissingForInstanceCommandHandlerException | 1 |
| ["Type","Java","Interface"] | org.axonframework.messaging.commandhandling.CommandPriorityCalculator | ["Type","Java","Class"] | org.axonframework.modelling.entity.EntityAlreadyExistsForCreationalCommandHandlerException | 1 |
| ["Type","Java","Class"] | org.axonframework.messaging.tracing.NoOpSpanFactory$NoOpSpan | ["Type","Java","Class"] | org.axonframework.extension.tracing.opentelemetry.OpenTelemetrySpan | 1 |
| ["Type","Java","Interface"] | org.axonframework.messaging.eventhandling.EventMessage | ["Type","Java","Interface"] | org.axonframework.messaging.eventhandling.replay.ResetContext | 1 |
| ["Type","Java","Interface"] | org.axonframework.messaging.eventhandling.EventMessage | ["Type","Java","Interface"] | org.axonframework.messaging.commandhandling.CommandMessage | 1 |
| ["Type","Java","Interface"] | org.axonframework.messaging.commandhandling.CommandPriorityCalculator | ["Type","Java","Class"] | org.axonframework.modelling.entity.ChildEntityNotFoundException | 1 |
| ["Type","Java","Class","Throwable"] | org.axonframework.messaging.commandhandling.CommandExecutionException | ["Type","Java","Class"] | org.axonframework.messaging.queryhandling.QueryExecutionException | 1 |
| ["Type","Java","Interface"] | org.axonframework.messaging.commandhandling.CommandMessage | ["Type","Java","Interface"] | org.axonframework.messaging.eventhandling.replay.ResetContext | 1 |
| ["Type","Java","Interface"] | org.axonframework.messaging.eventhandling.EventMessage | ["Type","Java","Interface"] | org.axonframework.messaging.core.ResultMessage | 1 |
| ["Type","Java","Interface"] | org.axonframework.messaging.commandhandling.CommandMessage | ["Type","Java","Interface"] | org.axonframework.messaging.eventhandling.EventMessage | 1 |

[Full data](./Java_Package/similarity/Package_Similarity.csv)
