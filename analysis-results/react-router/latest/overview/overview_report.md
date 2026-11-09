---
title: "Overview Report"
generated: "2026-11-09"
model_version: "v5.0.1"
dataset: "react-router-7.18.5"
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
| ["Git","Update","Change"] | 59603 | 28.501680845060996 |
| ["Type","TS","NotIdentified"] | 54186 | 25.911314502130345 |
| ["Git","Change","Create"] | 17539 | 8.387010391113279 |
| ["Git","Commit"] | 11000 | 5.260112566408921 |
| ["Type","TS","Declared"] | 10796 | 5.16256138790461 |
| ["Git","Change","Delete"] | 9797 | 4.684847528464382 |
| ["Type","TS","Primitive"] | 9747 | 4.660937925889796 |
| ["File","Git"] | 6453 | 3.08577330827607 |
| ["Type","TS","Union"] | 5476 | 2.6185796739686595 |
| ["Type","TS","Literal"] | 3406 | 1.6287221273807988 |

[Full data](./Node_label_combination_count.csv)


![Overview_General_Node_Label_Combination_Count_High](./Overview_General_Node_Label_Combination_Count_High.svg)

![Overview_General_Node_Label_Combination_Count_Low](./Overview_General_Node_Label_Combination_Count_Low.svg)

---

### 2.2 Node labels

Shows the number of nodes carrying each individual label, sorted by count descending.

| nodeLabel | nodesWithThatLabel | nodesWithThatLabelPercent |
| --- | --- | --- |
| Git | 109976 | 52.58964905485342 |
| TS | 94712 | 45.290525580883795 |
| Change | 89951 | 43.013853223731715 |
| Type | 88678 | 42.405114742182754 |
| Update | 59603 | 28.501680845060996 |
| NotIdentified | 54186 | 25.911314502130345 |
| Create | 17539 | 8.387010391113279 |
| Declared | 11041 | 5.279718440520082 |
| Commit | 11000 | 5.260112566408921 |
| Delete | 9797 | 4.684847528464382 |

[Full data](./Node_label_count.csv)



---

### 2.3 Relationship types

Shows the number of relationships for each type and their share of the total relationship count.

| relationshipType | nodesWithThatRelationshipType | nodesWithThatRelationshipTypePercent |
| --- | --- | --- |
| CONTAINS_CHANGE | 89951 | 20.007829547198604 |
| MODIFIES | 89951 | 20.007829547198604 |
| CONTAINS | 73603 | 16.371538706211812 |
| UPDATES | 59603 | 13.257514252222634 |
| COMMITTED | 22000 | 4.893466999125849 |
| CREATES | 20551 | 4.571165468137969 |
| DELETES | 12729 | 2.831315519630588 |
| HAS_PARENT | 12091 | 2.689404976655938 |
| HAS_COMMIT | 11000 | 2.4467334995629244 |
| DEPENDS_ON | 10085 | 2.2432097584629176 |

[Full data](./Relationship_type_count.csv)


![Overview_General_Relationship_Type_Count_High](./Overview_General_Relationship_Type_Count_High.svg)

![Overview_General_Relationship_Type_Count_Low](./Overview_General_Relationship_Type_Count_Low.svg)

---

### 2.4 Node labels and their relationships

Shows which node labels are connected by each relationship type, with count and percentage share.
| sourceLabels | relationshipType | targetLabels | relationshipCount |
| --- | --- | --- | --- |
| ["Git","Commit"] | CONTAINS_CHANGE | ["Git","Update","Change"] | 59603 |
| ["Git","Update","Change"] | MODIFIES | ["Git"] | 59603 |
| ["Git","Update","Change"] | UPDATES | ["Git"] | 59603 |
| ["TS","Union"] | CONTAINS | ["TS","NotIdentified"] | 53911 |
| ["Git","Commit"] | CONTAINS_CHANGE | ["Git","Change","Create"] | 17539 |
| ["Git","Change","Create"] | MODIFIES | ["Git"] | 17539 |
| ["Git","Change","Create"] | CREATES | ["Git"] | 17539 |
| ["Git","Commit"] | HAS_PARENT | ["Git","Commit"] | 12091 |
| ["Author","Person","Git","Committer"] | COMMITTED | ["Git","Commit"] | 11000 |
| ["Repository","Git"] | HAS_COMMIT | ["Git","Commit"] | 11000 |

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
| TS,Function | TS,Function | 838 | 0.4 |
| TS,Function | TS,ExternalModule | 446 | 0.21 |
| TS,Function | TS,Property | 388 | 0.19 |
| TS,Variable | TS,ExternalDeclaration | 383 | 0.18 |
| TS,Function | TS,Interface | 377 | 0.18 |
| File,TS,Local,Module | TS,ExternalDeclaration | 310 | 0.15 |
| TS,Function | TS,TypeAlias | 309 | 0.15 |
| TS,Function | TS,Variable | 299 | 0.14 |
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
| 209121 | 449579 | 11 | 160 | 1339 | 1561 | 341 | 142 | 14 | 128 |

[Full data](./Overview_size_for_Typescript.csv)

### 4.2 TypeScript overview charts


![Overview_Typescript_Elements_Per_Module_Stacked](./Overview_Typescript_Elements_Per_Module_Stacked.svg)

![Overview_Typescript_Function_Elements_Per_Module_Normalized](./Overview_Typescript_Function_Elements_Per_Module_Normalized.svg)

![Overview_Typescript_Interface_Elements_Per_Module_Normalized](./Overview_Typescript_Interface_Elements_Per_Module_Normalized.svg)

![Overview_Typescript_TypeAlias_Elements_Per_Module_Normalized](./Overview_Typescript_TypeAlias_Elements_Per_Module_Normalized.svg)

![Overview_Typescript_Variable_Elements_Per_Module_Normalized](./Overview_Typescript_Variable_Elements_Per_Module_Normalized.svg)
