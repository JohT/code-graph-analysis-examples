---
title: "Anomaly Detection Report"
generated: "2026-05-17"
model_version: "v4.0.1"
dataset: "AxonFramework-5.0.3"
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
| 1392 | 67 | 16 | 17 |

### 1.2 Overview of Analyzed Structures

| Abstraction Level | Units | Anomalies | Bridges | Outliers |
| --- | --- | --- | --- | --- |
| Type,Java,Interface | 273 | 38 | 6 | 0 |
| Type,Java,Class | 801 | 15 | 2 | 9 |
| Package,Java | 150 | 6 | 6 | 7 |
| Type,Java,Record | 56 | 5 | 2 | 0 |
| Type,Java,Annotation | 42 | 2 | 0 | 0 |
| Type,Java,Class,Throwable | 42 | 1 | 0 | 0 |
| Type,Java,Enum | 17 | 0 | 0 | 1 |
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
| 6 | 6 | 7 | 120 | 1528 | 0.107003 |

##### Top global contributing features (via SHAP)

| Feature | Mean absolute SHAP value |
| --- | --- |
| *Node embeddings aggregated* | 0.026003 |
| pageToArticleRankDifference | 0.018611 |
| incomingDependencies | 0.010040 |
| pageRank | 0.008611 |
| degree | 0.008247 |
| articleRank | 0.007968 |
| localClusteringCoefficient | 0.005998 |
| betweenness | 0.004935 |
| topologicalComponentLayer | 0.004022 |
| nodeEmbeddingPCA_18 | 0.003447 |
| nodeEmbeddingPCA_13 | 0.002863 |

#### Archetype Distribution

| Archetype | Count | Max. Score | Model Status | Examples |
| --- | --- | --- | --- | --- |
| Bridge | 6 | 0.0362 | Anomalous | org.axonframework.common.configuration, org.axonframework.messaging.core.annotation, org.axonframework.common.annotation |
| Outlier | 1 | 0.018 | Anomalous | org.axonframework.common.annotation |
| Outlier | 6 | -0.0125 | Typical | org.axonframework.conversion, org.axonframework.messaging.core.conversion, org.axonframework.messaging.eventhandling.processing.subscribing |

#### Top anomalies with their local contributing features (via SHAP)

| Name | Contained in | Anomaly Score | Archetypes | Top Feature 1 | Top Feature 1 SHAP | Top Feature 2 | Top Feature 2 SHAP | Top Feature 3 | Top Feature 3 SHAP | Model Status |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| org.axonframework.common.configuration | axon-common-5.0.3 | 0.0362 | Bridge, Outlier | pageToArticleRankDifference | -0.1589 | incomingDependencies | -0.1121 | degree | -0.0902 | Anomalous |
| org.axonframework.messaging.core.annotation | axon-messaging-5.0.3 | 0.026 | Bridge, Outlier | pageToArticleRankDifference | -0.1185 | betweenness | -0.1005 | pageRank | -0.0782 | Anomalous |
| org.axonframework.common.annotation | axon-common-5.0.3 | 0.018 | Bridge, Outlier | pageToArticleRankDifference | -0.1633 | pageRank | -0.0822 | incomingDependencies | -0.0716 | Anomalous |
| org.axonframework.messaging.core | axon-messaging-5.0.3 | 0.0099 | Bridge, Outlier | pageToArticleRankDifference | -0.1897 | incomingDependencies | -0.1506 | degree | -0.129 | Anomalous |
| org.axonframework.common.io | axon-common-5.0.3 | 0.0088 | Bridge, Outlier | nodeEmbeddingPCA_19 | -0.0895 | pageToArticleRankDifference | -0.0807 | nodeEmbeddingPCA_18 | -0.0743 | Anomalous |
| org.axonframework.messaging.core.unitofwork | axon-messaging-5.0.3 | 0.0024 | Bridge, Outlier | pageToArticleRankDifference | -0.1724 | incomingDependencies | -0.1501 | degree | -0.135 | Anomalous |

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
| 61 | 10 | 10 | 1206 | 11346 | 0.007807 |

##### Top global contributing features (via SHAP)

| Feature | Mean absolute SHAP value |
| --- | --- |
| *Node embeddings aggregated* | 0.036284 |
| articleRank | 0.016262 |
| pageRank | 0.013435 |
| incomingDependencies | 0.010596 |
| degree | 0.010514 |
| pageToArticleRankDifference | 0.010449 |
| topologicalComponentLayer | 0.003909 |
| nodeEmbeddingPCA_17 | 0.003521 |
| stronglyConnectedComponentSizeRatio | 0.003253 |
| betweenness | 0.002807 |
| nodeEmbeddingPCA_33 | 0.002531 |

#### Archetype Distribution

| Archetype | Count | Max. Score | Model Status | Examples |
| --- | --- | --- | --- | --- |
| Bridge | 10 | 0.0223 | Anomalous | org.axonframework.test.fixture.AxonTestPhase$When, org.axonframework.test.fixture.AxonTestPhase$When$Nothing, org.axonframework.messaging.eventstreaming.TagFilteredEventCriteria |
| Outlier | 10 | -0.0197 | Typical | org.axonframework.common.ObjectUtils, org.axonframework.common.lock.NullLockFactory, org.axonframework.messaging.queryhandling.distributed.PayloadConvertingQueryBusConnector |

#### Top anomalies with their local contributing features (via SHAP)

