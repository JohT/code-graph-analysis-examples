# Code Graph Analysis Pipeline Examples

This repository provides examples of how to analyze TypeScript code and Java artifacts using a fully automated GitHub Actions workflow pipeline with the [code-graph-analysis-pipeline](https://github.com/JohT/code-graph-analysis-pipeline).

The process involves three steps:

1. **Extract**: Upload TypeScript source code and/or Java artifacts, optionally including their Git history, using [actions/upload-artifact](https://github.com/actions/upload-artifact).

1. **Analyze**: Use the shared workflow [JohT/code-graph-analysis-pipeline/.github/workflows/public-analyze-code-graph.yml](https://github.com/JohT/code-graph-analysis-pipeline/blob/main/.github/workflows/public-analyze-code-graph.yml) to analyze the code and artifacts, then upload the results.

1. **Use**: Download the analysis results with [actions/download-artifact](https://github.com/actions/download-artifact) and consume them as needed.

## Table of Contents
<!-- TOC -->

- [Table of Contents](#table-of-contents)
- [:rocket: TypeScript Code Pipeline](#rocket-typescript-code-pipeline)
- [:coffee: Java Artifacts Pipeline](#coffee-java-artifacts-pipeline)
- [:bookmark_tabs: CSV Report Reference](#bookmark_tabs-csv-report-reference)
- [:notebook: Jupyter Notebook Report Reference](#notebook-jupyter-notebook-report-reference)
- [:framed_picture: Image Reference](#framed_picture-image-reference)
- [:recycle: Update Analysis Workflow with Renovate](#recycle-update-analysis-workflow-with-renovate)
- [:page_facing_up: License](#page_facing_up-license)
- [:bar_chart: Analysis Results](#bar_chart-analysis-results)
    - [External Dependencies of Java Packages](#external-dependencies-of-java-packages)
    - [Dependencies Graph of Java Artifacts](#dependencies-graph-of-java-artifacts)
    - [Longest Paths of Java Artifacts](#longest-paths-of-java-artifacts)
    - [All Pairs Shortest Paths of Java Packages per Artifact](#all-pairs-shortest-paths-of-java-packages-per-artifact)
    - [Object-Oriented Design Metrics for Java Packages](#object-oriented-design-metrics-for-java-packages)
    - [Effective Line Count of Java Methods](#effective-line-count-of-java-methods)
    - [Cyclomatic Complexity Distribution for Java Methods](#cyclomatic-complexity-distribution-for-java-methods)
    - [Visibility of Java Types](#visibility-of-java-types)
    - [Communities and Node Embeddings of Java Packages](#communities-and-node-embeddings-of-java-packages)
    - [Word Cloud of Git Authors](#word-cloud-of-git-authors)
    - [Number of distinct commit authors](#number-of-distinct-commit-authors)
    - [Main Authors with highest number of commits](#main-authors-with-highest-number-of-commits)
    - [Clustering coefficient vs. Page Rank](#clustering-coefficient-vs-page-rank)
    - [Java Types that are surprisingly central or popular](#java-types-that-are-surprisingly-central-or-popular)
    - [Largest Java Type Clusters](#largest-java-type-clusters)
    - [Java Type Top 1 Authority](#java-type-top-1-authority)
    - [Java Type Top 1 Bottleneck](#java-type-top-1-bottleneck)
    - [Java Type Top 1 Bridge](#java-type-top-1-bridge)
    - [Java Type Top 1 Hub](#java-type-top-1-hub)
    - [Java Type Top 1 Outlier](#java-type-top-1-outlier)

<!-- /TOC -->

## :rocket: TypeScript Code Pipeline

This example demonstrates how to analyze TypeScript code in a GitHub Actions workflow.

1. The first job, [prepare-code-to-analyze](https://github.com/JohT/code-graph-analysis-examples/blob/23143b34d8fc6e0ab7d80102d8de0b6e6a4ec98e/.github/workflows/typescript-code-analysis.yml#L40), in the workflow [typescript-code-analysis.yml](https://github.com/JohT/code-graph-analysis-examples/blob/23143b34d8fc6e0ab7d80102d8de0b6e6a4ec98e/.github/workflows/typescript-code-analysis.yml), shows how to extract TypeScript code from a repository and upload it for analysis.

2. The second job, [analyze-code-graph](https://github.com/JohT/code-graph-analysis-examples/blob/23143b34d8fc6e0ab7d80102d8de0b6e6a4ec98e/.github/workflows/typescript-code-analysis.yml#L89), calls the shared analysis workflow using the uploaded artifacts' names as parameters. Example:

  ```yaml
  name: Analyze Code Graph
  needs: [prepare-code-to-analyze]
  uses: JohT/code-graph-analysis-pipeline/.github/workflows/public-analyze-code-graph.yml
  with:
    analysis-name: ${{ needs.prepare-code-to-analyze.outputs.analysis-name }}
    sources-upload-name: ${{ needs.prepare-code-to-analyze.outputs.sources-upload-name }}
  ```

3. The third job, [analyze-code-graph](https://github.com/JohT/code-graph-analysis-examples/blob/23143b34d8fc6e0ab7d80102d8de0b6e6a4ec98e/.github/workflows/typescript-code-analysis.yml#L99), demonstrates how to download the analysis results and commit them back to the repository.

## :coffee: Java Artifacts Pipeline

Java artifacts are analyzed similarly to TypeScript code. The main difference is that Java artifacts are downloaded from a Maven repository instead of being part of the repository.

To include Git history in the analysis, checkout the corresponding source repository and upload it as the source artifact, as in the TypeScript example. The Java source code isn't used in the analysis, so a bare git clone is sufficient.

The first job, [prepare-code-to-analyze](https://github.com/JohT/code-graph-analysis-examples/blob/23143b34d8fc6e0ab7d80102d8de0b6e6a4ec98e/.github/workflows/java-code-analysis.yml#L40), in the workflow [java-code-analysis.yml](https://github.com/JohT/code-graph-analysis-examples/blob/23143b34d8fc6e0ab7d80102d8de0b6e6a4ec98e/.github/workflows/java-code-analysis.yml), shows how to prepare the Java artifacts and Git history for analysis.

The second and third jobs are the same as in the TypeScript example.

## :bookmark_tabs: CSV Report Reference

[CSV_REPORTS.md](./analysis-results/CSV_REPORTS.md) lists all CSV Cypher query result reports inside the [results](./results) directory. It can be generated as described in [Generate CSV Report Reference](./COMMANDS.md#generate-csv-cypher-query-report-reference).

## :notebook: Jupyter Notebook Report Reference

[JUPYTER_REPORTS.md](./analysis-results/JUPYTER_REPORTS.md) lists all Jupyter Notebook reports inside the [results](./results) directory. It can be generated as described in [Generate Jupyter Notebook Report Reference](./COMMANDS.md#generate-jupyter-notebook-report-reference).

## :framed_picture: Image Reference

[IMAGES.md](./analysis-results/IMAGES.md) lists all PNG images inside the [results](./results) directory. It can be generated as described in [Generate Image Reference](./COMMANDS.md#generate-image-reference).

## :recycle: Update Analysis Workflow with Renovate

This repository uses [Renovate](https://docs.renovatebot.com) to automatically update the analysis workflow to the latest version. To enable this, add the following extension to your Renovate configuration:

```json
"extends": [
  "github>JohT/code-graph-analysis-pipeline//renovate-presets/code-graph-analysis-workflow-latest-digest.json5"
]
```

You can find the complete configuration in the [renovate.json](./renovate.json) file.

## :page_facing_up: License

This repository is licensed under the Apache License, Version 2.0. See [LICENSE](./LICENSE) for the full license text.

## :bar_chart: Analysis Results

Below are examples drawn from more than a hundred reports produced by the analysis. They illustrate results from analyzing [AxonFramework](https://github.com/AxonFramework/AxonFramework), a Java framework for evolutionary, message-driven microservices on the JVM. For the complete set of reports, see the [analysis-results](./analysis-results) directory.

### External Dependencies of Java Packages

<img src="./analysis-results/AxonFramework/latest/external-dependencies-java/ExternalDependenciesJava_files/ExternalDependenciesJava_19_1.png" width="600" alt="External dependencies of Java packages">

### Dependencies Graph of Java Artifacts

<img src="./analysis-results/AxonFramework/latest/internal-dependencies-visualization/JavaArtifactBuildLevels.svg" width="600" alt="Dependencies graph of Java artifacts">

### Longest Path(s) of Java Artifacts

<img src="./analysis-results/AxonFramework/latest/path-finding-visualization/JavaArtifactLongestPaths.svg" width="600" alt="Longest path of Java artifacts">

### All Pairs Shortest Paths of Java Packages per Artifact

<img src="./analysis-results/AxonFramework/latest/path-finding-java/PathFindingJava_files/PathFindingJava_46_1.png" width="600" alt="All pairs shortest paths of Java packages per artifact">

### Object-Oriented Design Metrics for Java Packages

<img src="./analysis-results/AxonFramework/latest/object-oriented-design-metrics-java/ObjectOrientedDesignMetricsJava_files/ObjectOrientedDesignMetricsJava_41_0.png" width="600" alt="Object-oriented design metrics for Java packages">

### Effective Line Count of Java Methods

<img src="./analysis-results/AxonFramework/latest/method-metrics-java/MethodMetricsJava_files/MethodMetricsJava_13_1.png" width="600" alt="Effective line count of Java methods">

### Cyclomatic Complexity Distribution for Java Methods

<img src="./analysis-results/AxonFramework/latest/method-metrics-java/MethodMetricsJava_files/MethodMetricsJava_25_1.png" width="600" alt="Cyclomatic complexity distribution for Java methods">

### Visibility of Java Types

<img src="./analysis-results/AxonFramework/latest/visibility-metrics-java/VisibilityMetricsJava_files/VisibilityMetricsJava_23_2.png" width="600" alt="Visibility of Java types">

### Communities and Node Embeddings of Java Packages

<img src="./analysis-results/AxonFramework/latest/node-embeddings-java/NodeEmbeddingsJava_files/NodeEmbeddingsJava_21_0.png" width="600" alt="Communities and node embeddings of Java packages">

### Word Cloud of Git Authors

<img src="./analysis-results/AxonFramework/latest/wordcloud/Wordcloud_files/Wordcloud_16_0.png" width="600" alt="Word cloud of Git authors">

### Number of distinct commit authors

<img src="./analysis-results/AxonFramework/latest/git-history-general/GitHistoryGeneral_files/NumberOfDistinctCommitAuthors.svg" width="600" alt="Number of distinct commit authors">

### Main Authors with highest number of commits

<img src="./analysis-results/AxonFramework/latest/git-history-general/GitHistoryGeneral_files/MainAuthorsWithHighestNumberOfCommits.svg" width="600" alt="Main authors with highest number of commits">

### Clustering coefficient vs. Page Rank

The scatter plot below compares the importance of Java types to the density of their connections. The Y axis shows the [PageRank](https://en.wikipedia.org/wiki/PageRank) score (higher values indicate more important and frequently used types). The X axis shows the [clustering coefficient](https://en.wikipedia.org/wiki/Clustering_coefficient) (higher values indicate more densely connected neighborhoods). Important bridge or hub types appear toward the top-left; highly influential nodes in dense communities appear toward the top-right.

<img src="./analysis-results/AxonFramework/latest/anomaly-detection/Java_Type/ClusteringCoefficient_versus_PageRank.svg" width="600" alt="Clustering Coefficient vs. PageRank">

### Java Types that are surprisingly central or popular

<img src="./analysis-results/AxonFramework/latest/anomaly-detection/Java_Type/ClusterNoise_highly_central_and_popular.svg" width="600" alt="Surprisingly central or popular Java Types">

### Largest Java Type Clusters

<img src="./analysis-results/AxonFramework/latest/anomaly-detection/Java_Type/Clusters_largest_size.svg" width="600" alt="Largest Java Type Clusters">

### Java Type Top 1 Authority

An "Authority" is a code unit many important parts depend on: it has high global importance (PageRank) but low local support (ArticleRank). A large PageRank − ArticleRank gap flags widely used utilities or entry points that are central but not well supported locally.

<img src="./analysis-results/AxonFramework/AxonFramework-4.12.1/anomaly-detection/Java_Type/GraphVisualizations/TopAuthority1.svg" width="600" alt="Top 1 Java Type Authority Graph Visualization">

### Java Type Top 1 Bottleneck

A "Bottleneck" is a code unit with exceptionally high Betweenness centrality — it lies on many shortest paths between other nodes, so it mediates a large fraction of dependency flows and is a potential single point of failure or architectural hotspot. Potentially an unintended dependency concentration: if removed, communication between modules breaks.

<img src="./analysis-results/AxonFramework/AxonFramework-4.12.1/anomaly-detection/Java_Type/GraphVisualizations/TopBottleneck1.svg" width="600" alt="Top 1 Java Type Bottleneck Graph Visualization">

### Java Type Top 1 Bridge

A "Bridge" is a code unit that connects different parts of the codebase. It is detected as an anomaly with a high contribution of node embedding features, which encode the structural position in the graph. It shows code that might integrate various layers or boundaries (e.g., API facades) or violates architecture (tangled dependencies).

<img src="./analysis-results/AxonFramework/AxonFramework-4.12.1/anomaly-detection/Java_Type/GraphVisualizations/TopBridge1.svg" width="600" alt="Top 1 Java Type Bridge Graph Visualization">

### Java Type Top 1 Hub

A "Hub" is a code unit with a high out-degree (many dependencies) but low clustering coefficient (its neighbors are not well connected). Hubs are central dependencies that many other parts rely on, making them potential fragile hotspots in the architecture. The low clustering coefficient indicates that these hubs may not be well integrated into the surrounding code, increasing the risk of failure if the hub encounters issues.

<img src="./analysis-results/AxonFramework/AxonFramework-4.12.1/anomaly-detection/Java_Type/GraphVisualizations/TopHub1.svg" width="600" alt="Top 1 Java Type Hub Graph Visualization">

### Java Type Top 1 Outlier

A "Outlier" is a code unit that significantly deviates from typical patterns in the codebase. It has a low clustering probability and a high distance to the nearest cluster centroid in the node embedding space. This indicates that the outlier has a unique structural position in the dependency graph, potentially representing specialized functionality or an architectural anomaly.

<img src="./analysis-results/AxonFramework/AxonFramework-4.12.1/anomaly-detection/Java_Type/GraphVisualizations/TopOutlier1.svg" width="600" alt="Top 1 Java Type Outlier Graph Visualization">
