---
title: "Anomaly Detection Report"
generated: "2026-02-23"
model_version: "v3.3.1"
dataset: "AxonFramework-5.0.2"
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

| Analyzed Units | Anomalies | Authorities | Bottlenecks | Bridges | Hubs | Outliers |
| --- | --- | --- | --- | --- | --- | --- |
| 1343 | 66 | 24 | 22 | 16 | 12 | 13 |

### 1.2 Overview of Analyzed Structures

| Abstraction Level | Units | Anomalies | Authorities | Bottlenecks | Bridges | Hubs | Outliers |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Type,Java,Class | 777 | 34 | 7 | 2 | 5 | 2 | 7 |
| Type,Java,Interface | 253 | 18 | 2 | 6 | 1 | 7 | 3 |
| Package,Java | 146 | 6 | 10 | 10 | 6 | 0 | 3 |
| Type,Java,Record | 56 | 6 | 1 | 2 | 3 | 0 | 0 |
| Type,Java,Annotation | 41 | 1 | 0 | 0 | 0 | 0 | 0 |
| Type,Java,Enum | 17 | 1 | 0 | 0 | 1 | 1 | 0 |
| Type,Java,Class,Throwable | 42 | 0 | 0 | 0 | 0 | 0 | 0 |
| Artifact,Jar,Archive,Zip,Java | 11 | 0 | 4 | 2 | 0 | 2 | 0 |

### 1.3 Overview Charts

#### Treemap Charts

![JavaTreemap1AverageAnomalyScorePerDirectory](./JavaTreemap1AverageAnomalyScorePerDirectory.svg)

![JavaTreemap2ArchetypesOverviewPerDirectory](./JavaTreemap2ArchetypesOverviewPerDirectory.svg)

![JavaTreemap3ArchetypeAuthorityPerDirectory](./JavaTreemap3ArchetypeAuthorityPerDirectory.svg)

![JavaTreemap4ArchetypeBottleneckPerDirectory](./JavaTreemap4ArchetypeBottleneckPerDirectory.svg)

![JavaTreemap5ArchetypeBridgePerDirectory](./JavaTreemap5ArchetypeBridgePerDirectory.svg)

![JavaTreemap6ArchetypeHubPerDirectory](./JavaTreemap6ArchetypeHubPerDirectory.svg)

![JavaTreemap7ArchetypeOutlierPerDirectory](./JavaTreemap7ArchetypeOutlierPerDirectory.svg)

---

## 2. Deep Dives by Abstraction Level

Each abstraction level includes anomaly statistics, SHAP feature importance, archetype distribution, and example anomalies.

### 2.1 Java Artifact

#### Anomaly Results

##### Total anomalies

| Anomalies | Authorities | Bottlenecks | Bridges | Hubs | Outliers |
| --- | --- | --- | --- | --- | --- |
| 0 | 4 | 2 | 0 | 2 | 0 |

##### Top global contributing features (via SHAP)

⚠️ _No anomaly detection and SHAP data available for this level (model skipped or insufficient samples)._

#### Archetype Distribution

| Archetype | Count | Max. Score | Model Status | Examples |
| --- | --- | --- | --- | --- |
| Authority | 4 | null | Undetermined | /axon-common-5.0.2.jar, /axon-spring-boot-autoconfigure-5.0.2.jar, /axon-metrics-micrometer-5.0.2.jar |
| Bottleneck | 2 | null | Undetermined | /axon-conversion-5.0.2.jar, /axon-eventsourcing-5.0.2.jar |
| Hub | 2 | null | Undetermined | /axon-common-5.0.2.jar, /axon-messaging-5.0.2.jar |

#### Top anomalies with their local contributing features (via SHAP)

⚠️ _No anomaly detection and SHAP data available for this level (model skipped or insufficient samples)._

#### Visualizations

