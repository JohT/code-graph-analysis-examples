---
title: "Node Embeddings Report"
generated: "2026-06-08"
model_version: "v4.0.1"
dataset: "AxonFramework-5.1.1"
authors: ["JohT/code-graph-analysis-pipeline"]
---

# 🧬 Node Embeddings Report

## 1. Overview

This report summarises node embedding vectors computed from the code dependency graph via the Neo4j Graph Data Science Library.

Node embeddings approximate the structural position of each code unit (package, type, artifact, module) in the graph as a fixed-length vector of floating-point numbers. The embeddings are computed using:

- **FastRP** (Fast Random Projection) — efficient approximate embedding based on random projections
- **HashGNN** (Hash Graph Neural Networks) — lightweight GNN-inspired embedding
- **Node2Vec** — random-walk-based embedding that captures local neighbourhood structure

The UMAP scatter plots visualise the embeddings projected to 2D. Points are coloured by Leiden community (when available) to show how well the embeddings capture community structure.

## 📚 Table of Contents

1. [Overview](#1-overview)
1. [Embedding Properties](#2-embedding-properties)
1. [Embeddings with Community and Centrality](#3-embeddings-with-community-and-centrality)
1. [Package Embedding Charts](#4-package-embedding-charts)
1. [Artifact Embedding Charts](#5-artifact-embedding-charts)
1. [Type Embedding Charts](#6-type-embedding-charts)
1. [Module Embedding Charts](#7-module-embedding-charts)

---

## 2. Embedding Properties

Shows which embedding properties exist and on how many nodes per label.

| nodeLabels | nodeCount | fastRandomProjectionCount | hashGNNCount | node2VecCount | fastRandomProjectionDimensions | hashGNNDimensions | node2VecDimensions |
| --- | --- | --- | --- | --- | --- | --- | --- |
| ["Type","Java","Class","InternalJavaType","ConnectedInternalJavaType"] | 622 | 622 | 622 | 622 | 64 | 128 | 64 |
| ["Type","Java","Interface","InternalJavaType","ConnectedInternalJavaType"] | 177 | 177 | 177 | 177 | 64 | 128 | 64 |
| ["Type","Java","Class","GenericDeclaration","InternalJavaType","ConnectedInternalJavaType"] | 129 | 129 | 129 | 129 | 64 | 128 | 64 |
| ["Package","Java"] | 124 | 124 | 124 | 124 | 32 | 64 | 32 |
| ["Type","Java","Interface","GenericDeclaration","InternalJavaType","ConnectedInternalJavaType"] | 86 | 86 | 86 | 86 | 64 | 128 | 64 |
| ["Type","Java","Record","InternalJavaType","ConnectedInternalJavaType"] | 54 | 54 | 54 | 54 | 64 | 128 | 64 |
| ["Type","Java","Class","Throwable","InternalJavaType","ConnectedInternalJavaType"] | 43 | 43 | 43 | 43 | 64 | 128 | 64 |
| ["Type","Java","Annotation","InternalJavaType","ConnectedInternalJavaType"] | 42 | 42 | 42 | 42 | 64 | 128 | 64 |
| ["Type","Java","Enum","InternalJavaType","ConnectedInternalJavaType"] | 16 | 16 | 16 | 16 | 64 | 128 | 64 |
| ["Artifact","Jar","Archive","Zip","Java"] | 11 | 11 | 11 | 11 | 16 | 32 | 16 |

[Full data](./Package_Embeddings_Label_Random_Projection.csv)

---

## 3. Embeddings with Community and Centrality

Sample of nodes showing FastRP embedding dimension count alongside Leiden community id and PageRank centrality.
Useful to verify that the embedding pipeline ran end-to-end and that the properties are co-located on the same nodes.

| nodeLabels | nodeName | embeddingDimensions | communityLeidenId | pageRankScore |
| --- | --- | --- | --- | --- |
| ["Type","Java","Class","GenericDeclaration","InternalJavaType","ConnectedInternalJavaType"] | org.axonframework.common.TypeReference | 64 | 4 | 53.851810240695904 |
| ["Type","Java","Class","InternalJavaType","ConnectedInternalJavaType"] | org.axonframework.common.TypeReference$1 | 64 | 4 | 23.035178974074597 |
| ["Type","Java","Class","InternalJavaType","ConnectedInternalJavaType"] | org.axonframework.common.TypeReference$2 | 64 | 4 | 23.035178974074597 |
| ["Type","Java","Class","GenericDeclaration","InternalJavaType","ConnectedInternalJavaType"] | org.axonframework.messaging.core.Context$ResourceKey | 64 | 5 | 22.397207902024842 |
| ["Type","Java","Interface","InternalJavaType","ConnectedInternalJavaType"] | org.axonframework.messaging.core.Message | 64 | 3 | 18.598357575952384 |
| ["Type","Java","Interface","InternalJavaType","ConnectedInternalJavaType"] | org.axonframework.messaging.core.unitofwork.ProcessingContext | 64 | 5 | 16.888152914625255 |
| ["Package","Java"] | org.axonframework.common | 32 | 2 | 11.589884268040368 |
| ["Type","Java","Interface","InternalJavaType","ConnectedInternalJavaType"] | org.axonframework.common.infra.ComponentDescriptor | 64 | 0 | 11.167066256391257 |
| ["Type","Java","Interface","InternalJavaType","ConnectedInternalJavaType"] | org.axonframework.common.infra.DescribableComponent | 64 | 19 | 11.04251611045268 |
| ["Type","Java","Interface","InternalJavaType","ConnectedInternalJavaType"] | org.axonframework.conversion.Converter | 64 | 3 | 10.529095461653235 |

---

## 4. Package Embedding Charts

UMAP 2D projections of Package node embeddings. Each algorithm produces one scatter plot.


![Package_Embeddings_FastRP_UMAP2D_Scatter](./Package_Embeddings_FastRP_UMAP2D_Scatter.svg)

![Package_Embeddings_HashGNN_UMAP2D_Scatter](./Package_Embeddings_HashGNN_UMAP2D_Scatter.svg)

![Package_Embeddings_Node2Vec_UMAP2D_Scatter](./Package_Embeddings_Node2Vec_UMAP2D_Scatter.svg)

---

## 5. Artifact Embedding Charts

UMAP 2D projections of Artifact node embeddings. Each algorithm produces one scatter plot.


![Artifact_Embeddings_FastRP_UMAP2D_Scatter](./Artifact_Embeddings_FastRP_UMAP2D_Scatter.svg)

![Artifact_Embeddings_HashGNN_UMAP2D_Scatter](./Artifact_Embeddings_HashGNN_UMAP2D_Scatter.svg)

![Artifact_Embeddings_Node2Vec_UMAP2D_Scatter](./Artifact_Embeddings_Node2Vec_UMAP2D_Scatter.svg)

---

## 6. Type Embedding Charts

UMAP 2D projections of Java Type node embeddings. Each algorithm produces one scatter plot.


![Type_Embeddings_FastRP_UMAP2D_Scatter](./Type_Embeddings_FastRP_UMAP2D_Scatter.svg)

![Type_Embeddings_HashGNN_UMAP2D_Scatter](./Type_Embeddings_HashGNN_UMAP2D_Scatter.svg)

![Type_Embeddings_Node2Vec_UMAP2D_Scatter](./Type_Embeddings_Node2Vec_UMAP2D_Scatter.svg)

---

## 7. Module Embedding Charts

UMAP 2D projections of TypeScript Module node embeddings. Each algorithm produces one scatter plot.


