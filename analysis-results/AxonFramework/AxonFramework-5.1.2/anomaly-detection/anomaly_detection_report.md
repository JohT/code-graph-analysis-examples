---
title: "Anomaly Detection Report"
generated: "2026-07-13"
model_version: "v4.0.1"
dataset: "AxonFramework-5.1.2"
authors: ["JohT/code-graph-analysis-pipeline"]
---

# 📊 Anomaly Detection Report

## 1. Executive Overview

This report analyzes structural and dependency anomalies across multiple abstraction levels of the codebase.
The goal is to detect potential **software quality, design, and architecture issues** using graph-based features, anomaly detection (Isolation Forest), and SHAP explainability.

## 📚 Table of Contents

1. [Executive Overview](#1-executive-overview)
1. [Deep Dives by Abstraction Level](#2-deep-dives-by-abstraction-level)
1. [Plot Interpretation Guide](#3-plot-interpretation-guide)
1. [Taxonomy of Anomaly Archetypes](#4-taxonomy-of-anomaly-archetypes)
1. [Recommendations](#5-recommendations)
1. [Appendix](#6-appendix)

---

### 1.1 Anomalies in total

| Analyzed Units | Anomalies | Bridges | Outliers |
| --- | --- | --- | --- |
| 1483 | 65 | 17 | 16 |

### 1.2 Overview of Analyzed Structures

| Abstraction Level | Units | Anomalies | Bridges | Outliers |
| --- | --- | --- | --- | --- |
| Type,Java,Interface | 392 | 34 | 4 | 1 |
| Type,Java,Class | 758 | 17 | 4 | 8 |
| Package,Java | 157 | 7 | 7 | 6 |
| Type,Java,Record | 63 | 3 | 0 | 1 |
| Type,Java,Annotation | 43 | 2 | 1 | 0 |
| Type,Java,Class,Throwable | 43 | 1 | 0 | 0 |
| Type,Java,Enum | 16 | 1 | 1 | 0 |
| Artifact,Jar,Archive,Zip,Java | 11 | 0 | 0 | 0 |

### 1.3 Overview Charts

#### Treemap Charts

![JavaTreemap1AverageAnomalyScorePerDirectory](./JavaTreemap1AverageAnomalyScorePerDirectory.svg)

![JavaTreemap2ArchetypesOverviewPerDirectory](./JavaTreemap2ArchetypesOverviewPerDirectory.svg)

![JavaTreemap3ArchetypeBridgePerDirectory](./JavaTreemap3ArchetypeBridgePerDirectory.svg)

![JavaTreemap4ArchetypeOutlierPerDirectory](./JavaTreemap4ArchetypeOutlierPerDirectory.svg)

---

## 2. Deep Dives by Abstraction Level

Each abstraction level includes anomaly statistics, SHAP feature importance, archetype distribution, and example anomalies.

### 2.1 Java Package

#### Anomaly Results

##### Total anomalies

| Anomalies | Bridges | Outliers | CodeUnits | Dependencies | GraphDensity |
| --- | --- | --- | --- | --- | --- |
| 7 | 7 | 6 | 124 | 1554 | 0.101888 |

##### Top global contributing features (via SHAP)

| Feature | Mean absolute SHAP value |
| --- | --- |
| *Node embeddings aggregated* | 0.025710 |
| pageToArticleRankDifference | 0.022885 |
| pageRank | 0.013438 |
| incomingDependencies | 0.011982 |
| degree | 0.011755 |
| articleRank | 0.011166 |
| localClusteringCoefficient | 0.009065 |
| topologicalComponentLayer | 0.006156 |
| nodeEmbeddingPCA_9 | 0.004086 |
| clusterApproximateOutlierScore | 0.002404 |
| nodeEmbeddingPCA_4 | 0.002388 |

#### Archetype Distribution

| Archetype | Count | Max. Score | Model Status | Examples |
| --- | --- | --- | --- | --- |
| Bridge | 7 | 0.026 | Anomalous | org.axonframework.common.annotation, org.axonframework.common.configuration, org.axonframework.messaging.core |
| Outlier | 2 | 0.026 | Anomalous | org.axonframework.common.annotation, org.axonframework.conversion |
| Outlier | 4 | -0.0266 | Typical | org.axonframework.eventsourcing.snapshot.api, org.axonframework.modelling.configuration, org.axonframework.messaging.eventhandling.processing.subscribing |

#### Top anomalies with their local contributing features (via SHAP)

| Name | Contained in | Anomaly Score | Archetypes | Top Feature 1 | Top Feature 1 SHAP | Top Feature 2 | Top Feature 2 SHAP | Top Feature 3 | Top Feature 3 SHAP | Model Status |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| org.axonframework.common.annotation | axon-common-5.1.2 | 0.026 | Outlier, Bridge | pageToArticleRankDifference | -0.194 | pageRank | -0.1228 | degree | -0.1158 | Anomalous |
| org.axonframework.common.configuration | axon-common-5.1.2 | 0.0248 | Bridge, Outlier | pageToArticleRankDifference | -0.1952 | pageRank | -0.1234 | degree | -0.1223 | Anomalous |
| org.axonframework.messaging.core | axon-messaging-5.1.2 | 0.018 | Bridge, Outlier | pageToArticleRankDifference | -0.195 | incomingDependencies | -0.1329 | degree | -0.1277 | Anomalous |
| org.axonframework.messaging.core.unitofwork | axon-messaging-5.1.2 | 0.0056 | Bridge, Outlier | pageToArticleRankDifference | -0.1881 | incomingDependencies | -0.1326 | degree | -0.1295 | Anomalous |
| org.axonframework.conversion | axon-conversion-5.1.2 | 0.004 | Outlier, Bridge | pageToArticleRankDifference | -0.1952 | pageRank | -0.1175 | articleRank | -0.0975 | Anomalous |
| org.axonframework.messaging.eventhandling | axon-messaging-5.1.2 | 0.0017 | Bridge, Outlier | pageToArticleRankDifference | -0.1645 | degree | -0.1306 | incomingDependencies | -0.1252 | Anomalous |
| org.axonframework.common.io | axon-common-5.1.2 | 0.0001 | Bridge, Outlier | pageToArticleRankDifference | -0.1474 | topologicalComponentLayer | -0.0602 | nodeEmbeddingPCA_3 | -0.0552 | Anomalous |

#### Visualizations

##### Anomalies

![Anomalies](./Java_Package/Anomalies.svg)

##### Global feature importance SHAP summary plots

![Anomaly feature importance explained (global)](./Java_Package/Anomaly_feature_importance_explained.svg)

##### Feature dependence plots for top important features

![Anomaly feature dependence explained (global)](./Java_Package/Anomaly_feature_dependence_explained.svg)

---

##### Local SHAP Force Plots – Top 6 Anomalies

![Top 1 anomaly - local feature importance](./Java_Package/Anomaly_1_shap_explanation.svg)
![Top 2 anomaly - local feature importance](./Java_Package/Anomaly_2_shap_explanation.svg)
![Top 3 anomaly - local feature importance](./Java_Package/Anomaly_3_shap_explanation.svg)
![Top 4 anomaly - local feature importance](./Java_Package/Anomaly_4_shap_explanation.svg)
![Top 5 anomaly - local feature importance](./Java_Package/Anomaly_5_shap_explanation.svg)
![Top 6 anomaly - local feature importance](./Java_Package/Anomaly_6_shap_explanation.svg)

---

##### Cluster Diagnostics

![Cluster Overall](./Java_Package/Clusters_Overall.svg)

---



##### Cluster Membership Strength

![Cluster probabilities](./Java_Package/Cluster_probabilities.svg)

---

##### Cluster Noise and Bridge Analysis

![Cluster Noise: Highly central and popular](./Java_Package/ClusterNoise_highly_central_and_popular.svg)
![Cluster Noise: Poorly integrated bridges](./Java_Package/ClusterNoise_poorly_integrated_bridges.svg)
![Cluster Noise: Role inverted bridges](./Java_Package/ClusterNoise_role_inverted_bridges.svg)

---

##### Feature Distributions

![Betweenness Centrality Distribution](./Java_Package/BetweennessCentrality_distribution.svg)
![Clustering coefficient distribution](./Java_Package/ClusteringCoefficient_distribution.svg)
![PageRank minus ArticleRank distribution](./Java_Package/PageRank_Minus_ArticleRank_Distribution.svg)

---

##### Feature Relationships

![Clustering coefficient versus PageRank](./Java_Package/ClusteringCoefficient_versus_PageRank.svg)

---

#### Graph Visualizations

##### TopBridge Graph Visualizations

![TopBridge 1](./Java_Package/GraphVisualizations/TopBridge1.svg)

![TopBridge 2](./Java_Package/GraphVisualizations/TopBridge2.svg)

![TopBridge 3](./Java_Package/GraphVisualizations/TopBridge3.svg)

![TopBridge 4](./Java_Package/GraphVisualizations/TopBridge4.svg)

![TopBridge 5](./Java_Package/GraphVisualizations/TopBridge5.svg)

---

##### TopOutlier Graph Visualizations

![TopOutlier 1](./Java_Package/GraphVisualizations/TopOutlier1.svg)

![TopOutlier 2](./Java_Package/GraphVisualizations/TopOutlier2.svg)

![TopOutlier 3](./Java_Package/GraphVisualizations/TopOutlier3.svg)

![TopOutlier 4](./Java_Package/GraphVisualizations/TopOutlier4.svg)

![TopOutlier 5](./Java_Package/GraphVisualizations/TopOutlier5.svg)

--

### 2.2 Java Type

#### Anomaly Results

##### Total anomalies

| Anomalies | Bridges | Outliers | CodeUnits | Dependencies | GraphDensity |
| --- | --- | --- | --- | --- | --- |
| 58 | 10 | 10 | 1179 | 11380 | 0.008194 |

##### Top global contributing features (via SHAP)

| Feature | Mean absolute SHAP value |
| --- | --- |
| *Node embeddings aggregated* | 0.023957 |
| articleRank | 0.018109 |
| pageRank | 0.017536 |
| pageToArticleRankDifference | 0.013013 |
| incomingDependencies | 0.010022 |
| topologicalComponentLayer | 0.008593 |
| degree | 0.007238 |
| betweenness | 0.003859 |
| localClusteringCoefficient | 0.002768 |
| nodeEmbeddingPCA_31 | 0.002374 |
| abstractness | 0.001484 |

#### Archetype Distribution

| Archetype | Count | Max. Score | Model Status | Examples |
| --- | --- | --- | --- | --- |
| Bridge | 10 | 0.0184 | Anomalous | org.axonframework.eventsourcing.eventstore.StartPosition, org.axonframework.eventsourcing.eventstore.SourcingStrategy, org.axonframework.messaging.monitoring.MessageMonitor$MonitorCallback |
| Outlier | 1 | 0.0511 | Anomalous | org.axonframework.common.Assert |
| Outlier | 9 | -0.0224 | Typical | org.axonframework.eventsourcing.eventstore.DefaultSourcingCondition, org.axonframework.common.caching.EhCacheAdapter$1, org.axonframework.common.configuration.ComponentDecorator |

#### Top anomalies with their local contributing features (via SHAP)

| Name | Contained in | Anomaly Score | Archetypes | Top Feature 1 | Top Feature 1 SHAP | Top Feature 2 | Top Feature 2 SHAP | Top Feature 3 | Top Feature 3 SHAP | Model Status |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| org.axonframework.common.TypeReference | axon-common-5.1.2 | 0.0983 | Bridge, Outlier | pageRank | -0.1988 | articleRank | -0.1962 | pageToArticleRankDifference | -0.1628 | Anomalous |
| org.axonframework.messaging.core.Message | axon-messaging-5.1.2 | 0.0951 | Bridge, Outlier | pageRank | -0.1968 | articleRank | -0.1787 | pageToArticleRankDifference | -0.1483 | Anomalous |
| org.axonframework.messaging.core.unitofwork.ProcessingContext | axon-messaging-5.1.2 | 0.079 | Bridge, Outlier | pageRank | -0.1914 | articleRank | -0.1808 | pageToArticleRankDifference | -0.1486 | Anomalous |
| org.axonframework.messaging.core.MessageStream | axon-messaging-5.1.2 | 0.0746 | Bridge, Outlier | articleRank | -0.2105 | pageRank | -0.1987 | incomingDependencies | -0.1417 | Anomalous |
| org.axonframework.messaging.core.QualifiedName | axon-messaging-5.1.2 | 0.0724 | Bridge, Outlier | articleRank | -0.1906 | pageRank | -0.1678 | incomingDependencies | -0.1229 | Anomalous |
| org.axonframework.common.infra.DescribableComponent | axon-common-5.1.2 | 0.0719 | Bridge, Outlier | pageRank | -0.2021 | articleRank | -0.1905 | pageToArticleRankDifference | -0.1614 | Anomalous |
| org.axonframework.messaging.eventstreaming.EventCriteria | axon-messaging-5.1.2 | 0.0711 | Bridge, Outlier | articleRank | -0.2125 | pageRank | -0.1656 | incomingDependencies | -0.122 | Anomalous |
| org.axonframework.common.annotation.Internal | axon-common-5.1.2 | 0.0711 | Bridge, Outlier | pageRank | -0.2038 | articleRank | -0.1905 | pageToArticleRankDifference | -0.164 | Anomalous |
| org.axonframework.messaging.core.Metadata | axon-messaging-5.1.2 | 0.0681 | Bridge, Outlier | pageRank | -0.2123 | articleRank | -0.1917 | pageToArticleRankDifference | -0.1685 | Anomalous |
| org.axonframework.conversion.Converter | axon-conversion-5.1.2 | 0.0675 | Bridge, Outlier | pageRank | -0.2096 | articleRank | -0.1959 | pageToArticleRankDifference | -0.1586 | Anomalous |
| org.axonframework.messaging.core.Context$ResourceKey | axon-messaging-5.1.2 | 0.0591 | Bridge, Outlier | pageRank | -0.203 | articleRank | -0.1977 | pageToArticleRankDifference | -0.1561 | Anomalous |
| org.axonframework.messaging.eventhandling.EventMessage | axon-messaging-5.1.2 | 0.0585 | Bridge, Outlier | pageRank | -0.2067 | articleRank | -0.2024 | incomingDependencies | -0.1458 | Anomalous |
| org.axonframework.common.infra.ComponentDescriptor | axon-common-5.1.2 | 0.0514 | Bridge, Outlier | pageRank | -0.2066 | articleRank | -0.1914 | pageToArticleRankDifference | -0.1605 | Anomalous |
| org.axonframework.common.Assert | axon-common-5.1.2 | 0.0511 | Outlier, Bridge | articleRank | -0.2212 | pageRank | -0.1967 | topologicalComponentLayer | -0.1327 | Anomalous |
| org.axonframework.messaging.eventhandling.processing.streaming.token.TrackingToken | axon-messaging-5.1.2 | 0.0505 | Bridge, Outlier | articleRank | -0.2338 | pageRank | -0.1853 | incomingDependencies | -0.1812 | Anomalous |
| org.axonframework.eventsourcing.eventstore.Position | axon-eventsourcing-5.1.2 | 0.0501 | Bridge, Outlier | pageRank | -0.2476 | pageToArticleRankDifference | -0.1884 | articleRank | -0.1682 | Anomalous |
| org.axonframework.common.AxonException | axon-common-5.1.2 | 0.0478 | Bridge, Outlier | pageRank | -0.2525 | articleRank | -0.2207 | pageToArticleRankDifference | -0.193 | Anomalous |
| org.axonframework.messaging.core.MessageType | axon-messaging-5.1.2 | 0.0473 | Bridge, Outlier | articleRank | -0.1994 | pageRank | -0.1658 | incomingDependencies | -0.1384 | Anomalous |
| org.axonframework.common.AxonConfigurationException | axon-common-5.1.2 | 0.0409 | Bridge, Outlier | articleRank | -0.2297 | pageRank | -0.1838 | topologicalComponentLayer | -0.1408 | Anomalous |
| org.axonframework.messaging.core.annotation.ParameterResolverFactory | axon-messaging-5.1.2 | 0.039 | Bridge, Outlier | articleRank | -0.2154 | incomingDependencies | -0.1899 | degree | -0.1422 | Anomalous |

#### Visualizations

##### Anomalies

![Anomalies](./Java_Type/Anomalies.svg)

##### Global feature importance SHAP summary plots

![Anomaly feature importance explained (global)](./Java_Type/Anomaly_feature_importance_explained.svg)

##### Feature dependence plots for top important features

![Anomaly feature dependence explained (global)](./Java_Type/Anomaly_feature_dependence_explained.svg)

---

##### Local SHAP Force Plots – Top 6 Anomalies

![Top 1 anomaly - local feature importance](./Java_Type/Anomaly_1_shap_explanation.svg)
![Top 2 anomaly - local feature importance](./Java_Type/Anomaly_2_shap_explanation.svg)
![Top 3 anomaly - local feature importance](./Java_Type/Anomaly_3_shap_explanation.svg)
![Top 4 anomaly - local feature importance](./Java_Type/Anomaly_4_shap_explanation.svg)
![Top 5 anomaly - local feature importance](./Java_Type/Anomaly_5_shap_explanation.svg)
![Top 6 anomaly - local feature importance](./Java_Type/Anomaly_6_shap_explanation.svg)

---



##### Cluster Diagnostics

![Clusters largest average radius](./Java_Type/Clusters_largest_average_radius.svg)
![Clusters largest max radius](./Java_Type/Clusters_largest_max_radius.svg)
![Clusters largest size](./Java_Type/Clusters_largest_size.svg)

---

##### Cluster Membership Strength

![Cluster probabilities](./Java_Type/Cluster_probabilities.svg)

---

##### Cluster Noise and Bridge Analysis

![Cluster Noise: Highly central and popular](./Java_Type/ClusterNoise_highly_central_and_popular.svg)
![Cluster Noise: Poorly integrated bridges](./Java_Type/ClusterNoise_poorly_integrated_bridges.svg)
![Cluster Noise: Role inverted bridges](./Java_Type/ClusterNoise_role_inverted_bridges.svg)

---

##### Feature Distributions

![Betweenness Centrality Distribution](./Java_Type/BetweennessCentrality_distribution.svg)
![Clustering coefficient distribution](./Java_Type/ClusteringCoefficient_distribution.svg)
![PageRank minus ArticleRank distribution](./Java_Type/PageRank_Minus_ArticleRank_Distribution.svg)

---

##### Feature Relationships

![Clustering coefficient versus PageRank](./Java_Type/ClusteringCoefficient_versus_PageRank.svg)

---

#### Graph Visualizations

##### TopBridge Graph Visualizations

![TopBridge 1](./Java_Type/GraphVisualizations/TopBridge1.svg)

![TopBridge 2](./Java_Type/GraphVisualizations/TopBridge2.svg)

![TopBridge 3](./Java_Type/GraphVisualizations/TopBridge3.svg)

![TopBridge 4](./Java_Type/GraphVisualizations/TopBridge4.svg)

![TopBridge 5](./Java_Type/GraphVisualizations/TopBridge5.svg)

--


## 3. Plot Interpretation Guide

> **Applies to:** All abstraction levels.

| Plot | Purpose |
|------|----------|
| **Anomalies Plot** | 2D visualization showing clusters & anomalies. Guides investigation. |
| **SHAP Summary** | Global feature importance ranked by impact magnitude & direction. |
| **Local SHAP Force** | Per-sample feature contributions. Explains individual anomalies. |
| **Dependence Plot** | Feature–anomaly relationships revealing nonlinear effects. |
| **Cluster Metrics** | Cluster cohesion, size, noise; identifies weak groupings. |

> **Scope:** Applies to plots for *Java Type*, *Java Package*, and similar abstraction levels.

---

### 📘 Main Plots

| Plot | Purpose |
|------|----------|
| **Anomalies** | 2D visualization of all code units showing clusters and anomalies. Reveals isolated vs cluster-based anomalies. |
| **Global Feature Importance (SHAP Summary)** | Mean absolute SHAP values ranking global feature impact. Shows what drives anomalies consistently. |
| **Feature Dependence (Top Important Features)** | Shows how specific feature values affect anomaly score. Identifies nonlinear relationships & interactions. |

---

### 📙 Local Explanation Plots

| Plot | Purpose |
|------|----------|
| **Local SHAP Force Plots (Top Anomalies 1–6)** | Per-feature contributions to each anomaly's score relative to baseline. Enables case-by-case debugging. |

---

### 📗 Cluster-Level Diagnostic Plots

| Plot | Purpose |
|------|----------|
| **Clusters – Overall** | All clusters in one view. Holistic summary of distribution & key metrics. |
| **Clusters – Largest Radius (Avg)** | Ranks by mean member distance from centroid. Identifies dispersed clusters. |
| **Clusters – Largest Radius (Max)** | Shows farthest outlying member per cluster. Highlights extreme members. |
| **Clusters – Largest Size** | Membership counts per cluster. Reveals common design patterns vs. specialized groups. |
| **Cluster Probabilities** | HDBSCAN membership strength distribution. Detects weakly-defined or noisy clusters. |


---

### 📒 Cluster Noise & Bridge Diagnostics

| Plot | Purpose |
|------|----------|
| **Cluster Noise – Highly Central and Popular** | Central nodes that don't fit any cluster. May be key but unstable integration points. |
| **Cluster Noise – Poorly Integrated Bridges** | Nodes connecting clusters but weakly integrated. May reveal boundary violations. |
| **Cluster Noise – Role Inverted Bridges** | Bridges with reversed structural roles. Indicates architectural inversion. |

---

### 📙 Feature Distribution & Relationship Plots

| Plot | Purpose |
|------|----------|
| **Betweenness Centrality Distribution** | Histogram of betweenness values. Detects bottlenecks & single points of failure. |
| **Clustering Coefficient Distribution** | Histogram of local clustering coefficients. Reveals cohesion in different graph regions. |
| **PageRank – ArticleRank Difference Distribution** | Distribution of influence vs popularity. Highlights disproportionate architectural impact. |
| **Clustering Coefficient vs PageRank** | Scatterplot: local vs global influence trade-offs. Finds units both locally & globally critical. |

---

### 📕 Graph Visualizations (Archetype-Level Network Views)

| Plot | Purpose |
|------|----------|
| **Top Hub** | Most-connected node with dependencies. Detects over-centralization & bottlenecks. |
| **Top Bottleneck** | Highest betweenness: controls information flow. Reveals single points of failure. |
| **Top Authority** | Most authoritative (high PageRank). Indicates "sources of truth" in system. |
| **Top Bridge** | Cross-cluster connector. Identifies boundary leaks & undesired coupling. |
| **Top Outlier** | Anomalous isolated node. Highlights deviations from dependency norms. |

> **Note:**
> - In all Graph Visualizations, the **central node** represents the selected *Top Archetype* (e.g., *Top 1 Hub*).  
> - **Darker nodes** indicate *incoming dependencies*, while **brighter nodes** indicate *outgoing dependencies*.  
> - **Emphasized nodes** (thicker borders or larger size) mark particularly influential or anomalous dependencies, depending on the archetype.  
> - These visualizations are most effective for interpreting *local dependency topology* and *role significance* of key components.

---

### 📔 Summary Categories

| Category | Included Plots | Typical Usage |
|-----------|----------------|----------------|
| **Main Diagnostic** | Anomalies, Global SHAP, Feature Dependence | High-level anomaly review |
| **Local Explanation** | Local SHAP Force Plots | Case-by-case anomaly debugging |
| **Cluster Diagnostics** | Cluster Radius / Size / Probability | Assess cluster cohesion and outliers |
| **Cluster Noise Analysis** | Cluster Noise (3 types) | Identify special structural anomalies |
| **Feature Distributions** | Betweenness, Clustering, Rank Difference | Assess feature-based structure patterns |
| **Feature Relationships** | Clustering vs PageRank | Evaluate global vs local influence balance |
| **Archetype Graphs** | Top Hub / Bottleneck / Authority / Bridge / Outlier | Visualizing key dependency roles and structural importance |

---

### 💡 Reading Guidance

- **Color Conventions:**  
  Red = anomalous, Green = typical, Light grey = noise, Pale colors = clusters.  
- **Scales:**  
  SHAP values are normalized (mean absolute); graph metrics standardized by z-score.  
- **How to Use:**  
  1. Start with *Main Diagnostic* plots to identify anomalies and drivers.  
  2. Use *Local SHAP* for detailed case analysis.  
  3. Check *Cluster Diagnostics* and *Noise Plots* to verify grouping quality.  
  4. Use *Feature Distributions* to contextualize metrics.  
  5. Cross-reference *Feature Relationships* for architectural interpretation.

---

## 4. Taxonomy of Anomaly Archetypes

| Archetype | Feature Profile | Architectural Risk |
|-----------|-----------------|--------------------|
| **Hub** | High degree, low clustering coefficient | Central dependency; fragile hotspot |
| **Bottleneck** | High betweenness, low redundancy | Single point of failure; slows evolution |
| **Outlier** | High cluster distance, small cluster size | Misfit or irregular dependency pattern |
| **Authority** | High PageRank, low ArticleRank | Over-relied utility; low local stability |
| **Bridge** | Cross-cluster connection | Risky coupling; weak modular boundaries |

---

## 5. Recommendations

* **Refactor hubs:** Decompose large or over-connected utilities.
* **Mitigate bottlenecks:** Introduce redundancy or alternative communication paths.
* **Investigate outliers:** Determine if anomalies are justified exceptions.
* **Raise cohesion:** Increase local clustering by improving modular boundaries.
* **Stabilize authorities:** Encapsulate frequently used but fragile components.
* **Validate bridges:** Confirm cross-cluster connectors are intentional and safe.

---

## 6. Appendix

### 6.1 Methodology Overview

1. Build dependency graph (types, packages, artifacts).
1. Compute graph metrics: degree, PageRank, betweenness, clustering coefficient, etc.
1. Generate embeddings via Fast Random Projection.
1. Reduce embeddings with PCA (retain 90% variance).
1. Train Isolation Forest for anomaly detection.
1. Explain results using SHAP (via Random Forest proxy).
1. Cluster anomalies via HDBSCAN, tuned with Leiden reference communities (AMI score).
1. Hyperparameter optimization for both Isolation Forest and Random Forest proxy with their F1 score

### 6.2 Feature Set

* Degree (in/out)
* PageRank
* ArticleRank
* Page-to-Article Rank Difference
* Betweenness Centrality
* Local Clustering Coefficient
* Cluster Outlier Score (1.0 - cluster probability)
* Cluster Radius (avg, max)
* Cluster Size
* Node Embedding (PCA 20–35 dims)

### 6.3 Architecture Diagram

![Anomaly Detection Architecture](./AnomalyDetectionArchitecture.svg)
