---
title: "Overview Report"
generated: "2026-05-16"
model_version: "v4.0.0"
dataset: "react-router-7.13.2"
authors: ["JohT/code-graph-analysis-pipeline"]
---

# Overview Report

## 1. Overview

High-level summary of graph database contents: general graph structure (node labels, relationships), Java artifacts, and TypeScript modules.

## 📚 Table of Contents

1. [Overview](#1-overview)
1. [General](#2-general)
1. [Java](#3-java)
1. [TypeScript](#4-typescript)

---

## 2. General

### 2.1 Node label combinations

Shows how many nodes carry each combination of labels and their share of the total node count.

| nodeLabels | nodesWithThatLabels | nodesWithThatLabelsPercent |
| --- | --- | --- |
| ["Git","Change","Update"] | 57173 | 27.83427862028675 |
| ["Type","TS","NotIdentified"] | 54186 | 26.380078381733647 |
| ["Git","Change","Create"] | 17009 | 8.280713711934958 |
| ["Git","Commit"] | 10711 | 5.2145760814001605 |
| ["Type","TS","Declared"] | 10639 | 5.179523380638251 |
| ["Type","TS","Primitive"] | 9616 | 4.6814829239794555 |
| ["Git","Change","Delete"] | 8942 | 4.353350697402692 |
| ["File","Git"] | 6207 | 3.021834911516273 |
| ["Type","TS","Union"] | 5440 | 2.64842627978871 |
| ["Type","TS","Literal"] | 3421 | 1.665490129256834 |

[Full data](./Node_label_combination_count.csv)


![Overview_General_Node_Label_Combination_Count_High](./Overview_General_Node_Label_Combination_Count_High.svg)

![Overview_General_Node_Label_Combination_Count_Low](./Overview_General_Node_Label_Combination_Count_Low.svg)

---

### 2.2 Node labels

Shows the number of nodes carrying each individual label, sorted by count descending.

| nodeLabel | nodesWithThatLabel | nodesWithThatLabelPercent |
| --- | --- | --- |
| Git | 105846 | 51.53039117840365 |
| TS | 94102 | 45.812906209683305 |
| Type | 88226 | 42.95221635305859 |
| Change | 86046 | 41.890898468878554 |
| Update | 57173 | 27.83427862028675 |
| NotIdentified | 54186 | 26.380078381733647 |
| Create | 17009 | 8.280713711934958 |
| Declared | 10883 | 5.298313088775833 |
| Commit | 10711 | 5.2145760814001605 |
| Primitive | 9616 | 4.6814829239794555 |

[Full data](./Node_label_count.csv)



---

### 2.3 Relationship types

Shows the number of relationships for each type and their share of the total relationship count.

| relationshipType | nodesWithThatRelationshipType | nodesWithThatRelationshipTypePercent |
| --- | --- | --- |
| CONTAINS_CHANGE | 86046 | 19.631624697982904 |
| MODIFIES | 86046 | 19.631624697982904 |
| CONTAINS | 73561 | 16.78313860502894 |
| UPDATES | 57173 | 13.04417263856282 |
| COMMITTED | 21422 | 4.887486510473348 |
| CREATES | 19931 | 4.547310878547489 |
| DELETES | 11792 | 2.690376292199688 |
| HAS_PARENT | 11780 | 2.6876384601519954 |
| HAS_COMMIT | 10711 | 2.443743255236674 |
| DEPENDS_ON | 10273 | 2.343812385495878 |

[Full data](./Relationship_type_count.csv)


![Overview_General_Relationship_Type_Count_High](./Overview_General_Relationship_Type_Count_High.svg)

![Overview_General_Relationship_Type_Count_Low](./Overview_General_Relationship_Type_Count_Low.svg)

---

### 2.4 Node labels and their relationships

Shows which node labels are connected by each relationship type, with count and percentage share.
| sourceLabels | relationshipType | targetLabels | relationshipCount |
| --- | --- | --- | --- |
| ["Git","Commit"] | CONTAINS_CHANGE | ["Git","Change","Update"] | 57173 |
| ["Git","Change","Update"] | UPDATES | ["Git"] | 57173 |
| ["Git","Change","Update"] | MODIFIES | ["Git"] | 57173 |
| ["TS","Union"] | CONTAINS | ["TS","NotIdentified"] | 53911 |
| ["Git","Commit"] | CONTAINS_CHANGE | ["Git","Change","Create"] | 17009 |
| ["Git","Change","Create"] | CREATES | ["Git"] | 17009 |
| ["Git","Change","Create"] | MODIFIES | ["Git"] | 17009 |
| ["Git","Commit"] | HAS_PARENT | ["Git","Commit"] | 11780 |
| ["Author","Person","Git","Committer"] | COMMITTED | ["Git","Commit"] | 10711 |
| ["Repository","Git"] | HAS_COMMIT | ["Git","Commit"] | 10711 |

[Full data](./Node_labels_and_their_relationships.csv)

---

### 2.5 Graph density

Statistical measures of the graph structure: node count, relationship count, and density metric.



---

### 2.6 Dependency node labels

Shows node labels present on dependency nodes — nodes that represent external dependencies not scanned as artifacts.

| sourceLabels | targetLabels | numberOfNodes | percentageOfTotalNodes |
| --- | --- | --- | --- |
| TS,Function | TS,ExternalDeclaration | 1187 | 0.58 |
| TS,Function | TS,Function | 813 | 0.4 |
| TS,Function | TS,ExternalModule | 441 | 0.21 |
| TS,Variable | TS,ExternalDeclaration | 378 | 0.18 |
| TS,Function | TS,Property | 372 | 0.18 |
| TS,Function | TS,Interface | 365 | 0.18 |
| File,TS,Local,Module | TS,ExternalDeclaration | 310 | 0.15 |
| TS,Function | TS,TypeAlias | 295 | 0.14 |
| TS,Function | TS,Variable | 271 | 0.13 |
| TS,TypeAlias | TS,TypeAlias | 188 | 0.09 |

[Full data](./Dependency_node_labels.csv)

---

## 3. Java

### 3.1 Artifact size

Overview of scanned Java artifacts: number of packages, types, methods, and lines of code.

> No overview data available.
> Please run the analysis pipeline first to scan and import code artifacts into the graph database (e.g., `analyze.sh`), then start Neo4j and re-run the overview reports.

### 3.2 Java overview charts



---

## 4. TypeScript

### 4.1 Module size

Overview of scanned TypeScript modules: number of exported language elements per module.

| nodeCount | relationshipCount | projectCount | moduleCount | functionCount | objectCount | typeAliasCount | interfaceCount | classCount | methodCount |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 205405 | 438303 | 11 | 159 | 1308 | 1525 | 332 | 141 | 12 | 121 |

[Full data](./Overview_size_for_Typescript.csv)

### 4.2 TypeScript overview charts


![Overview_Typescript_Elements_Per_Module_Stacked](./Overview_Typescript_Elements_Per_Module_Stacked.svg)

![Overview_Typescript_Function_Elements_Per_Module_Normalized](./Overview_Typescript_Function_Elements_Per_Module_Normalized.svg)

![Overview_Typescript_Interface_Elements_Per_Module_Normalized](./Overview_Typescript_Interface_Elements_Per_Module_Normalized.svg)

![Overview_Typescript_TypeAlias_Elements_Per_Module_Normalized](./Overview_Typescript_TypeAlias_Elements_Per_Module_Normalized.svg)

![Overview_Typescript_Variable_Elements_Per_Module_Normalized](./Overview_Typescript_Variable_Elements_Per_Module_Normalized.svg)
