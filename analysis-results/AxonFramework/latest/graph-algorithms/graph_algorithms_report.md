---
title: "Graph Algorithms Report"
generated: "2026-09-01"
model_version: "v4.0.2"
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
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.common.TypeReference | 53.88884355019087 |
| ["Type","Java","Class"] | org.axonframework.common.TypeReference$2 | 23.050914895163437 |
| ["Type","Java","Class"] | org.axonframework.common.TypeReference$1 | 23.050914895163437 |
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.messaging.core.Context$ResourceKey | 22.415779759592734 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.Message | 18.587622448669745 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.unitofwork.ProcessingContext | 16.88448461381727 |
| ["Package","Java"] | org.axonframework.common | 11.605407781911776 |
| ["Type","Java","Interface"] | org.axonframework.common.infra.ComponentDescriptor | 11.165464275573271 |
| ["Type","Java","Interface"] | org.axonframework.common.infra.DescribableComponent | 11.040244162776043 |
| ["Type","Java","Interface"] | org.axonframework.conversion.Converter | 10.524578358009311 |

[Full data](./Java_Package/centrality/Package_Centrality_Page_Rank.csv)

### 2.2 Top Nodes by ArticleRank

| nodeLabels | nodeName | articleRankScore |
| --- | --- | --- |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.Message | 8.76143753951803 |
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.messaging.core.Context$ResourceKey | 7.6645584903429365 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.unitofwork.ProcessingContext | 7.158462095853328 |
| ["Package","Java"] | org.axonframework.common | 6.034603518270907 |
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.common.TypeReference | 5.9386639048500305 |
| ["Type","Java","Interface"] | org.axonframework.conversion.Converter | 4.5310774543255485 |
| ["Package","Java"] | org.axonframework.messaging.core | 4.520396567052293 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.Context | 3.2271814483597234 |
| ["Type","Java","GenericDeclaration","Interface"] | org.axonframework.messaging.core.MessageStream | 3.2248654589302523 |
| ["Type","Java","Interface"] | org.axonframework.messaging.eventhandling.EventMessage | 2.7517491051033205 |

[Full data](./Java_Package/centrality/Package_Centrality_Article_Rank.csv)

### 2.3 Top Nodes by Betweenness Centrality

| nodeLabels | nodeName | betweennessScore |
| --- | --- | --- |
| ["Type","Java","GenericDeclaration","Interface"] | org.axonframework.messaging.core.MessageStream | 11352.07135642136 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.Message | 9809.049206349211 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.unitofwork.ProcessingContext | 6610.471428571429 |
| ["Type","Java","Record"] | org.axonframework.messaging.core.QualifiedName | 4625.822222222221 |
| ["Type","Java","Class"] | org.axonframework.common.ReflectionUtils | 4488.466666666667 |
| ["Type","Java","Record"] | org.axonframework.messaging.core.MessageType | 4159.6111111111095 |
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.modelling.entity.annotation.AnnotatedEntityMetamodel | 3527.9704545454547 |
| ["Type","Java","Interface"] | org.axonframework.messaging.core.unitofwork.ProcessingLifecycle | 2523.442857142857 |
| ["Type","Java","Class"] | org.axonframework.common.TypeReflectionUtils | 2054 |
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.eventsourcing.configuration.SimpleEventSourcedEntityModule | 2006.2623015873016 |

[Full data](./Java_Package/centrality/Package_Centrality_Betweeness.csv)

---

## 3. Community Detection

High community sizes may indicate monolithic modules; many small = well-modularised.

### 3.1 Leiden Communities Overview

| communityId | communitySize |
| --- | --- |
| 1 | 193 |
| 4 | 186 |
| 0 | 135 |
| 2 | 114 |
| 6 | 103 |
| 11 | 95 |
| 5 | 64 |
| 9 | 64 |
| 10 | 61 |
| 3 | 60 |

[Full data](./Java_Package/communities/Package_Communities_Leiden.csv)

### 3.2 Strongly Connected Components (SCC)

Components with more than one member = circular dependencies.

| componentId | componentSize |
| --- | --- |
| 116 | 33 |
| 11 | 31 |
| 16 | 15 |
| 61 | 13 |
| 845 | 12 |
| 77 | 11 |
| 56 | 11 |
| 46 | 10 |
| 306 | 9 |
| 705 | 8 |

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
| ["Type","Java","Class"] | org.axonframework.modelling.entity.WrongPolymorphicEntityTypeException | ["Type","Java","Class"] | org.axonframework.modelling.entity.EntityMissingForInstanceCommandHandlerException | 1 |
| ["Type","Java","Class","Throwable"] | org.axonframework.test.FixtureExecutionException | ["Type","Java","Class","Throwable"] | org.axonframework.test.matchers.MatcherExecutionException | 1 |
| ["Type","Java","GenericDeclaration","Interface"] | org.axonframework.modelling.repository.SimpleRepositoryEntityLoader | ["Type","Java","GenericDeclaration","Interface"] | org.axonframework.modelling.repository.SimpleRepositoryEntityPersister | 1 |
| ["Type","Java","Class"] | org.axonframework.modelling.entity.EntityAlreadyExistsForCreationalCommandHandlerException | ["Type","Java","Class"] | org.axonframework.modelling.entity.ChildEntityNotFoundException | 1 |
| ["Type","Java","GenericDeclaration","Interface"] | org.axonframework.modelling.configuration.EntityModule | ["Type","Java","GenericDeclaration","Interface"] | org.axonframework.common.configuration.ModuleBuilder | 1 |
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.modelling.repository.SimpleRepository$SimpleEntity | ["Type","Java","Class","GenericDeclaration"] | org.axonframework.eventsourcing.EventSourcingRepository$EventSourcedEntity | 1 |
| ["Type","Java","Class"] | org.axonframework.modelling.entity.EntityAlreadyExistsForCreationalCommandHandlerException | ["Type","Java","Class"] | org.axonframework.modelling.entity.EntityMissingForInstanceCommandHandlerException | 1 |
| ["Type","Java","Class"] | org.axonframework.modelling.entity.EntityMissingForInstanceCommandHandlerException | ["Type","Java","Class"] | org.axonframework.modelling.entity.WrongPolymorphicEntityTypeException | 1 |
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.modelling.entity.child.GetterEvolverChildEntityFieldDefinition | ["Type","Java","Class","GenericDeclaration"] | org.axonframework.modelling.entity.child.GetterSetterChildEntityFieldDefinition | 1 |
| ["Type","Java","Class","GenericDeclaration"] | org.axonframework.modelling.entity.child.GetterSetterChildEntityFieldDefinition | ["Type","Java","Class","GenericDeclaration"] | org.axonframework.modelling.entity.child.GetterEvolverChildEntityFieldDefinition | 1 |

[Full data](./Java_Package/similarity/Package_Similarity.csv)
