---
title: "Git History Report"
generated: "2026-05-18"
model_version: "v4.0.1"
dataset: "AxonFramework-5.1.0"
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
| AxonFramework-5.1.0 | AxonFramework-5.1.0 |  |  | Steven van Beelen | Allard Buijze | Mitchell Herrijgers | 116 | 2935 | 6735 | 2026-04-25 | 2026-04-28 | 2026-04-28 | 20 | 23 | 20 | fff5f9f26176f13bcd2824e006f71d61da2ac8b1 | AxonFramework-5.1.0/update/src/test/resources/META-INF/maven/org.axonframework/axon-modelling/pom.properties | 1 | 1 |
| AxonFramework-5.1.0/.claude | .claude | AxonFramework-5.1.0 | AxonFramework-5.1.0 | Mateusz Nowak | Steven van Beelen | Jan Galinski | 5 | 5 | 14 | 2026-02-19 | 2026-02-24 | 2026-03-23 | 56 | 88 | 83 | f86e96cf1f82bb61b9c269c928ea1afba539c052 | AxonFramework-5.1.0/.claude/skills/issue-from-notes/references/examples.md | 2 | 1 |
| AxonFramework-5.1.0/.claude/rules | rules | AxonFramework-5.1.0/.claude | .claude | Mateusz Nowak | Steven van Beelen | Jan Galinski | 5 | 2 | 9 | 2026-02-19 | 2026-02-19 | 2026-03-23 | 56 | 88 | 88 | f86e96cf1f82bb61b9c269c928ea1afba539c052 | AxonFramework-5.1.0/.claude/rules/type-safety.md | 3 | 1 |
| AxonFramework-5.1.0/.claude/skills/issue-from-notes | skills/issue-from-notes | AxonFramework-5.1.0/.claude | .claude | Steven van Beelen | Mateusz Nowak | Jan Galinski | 5 | 2 | 11 | 2026-02-16 | 2026-02-24 | 2026-03-23 | 56 | 91 | 83 | f86e96cf1f82bb61b9c269c928ea1afba539c052 | AxonFramework-5.1.0/.claude/skills/issue-from-notes/references/examples.md | 4 | 2 |
| AxonFramework-5.1.0/.claude/skills/issue-from-notes/references | references | AxonFramework-5.1.0/.claude/skills/issue-from-notes | issue-from-notes | Steven van Beelen | Mateusz Nowak | Jan Galinski | 5 | 1 | 8 | 2026-02-16 | 2026-02-16 | 2026-03-23 | 56 | 91 | 91 | f86e96cf1f82bb61b9c269c928ea1afba539c052 | AxonFramework-5.1.0/.claude/skills/issue-from-notes/references/examples.md | 5 | 1 |
| AxonFramework-5.1.0/.github | .github | AxonFramework-5.1.0 | AxonFramework-5.1.0 | Steven van Beelen | dependabot[bot] | Mitchell Herrijgers | 31 | 16 | 790 | 2025-12-01 | 2026-04-28 | 2026-04-28 | 20 | 168 | 20 | ffe75820f3cb4bb5d167941acb0f05e2c801c30c | AxonFramework-5.1.0/.github/workflows/slack-release-notification.yml | 2 | 1 |
| AxonFramework-5.1.0/.github/ISSUE_TEMPLATE | ISSUE_TEMPLATE | AxonFramework-5.1.0/.github | .github | Steven van Beelen | Mitchell Herrijgers | Allard Buijze | 7 | 4 | 61 | 2025-08-13 | 2026-02-23 | 2026-02-23 | 84 | 277 | 84 | fa509a0b37d60e0d49b0a95686836dc59e5dc146 | AxonFramework-5.1.0/.github/ISSUE_TEMPLATE/4_documentation_change.md | 3 | 1 |
| AxonFramework-5.1.0/.github/workflows | workflows | AxonFramework-5.1.0/.github | .github | Steven van Beelen | dependabot[bot] | Mitchell Herrijgers | 31 | 8 | 759 | 2025-12-01 | 2026-04-28 | 2026-04-28 | 20 | 168 | 20 | ffe75820f3cb4bb5d167941acb0f05e2c801c30c | AxonFramework-5.1.0/.github/workflows/slack-release-notification.yml | 3 | 1 |
| AxonFramework-5.1.0/.idea | .idea | AxonFramework-5.1.0 | AxonFramework-5.1.0 | Steven van Beelen | Mitchell Herrijgers | Allard Buijze | 6 | 4 | 68 | 2025-12-16 | 2025-12-16 | 2026-02-23 | 84 | 153 | 153 | fe926a4970bdf1e538e8e7fb8d147ffdc676e713 | AxonFramework-5.1.0/.idea/inspectionProfiles/Project_Default.xml | 2 | 1 |
| AxonFramework-5.1.0/.idea/copyright | copyright | AxonFramework-5.1.0/.idea | .idea | Steven van Beelen | Allard Buijze | Jan Galinski | 3 | 1 | 28 | 2025-01-09 | 2025-01-09 | 2026-02-23 | 84 | 494 | 494 | fe926a4970bdf1e538e8e7fb8d147ffdc676e713 | AxonFramework-5.1.0/.idea/copyright/Axon_Framework_copyright_template.xml | 3 | 1 |

