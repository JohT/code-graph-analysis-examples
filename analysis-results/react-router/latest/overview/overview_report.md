---
title: "Overview Report"
generated: "2026-11-01"
model_version: "v5.0.0"
dataset: "react-router-7.18.4"
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
| ["Git","Update","Change"] | 59569 | 28.430904630539995 |
| ["Type","TS","NotIdentified"] | 54186 | 25.86172335124712 |
| ["Git","Change","Create"] | 17536 | 8.369526827731693 |
| ["Git","Commit"] | 10997 | 5.248613510753048 |
| ["Type","TS","Declared"] | 10795 | 5.1522035872127985 |
| ["Git","Change","Delete"] | 9795 | 4.674926738003647 |
| ["Type","TS","Primitive"] | 9734 | 4.645812850201888 |
| ["File","Git"] | 6450 | 3.0784356773990322 |
| ["Type","TS","Union"] | 5473 | 2.6121361957216904 |
| ["Type","TS","Literal"] | 3404 | 1.6246503947079542 |

[Full data](./Node_label_combination_count.csv)


![Overview_General_Node_Label_Combination_Count_High](./Overview_General_Node_Label_Combination_Count_High.svg)

![Overview_General_Node_Label_Combination_Count_Low](./Overview_General_Node_Label_Combination_Count_Low.svg)

---

### 2.2 Node labels

Shows the number of nodes carrying each individual label, sorted by count descending.

| nodeLabel | nodesWithThatLabel | nodesWithThatLabelPercent |
| --- | --- | --- |
| Git | 110409 | 52.69565964433329 |
| TS | 94680 | 45.18857208312254 |
| Change | 89912 | 42.912916066093295 |
| Type | 88658 | 42.31441089718502 |
| Update | 59569 | 28.430904630539995 |
| NotIdentified | 54186 | 25.86172335124712 |
| Create | 17536 | 8.369526827731693 |
| Declared | 11040 | 5.269136415269041 |
| Commit | 10997 | 5.248613510753048 |
| Delete | 9795 | 4.674926738003647 |

[Full data](./Node_label_count.csv)



---

### 2.3 Relationship types

Shows the number of relationships for each type and their share of the total relationship count.

| relationshipType | nodesWithThatRelationshipType | nodesWithThatRelationshipTypePercent |
| --- | --- | --- |
| CONTAINS_CHANGE | 89912 | 19.965093505882145 |
| MODIFIES | 89912 | 19.965093505882145 |
| CONTAINS | 73597 | 16.34232345796343 |
| UPDATES | 59569 | 13.227385166072308 |
| COMMITTED | 21994 | 4.883800455649656 |
| CREATES | 20548 | 4.562714002122812 |
| DELETES | 12727 | 2.826049304312684 |
| HAS_PARENT | 12088 | 2.6841584026504064 |
| HAS_COMMIT | 10997 | 2.441900227824828 |
| DEPENDS_ON | 10064 | 2.234726188308545 |

[Full data](./Relationship_type_count.csv)


![Overview_General_Relationship_Type_Count_High](./Overview_General_Relationship_Type_Count_High.svg)

![Overview_General_Relationship_Type_Count_Low](./Overview_General_Relationship_Type_Count_Low.svg)

---

### 2.4 Node labels and their relationships

Shows which node labels are connected by each relationship type, with count and percentage share.
| sourceLabels | relationshipType | targetLabels | relationshipCount |
| --- | --- | --- | --- |
| ["Git","Commit"] | CONTAINS_CHANGE | ["Git","Update","Change"] | 59569 |
| ["Git","Update","Change"] | MODIFIES | ["Git"] | 59569 |
| ["Git","Update","Change"] | UPDATES | ["Git"] | 59569 |
| ["TS","Union"] | CONTAINS | ["TS","NotIdentified"] | 53911 |
| ["Git","Commit"] | CONTAINS_CHANGE | ["Git","Change","Create"] | 17536 |
| ["Git","Change","Create"] | MODIFIES | ["Git"] | 17536 |
| ["Git","Change","Create"] | CREATES | ["Git"] | 17536 |
| ["Git","Commit"] | HAS_PARENT | ["Git","Commit"] | 12088 |
| ["Repository","Git"] | HAS_COMMIT | ["Git","Commit"] | 10997 |
| ["Author","Person","Git","Committer"] | COMMITTED | ["Git","Commit"] | 10997 |

[Full data](./Node_labels_and_their_relationships.csv)

---

### 2.5 Graph density

Statistical measures of the graph structure: node count, relationship count, and density metric.



---

### 2.6 Dependency node labels

Shows node labels present on dependency nodes — nodes that represent external dependencies not scanned as artifacts.

| sourceLabels | targetLabels | numberOfNodes | percentageOfTotalNodes |
| --- | --- | --- | --- |
| TS,Function | TS,ExternalDeclaration | 1189 | 0.57 |
| TS,Function | TS,Function | 834 | 0.4 |
| TS,Function | TS,ExternalModule | 446 | 0.21 |
| TS,Function | TS,Property | 384 | 0.18 |
| TS,Variable | TS,ExternalDeclaration | 383 | 0.18 |
| TS,Function | TS,Interface | 376 | 0.18 |
| File,TS,Local,Module | TS,ExternalDeclaration | 310 | 0.15 |
| TS,Function | TS,TypeAlias | 308 | 0.15 |
| TS,Function | TS,Variable | 296 | 0.14 |
| StronglyConnectedComponent,ModuleMembers | StronglyConnectedComponent,ModuleMembers | 195 | 0.09 |

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
| 209522 | 450346 | 11 | 160 | 1337 | 1561 | 341 | 142 | 14 | 128 |

[Full data](./Overview_size_for_Typescript.csv)

### 4.2 TypeScript overview charts


![Overview_Typescript_Elements_Per_Module_Stacked](./Overview_Typescript_Elements_Per_Module_Stacked.svg)

![Overview_Typescript_Function_Elements_Per_Module_Normalized](./Overview_Typescript_Function_Elements_Per_Module_Normalized.svg)

![Overview_Typescript_Interface_Elements_Per_Module_Normalized](./Overview_Typescript_Interface_Elements_Per_Module_Normalized.svg)

![Overview_Typescript_TypeAlias_Elements_Per_Module_Normalized](./Overview_Typescript_TypeAlias_Elements_Per_Module_Normalized.svg)

![Overview_Typescript_Variable_Elements_Per_Module_Normalized](./Overview_Typescript_Variable_Elements_Per_Module_Normalized.svg)
