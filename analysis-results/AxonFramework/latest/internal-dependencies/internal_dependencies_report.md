---
title: "Internal Dependencies Report"
generated: "2026-05-16"
model_version: "v4.0.0"
dataset: "AxonFramework-5.0.3"
authors: ["JohT/code-graph-analysis-pipeline"]
---

# 🔗 Internal Dependencies Report

## 1. Executive Overview

Analyzes internal dependencies: packages, artifacts, modules, NPM packages within codebase.

**Topics**:

- **Internal structure** — interface segregation, widely used types, and usage ratios between modules
- **Path finding** — shortest and longest path distributions revealing dependency chain depth and complexity
- **Topological sort** — build ordering derived from the acyclic view of the dependency graph

> Cyclic analysis is in `cyclic-dependencies` domain. Rows sorted by priority (highest first).

## 📚 Table of Contents

1. [Executive Overview](#1-executive-overview)
1. [Java Internal Structure](#2-java-internal-structure)
1. [TypeScript Internal Structure](#3-typescript-internal-structure)
1. [Path Finding](#4-path-finding)
1. [Topological Sort](#5-topological-sort)
1. [Graph Visualizations](#6-graph-visualizations)
1. [Glossary and Column Definitions](#7-glossary-and-column-definitions)
1. [Object Oriented Design Metrics](#8-object-oriented-design-metrics)
1. [Visibility Metrics](#9-visibility-metrics)
1. [Code Vocabulary](#10-code-vocabulary)

---

## 2. Java Internal Structure

### 2.1 Java Artifact Listing

Artifacts by size and connectivity. High incoming = shared library; high outgoing = aggregator/app-level.

| artifactName | packages | types | incomingDependencies | outgoingDependencies |
| --- | --- | --- | --- | --- |
| axon-messaging-5.0.3.jar | 59 | 579 | 7 | 2 |
| axon-common-5.0.3.jar | 15 | 156 | 10 | 0 |
| axon-eventsourcing-5.0.3.jar | 7 | 100 | 3 | 4 |
| axon-modelling-5.0.3.jar | 7 | 92 | 2 | 3 |
| axon-spring-boot-autoconfigure-5.0.3.jar | 7 | 75 | 1 | 7 |
| axon-test-5.0.3.jar | 6 | 78 | 1 | 3 |
| axon-server-connector-5.0.3.jar | 5 | 72 | 1 | 4 |
| axon-conversion-5.0.3.jar | 5 | 35 | 4 | 1 |
| axon-update-5.0.3.jar | 5 | 23 | 1 | 1 |
| axon-metrics-micrometer-5.0.3.jar | 3 | 16 | 0 | 3 |

[Full data](./Java_Artifact/List_all_Java_artifacts.csv)

### 2.2 Interface Segregation Principle Candidates

ISP (Robert C. Martin): Interfaces declaring many methods but callers use only a subset — extract focused sub-interfaces.

`usageRatio` (lower = stronger candidate), `callerCount` (high + low ratio = higher priority). `exampleCalledMethods` shows methods to extract.

| fullQualifiedTypeName | declaredMethodCount | distinctCalledMethodCount | usageRatio | callerCount | exampleCalledMethods |
| --- | --- | --- | --- | --- | --- |
| org.axonframework.messaging.commandhandling.CommandBus | 6 | 1 | 0.17 | 8 | ["dispatch"] |
| org.axonframework.messaging.core.unitofwork.ProcessingContext | 32 | 1 | 0.03 | 7 | ["computeResourceIfAbsent"] |
| org.axonframework.common.configuration.ComponentDefinition$ComponentCreator | 17 | 1 | 0.06 | 5 | ["createComponent"] |
| org.axonframework.messaging.core.MessageStream$Entry | 7 | 1 | 0.14 | 5 | ["message"] |
| org.axonframework.messaging.core.unitofwork.ProcessingContext | 32 | 1 | 0.03 | 4 | ["withResource"] |
| org.axonframework.messaging.eventhandling.EventMessage | 19 | 2 | 0.11 | 4 | ["identifier","timestamp"] |
| org.axonframework.messaging.eventhandling.EventMessage | 19 | 1 | 0.05 | 4 | ["timestamp"] |
| org.axonframework.messaging.core.MessageStream$Empty | 44 | 1 | 0.02 | 3 | ["cast"] |
| org.axonframework.messaging.eventhandling.EventMessage | 19 | 1 | 0.05 | 3 | ["andMetadata"] |
| org.axonframework.messaging.commandhandling.CommandMessage | 20 | 2 | 0.1 | 2 | ["priority","routingKey"] |

[Full data](./Java_Package/InterfaceSegregationCandidates.csv)

### 2.3 Widely Used Java Types

Types used by most packages (high ripple risk on changes). Sorted by usage count descending.

| fullQualifiedDependentTypeName | dependentTypeName | dependentTypeLabel | numberOfUsingPackages |
| --- | --- | --- | --- |
| org.axonframework.messaging.core.unitofwork.ProcessingContext | ProcessingContext | Interface InternalJavaType | 59 |
| org.axonframework.common.annotation.Internal | Internal | Annotation InternalJavaType | 55 |
| org.axonframework.messaging.core.Message | Message | Interface InternalJavaType | 47 |
| org.axonframework.common.infra.ComponentDescriptor | ComponentDescriptor | Interface InternalJavaType | 46 |
| org.axonframework.messaging.core.MessageStream | MessageStream | Interface GenericDeclaration | 36 |
| org.axonframework.messaging.eventhandling.EventMessage | EventMessage | Interface InternalJavaType | 35 |
| org.axonframework.messaging.core.MessageType | MessageType | Record InternalJavaType | 31 |
| org.axonframework.messaging.core.QualifiedName | QualifiedName | Record InternalJavaType | 30 |
| org.axonframework.common.configuration.Configuration | Configuration | Interface InternalJavaType | 29 |
| org.axonframework.common.FutureUtils | FutureUtils | Class InternalJavaType | 28 |

[Full data](./Java_Package/WidelyUsedTypes.csv)

### 2.4 Overly Broad Artifact Dependencies

Artifact dependencies where dependents use only a small `usedPackagesPercent`. Low % = optimization/removal candidate.

| artifactName | dependentArtifactName | dependentPackages | dependentArtifactPackages | packageUsagePercentage | dependentFullQualifiedPackageNames | dependentPackageNames |
| --- | --- | --- | --- | --- | --- | --- |
| axon-tracing-opentelemetry-5.0.3 | axon-messaging-5.0.3 | 2 | 59 | 0.03389830508474576 | ["org.axonframework.messaging.tracing","org.axonframework.messaging.core"] | ["tracing","core"] |
| axon-tracing-opentelemetry-5.0.3 | axon-common-5.0.3 | 1 | 15 | 0.06666666666666667 | ["org.axonframework.common"] | ["common"] |
| axon-metrics-micrometer-5.0.3 | axon-messaging-5.0.3 | 7 | 59 | 0.11864406779661017 | ["org.axonframework.messaging.core","org.axonframework.messaging.monitoring","org.axonframework.messaging.monitoring.configuration","org.axonframework.messaging.commandhandling","org.axonframework.messaging.eventhandling","org.axonframework.messaging.queryhandling","org.axonframework.messaging.eventhandling.processing"] | ["core","monitoring","configuration","commandhandling","eventhandling","queryhandling","processing"] |
| axon-metrics-micrometer-5.0.3 | axon-common-5.0.3 | 2 | 15 | 0.13333333333333333 | ["org.axonframework.common","org.axonframework.common.configuration"] | ["common","configuration"] |
| axon-test-5.0.3 | axon-eventsourcing-5.0.3 | 1 | 7 | 0.14285714285714285 | ["org.axonframework.eventsourcing.eventstore"] | ["eventstore"] |
| axon-server-connector-5.0.3 | axon-modelling-5.0.3 | 1 | 7 | 0.14285714285714285 | ["org.axonframework.modelling"] | ["modelling"] |
| axon-server-connector-5.0.3 | axon-eventsourcing-5.0.3 | 1 | 7 | 0.14285714285714285 | ["org.axonframework.eventsourcing.eventstore"] | ["eventstore"] |
| axon-metrics-micrometer-5.0.3 | axon-spring-boot-autoconfigure-5.0.3 | 1 | 7 | 0.14285714285714285 | ["org.axonframework.extension.springboot.autoconfig"] | ["autoconfig"] |
| axon-test-5.0.3 | axon-messaging-5.0.3 | 9 | 59 | 0.15254237288135594 | ["org.axonframework.messaging.core.unitofwork","org.axonframework.messaging.core.annotation","org.axonframework.messaging.eventhandling.processing.streaming.token","org.axonframework.messaging.commandhandling","org.axonframework.messaging.core","org.axonframework.messaging.eventhandling","org.axonframework.messaging.core.conversion","org.axonframework.messaging.eventstreaming","org.axonframework.messaging.monitoring"] | ["unitofwork","annotation","token","commandhandling","core","eventhandling","conversion","eventstreaming","monitoring"] |
| axon-spring-boot-autoconfigure-5.0.3 | axon-test-5.0.3 | 1 | 6 | 0.16666666666666666 | ["org.axonframework.test.server"] | ["server"] |

[Full data](./Java_Artifact/ArtifactPackageUsage.csv)

### 2.5 Class Usage Across Artifacts

Classes used across artifacts — extraction candidates. High reuse = type grown beyond original boundary.

> Rows are sorted by priority — most reused classes across artifacts first.

| artifactName | dependentArtifactName | fullPackageName | fullDependentPackageName | dependentTypes | dependentPackageTypes | typeUsagePercentage | dependentTypeNameExamples |
| --- | --- | --- | --- | --- | --- | --- | --- |
| axon-eventsourcing-5.0.3 | axon-messaging-5.0.3 | org.axonframework.eventsourcing.configuration | org.axonframework.messaging.core | 1 | 80 | 0.0125 | ["org.axonframework.messaging.core.MessageTypeResolver"] |
| axon-modelling-5.0.3 | axon-messaging-5.0.3 | org.axonframework.modelling.repository | org.axonframework.messaging.core | 1 | 80 | 0.0125 | ["org.axonframework.messaging.core.Context$ResourceKey"] |
| axon-test-5.0.3 | axon-messaging-5.0.3 | org.axonframework.test.matchers | org.axonframework.messaging.core | 1 | 80 | 0.0125 | ["org.axonframework.messaging.core.Message"] |
| axon-eventsourcing-5.0.3 | axon-messaging-5.0.3 | org.axonframework.eventsourcing.configuration | org.axonframework.messaging.core.annotation | 1 | 51 | 0.0196 | ["org.axonframework.messaging.core.annotation.ParameterResolverFactory"] |
| axon-messaging-5.0.3 | axon-common-5.0.3 | org.axonframework.messaging.core.unitofwork | org.axonframework.common.configuration | 1 | 46 | 0.0217 | ["org.axonframework.common.configuration.ComponentNotFoundException"] |
| axon-modelling-5.0.3 | axon-common-5.0.3 | org.axonframework.modelling.entity.annotation | org.axonframework.common.configuration | 1 | 46 | 0.0217 | ["org.axonframework.common.configuration.Configuration"] |
| axon-eventsourcing-5.0.3 | axon-common-5.0.3 | org.axonframework.eventsourcing.annotation | org.axonframework.common.configuration | 1 | 46 | 0.0217 | ["org.axonframework.common.configuration.Configuration"] |
| axon-messaging-5.0.3 | axon-common-5.0.3 | org.axonframework.messaging.core | org.axonframework.common.configuration | 1 | 46 | 0.0217 | ["org.axonframework.common.configuration.Configuration"] |
| axon-eventsourcing-5.0.3 | axon-common-5.0.3 | org.axonframework.eventsourcing.annotation.reflection | org.axonframework.common.configuration | 1 | 46 | 0.0217 | ["org.axonframework.common.configuration.Configuration"] |
| axon-metrics-micrometer-5.0.3 | axon-spring-boot-autoconfigure-5.0.3 | org.axonframework.extension.metrics.micrometer.springboot | org.axonframework.extension.springboot.autoconfig | 1 | 41 | 0.0244 | ["org.axonframework.extension.springboot.autoconfig.AxonAutoConfiguration"] |

[Full data](./Java_Artifact/ClassesPerPackageUsageAcrossArtifacts.csv)

### 2.6 File Distance Distribution

**File distance** = min directory changes to reach dependency. High distance = misalignment between architecture and folder structure. Distance 0 = same directory.

| directoryDistance | numberOfDependencies | percentageOfDependencies | numberOfDependencyUsers | numberOfDependencyProviders | examples |
| --- | --- | --- | --- | --- | --- |
| 0 | 2125 | 32.86 | 881 | 921 | ["/axon-spring-boot-autoconfigure-5.0.3.jar uses /axon-test-5.0.3.jar","/org/axonframework/test/extension uses /org/axonframework/test/fixture","/org/axonframework/test/fixture uses /org/axonframework/test/util","/org/axonframework/test/fixture uses /org/axonframework/test/matchers"] |
| 1 | 100 | 1.55 | 86 | 41 | ["/org/axonframework/test/matchers uses /org/axonframework/test","/org/axonframework/test/extension uses /org/axonframework/test","/org/axonframework/test/fixture uses /org/axonframework/test","/org/axonframework/messaging/monitoring/configuration uses /org/axonframework/messaging/monitoring"] |
| 2 | 2138 | 33.06 | 631 | 420 | ["/org/axonframework/test/fixture/AxonTestFixture$Customization.class uses /org/axonframework/test/matchers/FieldFilter.class","/org/axonframework/test/fixture/CommandValidator.class uses /org/axonframework/test/matchers/FieldFilter.class","/org/axonframework/test/fixture/AxonTestFixture$Customization.class uses /org/axonframework/test/matchers/IgnoreField.class","/org/axonframework/test/matchers/IgnoreField.class uses /org/axonframework/test/FixtureExecutionException.class"] |
| 4 | 2104 | 32.53 | 679 | 322 | ["/org/axonframework/extension/springboot/service/connection uses /org/axonframework/test/server","/org/axonframework/extension/springboot/service/connection/AxonServerTestContainerConnectionDetailsFactory$AxonServerContainerConnectionDetails.class uses /org/axonframework/test/server/AxonServerContainer.class","/org/axonframework/extension/springboot/service/connection/AxonServerTestContainerConnectionDetailsFactory.class uses /org/axonframework/test/server/AxonServerContainer.class","/org/axonframework/eventsourcing/configuration/SimpleEventSourcedEntityModule.class uses /org/axonframework/messaging/commandhandling/CommandBus.class"] |

[Full data](./Distance_distribution_between_dependent_files.csv)

---

## 3. TypeScript Internal Structure

### 3.1 TypeScript Module Listing

Modules by element count and dependency connectivity. Reveals central and complex modules.

⚠️ _No data available — TypeScript not detected in this codebase._

### 3.2 Widely Used TypeScript Elements

Elements imported by most modules (high ripple risk). Shared utilities or core domain concepts.

⚠️ _No data available — TypeScript not detected in this codebase._

### 3.3 Module Element Usage by Dependent Modules

Low `usedElementsPercent` = public API wider than needed. Candidates for narrower interface.

⚠️ _No data available — TypeScript not detected in this codebase._

---

## 4. Path Finding

Reveals dependency chain **depth and complexity**.

**All Pairs Shortest Path (APSP)**: Graph diameter = longest shortest path. Metric of structural depth.

**Longest Path**: Max directed path in DAG. Critical for build ordering. Requires acyclic graph — run after cyclic-dependencies domain.

### 4.1 Java Package Path Finding

Intra-artifact pairs highlighted; intermediate paths may cross artifact boundaries.

#### 4.1.1 All Pairs Shortest Path

Graph diameter = longest shortest path. Higher = deeper transitive dependencies.

| distance | pairCount | sourceNodeCount | targetNodeCount | examples |
| --- | --- | --- | --- | --- |
| 7 | 8 | 1 | 8 | ["/org/axonframework/extension/metrics/micrometer/springboot ->/org/axonframework/messaging/monitoring/interception","/org/axonframework/extension/metrics/micrometer/springboot ->/org/axonframework/messaging/commandhandling/interception"] |
| 6 | 62 | 7 | 13 | ["/org/axonframework/extension/springboot ->/org/axonframework/messaging/monitoring/interception","/org/axonframework/extension/springboot/actuator/axonserver ->/org/axonframework/messaging/monitoring/interception"] |
| 5 | 118 | 32 | 32 | ["/org/axonframework/messaging/core/unitofwork/transaction ->/org/axonframework/messaging/commandhandling","/org/axonframework/messaging/eventhandling/conversion ->/org/axonframework/messaging/commandhandling/gateway"] |
| 4 | 535 | 89 | 52 | ["/org/axonframework/extension/springboot ->/org/axonframework/messaging/monitoring","/org/axonframework/extension/springboot/actuator/axonserver ->/org/axonframework/messaging/monitoring"] |
| 3 | 888 | 94 | 68 | ["/org/axonframework/test/extension ->/org/axonframework/messaging/monitoring","/org/axonframework/messaging/eventhandling/processing/streaming/pooled ->/org/axonframework/messaging/monitoring/interception"] |
| 2 | 937 | 103 | 93 | ["/org/axonframework/extension/springboot/autoconfig ->/org/axonframework/test/server","/org/axonframework/eventsourcing/configuration ->/org/axonframework/messaging/monitoring"] |
| 1 | 764 | 114 | 101 | ["/org/axonframework/extension/springboot/service/connection ->/org/axonframework/test/server","/org/axonframework/extension/metrics/micrometer ->/org/axonframework/messaging/monitoring"] |

[Full data per project](./Java_Package/Package_all_pairs_shortest_paths_distribution_per_project.csv)


![Java_Package_AllPairsShortestPath_Bar](./Java_Package/Java_Package_AllPairsShortestPath_Bar.svg)

![Java_Package_AllPairsShortestPath_Pie](./Java_Package/Java_Package_AllPairsShortestPath_Pie.svg)

![Java_Package_AllPairsShortestPath_StackedBar_Log](./Java_Package/Java_Package_AllPairsShortestPath_StackedBar_Log.svg)

![Java_Package_AllPairsShortestPath_StackedBar_Normalised](./Java_Package/Java_Package_AllPairsShortestPath_StackedBar_Normalised.svg)

![Java_Package_GraphDiameter_per_Project](./Java_Package/Java_Package_GraphDiameter_per_Project.svg)

#### 4.1.2 Longest Path

Deepest sequential dependency chain. Worst-case build depth if non-parallelized.

| distance | pathsCount |
| --- | --- |
| 5 | 1 |
| 4 | 10 |
| 3 | 22 |
| 2 | 28 |
| 1 | 14 |
| 0 | 19 |

[Full data per project](./Java_Package/Package_longest_paths_distribution.csv)


![Java_Package_LongestPath_Bar](./Java_Package/Java_Package_LongestPath_Bar.svg)

![Java_Package_LongestPath_Pie](./Java_Package/Java_Package_LongestPath_Pie.svg)

![Java_Package_LongestPath_StackedBar_Log](./Java_Package/Java_Package_LongestPath_StackedBar_Log.svg)

![Java_Package_LongestPath_StackedBar_Normalised](./Java_Package/Java_Package_LongestPath_StackedBar_Normalised.svg)

![Java_Package_MaxLongestPath_per_Project](./Java_Package/Java_Package_MaxLongestPath_per_Project.svg)

### 4.2 Java Artifact Path Finding

Coarsest view — artifact (JAR) level. Build parallelism and max sequential depth.

#### 4.2.1 All Pairs Shortest Path

Artifact-level graph diameter. Cycles rare at this level.

| distance | pairCount | sourceNodeCount | targetNodeCount | examples |
| --- | --- | --- | --- | --- |
| 3 | 1 | 1 | 1 | ["/axon-metrics-micrometer-5.0.3.jar ->/axon-modelling-5.0.3.jar"] |
| 2 | 10 | 5 | 6 | ["/axon-metrics-micrometer-5.0.3.jar ->/axon-test-5.0.3.jar","/axon-metrics-micrometer-5.0.3.jar ->/axon-eventsourcing-5.0.3.jar"] |
| 1 | 30 | 10 | 9 | ["/axon-spring-boot-autoconfigure-5.0.3.jar ->/axon-test-5.0.3.jar","/axon-test-5.0.3.jar ->/axon-messaging-5.0.3.jar"] |

[Full data per project](./Java_Artifact/Artifact_all_pairs_shortest_paths_distribution_per_project.csv)


![Java_Artifact_AllPairsShortestPath_Bar](./Java_Artifact/Java_Artifact_AllPairsShortestPath_Bar.svg)

![Java_Artifact_AllPairsShortestPath_Pie](./Java_Artifact/Java_Artifact_AllPairsShortestPath_Pie.svg)

#### 4.2.2 Longest Path

Critical path for sequential artifact building.

| distance | pathsCount |
| --- | --- |
| 7 | 1 |
| 6 | 1 |
| 5 | 1 |
| 4 | 1 |
| 3 | 1 |
| 2 | 3 |
| 1 | 1 |
| 0 | 2 |

[Full data per project](./Java_Artifact/Artifact_longest_paths_distribution.csv)


![Java_Artifact_LongestPath_Bar](./Java_Artifact/Java_Artifact_LongestPath_Bar.svg)

![Java_Artifact_LongestPath_Pie](./Java_Artifact/Java_Artifact_LongestPath_Pie.svg)

### 4.3 TypeScript Module Path Finding

TypeScript module dependency chains. Comparable to Java Package view.

#### 4.3.1 All Pairs Shortest Path

Graph diameter = longest shortest path among module pairs. Higher = deeper transitive imports.

⚠️ _No data available — TypeScript not detected in this codebase._



#### 4.3.2 Longest Path

Deepest sequential TypeScript import chain.

⚠️ _No data available — TypeScript not detected in this codebase._



---

## 5. Topological Sort

Assigns **build level** to each node: Level 0 (no dependencies) → Level N (depends on level N−1).

**Critical path** = max level = min sequential build steps with full parallelism. Highest-level node = most central.

### 5.1 Critical Path Lengths

Max build level per abstraction. Higher = deeper sequential chain.

| abstractionLevel | nodeCount | maxBuildLevel |
| --- | --- | --- |
| Java Artifact | 11 | 7 |
| Java Package | 50 | 4 |

Full topological sort results (node-level build order and level assignments) are in the abstraction-level CSV files under each subdirectory of `reports/internal-dependencies/`.

---

## 6. Graph Visualizations

Directed graphs: node color = build level (darker = higher level = more transitive deps above).

### 6.1 Java Artifact Graphs

**Build levels**: Full artifact hierarchy. **Longest paths**: Isolated chain + contributor view.


![Java Artifact Build Levels](./Java_Artifact/Graph_Visualizations/JavaArtifactBuildLevels.svg)


![Java Artifact Longest Paths (Isolated)](./Java_Artifact/Graph_Visualizations/JavaArtifactLongestPathsIsolated.svg)


![Java Artifact Longest Paths (with contributors)](./Java_Artifact/Graph_Visualizations/JavaArtifactLongestPaths.svg)


### 6.2 TypeScript Module Graphs

**Build levels**: Module layering view. **Longest paths**: Isolated chain + contributor view.

⚠️ _No data available — TypeScript not detected in this codebase._

### 6.3 NPM Package Graphs

Build levels and longest paths for NPM packages (prod + dev dependencies).

⚠️ _No data available — TypeScript not detected in this codebase._

---

## 7. Glossary and Column Definitions

| Term | Definition |
|------|-----------|
| `Graph Diameter` | Longest shortest path. Structural depth metric. |
| `Longest Path` | Max directed path in DAG; critical build path. |
| `File Distance` | Min directory changes to dependency. |
| `Build Level` | Topological sort level (0 = no deps). |
| `usedTypesPercent` | % of package types actually used by dependents. Low = ISP violation. |
| `usedPackagesPercent` | % of artifact packages used by dependents. Low = wide API. |
| `usedElementsPercent` | % of module elements imported by dependents. |
| `Instability` | Outgoing / (incoming + outgoing) deps. 0 = stable; 1 = unstable. |
| `Abstractness` | (Abstract types) / (total types). 0 = concrete; 1 = abstract. |
| `Distance from Main Sequence` | Gap from ideal balance `A + I = 1`. High = pain or uselessness. |
| `Zone of Pain` | Concrete + stable = hard to change/remove. |
| `Zone of Uselessness` | Abstract + unstable = unused abstractions. |

---

## 8. Object-Oriented Design Metrics

Measures conformance to Stable Abstractions Principle(Robert C. Martin): stable components should be abstract; concrete ones unstable.

**Scatter chart**: Abstractness vs. Instability. Green diagonal = Main Sequence (`A + I = 1`). Far off = problem zone.

**Problem zones**: Zone of Pain (concrete + stable) | Zone of Uselessness (abstract + unstable).

**Bar charts**: Top connected packages/modules.

### 8.1 Java Packages (without sub-packages)


![Java Package Main Sequence](./Java_Package/Java_Package_MainSequence.svg)



![Java Package Incoming Dependencies](./Java_Package/Java_Package_IncomingDependencies_Bar.svg)



![Java Package Outgoing Dependencies](./Java_Package/Java_Package_OutgoingDependencies_Bar.svg)


### 8.2 Java Packages (including sub-packages)


![Java Package (Including Sub-packages) Main Sequence](./Java_Package/Java_Package_IncludingSubpackages_MainSequence.svg)



![Java Package (Including Sub-packages) Incoming Dependencies](./Java_Package/Java_Package_IncludingSubpackages_IncomingDependencies_Bar.svg)



![Java Package (Including Sub-packages) Outgoing Dependencies](./Java_Package/Java_Package_IncludingSubpackages_OutgoingDependencies_Bar.svg)


### 8.3 TypeScript Modules

⚠️ _No data available — TypeScript not detected in this codebase._

⚠️ _No data available — TypeScript not detected in this codebase._

⚠️ _No data available — TypeScript not detected in this codebase._

---

## 9. Visibility Metrics

Measures public vs. internal API exposure. High visibility = exposed more than necessary; low = tightly encapsulated.

**Percentile plots** (p25, p50, p75) vs. size (log scale): large artifacts vs. small visibility patterns.

**Scatter charts**: Artifact/project median visibility vs. size • Package/module individual visibility vs. size.

### 9.1 Java Visibility

#### 9.1.1 Artifact-Level Visibility Percentiles


![Java Artifact Visibility Percentiles](./Java_Artifact/Java_Artifact_VisibilityPercentiles.svg)


#### 9.1.2 Artifact-Level Relative Visibility


![Java Artifact Relative Visibility](./Java_Artifact/Java_Artifact_RelativeVisibility.svg)


#### 9.1.3 Package-Level Relative Visibility


![Java Package Relative Visibility](./Java_Package/Java_Package_RelativeVisibility.svg)


### 9.2 TypeScript Visibility

#### 9.2.1 Project-Level Visibility Percentiles

⚠️ _No data available — TypeScript not detected in this codebase._

#### 9.2.2 Project-Level Relative Visibility

⚠️ _No data available — TypeScript not detected in this codebase._

#### 9.2.3 Module-Level Relative Visibility

⚠️ _No data available — TypeScript not detected in this codebase._

---

## 10. Code Vocabulary

**Word cloud**: Vocabulary from all code element names (filtered for generic words). Reveals domain concepts and naming patterns.


![Code Names Wordcloud](./CodeNamesWordcloud.svg)

