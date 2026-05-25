---
title: "Overview Report"
generated: "2026-05-25"
model_version: "v4.0.1"
dataset: "react-router-7.15.1"
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
| ["Git","Update","Change"] | 58796 | 28.177491936759274 |
| ["Type","TS","NotIdentified"] | 54184 | 25.967229456108655 |
| ["Git","Change","Create"] | 17448 | 8.361808274586295 |
| ["Git","Commit"] | 10881 | 5.214628372064046 |
| ["Type","TS","Declared"] | 10745 | 5.149451507933846 |
| ["Type","TS","Primitive"] | 9683 | 4.640496877740663 |
| ["Git","Change","Delete"] | 9106 | 4.3639744468353285 |
| ["File","Git"] | 6386 | 3.0604371642313204 |
| ["Type","TS","Union"] | 5463 | 2.618097123112387 |
| ["Type","TS","Literal"] | 3396 | 1.6275046366629446 |

[Full data](./Node_label_combination_count.csv)


![Overview_General_Node_Label_Combination_Count_High](./Overview_General_Node_Label_Combination_Count_High.svg)

![Overview_General_Node_Label_Combination_Count_Low](./Overview_General_Node_Label_Combination_Count_Low.svg)

---

### 2.2 Node labels

Shows the number of nodes carrying each individual label, sorted by count descending.

| nodeLabel | nodesWithThatLabel | nodesWithThatLabelPercent |
| --- | --- | --- |
| Git | 108572 | 52.0322242084126 |
| TS | 94446 | 45.26245668853606 |
| Type | 88506 | 42.41576129931995 |
| Change | 88356 | 42.34387505211753 |
| Update | 58796 | 28.177491936759274 |
| NotIdentified | 54184 | 25.967229456108655 |
| Create | 17448 | 8.361808274586295 |
| Declared | 10990 | 5.266865711697809 |
| Commit | 10881 | 5.214628372064046 |
| Primitive | 9683 | 4.640496877740663 |

[Full data](./Node_label_count.csv)



---

### 2.3 Relationship types

Shows the number of relationships for each type and their share of the total relationship count.

| relationshipType | nodesWithThatRelationshipType | nodesWithThatRelationshipTypePercent |
| --- | --- | --- |
| CONTAINS_CHANGE | 88356 | 19.74678452100258 |
| MODIFIES | 88356 | 19.74678452100258 |
| CONTAINS | 73593 | 16.447384594754663 |
| UPDATES | 58796 | 13.14038596922527 |
| COMMITTED | 21762 | 4.863614522455274 |
| CREATES | 20454 | 4.571288091273788 |
| DELETES | 12032 | 2.6890455810211313 |
| HAS_PARENT | 11965 | 2.6740716736135166 |
| HAS_COMMIT | 10881 | 2.431807261227637 |
| DEPENDS_ON | 10399 | 2.3240845243549484 |

[Full data](./Relationship_type_count.csv)


![Overview_General_Relationship_Type_Count_High](./Overview_General_Relationship_Type_Count_High.svg)

![Overview_General_Relationship_Type_Count_Low](./Overview_General_Relationship_Type_Count_Low.svg)

---

### 2.4 Node labels and their relationships

Shows which node labels are connected by each relationship type, with count and percentage share.
| sourceLabels | relationshipType | targetLabels | relationshipCount |
| --- | --- | --- | --- |
| ["Git","Commit"] | CONTAINS_CHANGE | ["Git","Update","Change"] | 58796 |
| ["Git","Update","Change"] | UPDATES | ["Git"] | 58796 |
| ["Git","Update","Change"] | MODIFIES | ["Git"] | 58796 |
| ["TS","Union"] | CONTAINS | ["TS","NotIdentified"] | 53911 |
| ["Git","Commit"] | CONTAINS_CHANGE | ["Git","Change","Create"] | 17448 |
| ["Git","Change","Create"] | CREATES | ["Git"] | 17448 |
| ["Git","Change","Create"] | MODIFIES | ["Git"] | 17448 |
| ["Git","Commit"] | HAS_PARENT | ["Git","Commit"] | 11965 |
| ["Author","Person","Git","Committer"] | COMMITTED | ["Git","Commit"] | 10881 |
| ["Repository","Git"] | HAS_COMMIT | ["Git","Commit"] | 10881 |

[Full data](./Node_labels_and_their_relationships.csv)

---

### 2.5 Graph density

Statistical measures of the graph structure: node count, relationship count, and density metric.



---

### 2.6 Dependency node labels

Shows node labels present on dependency nodes — nodes that represent external dependencies not scanned as artifacts.

| sourceLabels | targetLabels | numberOfNodes | percentageOfTotalNodes |
| --- | --- | --- | --- |
| TS,Function | TS,ExternalDeclaration | 1168 | 0.56 |
| TS,Function | TS,Function | 808 | 0.39 |
| TS,Function | TS,ExternalModule | 438 | 0.21 |
| TS,Variable | TS,ExternalDeclaration | 382 | 0.18 |
| TS,Function | TS,Property | 377 | 0.18 |
| TS,Function | TS,Interface | 369 | 0.18 |
| File,TS,Local,Module | TS,ExternalDeclaration | 310 | 0.15 |
| TS,Function | TS,TypeAlias | 301 | 0.14 |
| TS,Function | TS,Variable | 287 | 0.14 |
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
| 208663 | 447445 | 11 | 159 | 1321 | 1555 | 337 | 141 | 13 | 124 |

[Full data](./Overview_size_for_Typescript.csv)

### 4.2 TypeScript overview charts


![Overview_Typescript_Elements_Per_Module_Stacked](./Overview_Typescript_Elements_Per_Module_Stacked.svg)

![Overview_Typescript_Function_Elements_Per_Module_Normalized](./Overview_Typescript_Function_Elements_Per_Module_Normalized.svg)

![Overview_Typescript_Interface_Elements_Per_Module_Normalized](./Overview_Typescript_Interface_Elements_Per_Module_Normalized.svg)

![Overview_Typescript_TypeAlias_Elements_Per_Module_Normalized](./Overview_Typescript_TypeAlias_Elements_Per_Module_Normalized.svg)

![Overview_Typescript_Variable_Elements_Per_Module_Normalized](./Overview_Typescript_Variable_Elements_Per_Module_Normalized.svg)
