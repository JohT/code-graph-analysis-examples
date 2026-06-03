---
title: "Overview Report"
generated: "2026-06-03"
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
| ["Git","Update","Change"] | 315032 | 52.252431564560865 |
| ["Git","Change","Create"] | 108443 | 17.986777331051044 |
| ["Git","Change","Delete"] | 66549 | 11.038075713546435 |
| ["Git","Change","Rename"] | 27910 | 4.629261043217494 |
| ["Git","Commit"] | 17573 | 2.9147260592067727 |
| ["File","Git"] | 17486 | 2.9002959011716625 |
| ["Java","ByteCode","Parameter"] | 9346 | 1.5501638735188354 |
| ["Java","ByteCode","Method","Member"] | 8985 | 1.4902870108674018 |
| ["Java","ByteCode","Bound"] | 6615 | 1.0971896023247483 |
| ["Java","ByteCode","ParameterizedType","Bound"] | 5068 | 0.8405981715165267 |

[Full data](./Node_label_combination_count.csv)


![Overview_General_Node_Label_Combination_Count_High](./Overview_General_Node_Label_Combination_Count_High.svg)

![Overview_General_Node_Label_Combination_Count_Low](./Overview_General_Node_Label_Combination_Count_Low.svg)

---

### 2.2 Node labels

Shows the number of nodes carrying each individual label, sorted by count descending.

| nodeLabel | nodesWithThatLabel | nodesWithThatLabelPercent |
| --- | --- | --- |
| Git | 555202 | 92.0879609357377 |
| Change | 519420 | 86.15301938617094 |
| Update | 315032 | 52.252431564560865 |
| Create | 108443 | 17.986777331051044 |
| Delete | 66549 | 11.038075713546435 |
| Java | 41445 | 6.874228732932607 |
| ByteCode | 41230 | 6.838567997558484 |
| Rename | 27910 | 4.629261043217494 |
| File | 20672 | 3.428738240250521 |
| Commit | 17573 | 2.9147260592067727 |

[Full data](./Node_label_count.csv)



---

### 2.3 Relationship types

Shows the number of relationships for each type and their share of the total relationship count.

| relationshipType | nodesWithThatRelationshipType | nodesWithThatRelationshipTypePercent |
| --- | --- | --- |
| CONTAINS_CHANGE | 519420 | 27.542769452988995 |
| MODIFIES | 519420 | 27.542769452988995 |
| UPDATES | 315032 | 16.70488958129073 |
| CREATES | 137839 | 7.309052016923781 |
| DELETES | 94459 | 5.008783758345631 |
| COMMITTED | 35146 | 1.8636521027198631 |
| RENAMES | 27910 | 1.4799559035711425 |
| INVOKES | 23108 | 1.22532500966399 |
| DEPENDS_ON | 21776 | 1.1546943660395987 |
| HAS_PARENT | 21377 | 1.1335369885575175 |

[Full data](./Relationship_type_count.csv)


![Overview_General_Relationship_Type_Count_High](./Overview_General_Relationship_Type_Count_High.svg)

![Overview_General_Relationship_Type_Count_Low](./Overview_General_Relationship_Type_Count_Low.svg)

---

### 2.4 Node labels and their relationships

Shows which node labels are connected by each relationship type, with count and percentage share.
| sourceLabels | relationshipType | targetLabels | relationshipCount |
| --- | --- | --- | --- |
| ["Git","Commit"] | CONTAINS_CHANGE | ["Git","Update","Change"] | 315032 |
| ["Git","Update","Change"] | MODIFIES | ["Git"] | 315032 |
| ["Git","Update","Change"] | UPDATES | ["Git"] | 315032 |
| ["Git","Commit"] | CONTAINS_CHANGE | ["Git","Change","Create"] | 108443 |
| ["Git","Change","Create"] | MODIFIES | ["Git"] | 108443 |
| ["Git","Change","Create"] | CREATES | ["Git"] | 108443 |
| ["Git","Commit"] | CONTAINS_CHANGE | ["Git","Change","Delete"] | 66549 |
| ["Git","Change","Delete"] | MODIFIES | ["Git"] | 66549 |
| ["Git","Change","Delete"] | DELETES | ["Git"] | 66549 |
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
| StronglyConnectedComponent,TypeMembers | StronglyConnectedComponent,TypeMembers | 4117 | 0.68 |
| StronglyConnectedComponent,PackageMembers | StronglyConnectedComponent,PackageMembers | 357 | 0.06 |
| Type,File,Java,ByteCode,Interface | Type,File,Java,ByteCode,ExternalAnnotation,ExternalType,JavaType | 124 | 0.02 |
| Type,File,Java,Class,ByteCode,InternalJavaType,ConnectedInternalJavaType | Type,File,Java,ByteCode,JavaType | 38 | 0.01 |
| Type,File,Java,Class,ByteCode,InternalJavaType,ConnectedInternalJavaType | Type,File,Java,ByteCode,JavaType | 34 | 0.01 |
| Type,File,Java,Class,ByteCode,InternalJavaType,ConnectedInternalJavaType | Type,File,Java,ByteCode,ResolvedDuplicateType | 32 | 0.01 |
| Type,File,Java,Class,ByteCode,InternalJavaType,ConnectedInternalJavaType | Type,File,Java,ByteCode,ResolvedDuplicateType,JavaType | 28 | 0 |
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
| 602904 | 1885867 | 11 | 137 | 1854 | 5615 | 7029 |

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


