# 📊 Archetypes Report

## 1. Executive Overview

This report classifies code units into structural archetypes based on graph-based features.
The goal is to identify code that plays a distinctive structural role — such as being a widely-referenced authority, a critical bottleneck, or a highly-connected hub — using centrality and clustering metrics.

## 📚 Table of Contents

1. [Executive Overview](#1-executive-overview)
1. [Deep Dives by Abstraction Level](#2-deep-dives-by-abstraction-level)

---

### 1.1 Archetypes in total

| Analyzed Units | Authorities | Bottlenecks | Hubs |
| --- | --- | --- | --- |
| 1483 | 27 | 23 | 8 |

### 1.2 Overview of Analyzed Structures

| Abstraction Level | Units | Authorities | Bottlenecks | Hubs |
| --- | --- | --- | --- | --- |
| Package,Java | 157 | 10 | 10 | 5 |
| Artifact,Jar,Archive,Zip,Java | 11 | 7 | 3 | 1 |
| Type,Java,Class | 758 | 6 | 4 | 1 |
| Type,Java,Interface | 392 | 3 | 4 | 0 |
| Type,Java,Record | 63 | 1 | 2 | 0 |
| Type,Java,Class,Throwable | 43 | 0 | 0 | 0 |
| Type,Java,Annotation | 43 | 0 | 0 | 1 |
| Type,Java,Enum | 16 | 0 | 0 | 0 |

### 1.3 Overview Charts

#### Treemap Charts

![JavaTreemap1ArchetypesOverviewPerDirectory](./JavaTreemap1ArchetypesOverviewPerDirectory.svg)

![JavaTreemap2ArchetypeAuthorityPerDirectory](./JavaTreemap2ArchetypeAuthorityPerDirectory.svg)

![JavaTreemap3ArchetypeBottleneckPerDirectory](./JavaTreemap3ArchetypeBottleneckPerDirectory.svg)

![JavaTreemap4ArchetypeHubPerDirectory](./JavaTreemap4ArchetypeHubPerDirectory.svg)

---

## 2. Deep Dives by Abstraction Level

### 2.1 Java Artifact

#### Archetype Distribution

| Archetype | Count | Max. Rank | Examples |
| --- | --- | --- | --- |
| Authority | 7 | 7 | /axon-common-5.1.2.jar, /axon-server-connector-5.1.2.jar, /axon-update-5.1.2.jar |
| Bottleneck | 3 | 3 | /axon-conversion-5.1.2.jar, /axon-modelling-5.1.2.jar, /axon-eventsourcing-5.1.2.jar |
| Hub | 1 | 1 | /axon-common-5.1.2.jar |

#### Graph Visualizations

#### Graph Visualizations

##### TopHub Graph Visualizations

![TopHub 1](./Java_Artifact/GraphVisualizations/TopHub1.svg)

---

##### TopBottleneck Graph Visualizations

![TopBottleneck 1](./Java_Artifact/GraphVisualizations/TopBottleneck1.svg)

![TopBottleneck 2](./Java_Artifact/GraphVisualizations/TopBottleneck2.svg)

![TopBottleneck 3](./Java_Artifact/GraphVisualizations/TopBottleneck3.svg)

---

##### TopAuthority Graph Visualizations

![TopAuthority 1](./Java_Artifact/GraphVisualizations/TopAuthority1.svg)

![TopAuthority 2](./Java_Artifact/GraphVisualizations/TopAuthority2.svg)

![TopAuthority 3](./Java_Artifact/GraphVisualizations/TopAuthority3.svg)

![TopAuthority 4](./Java_Artifact/GraphVisualizations/TopAuthority4.svg)

![TopAuthority 5](./Java_Artifact/GraphVisualizations/TopAuthority5.svg)

--

### 2.2 Java Package

#### Archetype Distribution

| Archetype | Count | Max. Rank | Examples |
| --- | --- | --- | --- |
| Authority | 10 | 10 | org.axonframework.common, org.axonframework.common.io, org.axonframework.common.function |
| Bottleneck | 10 | 10 | org.axonframework.messaging.core.annotation, org.axonframework.messaging.core, org.axonframework.messaging.core.sequencing |
| Hub | 5 | 5 | org.axonframework.common, org.axonframework.messaging.core, org.axonframework.common.infra |

#### Graph Visualizations

#### Graph Visualizations

##### TopHub Graph Visualizations

![TopHub 1](./Java_Package/GraphVisualizations/TopHub1.svg)

![TopHub 2](./Java_Package/GraphVisualizations/TopHub2.svg)

![TopHub 3](./Java_Package/GraphVisualizations/TopHub3.svg)

![TopHub 4](./Java_Package/GraphVisualizations/TopHub4.svg)

![TopHub 5](./Java_Package/GraphVisualizations/TopHub5.svg)

---

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

--

### 2.3 Java Type

#### Archetype Distribution

| Archetype | Count | Max. Rank | Examples |
| --- | --- | --- | --- |
| Authority | 10 | 10 | org.axonframework.common.TypeReference, org.axonframework.common.TypeReference$2, org.axonframework.common.TypeReference$1 |
| Bottleneck | 10 | 10 | org.axonframework.messaging.core.MessageStream, org.axonframework.messaging.core.Message, org.axonframework.messaging.core.unitofwork.ProcessingContext |
| Hub | 2 | 2 | org.axonframework.common.AxonNonTransientException, org.axonframework.common.Priority |

#### Graph Visualizations

#### Graph Visualizations

##### TopHub Graph Visualizations

![TopHub 1](./Java_Type/GraphVisualizations/TopHub1.svg)

![TopHub 2](./Java_Type/GraphVisualizations/TopHub2.svg)

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

--

