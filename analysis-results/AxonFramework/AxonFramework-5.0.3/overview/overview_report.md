---
title: "Overview Report"
generated: "2026-05-17"
model_version: "v4.0.1"
dataset: "AxonFramework-5.0.3"
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
| ["Git","Update","Change"] | 264852 | 49.147145274784 |
| ["Git","Change","Create"] | 99583 | 18.479075740031472 |
| ["Git","Change","Delete"] | 61316 | 11.378076660431697 |
| ["Git","Change","Rename"] | 24820 | 4.605712419464981 |
| ["File","Git"] | 16609 | 3.082041803984442 |
| ["Git","Commit"] | 16390 | 3.041403164989163 |
| ["Java","ByteCode","Parameter"] | 9457 | 1.7548840592618984 |
| ["Java","ByteCode","Member","Method"] | 9119 | 1.692163237433568 |
| ["Java","ByteCode","Bound"] | 6545 | 1.2145200558178202 |
| ["Java","Value","ByteCode","Annotation"] | 5562 | 1.0321100917431194 |

[Full data](./Node_label_combination_count.csv)


![Overview_General_Node_Label_Combination_Count_High](./Overview_General_Node_Label_Combination_Count_High.svg)

![Overview_General_Node_Label_Combination_Count_Low](./Overview_General_Node_Label_Combination_Count_Low.svg)

---

### 2.2 Node labels

Shows the number of nodes carrying each individual label, sorted by count descending.

| nodeLabel | nodesWithThatLabel | nodesWithThatLabelPercent |
| --- | --- | --- |
| Git | 484820 | 89.9654107657136 |
| Change | 451117 | 83.71132834535791 |
| Update | 264852 | 49.147145274784 |
| Create | 99583 | 18.479075740031472 |
| Delete | 61316 | 11.378076660431697 |
| Java | 46701 | 8.66605059232208 |
| ByteCode | 46492 | 8.627267598943025 |
| Rename | 24820 | 4.605712419464981 |
| File | 19861 | 3.6854977583800954 |
| Commit | 16390 | 3.041403164989163 |

[Full data](./Node_label_count.csv)



---

### 2.3 Relationship types

Shows the number of relationships for each type and their share of the total relationship count.

| relationshipType | nodesWithThatRelationshipType | nodesWithThatRelationshipTypePercent |
| --- | --- | --- |
| CONTAINS_CHANGE | 451117 | 26.903398908518174 |
| MODIFIES | 451117 | 26.903398908518174 |
| UPDATES | 264852 | 15.795057618575347 |
| CREATES | 124949 | 7.451620733025884 |
| DELETES | 86136 | 5.136918290341799 |
| COMMITTED | 32780 | 1.9549106245635297 |
| RENAMES | 24820 | 1.4801977334248568 |
| INVOKES | 22754 | 1.356987076001176 |
| DEPENDS_ON | 22707 | 1.354184123000734 |
| HAS_PARENT | 19906 | 1.1871400516339725 |

[Full data](./Relationship_type_count.csv)


![Overview_General_Relationship_Type_Count_High](./Overview_General_Relationship_Type_Count_High.svg)

![Overview_General_Relationship_Type_Count_Low](./Overview_General_Relationship_Type_Count_Low.svg)

---

### 2.4 Node labels and their relationships

Shows which node labels are connected by each relationship type, with count and percentage share.
| sourceLabels | relationshipType | targetLabels | relationshipCount |
| --- | --- | --- | --- |
| ["Git","Update","Change"] | MODIFIES | ["Git"] | 264852 |
| ["Git","Update","Change"] | UPDATES | ["Git"] | 264852 |
| ["Git","Commit"] | CONTAINS_CHANGE | ["Git","Update","Change"] | 264852 |
| ["Git","Change","Create"] | MODIFIES | ["Git"] | 99583 |
| ["Git","Commit"] | CONTAINS_CHANGE | ["Git","Change","Create"] | 99583 |
| ["Git","Change","Create"] | CREATES | ["Git"] | 99583 |
| ["Git","Change","Delete"] | MODIFIES | ["Git"] | 61316 |
| ["Git","Commit"] | CONTAINS_CHANGE | ["Git","Change","Delete"] | 61316 |
| ["Git","Change","Delete"] | DELETES | ["Git"] | 61316 |
| ["Git","Change","Rename"] | MODIFIES | ["Git"] | 24820 |

