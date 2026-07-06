---
title: "Java Report"
generated: "2026-07-06"
model_version: "v4.0.1"
dataset: "react-router-7.18.1"
authors: ["JohT/code-graph-analysis-pipeline"]
---

# ☕ Java Report

## 1. Overview

Analyzes the Java codebase:

- **Artifact dependencies** — which artifacts depend on which, and spread across modules
- **Method metrics** — effective LOC per type and package
- **Java code quality** — annotation usage, deprecated element usages, and reflection
- **Web framework annotations** — Spring Web and Jakarta EE REST endpoints

> High dependency counts may indicate coupling hotspots.  
> Deprecated element usages should be migrated to their replacements.

## 📚 Table of Contents

1. [Overview](#1-overview)
1. [Artifact Dependencies](#2-artifact-dependencies)
1. [Method Metrics](#3-method-metrics)
1. [Java Code Quality](#4-java-code-quality)
1. [Web Framework Annotations](#5-web-framework-annotations)
1. [Duplicate Package Names](#6-duplicate-package-names)
1. [Dependency Spread](#7-dependency-spread)
1. [Glossary and Column Definitions](#8-glossary-and-column-definitions)

---

## 2. Artifact Dependencies

Maven artifact dependencies. High incoming = central/shared; high outgoing = depends on many others.

### 2.1 Incoming Artifact Dependencies

⚠️ _No data available — no Java artifacts found in the graph database._

### 2.2 Outgoing Artifact Dependencies

⚠️ _No data available — no Java artifacts found in the graph database._

### 2.3 Most Used Internal Dependencies

⚠️ _No data available — no Java artifacts found in the graph database._

### 2.4 All Artifact Dependencies

⚠️ _No data available — no Java artifacts found in the graph database._

### 2.5 Artifact Dependency Charts



---

## 3. Method Metrics

Effective Lines Of Code (LOC) per type and package. High values = complex or large.

### 3.1 Effective Method Line Count Distribution

⚠️ _No data available — no Java artifacts found in the graph database._

### 3.2 Top Types by Effective LOC

⚠️ _No data available — no Java artifacts found in the graph database._

### 3.3 Top Packages by Effective LOC

⚠️ _No data available — no Java artifacts found in the graph database._

### 3.4 Method Metrics Charts



---

## 4. Java Code Quality

Annotations, deprecated API usages, and reflection calls.

### 4.1 Annotated Code Elements

⚠️ _No data available — no Java artifacts found in the graph database._

### 4.2 Annotated Code Elements per Artifact

⚠️ _No data available — no Java artifacts found in the graph database._

### 4.3 Deprecated Element Usages



### 4.4 Reflection Usages



### 4.5 Java Code Quality Charts



---

## 5. Web Framework Annotations

HTTP mapping annotations from Spring Web and Jakarta EE REST — declared REST endpoints.

### 5.1 Spring Web Request Annotations



### 5.2 Jakarta EE REST Annotations



### 5.3 Web Framework Charts



---

## 6. Duplicate Package Names

Package names in multiple artifacts. Can cause split-package issues on the module path.



---

## 7. Dependency Spread

How many distinct artifacts each internal module is depended on by (spread) and vice versa. Highly spread = critical infrastructure.

### 7.1 Spread per Dependency (most used by others)



### 7.2 Spread per Dependent (depends on most others)



---

## 8. Glossary and Column Definitions

| Term | Definition |
|------|-----------|
| `a.fileName` | File path of the artifact (JAR/WAR/EAR) |
| `incomingDependencies` | Number of other artifacts that depend on this artifact |
| `outgoingDependencies` | Number of artifacts this artifact depends on |
| `dependency` | Name of an internal artifact that others depend upon |
| `usedByPackages` | Number of distinct packages depending on this artifact |
| `dependencyArtifactName` | Name of the dependency artifact in a spread analysis |
| `usedInArtifacts` | Number of distinct artifacts using this dependency (spread) |
| `artifactDependencies` | Number of distinct dependency artifacts used by this artifact (spread) |
| `typeName` | Simple name of a Java type (class, interface, enum, annotation type) |
| `packageName` | Simple name of a Java package |
| `fullPackageName` | Fully qualified name of a Java package |
| `artifactName` | Name of the artifact (JAR/module) containing the element |
| `methods` | Number of methods with a given effective line count |
| `effectiveLineCount` | Non-blank, non-comment lines in a method |
| `sumEffectiveLinesOfMethodCode` | Sum of effective lines of method code in a type |
| `linesInPackage` | Sum of effective lines across all methods in a package |
| `annotationName` | Fully qualified name of a Java annotation type |
| `languageElement` | Kind of code element annotated (Class, Method, Field, Type, Parameter, etc.) |
| `numberOfAnnotatedElements` | Count of distinct elements annotated with a particular annotation |
| `deprecatedElement` | Kind of deprecated code element (Class, Method, Field, etc.) |
| `numberOfElementsUsingDeprecatedElements` | Count of distinct non-deprecated elements using a deprecated element |