[Full data](./List_git_file_directories_with_commit_statistics.csv)

### 2.2 Directory Commit Statistics (Charts)



---

## 3. Co-Changed Files

Files committed together = logical coupling signal. May belong to the same conceptual unit or share a concern.

### 3.1 Co-Changed File Pairs

| firstFile | secondFile | commitCount |
| --- | --- | --- |
| AxonFramework-5.1.0/.github/workflows/pullrequest.yml | AxonFramework-5.1.0/.github/workflows/main.yml | 362 |
| AxonFramework-5.1.0/eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/jpa/AggregateBasedJpaEventStorageEngine.java | AxonFramework-5.1.0/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/AggregateBasedStorageEngineTestSuite.java | 139 |
| AxonFramework-5.1.0/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/AggregateBasedStorageEngineTestSuite.java | AxonFramework-5.1.0/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/StorageEngineTestSuite.java | 138 |
| AxonFramework-5.1.0/eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/jpa/AggregateBasedJpaEventStorageEngine.java | AxonFramework-5.1.0/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/StorageEngineTestSuite.java | 108 |
| AxonFramework-5.1.0/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/AggregateBasedStorageEngineTestSuite.java | AxonFramework-5.1.0/axon-5/api-changes.md | 103 |
| AxonFramework-5.1.0/eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/jpa/AggregateBasedJpaEventStorageEngine.java | AxonFramework-5.1.0/axon-5/api-changes.md | 91 |
| AxonFramework-5.1.0/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/StorageEngineTestSuite.java | AxonFramework-5.1.0/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/DefaultEventStoreTransactionTest.java | 90 |
| AxonFramework-5.1.0/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/AggregateBasedStorageEngineTestSuite.java | AxonFramework-5.1.0/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/DefaultEventStoreTransactionTest.java | 88 |
| AxonFramework-5.1.0/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/StorageEngineTestSuite.java | AxonFramework-5.1.0/axon-5/api-changes.md | 84 |
| AxonFramework-5.1.0/.github/workflows/slack-release-notification.yml | AxonFramework-5.1.0/.github/workflows/main.yml | 80 |

### 3.2 Co-Changed File Pairs (All in One Commit)

Files changed together in a single large commit.

| firstFile | secondFile | commitCount |
| --- | --- | --- |
| AxonFramework-5.1.0/.github/workflows/main.yml | AxonFramework-5.1.0/.github/workflows/pullrequest.yml | 424 |
| AxonFramework-5.1.0/eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/jpa/AggregateBasedJpaEventStorageEngine.java | AxonFramework-5.1.0/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/AggregateBasedStorageEngineTestSuite.java | 161 |
| AxonFramework-5.1.0/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/AggregateBasedStorageEngineTestSuite.java | AxonFramework-5.1.0/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/StorageEngineTestSuite.java | 157 |
| AxonFramework-5.1.0/eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/jpa/AggregateBasedJpaEventStorageEngine.java | AxonFramework-5.1.0/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/StorageEngineTestSuite.java | 123 |
| AxonFramework-5.1.0/axon-5/api-changes.md | AxonFramework-5.1.0/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/AggregateBasedStorageEngineTestSuite.java | 119 |
| AxonFramework-5.1.0/axon-5/api-changes.md | AxonFramework-5.1.0/eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/jpa/AggregateBasedJpaEventStorageEngine.java | 104 |
| AxonFramework-5.1.0/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/AggregateBasedStorageEngineTestSuite.java | AxonFramework-5.1.0/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/DefaultEventStoreTransactionTest.java | 102 |
| AxonFramework-5.1.0/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/DefaultEventStoreTransactionTest.java | AxonFramework-5.1.0/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/StorageEngineTestSuite.java | 102 |
| AxonFramework-5.1.0/axon-5/api-changes.md | AxonFramework-5.1.0/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/StorageEngineTestSuite.java | 97 |
| AxonFramework-5.1.0/build/parent/pom.xml | AxonFramework-5.1.0/stash/migration/pom.xml | 90 |

### 3.3 Co-Changed With a Specific File

Shows all files that were changed together with another particular file.

| filePath | commitCount | coChangeRate | maxLift | avgLift |
| --- | --- | --- | --- | --- |
| AxonFramework-5.1.0/.github/workflows/pullrequest.yml | 375 | 0.0005310937699160164 | 5.085714285714286 | 2.6368687092909004 |
| AxonFramework-5.1.0/axon-5/api-changes.md | 232 | 0.0002508802436133676 | 3.330503144654088 | 1.1212748788773987 |
| AxonFramework-5.1.0/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/AggregateBasedStorageEngineTestSuite.java | 194 | 0.00041385077479691446 | 4.979035396590067 | 2.6751224874539843 |
| AxonFramework-5.1.0/eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/jpa/AggregateBasedJpaEventStorageEngine.java | 170 | 0.000500643474112315 | 5.255692852981161 | 2.5279827337757967 |
| AxonFramework-5.1.0/.github/workflows/main.yml | 169 | 0.00047672509605023385 | 5.075356415478615 | 1.8479094510838974 |
| AxonFramework-5.1.0/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/StorageEngineTestSuite.java | 162 | 0.0005647747873378888 | 5.335934526075372 | 2.4905522396689608 |
| AxonFramework-5.1.0/eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/DefaultEventStoreTransaction.java | 123 | 0.0006839488873319321 | 6.047328959700094 | 3.5177586254533835 |
| AxonFramework-5.1.0/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/DefaultEventStoreTransactionTest.java | 100 | 0.0012201818070892562 | 6.194230499929982 | 3.366812038436253 |
| AxonFramework-5.1.0/eventsourcing/src/test/java/org/axonframework/eventsourcing/configuration/EventSourcingConfigurerTest.java | 97 | 0.0009330152745181024 | 11.003826906093613 | 4.0622148023662294 |
| AxonFramework-5.1.0/.github/workflows/slack-release-notification.yml | 87 | 0.0015896217796455326 | 19.16923076923077 | 5.259641993649403 |

