---
title: "Internal Dependencies Report"
generated: "2026-08-31"
model_version: "v4.0.2"
dataset: "react-router-7.18.1"
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



### 2.2 Interface Segregation Principle Candidates

ISP (Robert C. Martin): Interfaces declaring many methods but callers use only a subset — extract focused sub-interfaces.

`usageRatio` (lower = stronger candidate), `callerCount` (high + low ratio = higher priority). `exampleCalledMethods` shows methods to extract.



### 2.3 Widely Used Java Types

Types used by most packages (high ripple risk on changes). Sorted by usage count descending.



### 2.4 Overly Broad Artifact Dependencies

Artifact dependencies where dependents use only a small `usedPackagesPercent`. Low % = optimization/removal candidate.



### 2.5 Class Usage Across Artifacts

Classes used across artifacts — extraction candidates. High reuse = type grown beyond original boundary.

> Rows are sorted by priority — most reused classes across artifacts first.



### 2.6 File Distance Distribution

**File distance** = min directory changes to reach dependency. High distance = misalignment between architecture and folder structure. Distance 0 = same directory.

| directoryDistance | numberOfDependencies | percentageOfDependencies | numberOfDependencyUsers | numberOfDependencyProviders | examples |
| --- | --- | --- | --- | --- | --- |
| 0 | 153 | 41.69 | 70 | 87 | ["./index.ts uses ./dom-export.ts","./index-react-server.ts uses ./dom-export.ts","./index.ts uses ./index-react-server-client.ts","./dom-export.ts uses ./index-react-server.ts"] |
| 3 | 43 | 11.72 | 22 | 33 | ["./lib/errors.ts uses ./index.ts","./lib/context.ts uses ./index.ts","./lib/server-runtime/server.ts uses ./lib/actions.ts","./lib/server-runtime/single-fetch.ts uses ./lib/actions.ts"] |
| 4 | 121 | 32.97 | 43 | 41 | ["./lib/rsc/route-modules.ts uses ./dom-export.ts","./lib/rsc/server.rsc.ts uses ./dom-export.ts","./lib/rsc/server.rsc.ts uses ./index-react-server-client.ts","./lib/server-runtime/errors.ts uses ./index-react-server.ts"] |
| 5 | 48 | 13.08 | 23 | 17 | ["./lib/server-runtime/sessions/memoryStorage.ts uses ./index-react-server.ts","./lib/dom/ssr/routeModules.ts uses ./index-react-server.ts","./lib/server-runtime/sessions/cookieStorage.ts uses ./index-react-server.ts","./lib/dom/ssr/entry.ts uses ./index.ts"] |
| 6 | 2 | 0.54 | 2 | 2 | ["./vendor/turbo-stream-v2/unflatten.ts uses ./lib/router/utils.ts","./lib/server-runtime/single-fetch.ts uses ./vendor/turbo-stream-v2/turbo-stream.ts"] |

[Full data](./Distance_distribution_between_dependent_files.csv)

---

## 3. TypeScript Internal Structure

### 3.1 TypeScript Module Listing

Modules by element count and dependency connectivity. Reveals central and complex modules.

| rootProjectName | moduleName | numberOfElements | numberOfGitCommits | incomingDependencies | outgoingDependencies |
| --- | --- | --- | --- | --- | --- |
| react-router-7.18.1 | dom-export | 7 | 0 | 19 | 0 |
| react-router-7.18.1 | react-router | 5 | 0 | 9 | 4 |
| react-router-7.18.1 | react-router | 40 | 0 | 109 | 4 |
| react-router-7.18.1 | react-router | 170 | 0 | 376 | 13 |
| react-router-7.18.1 | actions | 1 | 0 | 3 | 0 |
| react-router-7.18.1 | context | 19 | 0 | 11 | 10 |
| react-router-7.18.1 | errors | 4 | 0 | 2 | 0 |
| react-router-7.18.1 | href | 1 | 0 | 2 | 0 |
| react-router-7.18.1 | dom | 14 | 0 | 6 | 0 |
| react-router-7.18.1 | global | 2 | 0 | 0 | 0 |

[Full data](./Typescript_Module/List_all_Typescript_modules.csv)

### 3.2 Widely Used TypeScript Elements

Elements imported by most modules (high ripple risk). Shared utilities or core domain concepts.

