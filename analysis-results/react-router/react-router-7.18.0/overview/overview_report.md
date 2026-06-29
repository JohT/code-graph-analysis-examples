---
title: "Overview Report"
generated: "2026-06-29"
model_version: "v4.0.1"
dataset: "react-router-7.18.0"
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
| ["Git","Update","Change"] | 59408 | 28.402185813249698 |
| ["Type","TS","NotIdentified"] | 54184 | 25.90465991289257 |
| ["Git","Change","Create"] | 17514 | 8.373213747866536 |
| ["Git","Commit"] | 10970 | 5.244613155994971 |
| ["Type","TS","Declared"] | 10782 | 5.154732821142915 |
| ["Git","Change","Delete"] | 9784 | 4.677602107407 |
| ["Type","TS","Primitive"] | 9726 | 4.649873067931366 |
| ["File","Git"] | 6428 | 3.073142512920298 |
| ["Type","TS","Union"] | 5471 | 2.6156133615723323 |
| ["Type","TS","Literal"] | 3402 | 1.626451591312205 |

[Full data](./Node_label_combination_count.csv)


![Overview_General_Node_Label_Combination_Count_High](./Overview_General_Node_Label_Combination_Count_High.svg)

![Overview_General_Node_Label_Combination_Count_Low](./Overview_General_Node_Label_Combination_Count_Low.svg)

---

### 2.2 Node labels

Shows the number of nodes carrying each individual label, sorted by count descending.

| nodeLabel | nodesWithThatLabel | nodesWithThatLabelPercent |
| --- | --- | --- |
| Git | 110120 | 52.6469280527043 |
| TS | 94630 | 45.2413621651599 |
| Change | 89718 | 42.892999373706175 |
| Type | 88635 | 42.375231274531835 |
| Update | 59408 | 28.402185813249698 |
| NotIdentified | 54184 | 25.90465991289257 |
| Create | 17514 | 8.373213747866536 |
| Declared | 11027 | 5.2718641085830935 |
| Commit | 10970 | 5.244613155994971 |
| Delete | 9784 | 4.677602107407 |

[Full data](./Node_label_count.csv)



---

### 2.3 Relationship types

Shows the number of relationships for each type and their share of the total relationship count.

| relationshipType | nodesWithThatRelationshipType | nodesWithThatRelationshipTypePercent |
| --- | --- | --- |
| CONTAINS_CHANGE | 89718 | 19.938662577505166 |
| MODIFIES | 89718 | 19.938662577505166 |
| CONTAINS | 73591 | 16.354645865279906 |
| UPDATES | 59408 | 13.202657954974775 |
| COMMITTED | 21940 | 4.875880614263172 |
| CREATES | 20526 | 4.561637442496166 |
| DELETES | 12716 | 2.8259661755228125 |
| HAS_PARENT | 12061 | 2.6804009156165964 |
| HAS_COMMIT | 10970 | 2.437940307131586 |
| DEPENDS_ON | 10486 | 2.330377580727604 |

[Full data](./Relationship_type_count.csv)


![Overview_General_Relationship_Type_Count_High](./Overview_General_Relationship_Type_Count_High.svg)

![Overview_General_Relationship_Type_Count_Low](./Overview_General_Relationship_Type_Count_Low.svg)

---

### 2.4 Node labels and their relationships

Shows which node labels are connected by each relationship type, with count and percentage share.
| sourceLabels | relationshipType | targetLabels | relationshipCount |
| --- | --- | --- | --- |
| ["Git","Update","Change"] | UPDATES | ["Git"] | 59408 |
| ["Git","Commit"] | CONTAINS_CHANGE | ["Git","Update","Change"] | 59408 |
| ["Git","Update","Change"] | MODIFIES | ["Git"] | 59408 |
| ["TS","Union"] | CONTAINS | ["TS","NotIdentified"] | 53911 |
| ["Git","Commit"] | CONTAINS_CHANGE | ["Git","Change","Create"] | 17514 |
| ["Git","Change","Create"] | CREATES | ["Git"] | 17514 |
| ["Git","Change","Create"] | MODIFIES | ["Git"] | 17514 |
| ["Git","Commit"] | HAS_PARENT | ["Git","Commit"] | 12061 |
| ["Repository","Git"] | HAS_COMMIT | ["Git","Commit"] | 10970 |
| ["Committer","Person","Git","Author"] | COMMITTED | ["Git","Commit"] | 10970 |

[Full data](./Node_labels_and_their_relationships.csv)

---

### 2.5 Graph density

Statistical measures of the graph structure: node count, relationship count, and density metric.



---

### 2.6 Dependency node labels

Shows node labels present on dependency nodes — nodes that represent external dependencies not scanned as artifacts.

| sourceLabels | targetLabels | numberOfNodes | percentageOfTotalNodes |
| --- | --- | --- | --- |
| TS,Function | TS,ExternalDeclaration | 1186 | 0.57 |
| TS,Function | TS,Function | 826 | 0.39 |
| TS,Function | TS,ExternalModule | 445 | 0.21 |
| TS,Variable | TS,ExternalDeclaration | 383 | 0.18 |
| TS,Function | TS,Property | 381 | 0.18 |
| TS,Function | TS,Interface | 374 | 0.18 |
| File,TS,Local,Module | TS,ExternalDeclaration | 310 | 0.15 |
| TS,Function | TS,TypeAlias | 307 | 0.15 |
| TS,Function | TS,Variable | 295 | 0.14 |
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
| 209167 | 449970 | 11 | 159 | 1333 | 1561 | 340 | 142 | 13 | 127 |

[Full data](./Overview_size_for_Typescript.csv)

### 4.2 TypeScript overview charts


![Overview_Typescript_Elements_Per_Module_Stacked](./Overview_Typescript_Elements_Per_Module_Stacked.svg)

![Overview_Typescript_Function_Elements_Per_Module_Normalized](./Overview_Typescript_Function_Elements_Per_Module_Normalized.svg)

![Overview_Typescript_Interface_Elements_Per_Module_Normalized](./Overview_Typescript_Interface_Elements_Per_Module_Normalized.svg)

![Overview_Typescript_TypeAlias_Elements_Per_Module_Normalized](./Overview_Typescript_TypeAlias_Elements_Per_Module_Normalized.svg)

![Overview_Typescript_Variable_Elements_Per_Module_Normalized](./Overview_Typescript_Variable_Elements_Per_Module_Normalized.svg)