| Name | Contained in | Anomaly Score | Archetypes | Top Feature 1 | Top Feature 1 SHAP | Top Feature 2 | Top Feature 2 SHAP | Top Feature 3 | Top Feature 3 SHAP | Model Status |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| org.axonframework.messaging.core.unitofwork.ProcessingContext | axon-messaging-5.0.3 | 0.0964 | Bridge, Outlier | articleRank | -0.2304 | degree | -0.1833 | incomingDependencies | -0.1692 | Anomalous |
| org.axonframework.common.TypeReference | axon-common-5.0.3 | 0.0922 | Bridge, Outlier | articleRank | -0.2343 | degree | -0.1611 | incomingDependencies | -0.159 | Anomalous |
| org.axonframework.messaging.core.MessageStream | axon-messaging-5.0.3 | 0.086 | Bridge, Outlier | articleRank | -0.2294 | degree | -0.1887 | incomingDependencies | -0.1757 | Anomalous |
| org.axonframework.messaging.core.Message | axon-messaging-5.0.3 | 0.0798 | Bridge, Outlier | articleRank | -0.2272 | degree | -0.1755 | incomingDependencies | -0.1618 | Anomalous |
| org.axonframework.common.annotation.Internal | axon-common-5.0.3 | 0.0734 | Bridge, Outlier | articleRank | -0.2291 | degree | -0.1976 | incomingDependencies | -0.1752 | Anomalous |
| org.axonframework.conversion.Converter | axon-conversion-5.0.3 | 0.0733 | Bridge, Outlier | articleRank | -0.2409 | incomingDependencies | -0.1684 | degree | -0.1656 | Anomalous |
| org.axonframework.messaging.eventhandling.EventMessage | axon-messaging-5.0.3 | 0.0683 | Bridge, Outlier | articleRank | -0.2218 | degree | -0.1888 | incomingDependencies | -0.1775 | Anomalous |
| org.axonframework.common.infra.ComponentDescriptor | axon-common-5.0.3 | 0.0654 | Bridge, Outlier | articleRank | -0.2409 | degree | -0.1893 | incomingDependencies | -0.1713 | Anomalous |
| org.axonframework.messaging.eventstreaming.EventCriteria | axon-messaging-5.0.3 | 0.0621 | Bridge, Outlier | articleRank | -0.2336 | pageRank | -0.1452 | nodeEmbeddingPCA_17 | -0.1132 | Anomalous |
| org.axonframework.messaging.core.Context$ResourceKey | axon-messaging-5.0.3 | 0.062 | Bridge, Outlier | articleRank | -0.2389 | degree | -0.2047 | incomingDependencies | -0.174 | Anomalous |
| org.axonframework.messaging.core.QualifiedName | axon-messaging-5.0.3 | 0.0576 | Bridge, Outlier | articleRank | -0.2127 | incomingDependencies | -0.177 | degree | -0.1743 | Anomalous |
| org.axonframework.common.infra.DescribableComponent | axon-common-5.0.3 | 0.0561 | Bridge, Outlier | articleRank | -0.2299 | incomingDependencies | -0.1741 | degree | -0.1739 | Anomalous |
| org.axonframework.messaging.eventhandling.processing.streaming.token.TrackingToken | axon-messaging-5.0.3 | 0.0557 | Bridge, Outlier | articleRank | -0.2485 | degree | -0.2045 | incomingDependencies | -0.1756 | Anomalous |
| org.axonframework.common.configuration.Configuration | axon-common-5.0.3 | 0.0436 | Bridge, Outlier | articleRank | -0.2412 | degree | -0.2023 | incomingDependencies | -0.1763 | Anomalous |
| org.axonframework.messaging.core.Metadata | axon-messaging-5.0.3 | 0.0416 | Bridge, Outlier | articleRank | -0.2398 | incomingDependencies | -0.1755 | degree | -0.1674 | Anomalous |
| org.axonframework.messaging.core.Context | axon-messaging-5.0.3 | 0.04 | Bridge, Outlier | articleRank | -0.2925 | pageRank | -0.2011 | pageToArticleRankDifference | -0.1459 | Anomalous |
| org.axonframework.common.Assert | axon-common-5.0.3 | 0.037 | Bridge, Outlier | articleRank | -0.3111 | pageRank | -0.1881 | pageToArticleRankDifference | -0.1586 | Anomalous |
| org.axonframework.messaging.core.MessageStream$Entry | axon-messaging-5.0.3 | 0.0356 | Bridge, Outlier | articleRank | -0.238 | degree | -0.2078 | incomingDependencies | -0.1759 | Anomalous |
| org.axonframework.common.AxonException | axon-common-5.0.3 | 0.035 | Bridge, Outlier | articleRank | -0.3073 | pageRank | -0.201 | pageToArticleRankDifference | -0.1557 | Anomalous |
| org.axonframework.messaging.core.annotation.MessageHandlingMember | axon-messaging-5.0.3 | 0.0344 | Bridge, Outlier | articleRank | -0.2529 | degree | -0.1748 | pageRank | -0.1512 | Anomalous |

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

---

##### TopOutlier Graph Visualizations

![TopOutlier 1](./Java_Type/GraphVisualizations/TopOutlier1.svg)

![TopOutlier 2](./Java_Type/GraphVisualizations/TopOutlier2.svg)

![TopOutlier 3](./Java_Type/GraphVisualizations/TopOutlier3.svg)

![TopOutlier 4](./Java_Type/GraphVisualizations/TopOutlier4.svg)

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
