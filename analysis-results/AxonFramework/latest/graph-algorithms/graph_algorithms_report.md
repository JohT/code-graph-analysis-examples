---
title: "Graph Algorithms Report"
generated: "2026-07-13"
model_version: "v4.0.1"
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
| ["Type","Java","Class"] | org.axonframework.common.TypeReference$2 | 23.05091489516343 |
| ["Type","Java","Class"] | org.axonframework.common.TypeReference$1 | 23.05091489516343 |
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.messaging.core.Context$ResourceKey | 22.41577975959274 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.Message | 18.58762244866973 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.unitofwork.ProcessingContext | 16.88448461381728 |
| ["Package","Java"] | org.axonframework.common | 11.60540778191177 |
| ["Type","Java","Interface"] | org.axonframework.common.infra.ComponentDescriptor | 11.16546427557327 |
| ["Type","Java","Interface"] | org.axonframework.common.infra.DescribableComponent | 11.040244162776041 |
| ["Type","Java","Interface"] | org.axonframework.conversion.Converter | 10.524578358009308 |

[Full data](./Java_Package/centrality/Package_Centrality_Page_Rank.csv)

### 2.2 Top Nodes by ArticleRank

| nodeLabels | nodeName | articleRankScore |
| --- | --- | --- |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.Message | 8.761437539518028 |
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.messaging.core.Context$ResourceKey | 7.664558490342938 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.unitofwork.ProcessingContext | 7.158462095853332 |
| ["Package","Java"] | org.axonframework.common | 6.034603518270907 |
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.common.TypeReference | 5.9386639048500305 |
| ["Type","Java","Interface"] | org.axonframework.conversion.Converter | 4.531077454325549 |
| ["Package","Java"] | org.axonframework.messaging.core | 4.520396567052293 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.Context | 3.2271814483597234 |
| ["Type","Java","Interface","GenericDeclaration"] | org.axonframework.messaging.core.MessageStream | 3.224865458930251 |
| ["Type","Java","Interface"] | org.axonframework.messaging.eventhandling.EventMessage | 2.751749105103321 |

[Full data](./Java_Package/centrality/Package_Centrality_Article_Rank.csv)

### 2.3 Top Nodes by Betweenness Centrality

| nodeLabels | nodeName | betweennessScore |
| --- | --- | --- |
| ["Type","Java","Interface","GenericDeclaration"] | org.axonframework.messaging.core.MessageStream | 11352.071356421364 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.Message | 9809.049206349211 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.unitofwork.ProcessingContext | 6610.471428571431 |
| ["Type","Java","Record"] | org.axonframework.messaging.core.QualifiedName | 4625.822222222223 |
| ["Type","Java","Class"] | org.axonframework.common.ReflectionUtils | 4488.466666666667 |
| ["Type","Java","Record"] | org.axonframework.messaging.core.MessageType | 4159.611111111112 |
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.modelling.entity.annotation.AnnotatedEntityMetamodel | 3527.9704545454542 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.unitofwork.ProcessingLifecycle | 2523.4428571428566 |
| ["Type","Java","Class"] | org.axonframework.common.TypeReflectionUtils | 2054 |
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.eventsourcing.configuration.SimpleEventSourcedEntityModule | 2006.2623015873016 |

[Full data](./Java_Package/centrality/Package_Centrality_Betweeness.csv)

---

## 3. Community Detection

High community sizes may indicate monolithic modules; many small = well-modularised.

### 3.1 Leiden Communities Overview

| communityId | communitySize |
| --- | --- |
| 8 | 193 |
| 1 | 189 |
| 2 | 123 |
| 12 | 113 |
| 6 | 111 |
| 7 | 110 |
| 9 | 95 |
| 3 | 82 |
| 0 | 80 |
| 15 | 65 |

[Full data](./Java_Package/communities/Package_Communities_Leiden.csv)

### 3.2 Strongly Connected Components (SCC)

Components with more than one member = circular dependencies.

| componentId | componentSize |
| --- | --- |
| 411 | 33 |
| 54 | 20 |
| 195 | 14 |
| 853 | 12 |
| 202 | 12 |
| 131 | 12 |
| 856 | 10 |
| 10 | 9 |
| 607 | 9 |
| 232 | 9 |

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
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.eventsourcing.eventstore.StreamSpliterator | ["Type","Java","Class"] | org.axonframework.update.detection.KotlinVersion | 1 |
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.eventsourcing.eventstore.StreamSpliterator | ["Type","Java","Class"] | org.axonframework.update.detection.MachineId | 1 |
| ["Type","Java","Record"] | org.axonframework.eventsourcing.eventstore.jpa.AggregateBasedJpaEventStorageEngine$AggregateSource | ["Type","Java","Record"] | io.axoniq.framework.axonserver.connector.event.AggregateBasedAxonServerEventStorageEngine$AggregateSource | 1 |
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.eventsourcing.eventstore.StreamSpliterator | ["Type","Java","Class"] | org.axonframework.update.common.DelayedTask | 1 |
| ["Type","Java","Record"] | org.axonframework.eventsourcing.snapshot.api.Snapshot | ["Type","Java","Class"] | org.axonframework.eventsourcing.eventstore.StartPosition | 1 |
| ["Type","Java","Class"] | org.axonframework.eventsourcing.eventstore.EventStoreException | ["Type","Java","Class","Throwable"] | org.axonframework.common.infra.ComponentDescriptorException | 1 |
| ["Type","Java","Class"] | org.axonframework.eventsourcing.eventstore.GlobalIndexPosition | ["Type","Java","Class"] | org.axonframework.eventsourcing.eventstore.AggregateSequenceNumberPosition | 1 |
| ["Type","Java","Class"] | io.axoniq.framework.axonserver.connector.api.query.AxonServerQueryDispatchException | ["Type","Java","Class","Throwable"] | org.axonframework.messaging.eventhandling.processing.EventProcessingException | 1 |
| ["Type","Java","Class"] | org.axonframework.eventsourcing.eventstore.AggregateSequenceNumberPosition | ["Type","Java","Class"] | org.axonframework.eventsourcing.eventstore.GlobalIndexPosition | 1 |
| ["Type","Java","Class"] | org.axonframework.eventsourcing.eventstore.StartPosition | ["Type","Java","Record"] | org.axonframework.eventsourcing.snapshot.api.Snapshot | 1 |

[Full data](./Java_Package/similarity/Package_Similarity.csv)
