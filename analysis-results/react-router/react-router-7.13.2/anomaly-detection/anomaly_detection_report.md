---
title: "Anomaly Detection Report"
generated: "2026-04-06"
model_version: "v3.5.0"
dataset: "react-router-7.13.2"
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
| 159 | 7 | 10 | 10 | 7 | 0 | 9 |

### 1.2 Overview of Analyzed Structures

| Abstraction Level | Units | Anomalies | Authorities | Bottlenecks | Bridges | Hubs | Outliers |
| --- | --- | --- | --- | --- | --- | --- | --- |
| TS,Local,Module | 157 | 7 | 10 | 10 | 7 | 0 | 9 |
| TS,Local,Module,TestRelated,TestEnvironment | 2 | 0 | 0 | 0 | 0 | 0 | 0 |

### 1.3 Overview Charts

#### Treemap Charts

![ModuleTreemap1AverageAnomalyScorePerDirectory](./ModuleTreemap1AverageAnomalyScorePerDirectory.svg)

![ModuleTreemap2ArchetypesOverviewPerDirectory](./ModuleTreemap2ArchetypesOverviewPerDirectory.svg)

![ModuleTreemap3ArchetypeAuthorityPerDirectory](./ModuleTreemap3ArchetypeAuthorityPerDirectory.svg)

![ModuleTreemap4ArchetypeBottleneckPerDirectory](./ModuleTreemap4ArchetypeBottleneckPerDirectory.svg)

![ModuleTreemap5ArchetypeBridgePerDirectory](./ModuleTreemap5ArchetypeBridgePerDirectory.svg)

![ModuleTreemap6ArchetypeHubPerDirectory](./ModuleTreemap6ArchetypeHubPerDirectory.svg)

![ModuleTreemap7ArchetypeOutlierPerDirectory](./ModuleTreemap7ArchetypeOutlierPerDirectory.svg)

---

## 2. Deep Dives by Abstraction Level

Each abstraction level includes anomaly statistics, SHAP feature importance, archetype distribution, and example anomalies.

### 2.1 Typescript Module

#### Anomaly Results

##### Total anomalies

| Anomalies | Authorities | Bottlenecks | Bridges | Hubs | Outliers |
| --- | --- | --- | --- | --- | --- |
| 7 | 10 | 10 | 7 | 0 | 9 |

##### Top global contributing features (via SHAP)

| Feature | Mean absolute SHAP value |
| --- | --- |
| *Node embeddings aggregated* | 0.036138 |
| pageRank | 0.019091 |
| pageToArticleRankDifference | 0.018840 |
| articleRank | 0.013042 |
| incomingDependencies | 0.006924 |
| degree | 0.006871 |
| nodeEmbeddingPCA_16 | 0.006430 |
| nodeEmbeddingPCA_11 | 0.005370 |
| outgoingDependencies | 0.003732 |
| clusterDistanceToMedoid | 0.003142 |
| nodeEmbeddingPCA_5 | 0.002930 |

#### Archetype Distribution