[Full data](./Node_labels_and_their_relationships.csv)

---

### 2.5 Graph density

Statistical measures of the graph structure: node count, relationship count, and density metric.



---

### 2.6 Dependency node labels

Shows node labels present on dependency nodes — nodes that represent external dependencies not scanned as artifacts.

| sourceLabels | targetLabels | numberOfNodes | percentageOfTotalNodes |
| --- | --- | --- | --- |
| StronglyConnectedComponent,TypeMembers | StronglyConnectedComponent,TypeMembers | 4134 | 0.77 |
| StronglyConnectedComponent,PackageMembers | StronglyConnectedComponent,PackageMembers | 365 | 0.07 |
| Type,File,Java,ByteCode,Class,InternalJavaType,ConnectedInternalJavaType | Type,File,Java,ByteCode,JavaType | 33 | 0.01 |
| Type,File,Java,ByteCode,Class,InternalJavaType,ConnectedInternalJavaType | Type,File,Java,ByteCode,ResolvedDuplicateType | 32 | 0.01 |
| StronglyConnectedComponent,ArtifactMembers | StronglyConnectedComponent,ArtifactMembers | 30 | 0.01 |
| Type,File,Java,ByteCode,Class,InternalJavaType,ConnectedInternalJavaType | Type,File,Java,ByteCode,ResolvedDuplicateType | 30 | 0.01 |
| Type,File,Java,ByteCode,Class,InternalJavaType,ConnectedInternalJavaType | Type,File,Java,ByteCode,JavaType | 29 | 0.01 |
| Type,File,Java,ByteCode,Class,InternalJavaType,ConnectedInternalJavaType | Type,File,Java,ByteCode,JavaType | 27 | 0.01 |
| Type,File,Java,ByteCode,Class,InternalJavaType,ConnectedInternalJavaType,GenericDeclaration | Type,File,Java,ByteCode,JavaType | 24 | 0 |
| Type,File,Java,ByteCode,Class,InternalJavaType,ConnectedInternalJavaType | Type,File,Java,ByteCode,JavaType | 23 | 0 |

[Full data](./Dependency_node_labels.csv)

---

## 3. Java

### 3.1 Artifact size

Overview of scanned Java artifacts: number of packages, types, methods, and lines of code.

| nodeCount | relationshipCount | artifactCount | packageCount | typeCount | methodCount | memberCount |
| --- | --- | --- | --- | --- | --- | --- |
| 538896 | 1676803 | 11 | 128 | 1822 | 5709 | 7176 |

[Full data](./Overview_size.csv)

### 3.2 Java overview charts


![Overview_Java_Annotation_Types_Per_Artifact_Normalized](./Overview_Java_Annotation_Types_Per_Artifact_Normalized.svg)

![Overview_Java_Class_Types_Per_Artifact_Normalized](./Overview_Java_Class_Types_Per_Artifact_Normalized.svg)

![Overview_Java_Enum_Types_Per_Artifact_Normalized](./Overview_Java_Enum_Types_Per_Artifact_Normalized.svg)

![Overview_Java_Interface_Types_Per_Artifact_Normalized](./Overview_Java_Interface_Types_Per_Artifact_Normalized.svg)

![Overview_Java_Packages_Per_Artifact](./Overview_Java_Packages_Per_Artifact.svg)

![Overview_Java_Types_Per_Artifact_Stacked](./Overview_Java_Types_Per_Artifact_Stacked.svg)

---

## 4. TypeScript

### 4.1 Module size

Overview of scanned TypeScript modules: number of exported language elements per module.

> No overview data available.
> Please run the analysis pipeline first to scan and import code artifacts into the graph database (e.g., `analyze.sh`), then start Neo4j and re-run the overview reports.

### 4.2 TypeScript overview charts