[Full data](./List_git_files_that_were_changed_together_with_another_file.csv)

### 3.4 Co-Changed With a Specific File (All in One)

| filePath | commitCount |
| --- | --- |
| AxonFramework-5.1.0/.github/workflows/pullrequest.yml | 438 |
| AxonFramework-5.1.0/.github/workflows/main.yml | 435 |
| AxonFramework-5.1.0/axon-5/api-changes.md | 288 |
| AxonFramework-5.1.0/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/AggregateBasedStorageEngineTestSuite.java | 230 |
| AxonFramework-5.1.0/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/StorageEngineTestSuite.java | 199 |
| AxonFramework-5.1.0/eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/jpa/AggregateBasedJpaEventStorageEngine.java | 194 |
| AxonFramework-5.1.0/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/DefaultEventStoreTransactionTest.java | 135 |
| AxonFramework-5.1.0/eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/DefaultEventStoreTransaction.java | 132 |
| AxonFramework-5.1.0/eventsourcing/src/test/java/org/axonframework/eventsourcing/eventstore/SimpleEventStoreTest.java | 129 |
| AxonFramework-5.1.0/build/parent/pom.xml | 129 |

### 3.5 Co-Changed Files (Charts)



---

## 4. File Change Distribution

Files changed per commit. High proportion of large commits = low commit granularity.

### 4.1 Files per Commit Distribution

| filesPerCommit | commitCount |
| --- | --- |
| 1 | 6716 |
| 2 | 2754 |
| 3 | 1304 |
| 4 | 860 |
| 5 | 597 |
| 6 | 434 |
| 7 | 338 |
| 8 | 276 |
| 9 | 207 |
| 10 | 192 |

[Full data](./List_git_files_per_commit_distribution.csv)

### 4.2 Files per Commit Chart



---

## 5. Pairwise Changed Files

Commit overlap counts and dependency info between file pairs.

### 5.1 Pairwise Changed Files

