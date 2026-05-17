---
title: "Git History Report"
generated: "2026-05-17"
model_version: "v4.0.1"
dataset: "AxonFramework-5.0.3"
authors: ["JohT/code-graph-analysis-pipeline"]
---

# 📜 Git History Report

## 1. Overview

This report analyses the **git commit history** of the codebase. It covers:

- **Directory commit statistics** — which directories change most frequently and by how many authors
- **Co-changed files** — files that are frequently committed together (coupling signals)
- **File change distribution** — how many files are changed per commit
- **Pairwise changed files** — direct co-change relationships between specific file pairs
- **Data quality** — ambiguous or unresolved file references in the git log
- **Git author wordcloud** — visual overview of contributor activity

> High commit frequency in a directory = refactoring hotspot. Files that always change together = co-location or module consolidation candidates.

## 📚 Table of Contents

1. [Overview](#1-overview)
1. [Directory Commit Statistics](#2-directory-commit-statistics)
1. [Co-Changed Files](#3-co-changed-files)
1. [File Change Distribution](#4-file-change-distribution)
1. [Pairwise Changed Files](#5-pairwise-changed-files)
1. [Files by Author](#6-files-by-author)
1. [Data Quality](#7-data-quality)
1. [Git Author Wordcloud](#8-git-author-wordcloud)
1. [Glossary and Column Definitions](#9-glossary-and-column-definitions)

---

## 2. Directory Commit Statistics

Commit frequency and author count per directory. High values = active, potentially complex.

### 2.1 Directory Commit Statistics (Table)

| directoryPath | directoryName | directoryParentPath | directoryParentName | mainAuthor | secondAuthor | thirdAuthor | authorCount | fileCount | commitCount | lastCreationDate | lastModificationDate | lastCommitDate | daysSinceLastCommit | daysSinceLastCreation | daysSinceLastModification | maxCommitSha | maxFileRelativePath | directoryPathLength | combinedDirectoriesCount |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| AxonFramework-5.0.3 | AxonFramework-5.0.3 |  |  | Steven van Beelen | Allard Buijze | Mitchell Herrijgers | 117 | 2771 | 6350 | 2026-03-02 | 2026-03-06 | 2026-03-06 | 72 | 76 | 72 | fff5f9f26176f13bcd2824e006f71d61da2ac8b1 | AxonFramework-5.0.3/update/src/test/resources/META-INF/maven/org.axonframework/axon-modelling/pom.properties | 1 | 1 |
| AxonFramework-5.0.3/.github | .github | AxonFramework-5.0.3 | AxonFramework-5.0.3 | Steven van Beelen | dependabot[bot] | Mitchell Herrijgers | 27 | 16 | 708 | 2025-12-01 | 2026-02-23 | 2026-02-23 | 83 | 167 | 83 | ffdb987d127fe126d7d345fa72b94c51bdb220cf | AxonFramework-5.0.3/.github/workflows/slack-release-notification.yml | 2 | 1 |
| AxonFramework-5.0.3/.github/ISSUE_TEMPLATE | ISSUE_TEMPLATE | AxonFramework-5.0.3/.github | .github | Steven van Beelen | Mitchell Herrijgers | Allard Buijze | 7 | 4 | 61 | 2025-08-13 | 2026-02-23 | 2026-02-23 | 83 | 277 | 83 | fa509a0b37d60e0d49b0a95686836dc59e5dc146 | AxonFramework-5.0.3/.github/ISSUE_TEMPLATE/4_documentation_change.md | 3 | 1 |
| AxonFramework-5.0.3/.github/workflows | workflows | AxonFramework-5.0.3/.github | .github | Steven van Beelen | dependabot[bot] | Mitchell Herrijgers | 27 | 8 | 682 | 2025-12-01 | 2026-02-23 | 2026-02-23 | 83 | 167 | 83 | ffdb987d127fe126d7d345fa72b94c51bdb220cf | AxonFramework-5.0.3/.github/workflows/slack-release-notification.yml | 3 | 1 |
| AxonFramework-5.0.3/.idea | .idea | AxonFramework-5.0.3 | AxonFramework-5.0.3 | Steven van Beelen | Mitchell Herrijgers | Allard Buijze | 6 | 4 | 66 | 2025-12-16 | 2025-12-16 | 2026-02-23 | 83 | 152 | 152 | fe926a4970bdf1e538e8e7fb8d147ffdc676e713 | AxonFramework-5.0.3/.idea/inspectionProfiles/Project_Default.xml | 2 | 1 |
| AxonFramework-5.0.3/.idea/copyright | copyright | AxonFramework-5.0.3/.idea | .idea | Steven van Beelen | Allard Buijze | Jan Galinski | 3 | 1 | 28 | 2025-01-09 | 2025-01-09 | 2026-02-23 | 83 | 493 | 493 | fe926a4970bdf1e538e8e7fb8d147ffdc676e713 | AxonFramework-5.0.3/.idea/copyright/Axon_Framework_copyright_template.xml | 3 | 1 |
| AxonFramework-5.0.3/.idea/inspectionProfiles | inspectionProfiles | AxonFramework-5.0.3/.idea | .idea | Steven van Beelen | Mitchell Herrijgers | Allard Buijze | 6 | 1 | 53 | 2025-01-09 | 2025-08-22 | 2026-02-23 | 83 | 493 | 268 | fe926a4970bdf1e538e8e7fb8d147ffdc676e713 | AxonFramework-5.0.3/.idea/inspectionProfiles/Project_Default.xml | 3 | 1 |
| AxonFramework-5.0.3/.mvn/wrapper | .mvn/wrapper | AxonFramework-5.0.3 | AxonFramework-5.0.3 | Steven van Beelen | Jan Galinski | Allard Buijze | 13 | 2 | 96 | 2018-07-15 | 2026-02-23 | 2026-02-23 | 83 | 2863 | 83 | f89c41adfbfda2656db9987aaa87525f17308740 | AxonFramework-5.0.3/.mvn/wrapper/maven-wrapper.properties | 3 | 2 |
| AxonFramework-5.0.3/.run | .run | AxonFramework-5.0.3 | AxonFramework-5.0.3 | Steven van Beelen | Simon Zambrovski | Jan Galinski | 3 | 2 | 10 | 2025-11-28 | 2025-11-28 | 2026-02-23 | 83 | 170 | 170 | e5ef80fb51d51f626a32d37be0a02c4596864da5 | AxonFramework-5.0.3/.run/Example.run.xml | 2 | 1 |
| AxonFramework-5.0.3/axon-5 | axon-5 | AxonFramework-5.0.3 | AxonFramework-5.0.3 | Steven van Beelen | Mitchell Herrijgers | Simon Zambrovski | 8 | 9 | 680 | 2024-01-03 | 2026-02-26 | 2026-02-26 | 80 | 865 | 80 | ff99ea6ad4081bfbf75e91e533004bd112f36696 | AxonFramework-5.0.3/axon-5/reactive-native.md | 2 | 1 |

[Full data](./List_git_file_directories_with_commit_statistics.csv)

### 2.2 Directory Commit Statistics (Charts)



---

## 3. Co-Changed Files

Files committed together = logical coupling signal. May belong to the same conceptual unit or share a concern.

### 3.1 Co-Changed File Pairs

| firstFile | secondFile | commitCount |
| --- | --- | --- |
| AxonFramework-5.0.3/.github/workflows/main.yml | AxonFramework-5.0.3/.github/workflows/pullrequest.yml | 342 |
| AxonFramework-5.0.3/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/AggregateBasedStorageEngineTestSuite.java | AxonFramework-5.0.3/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/StorageEngineTestSuite.java | 119 |
| AxonFramework-5.0.3/axon-server-connector/src/main/java/org/axonframework/axonserver/connector/event/AggregateBasedAxonServerEventStorageEngine.java | AxonFramework-5.0.3/eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/jpa/AggregateBasedJpaEventStorageEngine.java | 117 |
| AxonFramework-5.0.3/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/AggregateBasedStorageEngineTestSuite.java | AxonFramework-5.0.3/eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/jpa/AggregateBasedJpaEventStorageEngine.java | 116 |
| AxonFramework-5.0.3/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/AggregateBasedStorageEngineTestSuite.java | AxonFramework-5.0.3/axon-server-connector/src/main/java/org/axonframework/axonserver/connector/event/AggregateBasedAxonServerEventStorageEngine.java | 115 |
| AxonFramework-5.0.3/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/AggregateBasedStorageEngineTestSuite.java | AxonFramework-5.0.3/axon-5/api-changes.md | 92 |
| AxonFramework-5.0.3/axon-5/api-changes.md | AxonFramework-5.0.3/axon-server-connector/src/main/java/org/axonframework/axonserver/connector/event/AggregateBasedAxonServerEventStorageEngine.java | 91 |
| AxonFramework-5.0.3/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/StorageEngineTestSuite.java | AxonFramework-5.0.3/eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/jpa/AggregateBasedJpaEventStorageEngine.java | 90 |
| AxonFramework-5.0.3/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/StorageEngineTestSuite.java | AxonFramework-5.0.3/axon-server-connector/src/main/java/org/axonframework/axonserver/connector/event/AggregateBasedAxonServerEventStorageEngine.java | 88 |
| AxonFramework-5.0.3/axon-5/api-changes.md | AxonFramework-5.0.3/eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/jpa/AggregateBasedJpaEventStorageEngine.java | 82 |

### 3.2 Co-Changed File Pairs (All in One Commit)

Files changed together in a single large commit.

| firstFile | secondFile | commitCount |
| --- | --- | --- |
| AxonFramework-5.0.3/.github/workflows/main.yml | AxonFramework-5.0.3/.github/workflows/pullrequest.yml | 398 |
| AxonFramework-5.0.3/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/AggregateBasedStorageEngineTestSuite.java | AxonFramework-5.0.3/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/StorageEngineTestSuite.java | 144 |
| AxonFramework-5.0.3/eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/jpa/AggregateBasedJpaEventStorageEngine.java | AxonFramework-5.0.3/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/AggregateBasedStorageEngineTestSuite.java | 142 |
| AxonFramework-5.0.3/axon-server-connector/src/main/java/org/axonframework/axonserver/connector/event/AggregateBasedAxonServerEventStorageEngine.java | AxonFramework-5.0.3/eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/jpa/AggregateBasedJpaEventStorageEngine.java | 141 |
| AxonFramework-5.0.3/axon-server-connector/src/main/java/org/axonframework/axonserver/connector/event/AggregateBasedAxonServerEventStorageEngine.java | AxonFramework-5.0.3/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/AggregateBasedStorageEngineTestSuite.java | 139 |
| AxonFramework-5.0.3/axon-5/api-changes.md | AxonFramework-5.0.3/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/AggregateBasedStorageEngineTestSuite.java | 116 |
| AxonFramework-5.0.3/axon-5/api-changes.md | AxonFramework-5.0.3/axon-server-connector/src/main/java/org/axonframework/axonserver/connector/event/AggregateBasedAxonServerEventStorageEngine.java | 110 |
| AxonFramework-5.0.3/eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/jpa/AggregateBasedJpaEventStorageEngine.java | AxonFramework-5.0.3/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/StorageEngineTestSuite.java | 109 |
| AxonFramework-5.0.3/axon-server-connector/src/main/java/org/axonframework/axonserver/connector/event/AggregateBasedAxonServerEventStorageEngine.java | AxonFramework-5.0.3/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/StorageEngineTestSuite.java | 107 |
| AxonFramework-5.0.3/axon-5/api-changes.md | AxonFramework-5.0.3/eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/jpa/AggregateBasedJpaEventStorageEngine.java | 101 |

### 3.3 Co-Changed With a Specific File

Shows all files that were changed together with another particular file.

| filePath | commitCount | coChangeRate | maxLift | avgLift |
| --- | --- | --- | --- | --- |
| AxonFramework-5.0.3/.github/workflows/main.yml | 347 | 0.0008650777822098126 | 4.603669724770642 | 3.303321776553514 |
| AxonFramework-5.0.3/axon-5/api-changes.md | 267 | 0.00022244068248467077 | 4.147107438016529 | 1.137739671744467 |
| AxonFramework-5.0.3/.github/workflows/pullrequest.yml | 187 | 0.0006804602385613542 | 4.572209567198177 | 2.3972065051804257 |
| AxonFramework-5.0.3/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/AggregateBasedStorageEngineTestSuite.java | 179 | 0.00040109528141651614 | 6.747310756972111 | 3.4460680344356405 |
| AxonFramework-5.0.3/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/StorageEngineTestSuite.java | 163 | 0.0005166533541262536 | 5.9126024590163935 | 3.3061979252896485 |
| AxonFramework-5.0.3/axon-server-connector/src/main/java/org/axonframework/axonserver/connector/event/AggregateBasedAxonServerEventStorageEngine.java | 135 | 0.0008593143308169215 | 7.8 | 3.9457751402962025 |
| AxonFramework-5.0.3/eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/DefaultEventStoreTransaction.java | 110 | 0.0009863701578192252 | 7.840625 | 4.425570323422612 |
| AxonFramework-5.0.3/eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/jpa/AggregateBasedJpaEventStorageEngine.java | 97 | 0.0013457269700332963 | 7.100943396226414 | 2.649145306018789 |
| AxonFramework-5.0.3/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/DefaultEventStoreTransactionTest.java | 92 | 0.0023840373153666754 | 6.493882352941177 | 3.938542220763463 |
| AxonFramework-5.0.3/eventsourcing/src/main/java/org/axonframework/eventsourcing/configuration/EventSourcingConfigurationDefaults.java | 84 | 0.0017314946509183107 | 7.448720716830401 | 3.6467331096014206 |

[Full data](./List_git_files_that_were_changed_together_with_another_file.csv)

### 3.4 Co-Changed With a Specific File (All in One)

| filePath | commitCount |
| --- | --- |
| AxonFramework-5.0.3/.github/workflows/pullrequest.yml | 412 |
| AxonFramework-5.0.3/.github/workflows/main.yml | 407 |
| AxonFramework-5.0.3/axon-5/api-changes.md | 303 |
| AxonFramework-5.0.3/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/AggregateBasedStorageEngineTestSuite.java | 211 |
| AxonFramework-5.0.3/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/StorageEngineTestSuite.java | 193 |
| AxonFramework-5.0.3/eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/jpa/AggregateBasedJpaEventStorageEngine.java | 168 |
| AxonFramework-5.0.3/axon-server-connector/src/main/java/org/axonframework/axonserver/connector/event/AggregateBasedAxonServerEventStorageEngine.java | 165 |
| AxonFramework-5.0.3/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/DefaultEventStoreTransactionTest.java | 133 |
| AxonFramework-5.0.3/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/SimpleEventStoreTest.java | 127 |
| AxonFramework-5.0.3/eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/DefaultEventStoreTransaction.java | 126 |

### 3.5 Co-Changed Files (Charts)



---

## 4. File Change Distribution

Files changed per commit. High proportion of large commits = low commit granularity.

### 4.1 Files per Commit Distribution

| filesPerCommit | commitCount |
| --- | --- |
| 1 | 6327 |
| 2 | 2609 |
| 3 | 1214 |
| 4 | 799 |
| 5 | 552 |
| 6 | 401 |
| 7 | 323 |
| 8 | 264 |
| 9 | 195 |
| 10 | 180 |

[Full data](./List_git_files_per_commit_distribution.csv)

### 4.2 Files per Commit Chart



---

## 5. Pairwise Changed Files

Commit overlap counts and dependency info between file pairs.

### 5.1 Pairwise Changed Files

| firstFileName | secondFileName | filePairLineBreak | filePairWithRelativePathLineBreak | filePair | filePairWithRelativePath | firstFileExtension | secondFileExtension | fileExtensionPair | updateCommitCount | updateCommitMinConfidence | updateCommitSupport | updateCommitLift | updateCommitJaccardSimilarity |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/AggregateBasedStorageEngineTestSuite.java | eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/InterceptingEventStoreTest.java | AggregateBasedStorageEngineTestSuite<br>InterceptingEventStoreTest | eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/AggregateBasedStorageEngineTestSuite.java<br>eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/InterceptingEventStoreTest.java | AggregateBasedStorageEngineTestSuite↔InterceptingEventStoreTest | eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/AggregateBasedStorageEngineTestSuite.java↔eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/InterceptingEventStoreTest.java | java | java | java↔java | 15 | 0.40540540540540543 | 0.005978477481068154 | 4.052438893076343 | 0.054945054945054944 |
| extensions/spring/spring/src/main/java/org/axonframework/extension/spring/config/SpringAxonApplication.java | extensions/spring/spring/src/main/java/org/axonframework/extension/spring/config/SpringComponentRegistry.java | SpringAxonApplication<br>SpringComponentRegistry | extensions/spring/spring/src/main/java/org/axonframework/extension/spring/config/SpringAxonApplication.java<br>extensions/spring/spring/src/main/java/org/axonframework/extension/spring/config/SpringComponentRegistry.java | SpringAxonApplication↔SpringComponentRegistry | extensions/spring/spring/src/main/java/org/axonframework/extension/spring/config/SpringAxonApplication.java↔extensions/spring/spring/src/main/java/org/axonframework/extension/spring/config/SpringComponentRegistry.java | java | java | java↔java | 4 | 0.2222222222222222 | 0.0015942606616181746 | 17.42361111111111 | 0.08695652173913043 |
| mvnw.cmd | .gitignore | mvnw<br> | mvnw.cmd<br>.gitignore | mvnw↔ | mvnw.cmd↔.gitignore | cmd | gitignore | cmd↔gitignore | 9 | 0.2 | 0.0035870864886408927 | 4.733962264150943 | 0.06338028169014084 |
| mvnw | .gitignore | mvn<br> | mvnw<br>.gitignore | mvn↔ | mvnw↔.gitignore |  | gitignore | ↔gitignore | 11 | 0.15714285714285714 | 0.00438421681944998 | 3.7195417789757412 | 0.06666666666666667 |
| .gitignore | axon-5/api-changes.md | <br>api-changes | .gitignore<br>axon-5/api-changes.md | ↔api-changes | .gitignore↔axon-5/api-changes.md | gitignore | md | gitignore↔md | 4 | 0.03773584905660377 | 0.0015942606616181746 | 0.15649462030251052 | 0.005657708628005658 |
| test/src/test/java/org/axonframework/test/fixture/AxonTestFixtureMessagingTest.java | axon-5/api-changes.md | AxonTestFixtureMessagingTest<br>api-changes | test/src/test/java/org/axonframework/test/fixture/AxonTestFixtureMessagingTest.java<br>axon-5/api-changes.md | AxonTestFixtureMessagingTest↔api-changes | test/src/test/java/org/axonframework/test/fixture/AxonTestFixtureMessagingTest.java↔axon-5/api-changes.md | java | md | java↔md | 27 | 0.2903225806451613 | 0.010761259465922678 | 1.203998933617702 | 0.040238450074515646 |
| axon-server-connector/src/main/java/org/axonframework/axonserver/connector/query/AxonServerQueryBusConnector.java | axon-5/api-changes.md | AxonServerQueryBusConnector<br>api-changes | axon-server-connector/src/main/java/org/axonframework/axonserver/connector/query/AxonServerQueryBusConnector.java<br>axon-5/api-changes.md | AxonServerQueryBusConnector↔api-changes | axon-server-connector/src/main/java/org/axonframework/axonserver/connector/query/AxonServerQueryBusConnector.java↔axon-5/api-changes.md | java | md | java↔md | 3 | 0.05660377358490566 | 0.0011956954962136308 | 0.23474193045376576 | 0.004580152671755725 |
| stash/todo/src/main/java/org/axonframework/messaging/eventhandling/annotation/AnnotationEventHandlerAdapter.java | axon-5/api-changes.md | AnnotationEventHandlerAdapter<br>api-changes | stash/todo/src/main/java/org/axonframework/messaging/eventhandling/annotation/AnnotationEventHandlerAdapter.java<br>axon-5/api-changes.md | AnnotationEventHandlerAdapter↔api-changes | stash/todo/src/main/java/org/axonframework/messaging/eventhandling/annotation/AnnotationEventHandlerAdapter.java↔axon-5/api-changes.md | java | md | java↔md | 4 | 0.6666666666666666 | 0.0015942606616181746 | 2.7647382920110193 | 0.006589785831960461 |
| eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/jpa/AggregateBasedJpaEventStorageEngineConfiguration.java | axon-5/api-changes.md | AggregateBasedJpaEventStorageEngineConfiguration<br>api-changes | eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/jpa/AggregateBasedJpaEventStorageEngineConfiguration.java<br>axon-5/api-changes.md | AggregateBasedJpaEventStorageEngineConfiguration↔api-changes | eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/jpa/AggregateBasedJpaEventStorageEngineConfiguration.java↔axon-5/api-changes.md | java | md | java↔md | 3 | 0.09375 | 0.0011956954962136308 | 0.3887913223140496 | 0.00473186119873817 |
| messaging/src/test/java/org/axonframework/messaging/commandhandling/SimpleCommandHandlingComponentTest.java | axon-5/api-changes.md | SimpleCommandHandlingComponentTest<br>api-changes | messaging/src/test/java/org/axonframework/messaging/commandhandling/SimpleCommandHandlingComponentTest.java<br>axon-5/api-changes.md | SimpleCommandHandlingComponentTest↔api-changes | messaging/src/test/java/org/axonframework/messaging/commandhandling/SimpleCommandHandlingComponentTest.java↔axon-5/api-changes.md | java | md | java↔md | 4 | 0.5 | 0.0015942606616181746 | 2.0735537190082645 | 0.006568144499178982 |

[Full data](./List_pairwise_changed_files.csv)

### 5.2 Pairwise Changed Files (Top by Lift)

File pairs that co-change more often than random chance (lift > 1).

| fileExtensionPair | firstFileNameShort | secondFileNameShort | updateCommitCount | updateCommitMinConfidence | updateCommitLift | updateCommitJaccardSimilarity | updateCommitSupport | firstFileName | secondFileName |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| java↔java | HandlerAttributes | SequencingPolicy | 3 | 1 | 836.3333333333335 | 1 | 0.0011956954962136308 | messaging/src/main/java/org/axonframework/messaging/core/annotation/HandlerAttributes.java | messaging/src/main/java/org/axonframework/messaging/core/annotation/SequencingPolicy.java |
| java↔java | FieldChildEntityFieldDefinitionTest | GetterEvolverChildEntityFieldDefinitionTest | 3 | 1 | 836.3333333333335 | 1 | 0.0011956954962136308 | modelling/src/test/java/org/axonframework/modelling/entity/child/FieldChildEntityFieldDefinitionTest.java | modelling/src/test/java/org/axonframework/modelling/entity/child/GetterEvolverChildEntityFieldDefinitionTest.java |
| java↔java | FieldChildEntityFieldDefinitionTest | GetterSetterChildEntityFieldDefinitionTest | 3 | 1 | 836.3333333333335 | 1 | 0.0011956954962136308 | modelling/src/test/java/org/axonframework/modelling/entity/child/FieldChildEntityFieldDefinitionTest.java | modelling/src/test/java/org/axonframework/modelling/entity/child/GetterSetterChildEntityFieldDefinitionTest.java |
| java↔java | GetterEvolverChildEntityFieldDefinitionTest | GetterSetterChildEntityFieldDefinitionTest | 3 | 1 | 836.3333333333335 | 1 | 0.0011956954962136308 | modelling/src/test/java/org/axonframework/modelling/entity/child/GetterEvolverChildEntityFieldDefinitionTest.java | modelling/src/test/java/org/axonframework/modelling/entity/child/GetterSetterChildEntityFieldDefinitionTest.java |
| java↔java | UpdateCheckerAutoConfigurationTest | UpdateCheckerTest | 3 | 1 | 627.25 | 0.75 | 0.0011956954962136308 | extensions/spring/spring-boot-autoconfigure/src/test/java/org/axonframework/extension/springboot/autoconfig/UpdateCheckerAutoConfigurationTest.java | update/src/test/java/org/axonframework/update/UpdateCheckerTest.java |
| java↔java | Command | AnnotationMessageTypeResolver | 3 | 1 | 627.25 | 0.75 | 0.0011956954962136308 | messaging/src/main/java/org/axonframework/messaging/commandhandling/annotation/Command.java | messaging/src/main/java/org/axonframework/messaging/core/annotation/AnnotationMessageTypeResolver.java |
| java↔java | Command | Event | 4 | 1 | 627.25 | 1 | 0.0015942606616181746 | messaging/src/main/java/org/axonframework/messaging/commandhandling/annotation/Command.java | messaging/src/main/java/org/axonframework/messaging/eventhandling/annotation/Event.java |
| java↔java | Command | Query | 4 | 1 | 627.25 | 1 | 0.0015942606616181746 | messaging/src/main/java/org/axonframework/messaging/commandhandling/annotation/Command.java | messaging/src/main/java/org/axonframework/messaging/queryhandling/annotation/Query.java |
| java↔java | Command | QueryResponse | 4 | 1 | 627.25 | 1 | 0.0015942606616181746 | messaging/src/main/java/org/axonframework/messaging/commandhandling/annotation/Command.java | messaging/src/main/java/org/axonframework/messaging/queryhandling/annotation/QueryResponse.java |
| java↔java | AnnotationMessageTypeResolver | Event | 3 | 1 | 627.25 | 0.75 | 0.0011956954962136308 | messaging/src/main/java/org/axonframework/messaging/core/annotation/AnnotationMessageTypeResolver.java | messaging/src/main/java/org/axonframework/messaging/eventhandling/annotation/Event.java |

[Full data](./List_pairwise_changed_files_top_lift.csv)

### 5.3 Pairwise Changed Files With Dependencies

Files that are co-changed and also have a structural dependency relationship between them.

| dependencyWeight | fileDistance | commitCount | updateCommitMinConfidence | updateCommitSupport | updateCommitLift | updateCommitJaccardSimilarity |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | null | 3 | 0.375 | 0.0011956954962136308 | 30.350806451612904 | 0.08333333333333333 |
| 1 | 4 | 3 | 0.6 | 0.0011956954962136308 | 215.05714285714285 | 0.3333333333333333 |
| 1 | 0 | 3 | 0.25 | 0.0011956954962136308 | 39.203125 | 0.12 |
| 1 | 0 | 3 | 0.14285714285714285 | 0.0011956954962136308 | 15.583850931677018 | 0.07317073170731707 |
| 1 | 0 | 3 | 0.14285714285714285 | 0.0011956954962136308 | 15.583850931677018 | 0.07317073170731707 |
| 1 | 0 | 5 | 0.10416666666666667 | 0.0019928258270227183 | 3.7336309523809526 | 0.04424778761061947 |
| 1 | 2 | 5 | 0.45454545454545453 | 0.0019928258270227183 | 76.03030303030303 | 0.23809523809523808 |
| 1 | 0 | 5 | 0.38461538461538464 | 0.0019928258270227183 | 64.33333333333333 | 0.21739130434782608 |
| 1 | 0 | 5 | 0.7142857142857143 | 0.0019928258270227183 | 224.01785714285714 | 0.5 |
| 1 | 0 | 36 | 0.6 | 0.01434834595456357 | 23.895238095238096 | 0.41379310344827586 |

[Full data](./List_pairwise_changed_files_with_dependencies.csv)

### 5.4 Pairwise Changed Files (Charts)



---

## 6. Files by Author

Per-author file commit stats. Useful for knowledge boundaries and bus-factor risk.

### 6.1 Files with Commit Statistics by Author

| filePath | author | commitCount | commitHashes | lastCommitDate | lastCreationDate | lastModificationDate | daysSinceLastCommit | daysSinceLastCreation | daysSinceLastModification | maxCommitSha |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| AxonFramework-5.0.3/.editorconfig | Steven van Beelen | 25 | ["ed4ef4798fb13591b00a27a457ea909965685a6d","9bbb65763e1c496502f177e324dd7ef0d628c30d","e5ef80fb51d51f626a32d37be0a02c4596864da5","6fab65a41e4e9de44b0a1501fb9502fc5a83f67c","11f108a3aa78920dd461d2fc9023370670ba69d1","3a58958aad104eac7db5373ffb58582a8798bf59","a6d283c8558acabb8e516e7fdd85a646761338ce","d6f25f0c8c238cc5fc55fee1d0a15665de45f9fc","3435d059f69531c41961efe31b1c7677eae74cf4","42e6bb2abf71de2ae6983ad74bb6e9cbbbddff88","0d4464fc942003f70fea27998e89b9bb1661f6ea","50a0255f0e5d684ef9b2f049c4223c69ad05eb19","400c9cf44f70325982fb1c6ae706d6770a1f5ce6","84429c4a349528b894414289d12edc41879fcdfe","f4746a871e454c40b72346d541bbcfc9ffc7680d","bb296a1a59fda71b2ba652557183b348dea6a45f","8e02e0f72febad8be5c6b9b3a4d520b2772f2876","523af9947b9a163be8712f16b8e4a09db2d1dd03","16b6216b13f5ea8b36d1a83d73c0b2937b4e2371","da9b783ce78ecc4248d5d9959704c3a7e54f916e","cd36b0ee3df842034b1a0af89712248e8088508f","113054bda3adda44476ac412b7602a7e02891ad7","d3db0040babf3e4efe690bc809e23944e1b07d6e","0aa12fb52f302cb2de367244488d588bf029ccda","9df62332f0f803d4eab8048eeb565d3c058c806b"] | 2026-02-23 | 2025-01-09 | 2025-01-09 | 83 | 493 | 493 | f4746a871e454c40b72346d541bbcfc9ffc7680d |
| AxonFramework-5.0.3/.editorconfig | Allard Buijze | 2 | ["fe926a4970bdf1e538e8e7fb8d147ffdc676e713","5cf026466da09d2c38cb7617e38c09ed388f6ec2"] | 2025-01-15 | 2025-01-09 | 2025-01-09 | 487 | 493 | 493 | fe926a4970bdf1e538e8e7fb8d147ffdc676e713 |
| AxonFramework-5.0.3/.editorconfig | Jan Galinski | 1 | ["1afe4ecfac2413ade046b76588845f02b194c5b5"] | 2026-02-04 | 2025-01-09 | 2025-01-09 | 102 | 493 | 493 | 1afe4ecfac2413ade046b76588845f02b194c5b5 |
| AxonFramework-5.0.3/.gitattributes | Steven van Beelen | 8 | ["9bbb65763e1c496502f177e324dd7ef0d628c30d","e5ef80fb51d51f626a32d37be0a02c4596864da5","6fab65a41e4e9de44b0a1501fb9502fc5a83f67c","11f108a3aa78920dd461d2fc9023370670ba69d1","3a58958aad104eac7db5373ffb58582a8798bf59","a6d283c8558acabb8e516e7fdd85a646761338ce","d6f25f0c8c238cc5fc55fee1d0a15665de45f9fc","3435d059f69531c41961efe31b1c7677eae74cf4"] | 2026-02-23 | 2015-08-28 | 2026-02-23 | 83 | 3915 | 83 | e5ef80fb51d51f626a32d37be0a02c4596864da5 |
| AxonFramework-5.0.3/.gitattributes | Rene de Waele | 5 | ["3ce1ec62a72d911ee9208e81074994a46bddbeab","bf03c7bee697b35e490595713bed4e8f9a00f5b8","b63347b7d467efadaf4796d387963eba173fa372","b879ea59bac67f22232116d594fd4d790226778b","4814228a9fe5fb185a5ef0d96c62d84d627626d2"] | 2016-06-09 | 2015-08-28 | 2026-02-23 | 3629 | 3915 | 83 | bf03c7bee697b35e490595713bed4e8f9a00f5b8 |
| AxonFramework-5.0.3/.gitattributes | Allard Buijze | 5 | ["6f9a453a0114505096687c5cab3d43eb48f45c74","df54dcf98807751a0368ee2e9906879b7f495330","81d544425252b6a6f4020da93f7909803023ab35","c789dee3e69f89858387ca30c63c14d2a71bb5d5","7de1e90034f018980e8dcf7bc10ddfb2ba917dbf"] | 2025-11-06 | 2015-08-28 | 2026-02-23 | 192 | 3915 | 83 | df54dcf98807751a0368ee2e9906879b7f495330 |
| AxonFramework-5.0.3/.gitattributes | Simon Zambrovski | 5 | ["8d6f2a1d98c65d3cdf07d8517041074c4310e962","53bd786a641f4b8d3078a35e78dda74ab56d34a7","0410f493e3e800979da378f09184cea9244afa48","43098d9a64b8c9b983e77b86cc6620205af44b93","029c6c9027896429ebf8b4ad60a8538d1ecca034"] | 2025-11-06 | 2015-08-28 | 2026-02-23 | 192 | 3915 | 83 | 8d6f2a1d98c65d3cdf07d8517041074c4310e962 |
| AxonFramework-5.0.3/.gitattributes | Jan Galinski | 3 | ["1afe4ecfac2413ade046b76588845f02b194c5b5","d7929be4a8b9905a880c6cd65e50b29b7f07bef3","7d2b7604190889be38e0a709600a333defcff95a"] | 2026-02-04 | 2015-08-28 | 2026-02-23 | 102 | 3915 | 83 | d7929be4a8b9905a880c6cd65e50b29b7f07bef3 |
| AxonFramework-5.0.3/.gitattributes | sara pellegrini | 3 | ["9139ffc65f4298abc08b966528da68cd214cc7a0","e38027184fa5221e622dcafa3a50704f38e5a153","8eff22810fff1a695194fd40f14792186a99635d"] | 2018-09-10 | 2015-08-28 | 2026-02-23 | 2806 | 3915 | 83 | e38027184fa5221e622dcafa3a50704f38e5a153 |
| AxonFramework-5.0.3/.gitattributes | Joris van der Kallen | 1 | ["6461d8599abc5333601d6d3f266cc75ef8fb4173"] | 2016-06-08 | 2015-08-28 | 2026-02-23 | 3630 | 3915 | 83 | 6461d8599abc5333601d6d3f266cc75ef8fb4173 |

[Full data](./List_git_files_with_commit_statistics_by_author.csv)

---

## 7. Data Quality

Files in git log that are unresolved (not found in codebase) or ambiguous (multiple matches). Affects reliability of co-change metrics.

### 7.1 File Resolution Summary

Resolved vs. ambiguous vs. unresolved files by extension.

| resolved | extension | gitFileCount | fileLabels | gitFileExamples |
| --- | --- | --- | --- | --- |
| false | java | 13270 | ["File","Git"] | ["eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/AggregateBasedStorageEngineTestSuite.java","eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/InterceptingEventStoreTest.java","eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/StorageEngineBackedEventStoreTestSuite.java","axon-server-connector/src/test/java/org/axonframework/axonserver/connector/event/TaggedEventConverterTest.java","axon-server-connector/src/test/java/org/axonframework/axonserver/connector/query/StreamingQueryIT.java","axon-server-connector/src/test/java/org/axonframework/axonserver/connector/util/EventProcessorInfoConfigurationTest.java","conversion/src/main/java/org/axonframework/conversion/json/ByteArrayToJsonNodeConverter.java","conversion/src/main/java/org/axonframework/conversion/json/JacksonConverter.java","conversion/src/main/java/org/axonframework/conversion/json/JsonNodeToByteArrayConverter.java"] |
| false | xml | 508 | ["File","Git"] | ["examples/university-java/pom.xml","axon-framework-bom/pom.xml","axon-server-connector/pom.xml","build/parent/pom.xml","common/pom.xml","conversion/pom.xml","eventsourcing/pom.xml","extensions/metrics/metrics-dropwizard/pom.xml","extensions/metrics/metrics-micrometer/pom.xml"] |
| false | adoc | 475 | ["File","Git"] | ["docs/reference-guide/modules/ROOT/pages/conversion.adoc","docs/reference-guide/modules/commands/pages/command-handlers.adoc","docs/reference-guide/modules/migration/pages/paths/aggregates/configuration-migration.adoc","docs/reference-guide/modules/migration/pages/paths/aggregates/polymorphism-migration.adoc","docs/reference-guide/modules/migration/pages/paths/event-store.adoc","docs/reference-guide/modules/migration/pages/paths/messages.adoc","docs/reference-guide/modules/migration/pages/paths/projectors-event-processors.adoc","docs/reference-guide/modules/migration/pages/paths/test-fixtures.adoc","docs/reference-guide/modules/testing/pages/basic-testing.adoc"] |
| false | png | 196 | ["File","Git"] | ["docs/getting-started/modules/ROOT/images/AxonServer_DCBContext_Creation.png","docs/getting-started/modules/ROOT/images/AxonServer_DCBEvents_Search.png","docs/getting-started/modules/ROOT/images/EventModeling_CreateCourse_Done.png","docs/getting-started/modules/ROOT/images/EventModeling_CreateCourse_GWT_Spec1.png","docs/getting-started/modules/ROOT/images/EventModeling_CreateCourse_GWT_Spec2.png","docs/getting-started/modules/ROOT/images/EventModeling_CreateCourse_Stickies.png","docs/getting-started/modules/ROOT/images/EventModeling_GWT_SubscribeStudent.png","docs/getting-started/modules/ROOT/images/FacultyContext_EventModeling.png","docs/reference-guide/modules/ROOT/images/axoniq-console-teaser.png"] |
| false | xsl | 160 | ["File","Git"] | ["documentation/src/main/docbook/styles/docbook/VERSION.xsl","documentation/src/main/docbook/styles/docbook/common/autoidx-kosek.xsl","documentation/src/main/docbook/styles/docbook/common/autoidx-kimber.xsl","documentation/src/main/docbook/styles/docbook/common/common.xsl","documentation/src/main/docbook/styles/docbook/common/charmap.xsl","documentation/src/main/docbook/styles/docbook/common/gentext.xsl","documentation/src/main/docbook/styles/docbook/common/insertfile.xsl","documentation/src/main/docbook/styles/docbook/common/labels.xsl","documentation/src/main/docbook/styles/docbook/common/l10n.xsl"] |
| false | properties | 157 | ["File","Git"] | ["extensions/spring/spring-boot-autoconfigure/src/test/resources/application.serializer-without-jackson.test.properties","spring-boot-4-integrationtests/src/test/resources/application-custom.properties","spring-boot-4-integrationtests/src/test/resources/application.serializertest.properties","spring-boot-4-integrationtests/src/test/resources/hsqldb.database.properties","spring-boot-4-integrationtests/src/test/resources/log4j2.properties",".mvn/wrapper/maven-wrapper.properties","axon-server-connector/src/test/resources/junit-platform.properties","axon-server-connector/src/test/resources/log4j2.properties","config/src/test/resources/log4j2.properties"] |
| false | as | 97 | ["File","Git"] | ["sample/addressbook/flex-ui/swf/src/main/flex/org/axonframework/examples/addressbook/commands/RemoveAddressCommand.as","sample/addressbook/flex-ui/swf/src/main/flex/org/axonframework/examples/addressbook/commands/RemoveContactCommand.as","sample/addressbook/flex-ui/swf/src/main/flex/org/axonframework/examples/addressbook/controllers/BaseController.as","sample/addressbook/flex-ui/swf/src/main/flex/org/axonframework/examples/addressbook/NotificationImagesCollection.as","sample/addressbook/flex-ui/swf/src/main/flex/org/axonframework/examples/addressbook/commands/ChangeContactNameCommand.as","sample/addressbook/flex-ui/swf/src/main/flex/org/axonframework/examples/addressbook/commands/CreateContactCommand.as","sample/addressbook/flex-ui/swf/src/main/flex/org/axonframework/examples/addressbook/commands/RegisterAddressCommand.as","sample/addressbook/flex-ui/swf/src/main/flex/org/axonframework/examples/addressbook/controllers/RemoveContactController.as","sample/addressbook/flex-ui/swf/src/main/flex/org/axonframework/examples/addressbook/controllers/RemovedItemController.as"] |
| false | svg | 65 | ["File","Git"] | [".idea/icon.svg","documentation/src/main/resources/images/callouts/10.svg","documentation/src/main/resources/images/callouts/1.svg","documentation/src/main/resources/images/callouts/12.svg","documentation/src/main/resources/images/callouts/11.svg","documentation/src/main/resources/images/callouts/14.svg","documentation/src/main/resources/images/callouts/13.svg","documentation/src/main/resources/images/callouts/18.svg","documentation/src/main/resources/images/callouts/17.svg"] |
| false | yml | 55 | ["File","Git"] | ["docs/meta-annotations-guide/antora.yml","spring-boot-4-integrationtests/test-docker-compose.yml",".github/dependabot.yml",".github/workflows/docs.yml",".github/workflows/examples.yml",".github/workflows/main.yml",".github/workflows/pullrequest.yml",".github/workflows/release-notes.yml",".github/workflows/slack-release-notification.yml"] |
| false | md | 44 | ["File","Git"] | ["axon-5/api-changes.md",".github/ISSUE_TEMPLATE.md",".github/ISSUE_TEMPLATE/1_feature_request.md",".github/ISSUE_TEMPLATE/2_enhancement_request.md",".github/ISSUE_TEMPLATE/3_bug_report.md",".github/ISSUE_TEMPLATE/4_documentation_change.md","README.md","axon-4-api-changes.md","axon-5/design-principles.md"] |

[Full data](./List_git_files_by_resolved_label_and_extension.csv)

### 7.2 Ambiguous Git Files

Match multiple codebase files — excluded from co-change analysis.

⚠️ _No data available — git history not imported for this codebase._

### 7.3 Unresolved Git Files

Not found in scanned codebase. May indicate deleted files, renames, or out-of-scope paths.

| codeFileExtension | firstThreeCodeFileLabels | codeFileCount | codeFileExamples |
| --- | --- | --- | --- |
| jar | ["File","Artifact"] | 11 | ["/axon-test-5.0.3.jar","/axon-messaging-5.0.3.jar","/axon-spring-boot-autoconfigure-5.0.3.jar","/axon-tracing-opentelemetry-5.0.3.jar","/axon-eventsourcing-5.0.3.jar","/axon-server-connector-5.0.3.jar"] |
| MF | ["File","Java"] | 1 | ["/META-INF/MANIFEST.MF"] |
| class | ["Type","File"] | 1109 | ["/org/axonframework/test/fixture/AxonTestPhase$Then.class","/org/axonframework/test/fixture/AxonTestPhase$Then$Nothing.class","/org/axonframework/test/fixture/AxonTestPhase$Then$Event.class","/org/axonframework/test/fixture/AxonTestPhase$When$Nothing.class","/org/axonframework/test/fixture/AxonTestPhase$When.class","/org/axonframework/test/fixture/AxonTestPhase$When$Event.class"] |
| xml | ["File","Maven"] | 11 | ["/META-INF/maven/org.axonframework/axon-test/pom.xml","/META-INF/maven/org.axonframework/axon-messaging/pom.xml","/META-INF/maven/org.axonframework.extensions.spring/axon-spring-boot-autoconfigure/pom.xml","/META-INF/maven/org.axonframework.extensions.tracing/axon-tracing-opentelemetry/pom.xml","/META-INF/maven/org.axonframework/axon-eventsourcing/pom.xml","/META-INF/maven/org.axonframework/axon-server-connector/pom.xml"] |
| properties | ["File","Java"] | 11 | ["/META-INF/maven/org.axonframework/axon-test/pom.properties","/META-INF/maven/org.axonframework/axon-messaging/pom.properties","/META-INF/spring-autoconfigure-metadata.properties","/META-INF/maven/org.axonframework.extensions.spring/axon-spring-boot-autoconfigure/pom.properties","/META-INF/maven/org.axonframework.extensions.tracing/axon-tracing-opentelemetry/pom.properties","/META-INF/maven/org.axonframework/axon-eventsourcing/pom.properties"] |

[Full data](./List_unresolved_git_files.csv)

---

## 8. Git Author Wordcloud

Visual overview of contributor names by commit frequency. Larger text = more commits.


![Git Author Wordcloud](./GitAuthorWordcloud.svg)


---

## 9. Glossary and Column Definitions

| Term | Definition |
|------|------------|
| `commits` | Number of git commits touching this file or directory. |
| `authors` | Number of distinct author identities contributing to this file or directory. |
| `coChanges` | Number of commits in which two files were changed together. |
| `coupling` | Ratio of co-changes to total commits (0–1). Higher = tighter logical coupling. |
| `coChangedWith` | The other file in a co-change pair. |
| `ambiguous` | A git file path that matches more than one node in the scanned codebase. |
| `unresolved` | A git file path that matches no node in the scanned codebase. |
| `filesPerCommit` | How many files were changed in a single commit. |
| `frequency` | Relative share of commits at a specific `filesPerCommit` count. |