| Archetype | Count | Max. Score | Model Status | Examples |
| --- | --- | --- | --- | --- |
|  | 7 | 0.0543 | Anomalous | /home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/source/react-router-7.13.2/packages/react-router/index.ts, /home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/source/react-router-7.13.2/packages/react-router-dev/config/config.ts, /home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/source/react-router-7.13.2/packages/react-router/index-react-server.ts |
| Authority | 4 | 0.0433 | Anomalous | /home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/source/react-router-7.13.2/packages/react-router-dev/config/config.ts, /home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/source/react-router-7.13.2/packages/react-router-dev/config/is-react-router-repo.ts, /home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/source/react-router-7.13.2/packages/react-router-dev/config/routes.ts |
| Bottleneck | 2 | 0.0543 | Anomalous | /home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/source/react-router-7.13.2/packages/react-router/index.ts, /home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/source/react-router-7.13.2/packages/react-router/index-react-server.ts |
| Bridge | 7 | 0.0543 | Anomalous | /home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/source/react-router-7.13.2/packages/react-router/index.ts, /home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/source/react-router-7.13.2/packages/react-router-dev/config/config.ts, /home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/source/react-router-7.13.2/packages/react-router/index-react-server.ts |
| Outlier | 2 | 0.0086 | Anomalous | /home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/source/react-router-7.13.2/packages/react-router-dev/config/is-react-router-repo.ts, /home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/source/react-router-7.13.2/packages/react-router-express/server.ts |
|  | 124 | -0.001 | Typical | /home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/source/react-router-7.13.2/packages/react-router-express/index.ts, /home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/source/react-router-7.13.2/packages/react-router/lib/types/register.ts, /home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/source/react-router-7.13.2/packages/react-router-dev/config.ts |
| Authority | 6 | -0.001 | Typical | /home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/source/react-router-7.13.2/packages/react-router-express/index.ts, /home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/source/react-router-7.13.2/packages/react-router-dev/config.ts, /home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/source/react-router-7.13.2/packages/react-router-cloudflare/worker.ts |
| Bottleneck | 8 | -0.0432 | Typical | /home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/source/react-router-7.13.2/packages/react-router/lib/router/router.ts, /home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/source/react-router-7.13.2/packages/react-router/lib/dom/ssr/entry.ts, /home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/source/react-router-7.13.2/packages/react-router/dom-export.ts |
| Outlier | 7 | -0.001 | Typical | /home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/source/react-router-7.13.2/packages/react-router-express/index.ts, /home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/source/react-router-7.13.2/packages/react-router-node/stream.ts, /home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/source/react-router-7.13.2/packages/react-router-node/index.ts |

#### Top anomalies with their local contributing features (via SHAP)

| Name | Contained in | Anomaly Score | Archetypes | Top Feature 1 | Top Feature 1 SHAP | Top Feature 2 | Top Feature 2 SHAP | Top Feature 3 | Top Feature 3 SHAP | Model Status |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| /home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/source/react-router-7.13.2/packages/react-router/index.ts | react-router | 0.0543 | , Bottleneck, Bridge | pageRank | -0.1875 | pageToArticleRankDifference | -0.1656 | articleRank | -0.1535 | Anomalous |
| /home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/source/react-router-7.13.2/packages/react-router-dev/config/config.ts | react-router-dev | 0.0433 | , Bridge, Authority | nodeEmbeddingPCA_16 | -0.1599 | pageToArticleRankDifference | -0.1579 | pageRank | -0.0992 | Anomalous |
| /home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/source/react-router-7.13.2/packages/react-router/index-react-server.ts | react-router | 0.0249 | , Bridge, Bottleneck | pageToArticleRankDifference | -0.1633 | pageRank | -0.1553 | articleRank | -0.1526 | Anomalous |
| /home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/source/react-router-7.13.2/packages/react-router-dev/config/is-react-router-repo.ts | react-router-dev | 0.0086 | Bridge, Outlier, , Authority | nodeEmbeddingPCA_16 | -0.1996 | pageRank | -0.0847 | nodeEmbeddingPCA_11 | -0.0661 | Anomalous |
| /home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/source/react-router-7.13.2/packages/react-router-dev/config/routes.ts | react-router-dev | 0.0079 | Authority, , Bridge | pageToArticleRankDifference | -0.1895 | pageRank | -0.1781 | articleRank | -0.1156 | Anomalous |
| /home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/source/react-router-7.13.2/packages/react-router-express/server.ts | react-router-express | 0.0058 | Outlier, Bridge, , Authority | pageToArticleRankDifference | -0.1293 | nodeEmbeddingPCA_11 | -0.0957 | pageRank | -0.082 | Anomalous |
| /home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/source/react-router-7.13.2/packages/react-router/lib/router/utils.ts | react-router | 0.001 | Bridge,  | pageToArticleRankDifference | -0.1606 | articleRank | -0.1589 | incomingDependencies | -0.1412 | Anomalous |

#### Visualizations

