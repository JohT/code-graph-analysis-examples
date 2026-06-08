---
title: "Overview Report"
generated: "2026-06-08"
model_version: "v4.0.1"
dataset: "AxonFramework-5.1.1"
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
| ["Git","Update","Change"] | 315032 | 52.25260490096234 |
| ["Git","Change","Create"] | 108443 | 17.986836998384483 |
| ["Git","Change","Delete"] | 66549 | 11.038112330030419 |
| ["Git","Change","Rename"] | 27910 | 4.629276399812905 |
| ["Git","Commit"] | 17573 | 2.914735728194632 |
| ["File","Git"] | 17486 | 2.9003055222905214 |
| ["Java","ByteCode","Parameter"] | 9346 | 1.5501690158599573 |
| ["Java","ByteCode","Method","Member"] | 8985 | 1.490291954579683 |
| ["Java","ByteCode","Bound"] | 6615 | 1.0971932420194328 |
| ["Java","ByteCode","ParameterizedType","Bound"] | 5068 | 0.8406009600233537 |

[Full data](./Node_label_combination_count.csv)


![Overview_General_Node_Label_Combination_Count_High](./Overview_General_Node_Label_Combination_Count_High.svg)

![Overview_General_Node_Label_Combination_Count_Low](./Overview_General_Node_Label_Combination_Count_Low.svg)

---

### 2.2 Node labels

Shows the number of nodes carrying each individual label, sorted by count descending.

| nodeLabel | nodesWithThatLabel | nodesWithThatLabelPercent |
| --- | --- | --- |
| Git | 555202 | 92.08826641809117 |
| Change | 519420 | 86.15330518060979 |
| Update | 315032 | 52.25260490096234 |
| Create | 108443 | 17.986836998384483 |
| Delete | 66549 | 11.038112330030419 |
| Java | 41443 | 6.873919807862637 |
| ByteCode | 41228 | 6.83825895419156 |
| Rename | 27910 | 4.629276399812905 |
| File | 20672 | 3.428749614365187 |
| Commit | 17573 | 2.914735728194632 |

[Full data](./Node_label_count.csv)



---

### 2.3 Relationship types

Shows the number of relationships for each type and their share of the total relationship count.

| relationshipType | nodesWithThatRelationshipType | nodesWithThatRelationshipTypePercent |
| --- | --- | --- |
| CONTAINS_CHANGE | 519420 | 27.542798662682642 |
| MODIFIES | 519420 | 27.542798662682642 |
| UPDATES | 315032 | 16.70490729718193 |
| CREATES | 137839 | 7.3090597683291225 |
| DELETES | 94459 | 5.00878907026749 |
| COMMITTED | 35146 | 1.8636540791626122 |
| RENAMES | 27910 | 1.4799574730959002 |
| INVOKES | 23108 | 1.2253263091472613 |
| DEPENDS_ON | 21776 | 1.154695590617568 |
| HAS_PARENT | 21377 | 1.1335381906976374 |

[Full data](./Relationship_type_count.csv)


![Overview_General_Relationship_Type_Count_High](./Overview_General_Relationship_Type_Count_High.svg)

![Overview_General_Relationship_Type_Count_Low](./Overview_General_Relationship_Type_Count_Low.svg)

---

### 2.4 Node labels and their relationships

Shows which node labels are connected by each relationship type, with count and percentage share.
| sourceLabels | relationshipType | targetLabels | relationshipCount |
| --- | --- | --- | --- |
| ["Git","Update","Change"] | MODIFIES | ["Git"] | 315032 |
| ["Git","Update","Change"] | UPDATES | ["Git"] | 315032 |
| ["Git","Commit"] | CONTAINS_CHANGE | ["Git","Update","Change"] | 315032 |
| ["Git","Change","Create"] | MODIFIES | ["Git"] | 108443 |
| ["Git","Commit"] | CONTAINS_CHANGE | ["Git","Change","Create"] | 108443 |
| ["Git","Change","Create"] | CREATES | ["Git"] | 108443 |
| ["Git","Change","Delete"] | MODIFIES | ["Git"] | 66549 |
| ["Git","Commit"] | CONTAINS_CHANGE | ["Git","Change","Delete"] | 66549 |
| ["Git","Change","Delete"] | DELETES | ["Git"] | 66549 |
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
| StronglyConnectedComponent,TypeMembers | StronglyConnectedComponent,TypeMembers | 4117 | 0.68 |
| StronglyConnectedComponent,PackageMembers | StronglyConnectedComponent,PackageMembers | 357 | 0.06 |
| Type,File,Java,ByteCode,Interface | Type,File,Java,ByteCode,ExternalAnnotation,ExternalType,JavaType | 124 | 0.02 |
| Type,File,Java,Class,ByteCode,InternalJavaType,ConnectedInternalJavaType | Type,File,Java,ByteCode,JavaType | 38 | 0.01 |
| Type,File,Java,Class,ByteCode,InternalJavaType,ConnectedInternalJavaType | Type,File,Java,ByteCode,JavaType | 34 | 0.01 |
| Type,File,Java,Class,ByteCode,InternalJavaType,ConnectedInternalJavaType | Type,File,Java,ByteCode,ResolvedDuplicateType | 32 | 0.01 |
| Type,File,Java,Class,ByteCode,InternalJavaType,ConnectedInternalJavaType | Type,File,Java,ByteCode,JavaType,ResolvedDuplicateType | 28 | 0 |
| StronglyConnectedComponent,ArtifactMembers | StronglyConnectedComponent,ArtifactMembers | 27 | 0 |
| Type,File,Java,Class,ByteCode,InternalJavaType,ConnectedInternalJavaType | Type,File,Java,ByteCode,JavaType | 27 | 0 |
| Type,File,Java,Class,ByteCode,InternalJavaType,ConnectedInternalJavaType | Type,File,Java,ByteCode,JavaType | 25 | 0 |

[Full data](./Dependency_node_labels.csv)

---

## 3. Java

### 3.1 Artifact size

Overview of scanned Java artifacts: number of packages, types, methods, and lines of code.

| nodeCount | relationshipCount | artifactCount | packageCount | typeCount | methodCount | memberCount |
| --- | --- | --- | --- | --- | --- | --- |
| 602902 | 1885865 | 11 | 137 | 1854 | 5615 | 7029 |

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


