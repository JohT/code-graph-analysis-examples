---
title: "Overview Report"
generated: "2026-06-29"
model_version: "v4.0.1"
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
| ["Git","Change","Update"] | 315202 | 52.23055534382136 |
| ["Git","Change","Create"] | 108637 | 18.001696819457745 |
| ["Git","Change","Delete"] | 66564 | 11.029989295455374 |
| ["Git","Change","Rename"] | 27910 | 4.62482725251126 |
| ["Git","Commit"] | 17612 | 2.91839690330449 |
| ["File","Git"] | 17554 | 2.908786011844595 |
| ["Java","ByteCode","Parameter"] | 9368 | 1.5523246757981182 |
| ["Java","ByteCode","Member","Method"] | 8998 | 1.4910138164849989 |
| ["Java","ByteCode","Bound"] | 6639 | 1.1001156621075692 |
| ["Java","ByteCode","Bound","ParameterizedType"] | 5076 | 0.8411187077659317 |

[Full data](./Node_label_combination_count.csv)


![Overview_General_Node_Label_Combination_Count_High](./Overview_General_Node_Label_Combination_Count_High.svg)

![Overview_General_Node_Label_Combination_Count_Low](./Overview_General_Node_Label_Combination_Count_Low.svg)

---

### 2.2 Node labels

Shows the number of nodes carrying each individual label, sorted by count descending.

| nodeLabel | nodesWithThatLabel | nodesWithThatLabelPercent |
| --- | --- | --- |
| Git | 555689 | 92.08045973202184 |
| Change | 519799 | 86.13330637864924 |
| Update | 315202 | 52.23055534382136 |
| Create | 108637 | 18.001696819457745 |
| Delete | 66564 | 11.029989295455374 |
| Java | 41535 | 6.882558220460594 |
| ByteCode | 41320 | 6.846931640048916 |
| Rename | 27910 | 4.62482725251126 |
| File | 20743 | 3.4372193371136173 |
| Commit | 17612 | 2.91839690330449 |

[Full data](./Node_label_count.csv)



---

### 2.3 Relationship types

Shows the number of relationships for each type and their share of the total relationship count.

| relationshipType | nodesWithThatRelationshipType | nodesWithThatRelationshipTypePercent |
| --- | --- | --- |
| CONTAINS_CHANGE | 519799 | 27.541660948679052 |
| MODIFIES | 519799 | 27.541660948679052 |
| UPDATES | 315202 | 16.701045239305067 |
| CREATES | 138033 | 7.31370796351862 |
| DELETES | 94474 | 5.005725052309653 |
| COMMITTED | 35224 | 1.8663511573825091 |
| RENAMES | 27910 | 1.4788173064542878 |
| INVOKES | 22970 | 1.217070352176818 |
| DEPENDS_ON | 21808 | 1.1555015341868544 |
| HAS_PARENT | 21427 | 1.135314167875171 |

[Full data](./Relationship_type_count.csv)


![Overview_General_Relationship_Type_Count_High](./Overview_General_Relationship_Type_Count_High.svg)

![Overview_General_Relationship_Type_Count_Low](./Overview_General_Relationship_Type_Count_Low.svg)

---

### 2.4 Node labels and their relationships

Shows which node labels are connected by each relationship type, with count and percentage share.
| sourceLabels | relationshipType | targetLabels | relationshipCount |
| --- | --- | --- | --- |
| ["Git","Change","Update"] | MODIFIES | ["Git"] | 315202 |
| ["Git","Commit"] | CONTAINS_CHANGE | ["Git","Change","Update"] | 315202 |
| ["Git","Change","Update"] | UPDATES | ["Git"] | 315202 |
| ["Git","Change","Create"] | MODIFIES | ["Git"] | 108637 |
| ["Git","Change","Create"] | CREATES | ["Git"] | 108637 |
| ["Git","Commit"] | CONTAINS_CHANGE | ["Git","Change","Create"] | 108637 |
| ["Git","Change","Delete"] | MODIFIES | ["Git"] | 66564 |
| ["Git","Commit"] | CONTAINS_CHANGE | ["Git","Change","Delete"] | 66564 |
| ["Git","Change","Delete"] | DELETES | ["Git"] | 66564 |
| ["Git","Commit"] | CONTAINS_CHANGE | ["Git","Change","Rename"] | 27910 |

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
| Type,File,Java,ByteCode,Interface | Type,File,Java,ByteCode,JavaType,ExternalType,ExternalAnnotation | 124 | 0.02 |
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
| 603482 | 1887319 | 11 | 137 | 1856 | 5623 | 7042 |

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