| fullQualifiedDependentElementName | dependentElementModuleName | dependentElementName | dependentElementLabels | numberOfUsingModules |
| --- | --- | --- | --- | --- |
| "/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.1/source/react-router-7.18.1/packages/react-router-dev/vite/vite.ts".getVite | vite.ts | getVite | Function | 11 |
| "/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.1/source/react-router-7.18.1/packages/react-router-dev/vite/vite.ts".preloadVite | vite.ts | preloadVite | Function | 10 |
| "/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.1/source/react-router-7.18.1/packages/react-router/lib/router/history.ts".Location | history.ts | Location | Interface | 9 |
| "/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.1/source/react-router-7.18.1/packages/react-router-dev/config/routes.ts".RouteManifestEntry | routes.ts | RouteManifestEntry | Interface | 9 |
| "/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.1/source/react-router-7.18.1/packages/react-router/lib/router/utils.ts".DataRouteObject | utils.ts | DataRouteObject | TypeAlias | 8 |
| "/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.1/source/react-router-7.18.1/packages/react-router/lib/router/utils.ts".RouteMatch | utils.ts | RouteMatch | Interface | 8 |
| "/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.1/source/react-router-7.18.1/packages/react-router/lib/dom/ssr/entry.ts".FutureConfig | entry.ts | FutureConfig | Interface | 7 |
| "/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.1/source/react-router-7.18.1/packages/react-router/lib/dom/ssr/routeModules.ts".RouteModules | routeModules.ts | RouteModules | Interface | 7 |
| "/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.1/source/react-router-7.18.1/packages/react-router/lib/router/router.ts".StaticHandlerContext | router.ts | StaticHandlerContext | Interface | 7 |
| "/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.1/source/react-router-7.18.1/packages/create-react-router/utils.ts".color | utils.ts | color | Variable | 7 |

[Full data](./Typescript_Module/WidelyUsedTypescriptElements.csv)

### 3.3 Module Element Usage by Dependent Modules

Low `usedElementsPercent` = public API wider than needed. Candidates for narrower interface.

| sourceModuleName | dependentModuleName | dependentElementsCount | dependentModuleElementsCount | elementUsagePercentage | dependentElementFullNameExamples | dependentElementNameExamples |
| --- | --- | --- | --- | --- | --- | --- |
| memoryStorage | react-router | 1 | 178 | 0.0056179775280898875 | ["\"/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.1/source/react-router-7.18.1/packages/react-router/lib/server-runtime/sessions\".SessionStorage"] | ["SessionStorage"] |
| route-data | react-router | 1 | 170 | 0.0058823529411764705 | ["\"/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.1/source/react-router-7.18.1/packages/react-router/lib/server-runtime/data.ts\".AppLoadContext"] | ["AppLoadContext"] |
| urls | react-router | 1 | 170 | 0.0058823529411764705 | ["\"/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.1/source/react-router-7.18.1/packages/react-router/lib/router/history.ts\".Path"] | ["Path"] |
| mode | react-router | 1 | 170 | 0.0058823529411764705 | ["\"/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.1/source/react-router-7.18.1/packages/react-router/lib/server-runtime/mode.ts\".ServerMode"] | ["ServerMode"] |
| links | utils | 1 | 91 | 0.01098901098901099 | ["\"/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.1/source/react-router-7.18.1/packages/react-router/lib/router/utils.ts\".DataRouteMatch"] | ["DataRouteMatch"] |
| headers | utils | 1 | 91 | 0.01098901098901099 | ["\"/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.1/source/react-router-7.18.1/packages/react-router/lib/router/utils.ts\".DataRouteMatch"] | ["DataRouteMatch"] |
| urls | utils | 1 | 91 | 0.01098901098901099 | ["\"/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.1/source/react-router-7.18.1/packages/react-router/lib/router/utils.ts\".stripBasename"] | ["stripBasename"] |
| route-module-annotations | react-router | 2 | 170 | 0.011764705882352941 | ["\"/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.1/source/react-router-7.18.1/packages/react-router/lib/router/links.ts\".LinkDescriptor","\"/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.1/source/react-router-7.18.1/packages/react-router/lib/dom/ssr/routeModules.ts\".MetaDescriptor"] | ["LinkDescriptor","MetaDescriptor"] |
| internal | react-router | 2 | 170 | 0.011764705882352941 | ["\"/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.1/source/react-router-7.18.1/packages/react-router/lib/router/links.ts\".LinkDescriptor","\"/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.1/source/react-router-7.18.1/packages/react-router/lib/dom/ssr/routeModules.ts\".MetaDescriptor"] | ["LinkDescriptor","MetaDescriptor"] |
| route-modules | react-router | 3 | 178 | 0.016853932584269662 | ["\"/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.1/source/react-router-7.18.1/packages/react-router/lib/rsc/server.rsc.ts\".RSCRouteManifest","\"/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.1/source/react-router-7.18.1/packages/react-router/lib/rsc/server.rsc.ts\".RSCRenderPayload","\"/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.1/source/react-router-7.18.1/packages/react-router/lib/dom/ssr/routeModules.ts\".RouteModules"] | ["RSCRouteManifest","RSCRenderPayload","RouteModules"] |