| firstFileName | secondFileName | filePairLineBreak | filePairWithRelativePathLineBreak | filePair | filePairWithRelativePath | firstFileExtension | secondFileExtension | fileExtensionPair | updateCommitCount | updateCommitMinConfidence | updateCommitSupport | updateCommitLift | updateCommitJaccardSimilarity |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| mvnw | docs/reference-guide/modules/tuning/pages/index.adoc | mvn<br>index | mvnw<br>docs/reference-guide/modules/tuning/pages/index.adoc | mvn↔index | mvnw↔docs/reference-guide/modules/tuning/pages/index.adoc |  | adoc | ↔adoc | 3 | 0.13636363636363635 | 0.0009630818619582664 | 5.445804195804196 | 0.030927835051546393 |
| docs/reference-guide/modules/tuning/pages/index.adoc | docs/reference-guide/modules/tuning/partials/nav.adoc | index<br>nav | docs/reference-guide/modules/tuning/pages/index.adoc<br>docs/reference-guide/modules/tuning/partials/nav.adoc | index↔nav | docs/reference-guide/modules/tuning/pages/index.adoc↔docs/reference-guide/modules/tuning/partials/nav.adoc | adoc | adoc | adoc↔adoc | 5 | 0.45454545454545453 | 0.0016051364365971107 | 64.35950413223141 | 0.17857142857142858 |
| mvnw | docs/reference-guide/modules/tuning/partials/nav.adoc | mvn<br>nav | mvnw<br>docs/reference-guide/modules/tuning/partials/nav.adoc | mvn↔nav | mvnw↔docs/reference-guide/modules/tuning/partials/nav.adoc |  | adoc | ↔adoc | 3 | 0.2727272727272727 | 0.0009630818619582664 | 10.891608391608392 | 0.03488372093023256 |
| extensions/spring/spring-boot-autoconfigure/src/main/resources/META-INF/spring/org.springframework.boot.autoconfigure.AutoConfiguration.imports | extensions/spring/spring-boot-autoconfigure/src/test/java/org/axonframework/extension/springboot/eventsourcing/eventstore/jpa/AggregateBasedJpaEventStorageEngineIT.java | org.springframework.boot.autoconfigure.AutoConfiguration<br>AggregateBasedJpaEventStorageEngineIT | extensions/spring/spring-boot-autoconfigure/src/main/resources/META-INF/spring/org.springframework.boot.autoconfigure.AutoConfiguration.imports<br>extensions/spring/spring-boot-autoconfigure/src/test/java/org/axonframework/extension/springboot/eventsourcing/eventstore/jpa/AggregateBasedJpaEventStorageEngineIT.java | org.springframework.boot.autoconfigure.AutoConfiguration↔AggregateBasedJpaEventStorageEngineIT | extensions/spring/spring-boot-autoconfigure/src/main/resources/META-INF/spring/org.springframework.boot.autoconfigure.AutoConfiguration.imports↔extensions/spring/spring-boot-autoconfigure/src/test/java/org/axonframework/extension/springboot/eventsourcing/eventstore/jpa/AggregateBasedJpaEventStorageEngineIT.java | imports | java | imports↔java | 3 | 0.05 | 0.0009630818619582664 | 1.9228395061728394 | 0.021739130434782608 |
| eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/DefaultEventStoreTransaction.java | extensions/spring/spring-boot-autoconfigure/src/test/java/org/axonframework/extension/springboot/eventsourcing/eventstore/jpa/AggregateBasedJpaEventStorageEngineIT.java | DefaultEventStoreTransaction<br>AggregateBasedJpaEventStorageEngineIT | eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/DefaultEventStoreTransaction.java<br>extensions/spring/spring-boot-autoconfigure/src/test/java/org/axonframework/extension/springboot/eventsourcing/eventstore/jpa/AggregateBasedJpaEventStorageEngineIT.java | DefaultEventStoreTransaction↔AggregateBasedJpaEventStorageEngineIT | eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/DefaultEventStoreTransaction.java↔extensions/spring/spring-boot-autoconfigure/src/test/java/org/axonframework/extension/springboot/eventsourcing/eventstore/jpa/AggregateBasedJpaEventStorageEngineIT.java | java | java | java↔java | 4 | 0.06666666666666667 | 0.0012841091492776886 | 1.070446735395189 | 0.016 |
| eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/ContinuousMessageStream.java | extensions/spring/spring-boot-autoconfigure/src/test/java/org/axonframework/extension/springboot/eventsourcing/eventstore/jpa/AggregateBasedJpaEventStorageEngineIT.java | ContinuousMessageStream<br>AggregateBasedJpaEventStorageEngineIT | eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/ContinuousMessageStream.java<br>extensions/spring/spring-boot-autoconfigure/src/test/java/org/axonframework/extension/springboot/eventsourcing/eventstore/jpa/AggregateBasedJpaEventStorageEngineIT.java | ContinuousMessageStream↔AggregateBasedJpaEventStorageEngineIT | eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/ContinuousMessageStream.java↔extensions/spring/spring-boot-autoconfigure/src/test/java/org/axonframework/extension/springboot/eventsourcing/eventstore/jpa/AggregateBasedJpaEventStorageEngineIT.java | java | java | java↔java | 5 | 0.09433962264150944 | 0.0016051364365971107 | 4.897798742138366 | 0.046296296296296294 |
| eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/ContinuousMessageStream.java | messaging/src/main/java/org/axonframework/messaging/core/EmptyMessageStream.java | ContinuousMessageStream<br>EmptyMessageStream | eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/ContinuousMessageStream.java<br>messaging/src/main/java/org/axonframework/messaging/core/EmptyMessageStream.java | ContinuousMessageStream↔EmptyMessageStream | eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/ContinuousMessageStream.java↔messaging/src/main/java/org/axonframework/messaging/core/EmptyMessageStream.java | java | java | java↔java | 5 | 0.1388888888888889 | 0.0016051364365971107 | 8.16299790356394 | 0.05952380952380952 |
| messaging/src/main/java/org/axonframework/messaging/core/EmptyMessageStream.java | messaging/src/main/java/org/axonframework/messaging/core/FailedMessageStream.java | EmptyMessageStream<br>FailedMessageStream | messaging/src/main/java/org/axonframework/messaging/core/EmptyMessageStream.java<br>messaging/src/main/java/org/axonframework/messaging/core/FailedMessageStream.java | EmptyMessageStream↔FailedMessageStream | messaging/src/main/java/org/axonframework/messaging/core/EmptyMessageStream.java↔messaging/src/main/java/org/axonframework/messaging/core/FailedMessageStream.java | java | java | java↔java | 8 | 0.24242424242424243 | 0.002568218298555377 | 20.976430976430972 | 0.13114754098360656 |
| eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/ContinuousMessageStream.java | messaging/src/main/java/org/axonframework/messaging/core/FailedMessageStream.java | ContinuousMessageStream<br>FailedMessageStream | eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/ContinuousMessageStream.java<br>messaging/src/main/java/org/axonframework/messaging/core/FailedMessageStream.java | ContinuousMessageStream↔FailedMessageStream | eventsourcing/src/main/java/org/axonframework/eventsourcing/eventstore/ContinuousMessageStream.java↔messaging/src/main/java/org/axonframework/messaging/core/FailedMessageStream.java | java | java | java↔java | 5 | 0.15151515151515152 | 0.0016051364365971107 | 8.905088622069755 | 0.06172839506172839 |
| messaging/src/main/java/org/axonframework/messaging/core/FailedMessageStream.java | messaging/src/main/java/org/axonframework/messaging/core/FilteringMessageStream.java | FailedMessageStream<br>FilteringMessageStream | messaging/src/main/java/org/axonframework/messaging/core/FailedMessageStream.java<br>messaging/src/main/java/org/axonframework/messaging/core/FilteringMessageStream.java | FailedMessageStream↔FilteringMessageStream | messaging/src/main/java/org/axonframework/messaging/core/FailedMessageStream.java↔messaging/src/main/java/org/axonframework/messaging/core/FilteringMessageStream.java | java | java | java↔java | 5 | 0.16129032258064516 | 0.0016051364365971107 | 15.224828934506354 | 0.0847457627118644 |

