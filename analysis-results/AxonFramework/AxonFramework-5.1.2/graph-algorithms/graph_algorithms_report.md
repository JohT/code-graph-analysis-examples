---
title: "Graph Algorithms Report"
generated: "2026-11-02"
model_version: "v5.0.0"
dataset: "AxonFramework-5.1.2"
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
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.common.TypeReference | 53.88884355019086 |
| ["Type","Java","Class"] | org.axonframework.common.TypeReference$1 | 23.050914895163434 |
| ["Type","Java","Class"] | org.axonframework.common.TypeReference$2 | 23.050914895163434 |
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.messaging.core.Context$ResourceKey | 22.41577975959273 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.Message | 18.587622448669748 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.unitofwork.ProcessingContext | 16.884484613817275 |
| ["Package","Java"] | org.axonframework.common | 11.605407781911774 |
| ["Type","Java","Interface"] | org.axonframework.common.infra.ComponentDescriptor | 11.165464275573273 |
| ["Type","Java","Interface"] | org.axonframework.common.infra.DescribableComponent | 11.040244162776045 |
| ["Type","Java","Interface"] | org.axonframework.conversion.Converter | 10.524578358009313 |

[Full data](./Java_Package/centrality/Package_Centrality_Page_Rank.csv)

### 2.2 Top Nodes by ArticleRank

| nodeLabels | nodeName | articleRankScore |
| --- | --- | --- |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.Message | 8.761437539518028 |
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.messaging.core.Context$ResourceKey | 7.664558490342937 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.unitofwork.ProcessingContext | 7.15846209585333 |
| ["Package","Java"] | org.axonframework.common | 6.034603518270909 |
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.common.TypeReference | 5.938663904850031 |
| ["Type","Java","Interface"] | org.axonframework.conversion.Converter | 4.5310774543255485 |
| ["Package","Java"] | org.axonframework.messaging.core | 4.520396567052293 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.Context | 3.227181448359723 |
| ["Type","Java","Interface","GenericDeclaration"] | org.axonframework.messaging.core.MessageStream | 3.224865458930252 |
| ["Type","Java","Interface"] | org.axonframework.messaging.eventhandling.EventMessage | 2.75174910510332 |

[Full data](./Java_Package/centrality/Package_Centrality_Article_Rank.csv)

### 2.3 Top Nodes by Betweenness Centrality

| nodeLabels | nodeName | betweennessScore |
| --- | --- | --- |
| ["Type","Java","Interface","GenericDeclaration"] | org.axonframework.messaging.core.MessageStream | 11352.071356421367 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.Message | 9809.04920634921 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.unitofwork.ProcessingContext | 6610.471428571431 |
| ["Type","Java","Record"] | org.axonframework.messaging.core.QualifiedName | 4625.82222222222 |
| ["Type","Java","Class"] | org.axonframework.common.ReflectionUtils | 4488.466666666665 |
| ["Type","Java","Record"] | org.axonframework.messaging.core.MessageType | 4159.611111111112 |
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.modelling.entity.annotation.AnnotatedEntityMetamodel | 3527.9704545454547 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.unitofwork.ProcessingLifecycle | 2523.442857142858 |
| ["Type","Java","Class"] | org.axonframework.common.TypeReflectionUtils | 2054 |
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.eventsourcing.configuration.SimpleEventSourcedEntityModule | 2006.2623015873016 |

[Full data](./Java_Package/centrality/Package_Centrality_Betweeness.csv)

---

## 3. Community Detection

High community sizes may indicate monolithic modules; many small = well-modularised.

### 3.1 Leiden Communities Overview

| communityId | communitySize |
| --- | --- |
| 1 | 222 |
| 0 | 191 |
| 4 | 116 |
| 10 | 109 |
| 12 | 102 |
| 11 | 94 |
| 7 | 87 |
| 13 | 77 |
| 14 | 68 |
| 2 | 64 |

[Full data](./Java_Package/communities/Package_Communities_Leiden.csv)

### 3.2 Strongly Connected Components (SCC)

Components with more than one member = circular dependencies.

| componentId | componentSize |
| --- | --- |
| 108 | 33 |
| 21 | 20 |
| 639 | 14 |
| 634 | 12 |
| 550 | 12 |
| 775 | 12 |
| 553 | 10 |
| 315 | 9 |
| 669 | 9 |
| 73 | 8 |

[Full data](./Java_Package/communities/Package_Communities_Strongly_Connected_Components.csv)

### 3.3 Weakly Connected Components (WCC)

Weakly connected components identify isolated clusters of code units.

| componentId | componentSize |
| --- | --- |
| 0 | 1304 |
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
| ["Type","Java","Class"] | org.axonframework.conversion.jackson.ByteArrayToJsonNodeConverter | ["Type","Java","Class"] | org.axonframework.conversion.jackson.JsonNodeToObjectNodeConverter | 1 |
| ["Type","Java","Class"] | org.axonframework.conversion.jackson.JsonNodeToObjectNodeConverter | ["Type","Java","Class"] | org.axonframework.conversion.converter.InputStreamToByteArrayConverter | 1 |
| ["Type","Java","Class"] | org.axonframework.conversion.jackson.JsonNodeToObjectNodeConverter | ["Type","Java","Class"] | org.axonframework.conversion.jackson.ByteArrayToJsonNodeConverter | 1 |
| ["Type","Java","Class"] | org.axonframework.conversion.jackson.ByteArrayToJsonNodeConverter | ["Type","Java","Class"] | org.axonframework.conversion.jackson.JsonNodeToByteArrayConverter | 1 |
| ["Type","Java","Class"] | org.axonframework.conversion.jackson.ObjectNodeToJsonNodeConverter | ["Type","Java","Class"] | org.axonframework.conversion.converter.ByteArrayToInputStreamConverter | 1 |
| ["Type","Java","Class"] | org.axonframework.conversion.jackson.JsonNodeToObjectNodeConverter | ["Type","Java","Class"] | org.axonframework.conversion.jackson.JsonNodeToByteArrayConverter | 1 |
| ["Type","Java","Class"] | io.axoniq.framework.axonserver.connector.api.command.AxonServerRemoteCommandHandlingException | ["Type","Java","Class"] | io.axoniq.framework.axonserver.connector.api.query.AxonServerRemoteQueryHandlingException | 1 |
| ["Type","Java","Class"] | io.axoniq.framework.axonserver.connector.api.query.AxonServerQueryDispatchException | ["Type","Java","Class","Throwable"] | org.axonframework.messaging.eventhandling.processing.EventProcessingException | 1 |
| ["Type","Java","Class"] | org.axonframework.conversion.jackson.ObjectNodeToJsonNodeConverter | ["Type","Java","Class"] | org.axonframework.conversion.converter.StringToByteArrayConverter | 1 |
| ["Type","Java","Class"] | org.axonframework.conversion.jackson.JsonNodeToByteArrayConverter | ["Type","Java","Class"] | org.axonframework.conversion.jackson.ByteArrayToJsonNodeConverter | 1 |

[Full data](./Java_Package/similarity/Package_Similarity.csv)