[Full data](./Typescript_Module/ModuleElementsUsageTypescript.csv)

---

## 4. Path Finding

Reveals dependency chain **depth and complexity**.

**All Pairs Shortest Path (APSP)**: Graph diameter = longest shortest path. Metric of structural depth.

**Longest Path**: Max directed path in DAG. Critical for build ordering. Requires acyclic graph — run after cyclic-dependencies domain.

### 4.1 Java Package Path Finding

Intra-artifact pairs highlighted; intermediate paths may cross artifact boundaries.

#### 4.1.1 All Pairs Shortest Path

Graph diameter = longest shortest path. Higher = deeper transitive dependencies.

⚠️ _No data available — Java not detected in this codebase._



#### 4.1.2 Longest Path

Deepest sequential dependency chain. Worst-case build depth if non-parallelized.

⚠️ _No data available — Java not detected in this codebase._



### 4.2 Java Artifact Path Finding

Coarsest view — artifact (JAR) level. Build parallelism and max sequential depth.

#### 4.2.1 All Pairs Shortest Path

Artifact-level graph diameter. Cycles rare at this level.

⚠️ _No data available — Java not detected in this codebase._



#### 4.2.2 Longest Path

Critical path for sequential artifact building.

⚠️ _No data available — Java not detected in this codebase._



### 4.3 TypeScript Module Path Finding

TypeScript module dependency chains. Comparable to Java Package view.

#### 4.3.1 All Pairs Shortest Path

Graph diameter = longest shortest path among module pairs. Higher = deeper transitive imports.

| distance | pairCount | sourceNodeCount | targetNodeCount | examples |
| --- | --- | --- | --- | --- |
| 7 | 1 | 1 | 1 | ["./vendor/turbo-stream-v2/turbo-stream.ts ->./lib/types/utils.ts"] |
| 6 | 7 | 3 | 6 | ["./vendor/turbo-stream-v2/turbo-stream.ts ->./lib/dom/ssr/markup.ts","./vendor/turbo-stream-v2/turbo-stream.ts ->./lib/types/route-module.ts"] |
| 5 | 134 | 37 | 23 | ["./vendor/turbo-stream-v2/turbo-stream.ts ->./lib/actions.ts","./vendor/turbo-stream-v2/turbo-stream.ts ->./lib/errors.ts"] |
| 4 | 181 | 44 | 69 | ["./vendor/turbo-stream-v2/turbo-stream.ts ->./dom-export.ts","./vendor/turbo-stream-v2/turbo-stream.ts ->./index-react-server-client.ts"] |
| 3 | 560 | 51 | 81 | ["./lib/server-runtime/serverHandoff.ts ->./dom-export.ts","./vendor/turbo-stream-v2/unflatten.ts ->./dom-export.ts"] |
| 2 | 947 | 62 | 97 | ["./index-react-server-client.ts ->./dom-export.ts","./lib/context.ts ->./dom-export.ts"] |
| 1 | 350 | 87 | 115 | ["./index-react-server.ts ->./dom-export.ts","./index.ts ->./copy-template.ts"] |

[Full data per project](./Typescript_Module/Module_all_pairs_shortest_paths_distribution_per_project.csv)


![Typescript_Module_AllPairsShortestPath_Bar](./Typescript_Module/Typescript_Module_AllPairsShortestPath_Bar.svg)

![Typescript_Module_AllPairsShortestPath_Pie](./Typescript_Module/Typescript_Module_AllPairsShortestPath_Pie.svg)

![Typescript_Module_AllPairsShortestPath_StackedBar_Log](./Typescript_Module/Typescript_Module_AllPairsShortestPath_StackedBar_Log.svg)

![Typescript_Module_AllPairsShortestPath_StackedBar_Normalised](./Typescript_Module/Typescript_Module_AllPairsShortestPath_StackedBar_Normalised.svg)

![Typescript_Module_GraphDiameter_per_Project](./Typescript_Module/Typescript_Module_GraphDiameter_per_Project.svg)

#### 4.3.2 Longest Path

Deepest sequential TypeScript import chain.

| distance | pathsCount |
| --- | --- |
| 5 | 1 |
| 4 | 2 |
| 3 | 6 |
| 2 | 15 |
| 1 | 28 |
| 0 | 15 |

[Full data per project](./Typescript_Module/Module_longest_paths_distribution.csv)


![Typescript_Module_LongestPath_Bar](./Typescript_Module/Typescript_Module_LongestPath_Bar.svg)

![Typescript_Module_LongestPath_Pie](./Typescript_Module/Typescript_Module_LongestPath_Pie.svg)

![Typescript_Module_LongestPath_StackedBar_Log](./Typescript_Module/Typescript_Module_LongestPath_StackedBar_Log.svg)

