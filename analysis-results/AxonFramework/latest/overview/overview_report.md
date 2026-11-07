---
title: "Overview Report"
generated: "2026-11-07"
model_version: "v5.0.1"
dataset: "AxonFramework-5.1.2"
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
| ["Git","Change","Update"] | 315202 | 52.2363547475618 |
| ["Git","Change","Create"] | 108637 | 18.003695632359157 |
| ["Git","Change","Delete"] | 66564 | 11.031214006943811 |
| ["Git","Change","Rename"] | 27910 | 4.625340768790965 |
| ["Git","Commit"] | 17612 | 2.918720946612199 |
| ["File","Git"] | 17554 | 2.90910898800991 |
| ["Java","ByteCode","Parameter"] | 9368 | 1.5524970376937928 |
| ["Java","ByteCode","Member","Method"] | 8947 | 1.4827274761151115 |
| ["Java","ByteCode","Bound"] | 6639 | 1.1002378131136945 |
| ["Java","ByteCode","ParameterizedType","Bound"] | 5076 | 0.8412121011244336 |

[Full data](./Node_label_combination_count.csv)


![Overview_General_Node_Label_Combination_Count_High](./Overview_General_Node_Label_Combination_Count_High.svg)

![Overview_General_Node_Label_Combination_Count_Low](./Overview_General_Node_Label_Combination_Count_Low.svg)

---

### 2.2 Node labels

Shows the number of nodes carrying each individual label, sorted by count descending.

| nodeLabel | nodesWithThatLabel | nodesWithThatLabelPercent |
| --- | --- | --- |
| Git | 555689 | 92.09068385770986 |
| Change | 519799 | 86.14287016398333 |
| Update | 315202 | 52.2363547475618 |
| Create | 108637 | 18.003695632359157 |
| Delete | 66564 | 11.031214006943811 |
| Java | 41468 | 6.872218953788023 |
| ByteCode | 41253 | 6.8365884175898834 |
| Rename | 27910 | 4.625340768790965 |
| File | 20743 | 3.437600987711608 |
| Commit | 17612 | 2.918720946612199 |

[Full data](./Node_label_count.csv)



---

### 2.3 Relationship types

Shows the number of relationships for each type and their share of the total relationship count.

| relationshipType | nodesWithThatRelationshipType | nodesWithThatRelationshipTypePercent |
| --- | --- | --- |
| CONTAINS_CHANGE | 519799 | 27.54309113770989 |
| MODIFIES | 519799 | 27.54309113770989 |
| UPDATES | 315202 | 16.701912494615097 |
| CREATES | 138033 | 7.314087751249058 |
| DELETES | 94474 | 5.005984990629078 |
| COMMITTED | 35224 | 1.866448073649032 |
| RENAMES | 27910 | 1.4788940987833434 |
| INVOKES | 22950 | 1.2160737931593597 |
| DEPENDS_ON | 21808 | 1.1555615373080312 |
| HAS_PARENT | 21427 | 1.1353731227026405 |

[Full data](./Relationship_type_count.csv)


![Overview_General_Relationship_Type_Count_High](./Overview_General_Relationship_Type_Count_High.svg)

![Overview_General_Relationship_Type_Count_Low](./Overview_General_Relationship_Type_Count_Low.svg)

---

### 2.4 Node labels and their relationships

Shows which node labels are connected by each relationship type, with count and percentage share.
| sourceLabels | relationshipType | targetLabels | relationshipCount |
| --- | --- | --- | --- |
| ["Git","Change","Update"] | MODIFIES | ["Git"] | 315202 |
| ["Git","Change","Update"] | UPDATES | ["Git"] | 315202 |
| ["Git","Commit"] | CONTAINS_CHANGE | ["Git","Change","Update"] | 315202 |
| ["Git","Change","Create"] | MODIFIES | ["Git"] | 108637 |
| ["Git","Change","Create"] | CREATES | ["Git"] | 108637 |
| ["Git","Commit"] | CONTAINS_CHANGE | ["Git","Change","Create"] | 108637 |
| ["Git","Change","Delete"] | MODIFIES | ["Git"] | 66564 |
| ["Git","Commit"] | CONTAINS_CHANGE | ["Git","Change","Delete"] | 66564 |
| ["Git","Change","Delete"] | DELETES | ["Git"] | 66564 |
| ["Git","Change","Rename"] | MODIFIES | ["Git"] | 27910 |

[Full data](./Node_labels_and_their_relationships.csv)

---

### 2.5 Graph density

Statistical measures of the graph structure: node count, relationship count, and density metric.



---

### 2.6 Dependency node labels

Shows node labels present on dependency nodes — nodes that represent external dependencies not scanned as artifacts.

| sourceLabels | targetLabels | numberOfNodes | percentageOfTotalNodes |
| --- | --- | --- | --- |
| StronglyConnectedComponent,TypeMembers | StronglyConnectedComponent,TypeMembers | 4124 | 0.68 |
| StronglyConnectedComponent,PackageMembers | StronglyConnectedComponent,PackageMembers | 357 | 0.06 |
| Type,File,Java,ByteCode,Interface | Type,File,Java,ByteCode,JavaType,ExternalAnnotation,ExternalType | 124 | 0.02 |
| Type,File,Java,ByteCode,Class,InternalJavaType,ConnectedInternalJavaType | Type,File,Java,ByteCode,JavaType | 38 | 0.01 |
| Type,File,Java,ByteCode,Class,InternalJavaType,ConnectedInternalJavaType | Type,File,Java,ByteCode,JavaType | 34 | 0.01 |
| Type,File,Java,ByteCode,Class,InternalJavaType,ConnectedInternalJavaType | Type,File,Java,ByteCode,ResolvedDuplicateType | 32 | 0.01 |
| Type,File,Java,ByteCode,Class,InternalJavaType,ConnectedInternalJavaType | Type,File,Java,ByteCode,JavaType,ResolvedDuplicateType | 28 | 0 |
| StronglyConnectedComponent,ArtifactMembers | StronglyConnectedComponent,ArtifactMembers | 27 | 0 |
| Type,File,Java,ByteCode,Class,InternalJavaType,ConnectedInternalJavaType | Type,File,Java,ByteCode,JavaType | 27 | 0 |
| Type,File,Java,ByteCode,Class,InternalJavaType,ConnectedInternalJavaType | Type,File,Java,ByteCode,JavaType | 25 | 0 |

[Full data](./Dependency_node_labels.csv)

---

## 3. Java

### 3.1 Artifact size

Overview of scanned Java artifacts: number of packages, types, methods, and lines of code.

| nodeCount | relationshipCount | artifactCount | packageCount | typeCount | methodCount | memberCount |
| --- | --- | --- | --- | --- | --- | --- |
| 603415 | 1887221 | 11 | 137 | 1856 | 5623 | 7042 |

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