See [Plot Interpretation Guide](#3-plot-interpretation-guide) on how to read the plots in detail.









⚠️ _No anomaly detection and SHAP data available for this level (model skipped or insufficient samples)._

#### Graph Visualizations

##### TopHub Graph Visualizations

![TopHub 1](./Java_Artifact/GraphVisualizations/TopHub1.svg)

![TopHub 2](./Java_Artifact/GraphVisualizations/TopHub2.svg)

---

##### TopBottleneck Graph Visualizations

![TopBottleneck 1](./Java_Artifact/GraphVisualizations/TopBottleneck1.svg)

![TopBottleneck 2](./Java_Artifact/GraphVisualizations/TopBottleneck2.svg)

---

##### TopAuthority Graph Visualizations

![TopAuthority 1](./Java_Artifact/GraphVisualizations/TopAuthority1.svg)

![TopAuthority 2](./Java_Artifact/GraphVisualizations/TopAuthority2.svg)

![TopAuthority 3](./Java_Artifact/GraphVisualizations/TopAuthority3.svg)

![TopAuthority 4](./Java_Artifact/GraphVisualizations/TopAuthority4.svg)

--

### 2.2 Java Package

#### Anomaly Results

##### Total anomalies

| Anomalies | Authorities | Bottlenecks | Bridges | Hubs | Outliers |
| --- | --- | --- | --- | --- | --- |
| 6 | 10 | 10 | 6 | 0 | 3 |

##### Top global contributing features (via SHAP)

| Feature | Mean absolute SHAP value |
| --- | --- |
| *Node embeddings aggregated* | 0.035160 |
| pageToArticleRankDifference | 0.016680 |
| pageRank | 0.015120 |
| articleRank | 0.013749 |
| incomingDependencies | 0.011156 |
| degree | 0.005441 |
| nodeEmbeddingPCA_13 | 0.005388 |
| nodeEmbeddingPCA_7 | 0.004327 |
| nodeEmbeddingPCA_12 | 0.002875 |
| nodeEmbeddingPCA_16 | 0.002807 |
| localClusteringCoefficient | 0.002689 |

#### Archetype Distribution

| Archetype | Count | Max. Score | Model Status | Examples |
| --- | --- | --- | --- | --- |
|  | 6 | 0.0295 | Anomalous | org.axonframework.common.annotation, org.axonframework.messaging.core, org.axonframework.messaging.core.unitofwork |
| Authority | 1 | 0.0025 | Anomalous | org.axonframework.common.function |
| Bottleneck | 2 | 0.0288 | Anomalous | org.axonframework.messaging.core, org.axonframework.messaging.core.unitofwork |
| Bridge | 6 | 0.0295 | Anomalous | org.axonframework.common.annotation, org.axonframework.messaging.core, org.axonframework.messaging.core.unitofwork |
| Outlier | 1 | 0.0295 | Anomalous | org.axonframework.common.annotation |
|  | 110 | -0.0008 | Typical | org.axonframework.common, org.axonframework.common.io, org.axonframework.common.util |
| Authority | 9 | -0.0008 | Typical | org.axonframework.common, org.axonframework.common.io, org.axonframework.extension.springboot.actuator |
| Bottleneck | 8 | -0.0165 | Typical | org.axonframework.messaging.core.annotation, org.axonframework.axonserver.connector, org.axonframework.axonserver.connector.event |
| Outlier | 2 | -0.058 | Typical | org.axonframework.eventsourcing.eventstore.jpa, org.axonframework.messaging.core.unitofwork.transaction |

#### Top anomalies with their local contributing features (via SHAP)

| Name | Contained in | Anomaly Score | Archetypes | Top Feature 1 | Top Feature 1 SHAP | Top Feature 2 | Top Feature 2 SHAP | Top Feature 3 | Top Feature 3 SHAP | Model Status |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| org.axonframework.common.annotation | axon-common-5.0.2 | 0.0295 | , Bridge, Outlier | pageToArticleRankDifference | -0.1622 | pageRank | -0.1504 | articleRank | -0.1398 | Anomalous |
| org.axonframework.messaging.core | axon-messaging-5.0.2 | 0.0288 | , Bottleneck, Bridge | pageToArticleRankDifference | -0.1648 | incomingDependencies | -0.1598 | pageRank | -0.1502 | Anomalous |
| org.axonframework.messaging.core.unitofwork | axon-messaging-5.0.2 | 0.0226 | , Bottleneck, Bridge | pageToArticleRankDifference | -0.1583 | incomingDependencies | -0.1578 | pageRank | -0.1427 | Anomalous |
| org.axonframework.common.configuration | axon-common-5.0.2 | 0.0208 | , Bridge | pageToArticleRankDifference | -0.1645 | pageRank | -0.145 | articleRank | -0.1364 | Anomalous |
| org.axonframework.conversion | axon-conversion-5.0.2 | 0.0035 | Bridge,  | pageToArticleRankDifference | -0.171 | articleRank | -0.1497 | pageRank | -0.1462 | Anomalous |
| org.axonframework.common.function | axon-common-5.0.2 | 0.0025 | Bridge, Authority,  | nodeEmbeddingPCA_16 | -0.1027 | nodeEmbeddingPCA_12 | -0.0973 | nodeEmbeddingPCA_15 | -0.0698 | Anomalous |

#### Visualizations

See [Plot Interpretation Guide](#3-plot-interpretation-guide) on how to read the plots in detail.

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

##### TopBottleneck Graph Visualizations

![TopBottleneck 1](./Java_Package/GraphVisualizations/TopBottleneck1.svg)

![TopBottleneck 2](./Java_Package/GraphVisualizations/TopBottleneck2.svg)

![TopBottleneck 3](./Java_Package/GraphVisualizations/TopBottleneck3.svg)

![TopBottleneck 4](./Java_Package/GraphVisualizations/TopBottleneck4.svg)

![TopBottleneck 5](./Java_Package/GraphVisualizations/TopBottleneck5.svg)

---

##### TopAuthority Graph Visualizations

![TopAuthority 1](./Java_Package/GraphVisualizations/TopAuthority1.svg)

![TopAuthority 2](./Java_Package/GraphVisualizations/TopAuthority2.svg)

![TopAuthority 3](./Java_Package/GraphVisualizations/TopAuthority3.svg)

![TopAuthority 4](./Java_Package/GraphVisualizations/TopAuthority4.svg)

![TopAuthority 5](./Java_Package/GraphVisualizations/TopAuthority5.svg)

---

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

--

### 2.3 Java Type

#### Anomaly Results

##### Total anomalies

| Anomalies | Authorities | Bottlenecks | Bridges | Hubs | Outliers |
| --- | --- | --- | --- | --- | --- |
| 60 | 10 | 10 | 10 | 10 | 10 |

##### Top global contributing features (via SHAP)

| Feature | Mean absolute SHAP value |
| --- | --- |
| *Node embeddings aggregated* | 0.058197 |
| articleRank | 0.013882 |
| pageToArticleRankDifference | 0.012336 |
| pageRank | 0.010581 |
| nodeEmbeddingPCA_19 | 0.005462 |
| degree | 0.004679 |
| incomingDependencies | 0.004449 |
| nodeEmbeddingPCA_21 | 0.003950 |
| nodeEmbeddingPCA_28 | 0.003741 |
| nodeEmbeddingPCA_31 | 0.003443 |
| nodeEmbeddingPCA_33 | 0.003319 |

#### Archetype Distribution

| Archetype | Count | Max. Score | Model Status | Examples |
| --- | --- | --- | --- | --- |
|  | 60 | 0.1185 | Anomalous | org.axonframework.messaging.core.Message, org.axonframework.messaging.core.unitofwork.ProcessingContext, org.axonframework.common.TypeReference |
| Authority | 8 | 0.0857 | Anomalous | org.axonframework.common.TypeReference, org.axonframework.common.infra.DescribableComponent, org.axonframework.common.infra.ComponentDescriptor |
| Bottleneck | 8 | 0.1185 | Anomalous | org.axonframework.messaging.core.Message, org.axonframework.messaging.core.unitofwork.ProcessingContext, org.axonframework.messaging.core.MessageStream |
| Bridge | 10 | 0.0399 | Anomalous | org.axonframework.extension.springboot.autoconfig.ConverterAutoConfiguration, org.axonframework.test.util.MessageMonitorReport$Report, org.axonframework.extension.springboot.autoconfig.ConverterAutoConfiguration$1 |
| Hub | 7 | 0.1185 | Anomalous | org.axonframework.messaging.core.Message, org.axonframework.messaging.core.unitofwork.ProcessingContext, org.axonframework.common.infra.DescribableComponent |
| Outlier | 1 | 0.0091 | Anomalous | org.axonframework.messaging.eventhandling.processing.streaming.token.TrackingToken |
|  | 1126 | -0.0001 | Typical | org.axonframework.axonserver.connector.query.AxonServerQueryBusConnector, org.axonframework.common.configuration.ComponentLifecycleHandler, org.axonframework.eventsourcing.eventstore.ConsistencyMarker |
| Authority | 2 | -0.0148 | Typical | org.axonframework.common.StringUtils, org.axonframework.messaging.core.Metadata$MetadataCollector |
| Bottleneck | 2 | -0.0169 | Typical | org.axonframework.modelling.entity.annotation.AnnotatedEntityMetamodel, org.axonframework.messaging.core.unitofwork.ProcessingLifecycle |
| Hub | 3 | -0.0129 | Typical | org.axonframework.common.configuration.Configuration, org.axonframework.common.BuilderUtils, org.axonframework.axonserver.connector.ErrorCode |
| Outlier | 9 | -0.0257 | Typical | org.axonframework.messaging.core.RemoteNonTransientHandlingException, org.axonframework.messaging.core.timeout.UnitOfWorkTimeoutInterceptorBuilder, org.axonframework.common.ObjectUtils |

#### Top anomalies with their local contributing features (via SHAP)

| Name | Contained in | Anomaly Score | Archetypes | Top Feature 1 | Top Feature 1 SHAP | Top Feature 2 | Top Feature 2 SHAP | Top Feature 3 | Top Feature 3 SHAP | Model Status |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| org.axonframework.messaging.core.Message | axon-messaging-5.0.2 | 0.1185 | , Bottleneck, Hub | articleRank | -0.2871 | pageRank | -0.1658 | pageToArticleRankDifference | -0.1477 | Anomalous |
| org.axonframework.messaging.core.unitofwork.ProcessingContext | axon-messaging-5.0.2 | 0.0942 | Hub, , Bottleneck | articleRank | -0.2954 | pageRank | -0.1672 | pageToArticleRankDifference | -0.1413 | Anomalous |
| org.axonframework.common.TypeReference | axon-common-5.0.2 | 0.0857 | Authority,  | articleRank | -0.3307 | pageRank | -0.2152 | pageToArticleRankDifference | -0.1759 | Anomalous |
| org.axonframework.common.infra.DescribableComponent | axon-common-5.0.2 | 0.0777 | , Authority, Hub | articleRank | -0.3319 | pageRank | -0.2152 | pageToArticleRankDifference | -0.1652 | Anomalous |
| org.axonframework.messaging.core.MessageStream | axon-messaging-5.0.2 | 0.0642 | Bottleneck, , Hub | articleRank | -0.2963 | pageRank | -0.1564 | degree | -0.115 | Anomalous |
| org.axonframework.messaging.core.QualifiedName | axon-messaging-5.0.2 | 0.0517 | Bottleneck,  | articleRank | -0.3101 | pageRank | -0.1466 | degree | -0.1246 | Anomalous |
| org.axonframework.conversion.Converter | axon-conversion-5.0.2 | 0.0497 |  | articleRank | -0.3608 | pageRank | -0.2428 | pageToArticleRankDifference | -0.1757 | Anomalous |
| org.axonframework.messaging.eventhandling.EventMessage | axon-messaging-5.0.2 | 0.0474 | Hub, , Bottleneck | articleRank | -0.2981 | pageRank | -0.1624 | pageToArticleRankDifference | -0.1223 | Anomalous |
| org.axonframework.messaging.core.MessageType | axon-messaging-5.0.2 | 0.0421 | Bottleneck,  | articleRank | -0.307 | degree | -0.1377 | betweenness | -0.1234 | Anomalous |
| org.axonframework.common.Assert | axon-common-5.0.2 | 0.04 | Hub,  | articleRank | -0.3678 | pageRank | -0.2117 | pageToArticleRankDifference | -0.1507 | Anomalous |
| org.axonframework.extension.springboot.autoconfig.ConverterAutoConfiguration | axon-spring-boot-autoconfigure-5.0.2 | 0.0399 | Bridge,  | nodeEmbeddingPCA_19 | -0.2356 | nodeEmbeddingPCA_23 | -0.2052 | nodeEmbeddingPCA_21 | -0.1342 | Anomalous |
| org.axonframework.common.infra.ComponentDescriptor | axon-common-5.0.2 | 0.035 | Authority,  | articleRank | -0.3221 | pageRank | -0.1943 | pageToArticleRankDifference | -0.1478 | Anomalous |
| org.axonframework.common.ReflectionUtils | axon-common-5.0.2 | 0.0348 | Bottleneck,  | betweenness | -0.2049 | pageToArticleRankDifference | -0.1174 | pageRank | -0.0619 | Anomalous |
| org.axonframework.common.annotation.Internal | axon-common-5.0.2 | 0.0339 |  | articleRank | -0.3047 | pageRank | -0.1713 | pageToArticleRankDifference | -0.1304 | Anomalous |
| org.axonframework.eventsourcing.eventstore.Position | axon-eventsourcing-5.0.2 | 0.0297 |  | pageRank | -0.2444 | pageToArticleRankDifference | -0.2096 | nodeEmbeddingPCA_15 | -0.0453 | Anomalous |
| org.axonframework.messaging.core.Context$ResourceKey | axon-messaging-5.0.2 | 0.0277 |  | articleRank | -0.3397 | pageRank | -0.2265 | pageToArticleRankDifference | -0.1551 | Anomalous |
| org.axonframework.eventsourcing.eventstore.StartPosition | axon-eventsourcing-5.0.2 | 0.026 |  | pageRank | -0.2416 | pageToArticleRankDifference | -0.2062 | nodeEmbeddingPCA_15 | -0.0596 | Anomalous |
| org.axonframework.extension.springboot.autoconfig.ObjectMapperAutoConfiguration$JacksonConfiguredCondition | axon-spring-boot-autoconfigure-5.0.2 | 0.0259 |  | nodeEmbeddingPCA_19 | -0.1876 | pageToArticleRankDifference | -0.1399 | nodeEmbeddingPCA_29 | -0.0936 | Anomalous |
| org.axonframework.messaging.core.Context | axon-messaging-5.0.2 | 0.0254 | Bottleneck,  | articleRank | -0.3395 | pageRank | -0.2224 | pageToArticleRankDifference | -0.1604 | Anomalous |
| org.axonframework.common.AxonException | axon-common-5.0.2 | 0.0253 | Authority,  | articleRank | -0.3663 | pageRank | -0.2377 | pageToArticleRankDifference | -0.1899 | Anomalous |

#### Visualizations

See [Plot Interpretation Guide](#3-plot-interpretation-guide) on how to read the plots in detail.

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

##### TopHub Graph Visualizations

![TopHub 1](./Java_Type/GraphVisualizations/TopHub1.svg)

![TopHub 2](./Java_Type/GraphVisualizations/TopHub2.svg)

![TopHub 3](./Java_Type/GraphVisualizations/TopHub3.svg)

![TopHub 4](./Java_Type/GraphVisualizations/TopHub4.svg)

![TopHub 5](./Java_Type/GraphVisualizations/TopHub5.svg)

---

##### TopBottleneck Graph Visualizations

![TopBottleneck 1](./Java_Type/GraphVisualizations/TopBottleneck1.svg)

![TopBottleneck 2](./Java_Type/GraphVisualizations/TopBottleneck2.svg)

![TopBottleneck 3](./Java_Type/GraphVisualizations/TopBottleneck3.svg)

![TopBottleneck 4](./Java_Type/GraphVisualizations/TopBottleneck4.svg)

![TopBottleneck 5](./Java_Type/GraphVisualizations/TopBottleneck5.svg)

---

##### TopAuthority Graph Visualizations

![TopAuthority 1](./Java_Type/GraphVisualizations/TopAuthority1.svg)

![TopAuthority 2](./Java_Type/GraphVisualizations/TopAuthority2.svg)

![TopAuthority 3](./Java_Type/GraphVisualizations/TopAuthority3.svg)

![TopAuthority 4](./Java_Type/GraphVisualizations/TopAuthority4.svg)

![TopAuthority 5](./Java_Type/GraphVisualizations/TopAuthority5.svg)

---

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

![TopOutlier 5](./Java_Type/GraphVisualizations/TopOutlier5.svg)

--


## 3. Plot Interpretation Guide

> **Purpose:** Understand each plot type’s diagnostic value.  
> **Applies to:** All abstraction levels.

| Plot Type | Best For | Adds | Why It Matters |
| --- | --- | --- | --- |
| **Anomalies Plot** | Seeing distribution of anomalies in clusters | Context of clusters & outliers | Reveals isolation or cluster-based anomalies |
| **SHAP Summary** | Global feature importance | Feature impact direction | Shows what drives anomalies overall |
| **Local SHAP Force** | Explaining a single anomaly | Feature contribution breakdown | Useful for debugging individual outliers |
| **Dependence Plot** | Understanding feature influence | Interaction visualization | Reveals nonlinear feature effects |
| **Cluster Metrics** | Cluster characteristics | Radius, cohesion, noise | Identifies weakly defined or noisy clusters |

## 3. Plot Interpretation Guide

> **Purpose:** Provide a direct mapping between all plots and their analytical meaning.  
> **Scope:** Applies to plots for *Java Type*, *Java Package*, and similar abstraction levels.  
> **Format:** Each entry includes `Best for`, `Adds`, and `Why`, matching the in-report descriptions.

---

### 📘 Main Plots

| Plot | Description | Best For | Adds | Why |
|------|--------------|----------|------|-----|
| **Anomalies** | 2D visualization of all code units showing clusters and anomalies. | Understanding the overall distribution of anomalies in relation to clusters. | Context of clusters and outliers. | Reveals whether anomalies are isolated or cluster-based, guiding investigation. |
| **Global Feature Importance (SHAP Summary)** | Mean absolute SHAP values ranking global feature impact. | Global understanding of which features drive anomalies. | Direction of impact (color shows feature value). | Explains which metrics consistently influence anomaly detection. |
| **Feature Dependence (Top Important Features)** | Shows how specific feature values affect anomaly score; colored by interacting feature. | Understanding how one feature affects anomaly scores. | Color shows feature interaction or threshold effect. | Helps identify nonlinear relationships and feature interactions. |

---

### 📙 Local Explanation Plots

| Plot | Description | Best For | Adds | Why |
|------|--------------|----------|------|-----|
| **Local SHAP Force Plots (Top Anomalies 1–6)** | Visualizes per-feature contributions to each anomaly’s score relative to baseline. | Explaining *why a specific data point* is anomalous. | Visual breakdown of how each feature contributes to anomaly score. | Enables debugging of individual anomalies through transparent explanation. |

---

### 📗 Cluster-Level Diagnostic Plots

| Plot | Description | Best For | Adds | Why |
|------|--------------|----------|------|-----|
| **Clusters – Overall** | Shows all clusters since they all fit into one plot. | Gaining a holistic view of cluster characteristics in the dataset. | An overall summary of how all clusters are distributed and their key metrics. | Understanding the general structure and properties of clusters can help identify patterns and potential anomalies in the data. |
| **Clusters – Largest Average Radius** | Ranks clusters by mean distance of members from their centroid. | Getting an overview of clusters that are more dispersed. | Identifies clusters with internal variability. | Large average radius suggests less cohesion and potential outliers. |
| **Clusters – Largest Max Radius** | Shows clusters with the farthest outlying member. | Identifying clusters that have members farthest from cluster center. | Highlights clusters containing extreme outliers. | Indicates clusters that may contain hidden anomalies. |
| **Clusters – Largest Size** | Displays cluster membership counts. | Understanding which clusters contain the most code units. | Provides sense of frequency of code structures. | Large clusters may represent common design patterns; small clusters are specialized. |
| **Cluster Probabilities** | Distribution of HDBSCAN membership probabilities. | Detecting code units that don’t strongly belong to any cluster. | Measures how well-defined clusters are. | Highlights noisy or weakly defined clusters. |

---

### 📒 Cluster Noise & Bridge Diagnostics

| Plot | Description | Best For | Adds | Why |
|------|--------------|----------|------|-----|
| **Cluster Noise – Highly Central and Popular** | Central nodes that don’t fit any cluster. | Detecting code units that are highly connected but anomalous. | Reveals influential but misfit nodes. | Such nodes may be key but unstable integration points. |
| **Cluster Noise – Poorly Integrated Bridges** | Nodes connecting clusters but weakly integrated. | Detecting code units that bridge modules unusually. | Identifies cross-cutting or leaking dependencies. | May reveal architectural boundary violations. |
| **Cluster Noise – Role Inverted Bridges** | Bridges with reversed structural roles compared to expected topology. | Detecting code units connecting clusters in unexpected ways. | Highlights anomalous coupling roles. | Indicates architectural inversion or misuse of interfaces. |

---

### 📙 Feature Distribution & Relationship Plots

| Plot | Description | Best For | Adds | Why |
|------|--------------|----------|------|-----|
| **Betweenness Centrality Distribution** | Histogram of betweenness values. | Identifying code units that act as structural bridges. | Insight into flow of dependency control. | Detects potential bottlenecks or single points of failure. |
| **Clustering Coefficient Distribution** | Histogram of local clustering coefficients. | Identifying modularity and local cohesion. | Insight into how tightly code units cluster. | Reveals how cohesive or isolated different regions of the graph are. |
| **PageRank – ArticleRank Difference Distribution** | Distribution of `PageRank - ArticleRank`. | Identifying influential nodes beyond local connectivity. | Shows imbalance between influence and popularity. | Highlights components with disproportionate architectural impact. |
| **Clustering Coefficient vs PageRank** | Scatterplot comparing local clustering to global influence. | Identifying relationships between cohesion and centrality. | Visualizes trade-offs between modularity and reach. | Helps spot code units that are both locally and globally critical. |

---

### 📕 Graph Visualizations (Archetype-Level Network Views)

| Plot | Description | Best For | Adds | Why |
|------|--------------|----------|------|-----|
| **Top Hub Graph Visualization** | Displays the most connected node (e.g., **#1 Hub**) at the center, surrounded by its direct dependencies. Incoming nodes show who is dependent on the hub. | Understanding highly connected code units or components that serve as central integrators. | Highlights nodes that act as major dependency aggregators. | Helps detect over-centralized modules or potential architectural bottlenecks. |
| **Top Bottleneck Graph Visualization** | Shows the node with the highest betweenness centrality (e.g., **#1 Bottleneck**) and its local neighborhood. | Identifying code units that control information or dependency flow. | Emphasizes nodes that mediate critical paths between modules. | Reveals single points of failure or routing constraints in dependency flow. |
| **Top Authority Graph Visualization** | Centers the most authoritative node (e.g., **#1 Authority**) with incoming and outgoing links from dependent nodes with high PageRank and emphasized PageRank to ArticleRank difference. | Detecting key knowledge or functionality providers. | Highlights components with high centrality. | Indicates structural or semantic “sources of truth” in the system. |
| **Top Bridge Graph Visualization** | Displays a node acting as a structural bridge between clusters (e.g., **#1 Bridge**) and its cross-cluster connections based on node embeddings encoding the Graph structure. | Understanding cross-cutting dependencies between modules. | Reveals links connecting distinct architectural domains. | Useful for spotting boundary leaks or undesired coupling between subsystems. |
| **Top Outlier Graph Visualization** | Centers an unusual or isolated node (e.g., **#1 Outlier**) that can hardly be assigned to a cluster and visualizes its sparse or unexpected dependency patterns. | Identifying structurally or behaviorally anomalous nodes. | Highlights nodes with rare or unexpected connection patterns. | Helps pinpoint code units that deviate from established dependency norms. |

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

### 📄 Structured Form (YAML Summary)

You can include this in your appendix for machine-readable mapping:

```yaml
plots:
  main:
    - name: Anomalies
      purpose: Distribution of anomalies and clusters
    - name: Global Feature Importance (SHAP)
      purpose: Global feature ranking
    - name: Feature Dependence
      purpose: Feature–score relationship
  local:
    - name: Local SHAP Force Plots
      purpose: Local explanations for top anomalies
  cluster:
    - name: Clusters Largest Average Radius
      purpose: Identify dispersed clusters
    - name: Clusters Largest Max Radius
      purpose: Identify extreme outlier clusters
    - name: Clusters Largest Size
      purpose: Identify dominant cluster types
    - name: Cluster Probabilities
      purpose: Assess cluster definition strength
  cluster_noise:
    - name: Cluster Noise – Highly Central and Popular
      purpose: Central anomalies without cluster fit
    - name: Cluster Noise – Poorly Integrated Bridges
      purpose: Weakly integrated bridges
    - name: Cluster Noise – Role Inverted Bridges
      purpose: Inverted bridge roles
  feature_distributions:
    - name: Betweenness Centrality Distribution
      purpose: Bridge and bottleneck detection
    - name: Clustering Coefficient Distribution
      purpose: Cohesion and modularity measurement
    - name: PageRank – ArticleRank Difference Distribution
      purpose: Influence vs popularity analysis
  feature_relationships:
    - name: Clustering Coefficient vs PageRank
      purpose: Local vs global influence comparison
```

## 4. Taxonomy of Anomaly Archetypes

| Archetype | Feature Profile | Architectural Risk |
|-----------|-----------------|--------------------|
| **Hub** | High degree, low clustering coefficient | Central dependency; fragile hotspot |
| **Bottleneck** | High betweenness, low redundancy | Single point of failure; slows evolution |
| **Outlier** | High cluster distance, small cluster size | Misfit or irregular dependency pattern |
| **Authority** | High PageRank, low ArticleRank | Over-relied utility; low local stability |
| **Bridge** | Cross-cluster connection | Risky coupling; weak modular boundaries |

**Structured form (for LLM parsing):**

```yaml
archetypes:
  - name: Hub
    profile: High degree, low clustering coefficient
    risk: Central dependency, fragile hotspot
  - name: Bottleneck
    profile: High betweenness, low redundancy
    risk: Single point of failure
  - name: Outlier
    profile: High cluster distance, small cluster size
    risk: Misfit component
  - name: Authority
    profile: High PageRank, low ArticleRank
    risk: Over-relied utility
  - name: Bridge
    profile: Cross-cluster connector
    risk: Risky coupling
```

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