![Typescript_Module_LongestPath_StackedBar_Normalised](./Typescript_Module/Typescript_Module_LongestPath_StackedBar_Normalised.svg)

![Typescript_Module_MaxLongestPath_per_Project](./Typescript_Module/Typescript_Module_MaxLongestPath_per_Project.svg)

---

## 5. Topological Sort

Assigns **build level** to each node: Level 0 (no dependencies) → Level N (depends on level N−1).

**Critical path** = max level = min sequential build steps with full parallelism. Highest-level node = most central.

### 5.1 Critical Path Lengths

Max build level per abstraction. Higher = deeper sequential chain.

| abstractionLevel | nodeCount | maxBuildLevel |
| --- | --- | --- |
| Java Package | 7 | 4 |
| TypeScript Module | 39 | 5 |

Full topological sort results (node-level build order and level assignments) are in the abstraction-level CSV files under each subdirectory of `reports/internal-dependencies/`.

---

## 6. Graph Visualizations

Directed graphs: node color = build level (darker = higher level = more transitive deps above).

### 6.1 Java Artifact Graphs

**Build levels**: Full artifact hierarchy. **Longest paths**: Isolated chain + contributor view.



### 6.2 TypeScript Module Graphs

**Build levels**: Module layering view. **Longest paths**: Isolated chain + contributor view.


![TypeScript Module Build Levels](./Typescript_Module/Graph_Visualizations/TypeScriptModuleBuildLevels.svg)


![TypeScript Module Longest Paths (Isolated)](./Typescript_Module/Graph_Visualizations/TypeScriptModuleLongestPathsIsolated.svg)


![TypeScript Module Longest Paths (with contributors)](./Typescript_Module/Graph_Visualizations/TypeScriptModuleLongestPaths.svg)


### 6.3 NPM Package Graphs

Build levels and longest paths for NPM packages (prod + dev dependencies).


![NPM Package Build Levels](./NPM_NonDevPackage/Graph_Visualizations/NpmPackageBuildLevels.svg)


![NPM Non-Dev Package Longest Paths (Isolated)](./NPM_NonDevPackage/Graph_Visualizations/NpmNonDevPackageLongestPathsIsolated.svg)


![NPM Non-Dev Package Longest Paths (with contributors)](./NPM_NonDevPackage/Graph_Visualizations/NpmNonDevPackageLongestPaths.svg)


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

⚠️ _No data available — Java not detected in this codebase._

⚠️ _No data available — Java not detected in this codebase._

⚠️ _No data available — Java not detected in this codebase._

### 8.2 Java Packages (including sub-packages)

⚠️ _No data available — Java not detected in this codebase._

⚠️ _No data available — Java not detected in this codebase._

⚠️ _No data available — Java not detected in this codebase._

### 8.3 TypeScript Modules


![TypeScript Module Main Sequence](./Typescript_Module/Typescript_Module_MainSequence.svg)



![TypeScript Module Incoming Dependencies](./Typescript_Module/Typescript_Module_IncomingDependencies_Bar.svg)



![TypeScript Module Outgoing Dependencies](./Typescript_Module/Typescript_Module_OutgoingDependencies_Bar.svg)


---

## 9. Visibility Metrics

Measures public vs. internal API exposure. High visibility = exposed more than necessary; low = tightly encapsulated.

**Percentile plots** (p25, p50, p75) vs. size (log scale): large artifacts vs. small visibility patterns.

**Scatter charts**: Artifact/project median visibility vs. size • Package/module individual visibility vs. size.

### 9.1 Java Visibility

#### 9.1.1 Artifact-Level Visibility Percentiles

⚠️ _No data available — Java not detected in this codebase._

#### 9.1.2 Artifact-Level Relative Visibility

⚠️ _No data available — Java not detected in this codebase._

#### 9.1.3 Package-Level Relative Visibility

⚠️ _No data available — Java not detected in this codebase._

### 9.2 TypeScript Visibility

#### 9.2.1 Project-Level Visibility Percentiles


![TypeScript Module Visibility Percentiles](./Typescript_Module/Typescript_Module_VisibilityPercentiles.svg)


#### 9.2.2 Project-Level Relative Visibility


![TypeScript Project Relative Visibility](./Typescript_Module/Typescript_Project_RelativeVisibility.svg)


#### 9.2.3 Module-Level Relative Visibility


![TypeScript Module Relative Visibility](./Typescript_Module/Typescript_Module_RelativeVisibility.svg)


---

## 10. Code Vocabulary

**Word cloud**: Vocabulary from all code element names (filtered for generic words). Reveals domain concepts and naming patterns.


![Code Names Wordcloud](./CodeNamesWordcloud.svg)