[Full data](./List_pairwise_changed_files.csv)

### 5.2 Pairwise Changed Files (Top by Lift)

File pairs that co-change more often than random chance (lift > 1).

| fileExtensionPair | firstFileNameShort | secondFileNameShort | updateCommitCount | updateCommitMinConfidence | updateCommitLift | updateCommitJaccardSimilarity | updateCommitSupport | firstFileName | secondFileName |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| java↔java | NoOpSequencingPolicy | RoutingKeySequencingPolicy | 3 | 1 | 1038.3333333333333 | 1 | 0.0009630818619582664 | messaging/src/main/java/org/axonframework/messaging/core/sequencing/NoOpSequencingPolicy.java | messaging/src/main/java/org/axonframework/messaging/core/sequencing/RoutingKeySequencingPolicy.java |
| java↔java | NoOpSequencingPolicy | FullConcurrencyPolicyTest | 3 | 1 | 1038.3333333333333 | 1 | 0.0009630818619582664 | messaging/src/main/java/org/axonframework/messaging/core/sequencing/NoOpSequencingPolicy.java | messaging/src/test/java/org/axonframework/messaging/core/sequencing/FullConcurrencyPolicyTest.java |
| java↔java | NoOpSequencingPolicy | RoutingKeySequencingPolicyTest | 3 | 1 | 1038.3333333333333 | 1 | 0.0009630818619582664 | messaging/src/main/java/org/axonframework/messaging/core/sequencing/NoOpSequencingPolicy.java | messaging/src/test/java/org/axonframework/messaging/core/sequencing/RoutingKeySequencingPolicyTest.java |
| java↔java | NoOpSequencingPolicy | SequentialPolicyTest | 3 | 1 | 1038.3333333333333 | 1 | 0.0009630818619582664 | messaging/src/main/java/org/axonframework/messaging/core/sequencing/NoOpSequencingPolicy.java | messaging/src/test/java/org/axonframework/messaging/core/sequencing/SequentialPolicyTest.java |
| java↔java | RoutingKeySequencingPolicy | FullConcurrencyPolicyTest | 3 | 1 | 1038.3333333333333 | 1 | 0.0009630818619582664 | messaging/src/main/java/org/axonframework/messaging/core/sequencing/RoutingKeySequencingPolicy.java | messaging/src/test/java/org/axonframework/messaging/core/sequencing/FullConcurrencyPolicyTest.java |
| java↔java | RoutingKeySequencingPolicy | RoutingKeySequencingPolicyTest | 3 | 1 | 1038.3333333333333 | 1 | 0.0009630818619582664 | messaging/src/main/java/org/axonframework/messaging/core/sequencing/RoutingKeySequencingPolicy.java | messaging/src/test/java/org/axonframework/messaging/core/sequencing/RoutingKeySequencingPolicyTest.java |
| java↔java | RoutingKeySequencingPolicy | SequentialPolicyTest | 3 | 1 | 1038.3333333333333 | 1 | 0.0009630818619582664 | messaging/src/main/java/org/axonframework/messaging/core/sequencing/RoutingKeySequencingPolicy.java | messaging/src/test/java/org/axonframework/messaging/core/sequencing/SequentialPolicyTest.java |
| java↔java | FullConcurrencyPolicyTest | RoutingKeySequencingPolicyTest | 3 | 1 | 1038.3333333333333 | 1 | 0.0009630818619582664 | messaging/src/test/java/org/axonframework/messaging/core/sequencing/FullConcurrencyPolicyTest.java | messaging/src/test/java/org/axonframework/messaging/core/sequencing/RoutingKeySequencingPolicyTest.java |
| java↔java | FullConcurrencyPolicyTest | SequentialPolicyTest | 3 | 1 | 1038.3333333333333 | 1 | 0.0009630818619582664 | messaging/src/test/java/org/axonframework/messaging/core/sequencing/FullConcurrencyPolicyTest.java | messaging/src/test/java/org/axonframework/messaging/core/sequencing/SequentialPolicyTest.java |
| java↔java | RoutingKeySequencingPolicyTest | SequentialPolicyTest | 3 | 1 | 1038.3333333333333 | 1 | 0.0009630818619582664 | messaging/src/test/java/org/axonframework/messaging/core/sequencing/RoutingKeySequencingPolicyTest.java | messaging/src/test/java/org/axonframework/messaging/core/sequencing/SequentialPolicyTest.java |

[Full data](./List_pairwise_changed_files_top_lift.csv)

### 5.3 Pairwise Changed Files With Dependencies

Files that are co-changed and also have a structural dependency relationship between them.