See [Plot Interpretation Guide](#3-plot-interpretation-guide) on how to read the plots in detail.

##### Anomalies

![Anomalies](./Typescript_Module/Anomalies.svg)

##### Global feature importance SHAP summary plots

![Anomaly feature importance explained (global)](./Typescript_Module/Anomaly_feature_importance_explained.svg)

##### Feature dependence plots for top important features

![Anomaly feature dependence explained (global)](./Typescript_Module/Anomaly_feature_dependence_explained.svg)

---

##### Local SHAP Force Plots – Top 6 Anomalies

![Top 1 anomaly - local feature importance](./Typescript_Module/Anomaly_1_shap_explanation.svg)
![Top 2 anomaly - local feature importance](./Typescript_Module/Anomaly_2_shap_explanation.svg)
![Top 3 anomaly - local feature importance](./Typescript_Module/Anomaly_3_shap_explanation.svg)
![Top 4 anomaly - local feature importance](./Typescript_Module/Anomaly_4_shap_explanation.svg)
![Top 5 anomaly - local feature importance](./Typescript_Module/Anomaly_5_shap_explanation.svg)
![Top 6 anomaly - local feature importance](./Typescript_Module/Anomaly_6_shap_explanation.svg)

---

##### Cluster Diagnostics

![Cluster Overall](./Typescript_Module/Clusters_Overall.svg)

---



##### Cluster Membership Strength

![Cluster probabilities](./Typescript_Module/Cluster_probabilities.svg)

---

##### Cluster Noise and Bridge Analysis

![Cluster Noise: Highly central and popular](./Typescript_Module/ClusterNoise_highly_central_and_popular.svg)
![Cluster Noise: Poorly integrated bridges](./Typescript_Module/ClusterNoise_poorly_integrated_bridges.svg)
![Cluster Noise: Role inverted bridges](./Typescript_Module/ClusterNoise_role_inverted_bridges.svg)

---

##### Feature Distributions

![Betweenness Centrality Distribution](./Typescript_Module/BetweennessCentrality_distribution.svg)
![Clustering coefficient distribution](./Typescript_Module/ClusteringCoefficient_distribution.svg)
![PageRank minus ArticleRank distribution](./Typescript_Module/PageRank_Minus_ArticleRank_Distribution.svg)

---

##### Feature Relationships

![Clustering coefficient versus PageRank](./Typescript_Module/ClusteringCoefficient_versus_PageRank.svg)

---

#### Graph Visualizations

##### TopBottleneck Graph Visualizations

![TopBottleneck 1](./Typescript_Module/GraphVisualizations/TopBottleneck1.svg)

![TopBottleneck 2](./Typescript_Module/GraphVisualizations/TopBottleneck2.svg)

![TopBottleneck 3](./Typescript_Module/GraphVisualizations/TopBottleneck3.svg)

![TopBottleneck 4](./Typescript_Module/GraphVisualizations/TopBottleneck4.svg)

![TopBottleneck 5](./Typescript_Module/GraphVisualizations/TopBottleneck5.svg)

---

##### TopAuthority Graph Visualizations

![TopAuthority 1](./Typescript_Module/GraphVisualizations/TopAuthority1.svg)

![TopAuthority 2](./Typescript_Module/GraphVisualizations/TopAuthority2.svg)

![TopAuthority 3](./Typescript_Module/GraphVisualizations/TopAuthority3.svg)

![TopAuthority 4](./Typescript_Module/GraphVisualizations/TopAuthority4.svg)

![TopAuthority 5](./Typescript_Module/GraphVisualizations/TopAuthority5.svg)

---

##### TopBridge Graph Visualizations

![TopBridge 1](./Typescript_Module/GraphVisualizations/TopBridge1.svg)

![TopBridge 2](./Typescript_Module/GraphVisualizations/TopBridge2.svg)

![TopBridge 3](./Typescript_Module/GraphVisualizations/TopBridge3.svg)

![TopBridge 4](./Typescript_Module/GraphVisualizations/TopBridge4.svg)

![TopBridge 5](./Typescript_Module/GraphVisualizations/TopBridge5.svg)

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