| dependencyWeight | fileDistance | commitCount | updateCommitMinConfidence | updateCommitSupport | updateCommitLift | updateCommitJaccardSimilarity |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | 2 | 3 | 0.12 | 0.0009630818619582664 | 7.052830188679247 | 0.04 |
| 1 | 0 | 3 | 0.09090909090909091 | 0.0009630818619582664 | 6.43595041322314 | 0.04054054054054054 |
| 1 | 0 | 4 | 0.12121212121212122 | 0.0012841091492776886 | 10.204750204750205 | 0.06060606060606061 |
| 1 | 0 | 4 | 0.09523809523809523 | 0.0012841091492776886 | 6.742424242424242 | 0.04878048780487805 |
| 1 | 0 | 4 | 0.09523809523809523 | 0.0012841091492776886 | 7.063492063492063 | 0.05 |
| 1 | 0 | 4 | 0.09523809523809523 | 0.0012841091492776886 | 6.742424242424242 | 0.04878048780487805 |
| 1 | 4 | 4 | 0.10256410256410256 | 0.0012841091492776886 | 7.261072261072261 | 0.05063291139240506 |
| 1 | 0 | 5 | 0.1282051282051282 | 0.0016051364365971107 | 6.88549955791335 | 0.05434782608695652 |
| 1 | 0 | 6 | 0.08955223880597014 | 0.0019261637239165329 | 2.3842326827401457 | 0.033707865168539325 |
| 1 | 0 | 6 | 0.1935483870967742 | 0.0019261637239165329 | 15.072580645161292 | 0.09230769230769231 |

[Full data](./List_pairwise_changed_files_with_dependencies.csv)

### 5.4 Pairwise Changed Files (Charts)



---

## 6. Files by Author

Per-author file commit stats. Useful for knowledge boundaries and bus-factor risk.

### 6.1 Files with Commit Statistics by Author

| filePath | author | commitCount | commitHashes | lastCommitDate | lastCreationDate | lastModificationDate | daysSinceLastCommit | daysSinceLastCreation | daysSinceLastModification | maxCommitSha |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| AxonFramework-5.1.0/.claude/.mcp.json | Steven van Beelen | 3 | ["0d8494935f3df632c2f51767b80f3624b5d8ac14","5066f797b0ded94ff826b40752e4affd0f88f7dd","f86e96cf1f82bb61b9c269c928ea1afba539c052"] | 2026-03-23 | 2026-02-16 | 2026-02-16 | 56 | 91 | 91 | f86e96cf1f82bb61b9c269c928ea1afba539c052 |
| AxonFramework-5.1.0/.claude/.mcp.json | Mateusz Nowak | 2 | ["99bdfbc6fd46aea88993c080da524a14afcff9da","56bd673b907885495d8442ffbea9a5d2e4b6c5f5"] | 2026-02-16 | 2026-02-16 | 2026-02-16 | 91 | 91 | 91 | 99bdfbc6fd46aea88993c080da524a14afcff9da |
| AxonFramework-5.1.0/.claude/.mcp.json | Jan Galinski | 1 | ["be2d983a48bccdd3830d0d967e21cf5173a9c83b"] | 2026-02-19 | 2026-02-16 | 2026-02-16 | 88 | 91 | 91 | be2d983a48bccdd3830d0d967e21cf5173a9c83b |
| AxonFramework-5.1.0/.claude/.mcp.json | John Hendrikx | 1 | ["346c595d30b9744f3c62e68e2ae0410ef66ba4a2"] | 2026-03-11 | 2026-02-16 | 2026-02-16 | 68 | 91 | 91 | 346c595d30b9744f3c62e68e2ae0410ef66ba4a2 |
| AxonFramework-5.1.0/.claude/.mcp.json | hatzlj | 1 | ["28ead9298f9202653d199ccc5c96d9d6e176646f"] | 2026-03-20 | 2026-02-16 | 2026-02-16 | 59 | 91 | 91 | 28ead9298f9202653d199ccc5c96d9d6e176646f |
| AxonFramework-5.1.0/.claude/rules/completablefuture-blocking.md | Steven van Beelen | 3 | ["0d8494935f3df632c2f51767b80f3624b5d8ac14","5066f797b0ded94ff826b40752e4affd0f88f7dd","f86e96cf1f82bb61b9c269c928ea1afba539c052"] | 2026-03-23 | 2026-02-19 | 2026-02-19 | 56 | 88 | 88 | f86e96cf1f82bb61b9c269c928ea1afba539c052 |
| AxonFramework-5.1.0/.claude/rules/completablefuture-blocking.md | Mateusz Nowak | 2 | ["b5e771cf5a3bc0c91adcff8aa469393626f60f6f","534620c2aea7e5a5864d7d9bb59ecc9c866379a7"] | 2026-02-19 | 2026-02-19 | 2026-02-19 | 88 | 88 | 88 | b5e771cf5a3bc0c91adcff8aa469393626f60f6f |
| AxonFramework-5.1.0/.claude/rules/completablefuture-blocking.md | Jan Galinski | 1 | ["8a7cfbddb3ca69a62e0fd88926fce6d014c42ac4"] | 2026-02-24 | 2026-02-19 | 2026-02-19 | 83 | 88 | 88 | 8a7cfbddb3ca69a62e0fd88926fce6d014c42ac4 |
| AxonFramework-5.1.0/.claude/rules/completablefuture-blocking.md | John Hendrikx | 1 | ["346c595d30b9744f3c62e68e2ae0410ef66ba4a2"] | 2026-03-11 | 2026-02-19 | 2026-02-19 | 68 | 88 | 88 | 346c595d30b9744f3c62e68e2ae0410ef66ba4a2 |
| AxonFramework-5.1.0/.claude/rules/completablefuture-blocking.md | hatzlj | 1 | ["28ead9298f9202653d199ccc5c96d9d6e176646f"] | 2026-03-20 | 2026-02-19 | 2026-02-19 | 59 | 88 | 88 | 28ead9298f9202653d199ccc5c96d9d6e176646f |

[Full data](./List_git_files_with_commit_statistics_by_author.csv)

---

## 7. Data Quality

Files in git log that are unresolved (not found in codebase) or ambiguous (multiple matches). Affects reliability of co-change metrics.

### 7.1 File Resolution Summary

Resolved vs. ambiguous vs. unresolved files by extension.

| resolved | extension | gitFileCount | fileLabels | gitFileExamples |
| --- | --- | --- | --- | --- |
| false | java | 13838 | ["File","Git"] | ["extensions/spring/spring-boot-autoconfigure/src/test/java/org/axonframework/extension/springboot/autoconfig/EventProcessorPropertiesAndDefinitionInteractionTest.java","extensions/spring/spring-boot-autoconfigure/src/test/java/org/axonframework/extension/springboot/eventsourcing/eventstore/jpa/AggregateBasedJpaEventStorageEngineIT.java","integrationtests/src/test/java/org/axonframework/integrationtests/queryhandling/AbstractSubscriptionQueryTestSuite.java","messaging/src/test/java/org/axonframework/messaging/core/CloseCallbackMessageStreamTest.java","messaging/src/test/java/org/axonframework/messaging/core/ConcatenatingMessageStreamTest.java","messaging/src/test/java/org/axonframework/messaging/core/DelayedMessageStreamTest.java","messaging/src/test/java/org/axonframework/messaging/core/EmptyMessageStreamTest.java","messaging/src/test/java/org/axonframework/messaging/core/FluxMessageStreamTest.java","messaging/src/test/java/org/axonframework/messaging/core/MessageStreamGenericsTest.java"] |
| false | xml | 521 | ["File","Git"] | ["axon-server-connector/pom.xml","extensions/kotlin/kotlin-test/pom.xml","extensions/kotlin/kotlin/pom.xml","extensions/kotlin/pom.xml","extensions/pom.xml","pom.xml","build/parent/pom.xml","examples/pom.xml","examples/university-java-springboot-3/pom.xml"] |
| false | adoc | 494 | ["File","Git"] | ["docs/reference-guide/modules/monitoring/pages/index.adoc","docs/reference-guide/modules/monitoring/pages/tracing.adoc","docs/reference-guide/modules/monitoring/partials/nav.adoc","docs/reference-guide/modules/queries/pages/infrastructure.adoc","docs/reference-guide/modules/release-notes/partials/nav.adoc","docs/reference-guide/modules/sagas/pages/associations.adoc","docs/reference-guide/modules/sagas/pages/implementation.adoc","docs/reference-guide/modules/sagas/pages/index.adoc","docs/reference-guide/modules/sagas/pages/infrastructure.adoc"] |
| false | png | 199 | ["File","Git"] | ["examples/university-demo-kotlin/docs/images/AxonServer_DCBContext_Creation.png","examples/university-demo-kotlin/docs/images/EventModeling_GWT_SubscribeStudent.png","examples/university-demo-kotlin/docs/images/FacultyContext_EventModeling.png","docs/reference-guide/modules/commands/images/distributed-command-bus.png","docs/getting-started/modules/ROOT/images/AxonServer_DCBContext_Creation.png","docs/af5-getting-started/modules/ROOT/images/AxonServer_DCBContext_Creation.png","docs/af5-getting-started/modules/ROOT/images/AxonServer_DCBEvents_Search.png","docs/getting-started/modules/ROOT/images/AxonServer_DCBEvents_Search.png","docs/getting-started/modules/ROOT/images/EventModeling_CreateCourse_Done.png"] |
| false | xsl | 160 | ["File","Git"] | ["documentation/src/main/docbook/styles/docbook/VERSION.xsl","documentation/src/main/docbook/styles/docbook/common/autoidx-kimber.xsl","documentation/src/main/docbook/styles/docbook/common/autoidx-kosek.xsl","documentation/src/main/docbook/styles/docbook/common/charmap.xsl","documentation/src/main/docbook/styles/docbook/common/common.xsl","documentation/src/main/docbook/styles/docbook/common/gentext.xsl","documentation/src/main/docbook/styles/docbook/common/insertfile.xsl","documentation/src/main/docbook/styles/docbook/common/l10n.xsl","documentation/src/main/docbook/styles/docbook/common/labels.xsl"] |
| false | properties | 159 | ["File","Git"] | ["examples/university-demo-kotlin/src/test/resources/application.properties","extensions/spring/spring-boot-autoconfigure/src/test/resources/application-custom.properties","extensions/spring/spring-boot-autoconfigure/src/test/resources/log4j2.properties","extensions/spring/spring-boot-autoconfigure/src/test/resources/test.jgroups.application.properties","extensions/spring/spring-boot-autoconfigure/src/test/resources/test.metrics.application.properties","extensions/spring/spring-boot-autoconfigure/src/test/resources/test.springcloud.application.properties","integrationtests/src/test/resources/log4j2.properties","axon-server-connector/src/test/resources/junit-platform.properties","axon-server-connector/src/test/resources/log4j2.properties"] |
| false | as | 97 | ["File","Git"] | ["sample/addressbook/flex-ui/swf/src/main/flex/org/axonframework/examples/addressbook/commands/RemoveAddressCommand.as","sample/addressbook/flex-ui/swf/src/main/flex/org/axonframework/examples/addressbook/commands/RemoveContactCommand.as","sample/addressbook/flex-ui/swf/src/main/flex/org/axonframework/examples/addressbook/controllers/BaseController.as","sample/addressbook/flex-ui/swf/src/main/flex/org/axonframework/examples/addressbook/NotificationImagesCollection.as","sample/addressbook/flex-ui/swf/src/main/flex/org/axonframework/examples/addressbook/commands/ChangeContactNameCommand.as","sample/addressbook/flex-ui/swf/src/main/flex/org/axonframework/examples/addressbook/commands/CreateContactCommand.as","sample/addressbook/flex-ui/swf/src/main/flex/org/axonframework/examples/addressbook/commands/RegisterAddressCommand.as","sample/addressbook/flex-ui/swf/src/main/flex/org/axonframework/examples/addressbook/controllers/RemoveContactController.as","sample/addressbook/flex-ui/swf/src/main/flex/org/axonframework/examples/addressbook/controllers/RemovedItemController.as"] |
| false | svg | 65 | ["File","Git"] | [".idea/icon.svg","documentation/src/main/resources/images/callouts/11.svg","documentation/src/main/resources/images/callouts/12.svg","documentation/src/main/resources/images/callouts/1.svg","documentation/src/main/resources/images/callouts/10.svg","documentation/src/main/resources/images/callouts/15.svg","documentation/src/main/resources/images/callouts/16.svg","documentation/src/main/resources/images/callouts/17.svg","documentation/src/main/resources/images/callouts/18.svg"] |
| false | yml | 62 | ["File","Git"] | [".github/workflows/pullrequest.yml",".github/workflows/slack-release-notification.yml","docs/_reference-guide-preview/antora.yml","docs/getting-started/antora.yml","docs/identifier-generation-guide/antora.yml","docs/message-handler-customization-guide/antora.yml","docs/meta-annotations-guide/antora.yml","docs/reference-guide/antora.yml","examples/university-demo-kotlin/src/main/resources/application.yml"] |
| false | md | 58 | ["File","Git"] | ["README.md","CLAUDE.md",".claude/rules/completablefuture-blocking.md",".claude/rules/type-safety.md",".claude/skills/issue-from-notes/SKILL.md",".claude/skills/issue-from-notes/references/examples.md","AGENTS.md","axon-5/api-changes.md","docs/AGENTS.md"] |

[Full data](./List_git_files_by_resolved_label_and_extension.csv)

### 7.2 Ambiguous Git Files

Match multiple codebase files — excluded from co-change analysis.

⚠️ _No data available — git history not imported for this codebase._

### 7.3 Unresolved Git Files

Not found in scanned codebase. May indicate deleted files, renames, or out-of-scope paths.

| codeFileExtension | firstThreeCodeFileLabels | codeFileCount | codeFileExamples |
| --- | --- | --- | --- |
| jar | ["File","Artifact"] | 11 | ["/axon-eventsourcing-5.1.0.jar","/axon-conversion-5.1.0.jar","/axon-update-5.1.0.jar","/axoniq-spring-boot-autoconfigure-5.1.0.jar","/axon-modelling-5.1.0.jar","/axon-metrics-micrometer-5.1.0.jar"] |
| MF | ["File","Java"] | 1 | ["/META-INF/MANIFEST.MF"] |
| class | ["Type","File"] | 1091 | ["/java/lang/Object.class","/org/axonframework/modelling/repository/Repository$LifecycleManagement.class","/org/axonframework/messaging/core/Context$ResourceKey.class","/org/axonframework/eventsourcing/EventSourcingRepository$EventSourcedEntity.class","/java/lang/invoke/MethodHandles$Lookup.class","/java/util/Map.class"] |
| xml | ["File","Document"] | 11 | ["/META-INF/maven/org.axonframework/axon-eventsourcing/pom.xml","/META-INF/maven/org.axonframework/axon-conversion/pom.xml","/META-INF/maven/org.axonframework/axon-update/pom.xml","/META-INF/maven/io.axoniq.framework/axoniq-spring-boot-autoconfigure/pom.xml","/META-INF/maven/org.axonframework/axon-modelling/pom.xml","/META-INF/maven/org.axonframework.extensions.metrics/axon-metrics-micrometer/pom.xml"] |
| properties | ["File","Java"] | 10 | ["/META-INF/maven/org.axonframework/axon-eventsourcing/pom.properties","/META-INF/maven/org.axonframework/axon-conversion/pom.properties","/META-INF/maven/org.axonframework/axon-update/pom.properties","/META-INF/maven/io.axoniq.framework/axoniq-spring-boot-autoconfigure/pom.properties","/META-INF/maven/org.axonframework.extensions.metrics/axon-metrics-micrometer/pom.properties","/META-INF/maven/org.axonframework/axon-test/pom.properties"] |

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
