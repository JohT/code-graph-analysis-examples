---
title: "Git History Report"
generated: "2026-11-01"
model_version: "v5.0.0"
dataset: "react-router-7.18.4"
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
| react-router-7.18.4 | react-router-7.18.4 |  |  | Matt Brophy | github-actions[bot] | Remix Run Bot | 603 | 1187 | 4930 | 2026-08-27 | 2026-09-15 | 2026-09-15 | 47 | 65 | 46 | fff84b5f20f35c347c9d6313dfc603db0eac6e19 | react-router-7.18.4/typedoc.mjs | 1 | 1 |
| react-router-7.18.4/.agents/skills | .agents/skills | react-router-7.18.4 | react-router-7.18.4 | Matt Brophy | Brooks Lybrand | null | 2 | 7 | 12 | 2026-06-16 | 2026-06-16 | 2026-06-16 | 138 | 137 | 137 | fadd6c490cc84abc560a2413ee6fa0f2617d098d | react-router-7.18.4/.agents/skills/react-router/references/rsc.md | 3 | 2 |
| react-router-7.18.4/.agents/skills/fix-bug | fix-bug | react-router-7.18.4/.agents/skills | skills | Matt Brophy | Brooks Lybrand | null | 2 | 1 | 8 | 2026-03-18 | 2026-06-04 | 2026-06-04 | 150 | 227 | 149 | d6f3a05d4124ae9c1f2f74c599f80d091268ce0c | react-router-7.18.4/.agents/skills/fix-bug/SKILL.md | 4 | 1 |
| react-router-7.18.4/.agents/skills/implement-rfc | implement-rfc | react-router-7.18.4/.agents/skills | skills | Matt Brophy | null | null | 1 | 1 | 4 | 2026-05-07 | 2026-06-04 | 2026-06-04 | 150 | 177 | 149 | fadd6c490cc84abc560a2413ee6fa0f2617d098d | react-router-7.18.4/.agents/skills/implement-rfc/SKILL.md | 4 | 1 |
| react-router-7.18.4/.agents/skills/react-router | react-router | react-router-7.18.4/.agents/skills | skills | Brooks Lybrand | null | null | 1 | 5 | 1 | 2026-06-16 | 2026-06-16 | 2026-06-16 | 138 | 137 | 137 | 8f364c820ef698952e4bed876d6c93c895357692 | react-router-7.18.4/.agents/skills/react-router/references/rsc.md | 4 | 1 |
| react-router-7.18.4/.agents/skills/react-router/references | references | react-router-7.18.4/.agents/skills/react-router | react-router | Brooks Lybrand | null | null | 1 | 4 | 1 | 2026-06-16 | 2026-06-16 | 2026-06-16 | 138 | 137 | 137 | 8f364c820ef698952e4bed876d6c93c895357692 | react-router-7.18.4/.agents/skills/react-router/references/rsc.md | 5 | 1 |
| react-router-7.18.4/.github | .github | react-router-7.18.4 | react-router-7.18.4 | Matt Brophy | Michael Jackson | Michaël De Boey | 22 | 19 | 221 | 2026-05-26 | 2026-06-16 | 2026-06-16 | 138 | 158 | 137 | ff67b74a33c9f13fac28afc4923d0bf5628998ec | react-router-7.18.4/.github/workflows/test.yml | 2 | 1 |
| react-router-7.18.4/.github/ISSUE_TEMPLATE | ISSUE_TEMPLATE | react-router-7.18.4/.github | .github | Matt Brophy | Pedro Cattori | Tim Dorr | 13 | 3 | 51 | 2023-01-11 | 2026-06-04 | 2026-06-04 | 150 | 1389 | 149 | ff67b74a33c9f13fac28afc4923d0bf5628998ec | react-router-7.18.4/.github/ISSUE_TEMPLATE/documentation_isse.yml | 3 | 1 |
| react-router-7.18.4/.github/workflows | workflows | react-router-7.18.4/.github | .github | Matt Brophy | dependabot[bot] | Michael Jackson | 16 | 14 | 182 | 2026-05-26 | 2026-06-16 | 2026-06-16 | 138 | 158 | 137 | ff4c0712f7b24d38f51f7b967d7c31aeac531bed | react-router-7.18.4/.github/workflows/test.yml | 3 | 1 |
| react-router-7.18.4/decisions | decisions | react-router-7.18.4 | react-router-7.18.4 | Matt Brophy | Pedro Cattori | Michael Jackson | 10 | 20 | 69 | 2026-02-19 | 2026-06-04 | 2026-06-04 | 150 | 254 | 149 | ff67b74a33c9f13fac28afc4923d0bf5628998ec | react-router-7.18.4/decisions/template.md | 2 | 1 |

[Full data](./List_git_file_directories_with_commit_statistics.csv)

### 2.2 Directory Commit Statistics (Charts)



---

## 3. Co-Changed Files

Files committed together = logical coupling signal. May belong to the same conceptual unit or share a concern.

### 3.1 Co-Changed File Pairs

| firstFile | secondFile | commitCount |
| --- | --- | --- |
| react-router-7.18.4/packages/react-router/package.json | react-router-7.18.4/packages/react-router-dom/package.json | 350 |
| react-router-7.18.4/packages/react-router/CHANGELOG.md | react-router-7.18.4/packages/react-router/package.json | 181 |
| react-router-7.18.4/packages/react-router/CHANGELOG.md | react-router-7.18.4/packages/react-router-dom/package.json | 179 |
| react-router-7.18.4/packages/react-router/package.json | react-router-7.18.4/contributors.yml | 91 |
| react-router-7.18.4/contributors.yml | react-router-7.18.4/packages/react-router-dom/package.json | 91 |
| react-router-7.18.4/packages/react-router/lib/components.tsx | react-router-7.18.4/packages/react-router/lib/hooks.tsx | 91 |
| react-router-7.18.4/packages/react-router-node/CHANGELOG.md | react-router-7.18.4/packages/react-router-dev/CHANGELOG.md | 88 |
| react-router-7.18.4/packages/react-router-node/CHANGELOG.md | react-router-7.18.4/packages/react-router-serve/CHANGELOG.md | 88 |
| react-router-7.18.4/packages/react-router-serve/CHANGELOG.md | react-router-7.18.4/packages/react-router-dev/CHANGELOG.md | 86 |
| react-router-7.18.4/packages/react-router/CHANGELOG.md | react-router-7.18.4/contributors.yml | 85 |

### 3.2 Co-Changed File Pairs (All in One Commit)

Files changed together in a single large commit.

| firstFile | secondFile | commitCount |
| --- | --- | --- |
| react-router-7.18.4/packages/react-router-dom/package.json | react-router-7.18.4/packages/react-router/package.json | 604 |
| react-router-7.18.4/packages/react-router/CHANGELOG.md | react-router-7.18.4/packages/react-router/package.json | 430 |
| react-router-7.18.4/packages/react-router-dom/package.json | react-router-7.18.4/packages/react-router/CHANGELOG.md | 427 |
| react-router-7.18.4/packages/react-router-dev/CHANGELOG.md | react-router-7.18.4/packages/react-router-node/CHANGELOG.md | 241 |
| react-router-7.18.4/packages/react-router-node/CHANGELOG.md | react-router-7.18.4/packages/react-router-serve/CHANGELOG.md | 241 |
| react-router-7.18.4/packages/react-router-dev/CHANGELOG.md | react-router-7.18.4/packages/react-router-serve/CHANGELOG.md | 239 |
| react-router-7.18.4/packages/react-router-express/CHANGELOG.md | react-router-7.18.4/packages/react-router-node/CHANGELOG.md | 235 |
| react-router-7.18.4/packages/react-router-dev/CHANGELOG.md | react-router-7.18.4/packages/react-router-express/CHANGELOG.md | 234 |
| react-router-7.18.4/packages/react-router-dev/CHANGELOG.md | react-router-7.18.4/packages/react-router/CHANGELOG.md | 233 |
| react-router-7.18.4/packages/react-router-express/CHANGELOG.md | react-router-7.18.4/packages/react-router-serve/CHANGELOG.md | 233 |

### 3.3 Co-Changed With a Specific File

Shows all files that were changed together with another particular file.

| filePath | commitCount | coChangeRate | maxLift | avgLift |
| --- | --- | --- | --- | --- |
| react-router-7.18.4/packages/react-router/package.json | 371 | 0.0004998086985574255 | 2.3052918424753868 | 1.1996911268745287 |
| react-router-7.18.4/packages/react-router/CHANGELOG.md | 243 | 0.00040755947349353945 | 1.6138461538461542 | 1.1876732231699025 |
| react-router-7.18.4/contributors.yml | 224 | 0.00047636060497796833 | 1.549752324671939 | 0.5329775982192774 |
| react-router-7.18.4/packages/react-router/lib/components.tsx | 158 | 0.0011099246937169834 | 6.086841070023603 | 2.9144028385096163 |
| react-router-7.18.4/pnpm-lock.yaml | 150 | 0.0006697475051905432 | 5.994285714285715 | 1.5146981543349285 |
| react-router-7.18.4/packages/react-router/lib/hooks.tsx | 144 | 0.0014333207254195448 | 3.6212227336401837 | 1.8022023284113415 |
| react-router-7.18.4/packages/react-router/lib/router/router.ts | 98 | 0.0011196800914024564 | 8.15888888888889 | 2.2632094886222367 |
| react-router-7.18.4/packages/react-router-node/CHANGELOG.md | 91 | 0.0004031543505227716 | 3.458025847536992 | 2.166061447208173 |
| react-router-7.18.4/packages/react-router-serve/CHANGELOG.md | 88 | 0.0005167776564133282 | 3.3097552922185125 | 2.105570988964255 |
| react-router-7.18.4/packages/react-router-dev/CHANGELOG.md | 81 | 0.002002521693985018 | 3.1738009861048857 | 2.1586005093209386 |

[Full data](./List_git_files_that_were_changed_together_with_another_file.csv)

### 3.4 Co-Changed With a Specific File (All in One)

| filePath | commitCount |
| --- | --- |
| react-router-7.18.4/packages/react-router/package.json | 638 |
| react-router-7.18.4/packages/react-router-dom/package.json | 610 |
| react-router-7.18.4/packages/react-router/CHANGELOG.md | 493 |
| react-router-7.18.4/contributors.yml | 438 |
| react-router-7.18.4/packages/react-router-dev/package.json | 259 |
| react-router-7.18.4/packages/react-router-dev/CHANGELOG.md | 248 |
| react-router-7.18.4/packages/react-router-node/CHANGELOG.md | 244 |
| react-router-7.18.4/packages/react-router-serve/CHANGELOG.md | 241 |
| react-router-7.18.4/packages/react-router-express/CHANGELOG.md | 236 |
| react-router-7.18.4/packages/react-router-architect/CHANGELOG.md | 212 |

### 3.5 Co-Changed Files (Charts)



---

## 4. File Change Distribution

Files changed per commit. High proportion of large commits = low commit granularity.

### 4.1 Files per Commit Distribution

| filesPerCommit | commitCount |
| --- | --- |
| 1 | 4666 |
| 2 | 1807 |
| 3 | 922 |
| 4 | 577 |
| 5 | 478 |
| 6 | 289 |
| 7 | 198 |
| 8 | 164 |
| 9 | 103 |
| 10 | 133 |

[Full data](./List_git_files_per_commit_distribution.csv)

### 4.2 Files per Commit Chart



---

## 5. Pairwise Changed Files

Commit overlap counts and dependency info between file pairs.

### 5.1 Pairwise Changed Files

| firstFileName | secondFileName | filePairLineBreak | filePairWithRelativePathLineBreak | filePair | filePairWithRelativePath | firstFileExtension | secondFileExtension | fileExtensionPair | updateCommitCount | updateCommitMinConfidence | updateCommitSupport | updateCommitLift | updateCommitJaccardSimilarity |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| integration/package.json | packages/react-router-express/package.json | package<br>package | integration/package.json<br>packages/react-router-express/package.json | package↔package | integration/package.json↔packages/react-router-express/package.json | json | json | json↔json | 3 | 0.03409090909090909 | 0.0009532888465204957 | 0.45652804642166345 | 0.009375 |
| packages/react-router-cloudflare/package.json | packages/react-router-fs-routes/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-cloudflare/package.json<br>packages/react-router-fs-routes/CHANGELOG.md | package↔CHANGELOG | packages/react-router-cloudflare/package.json↔packages/react-router-fs-routes/CHANGELOG.md | json | md | json↔md | 27 | 0.12857142857142856 | 0.008579599618684462 | 1.707233273056058 | 0.06428571428571428 |
| integration/CHANGELOG.md | packages/react-router-fs-routes/CHANGELOG.md | CHANGELOG<br>CHANGELOG | integration/CHANGELOG.md<br>packages/react-router-fs-routes/CHANGELOG.md | CHANGELOG↔CHANGELOG | integration/CHANGELOG.md↔packages/react-router-fs-routes/CHANGELOG.md | md | md | md↔md | 4 | 0.041237113402061855 | 0.001271051795360661 | 0.6179675994108984 | 0.013201320132013201 |
| packages/create-react-router/package.json | packages/react-router-fs-routes/CHANGELOG.md | package<br>CHANGELOG | packages/create-react-router/package.json<br>packages/react-router-fs-routes/CHANGELOG.md | package↔CHANGELOG | packages/create-react-router/package.json↔packages/react-router-fs-routes/CHANGELOG.md | json | md | json↔md | 27 | 0.12857142857142856 | 0.008579599618684462 | 1.766874610106051 | 0.06553398058252427 |
| packages/react-router-express/package.json | packages/react-router-fs-routes/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-express/package.json<br>packages/react-router-fs-routes/CHANGELOG.md | package↔CHANGELOG | packages/react-router-express/package.json↔packages/react-router-fs-routes/CHANGELOG.md | json | md | json↔md | 27 | 0.12857142857142856 | 0.008579599618684462 | 1.7217629179331306 | 0.0645933014354067 |
| packages/react-router-dom/package.json | packages/react-router-fs-routes/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-dom/package.json<br>packages/react-router-fs-routes/CHANGELOG.md | package↔CHANGELOG | packages/react-router-dom/package.json↔packages/react-router-fs-routes/CHANGELOG.md | json | md | json↔md | 27 | 0.12857142857142856 | 0.008579599618684462 | 0.6021045918367347 | 0.031578947368421054 |
| packages/react-router-architect/package.json | packages/react-router-fs-routes/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-architect/package.json<br>packages/react-router-fs-routes/CHANGELOG.md | package↔CHANGELOG | packages/react-router-architect/package.json↔packages/react-router-fs-routes/CHANGELOG.md | json | md | json↔md | 27 | 0.12857142857142856 | 0.008579599618684462 | 1.7217629179331306 | 0.0645933014354067 |
| packages/react-router-dev/package.json | packages/react-router-fs-routes/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-dev/package.json<br>packages/react-router-fs-routes/CHANGELOG.md | package↔CHANGELOG | packages/react-router-dev/package.json↔packages/react-router-fs-routes/CHANGELOG.md | json | md | json↔md | 27 | 0.12857142857142856 | 0.008579599618684462 | 1.3094313453536754 | 0.054878048780487805 |
| packages/react-router-remix-routes-option-adapter/package.json | packages/react-router-fs-routes/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-remix-routes-option-adapter/package.json<br>packages/react-router-fs-routes/CHANGELOG.md | package↔CHANGELOG | packages/react-router-remix-routes-option-adapter/package.json↔packages/react-router-fs-routes/CHANGELOG.md | json | md | json↔md | 27 | 0.12857142857142856 | 0.008579599618684462 | 1.8475538160469671 | 0.06716417910447761 |
| packages/react-router/package.json | packages/react-router-fs-routes/CHANGELOG.md | package<br>CHANGELOG | packages/react-router/package.json<br>packages/react-router-fs-routes/CHANGELOG.md | package↔CHANGELOG | packages/react-router/package.json↔packages/react-router-fs-routes/CHANGELOG.md | json | md | json↔md | 27 | 0.12857142857142856 | 0.008579599618684462 | 0.5690777576853526 | 0.030201342281879196 |

[Full data](./List_pairwise_changed_files.csv)

### 5.2 Pairwise Changed Files (Top by Lift)

File pairs that co-change more often than random chance (lift > 1).

| fileExtensionPair | firstFileNameShort | secondFileNameShort | updateCommitCount | updateCommitMinConfidence | updateCommitLift | updateCommitJaccardSimilarity | updateCommitSupport | firstFileName | secondFileName |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ts↔ts | actions-test | actions | 3 | 0.5 | 174.83333333333337 | 0.25 | 0.0009532888465204957 | packages/react-router/__tests__/server-runtime/actions-test.ts | packages/react-router/lib/actions.ts |
| ts↔ts | vite-dev-custom-entry-test | vite-absolute-base-test | 3 | 1 | 157.35 | 0.15 | 0.0009532888465204957 | integration/vite-dev-custom-entry-test.ts | integration/vite-absolute-base-test.ts |
| ts↔ts | vite-loader-context-test | vite-node-env-test | 4 | 0.8 | 148.09411764705882 | 0.2222222222222222 | 0.001271051795360661 | integration/vite-loader-context-test.ts | integration/vite-node-env-test.ts |
| ts↔ts | sessions-test | sessions | 3 | 0.375 | 118.01249999999999 | 0.2 | 0.0009532888465204957 | packages/react-router/__tests__/server-runtime/sessions-test.ts | packages/react-router/lib/server-runtime/sessions.ts |
| ts↔ts | remove-exports-test | remove-exports | 4 | 0.36363636363636365 | 104.03305785123966 | 0.2222222222222222 | 0.001271051795360661 | packages/react-router-dev/vite/remove-exports-test.ts | packages/react-router-dev/vite/remove-exports.ts |
| ts↔ts | vite-dotenv-test | vite-node-env-test | 4 | 0.8 | 93.24444444444444 | 0.14285714285714285 | 0.001271051795360661 | integration/vite-dotenv-test.ts | integration/vite-node-env-test.ts |
| ts↔ts | fileStorage | sessions-test | 3 | 0.3 | 85.82727272727273 | 0.16666666666666666 | 0.0009532888465204957 | packages/react-router-node/sessions/fileStorage.ts | packages/react-router-node/__tests__/sessions-test.ts |
| ts↔ts | routes | routes | 3 | 0.75 | 81.38793103448276 | 0.1 | 0.0009532888465204957 | packages/react-router-dev/config/routes.ts | packages/react-router-dev/routes.ts |
| ts↔ts | vite-server-bundles-test | vite-node-env-test | 5 | 1 | 74.92857142857143 | 0.11904761904761904 | 0.0015888147442008262 | integration/vite-server-bundles-test.ts | integration/vite-node-env-test.ts |
| ts↔ts | vite-dot-server-test | vite-node-env-test | 5 | 1 | 73.1860465116279 | 0.11627906976744186 | 0.0015888147442008262 | integration/vite-dot-server-test.ts | integration/vite-node-env-test.ts |

[Full data](./List_pairwise_changed_files_top_lift.csv)

### 5.3 Pairwise Changed Files With Dependencies

Files that are co-changed and also have a structural dependency relationship between them.

| dependencyWeight | fileDistance | commitCount | updateCommitMinConfidence | updateCommitSupport | updateCommitLift | updateCommitJaccardSimilarity |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | 5 | 3 | 0.07317073170731707 | 0.0009532888465204957 | 1.0234146341463415 | 0.011406844106463879 |
| 1 | 6 | 3 | 0.15 | 0.0009532888465204957 | 5.553529411764705 | 0.029411764705882353 |
| 1 | 4 | 4 | 0.16 | 0.001271051795360661 | 2.2084210526315786 | 0.01606425702811245 |
| 1 | 4 | 9 | 0.36 | 0.002859866539561487 | 37.764 | 0.1956521739130435 |
| 2 | 5 | 3 | 0.07317073170731707 | 0.0009532888465204957 | 1.0099486521181 | 0.011278195488721804 |
| 2 | 5 | 9 | 0.14285714285714285 | 0.002859866539561487 | 1.971804511278195 | 0.031914893617021274 |
| 2 | 0 | 9 | 0.36 | 0.002859866539561487 | 8.8509375 | 0.0625 |
| 3 | 0 | 3 | 0.058823529411764705 | 0.0009532888465204957 | 2.9383753501400562 | 0.02702702702702703 |
| 3 | 4 | 9 | 0.0703125 | 0.002859866539561487 | 0.9704975328947366 | 0.025936599423631124 |
| 6 | 4 | 3 | 0.13636363636363635 | 0.0009532888465204957 | 1.8821770334928227 | 0.012145748987854251 |

[Full data](./List_pairwise_changed_files_with_dependencies.csv)

### 5.4 Pairwise Changed Files (Charts)



---

## 6. Files by Author

Per-author file commit stats. Useful for knowledge boundaries and bus-factor risk.

### 6.1 Files with Commit Statistics by Author

| filePath | author | commitCount | commitHashes | lastCommitDate | lastCreationDate | lastModificationDate | daysSinceLastCommit | daysSinceLastCreation | daysSinceLastModification | maxCommitSha |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| react-router-7.18.4/.agents/skills/fix-bug/SKILL.md | Matt Brophy | 7 | ["2469dd6621fbcaec689571c3f003af5711bc54de","a842fca719e81505f454a8e6a8c728cdaed22067","06c1149bc0b4f50db0cc6fc10471b4ad963b8969","1497c6ba52e55158e4f12b54617b1255935c75d5","46321cf2767cb820c1be8bbea3bafbc32c6c4ffd","963affeb924f2256bd20c0c5c87e4c4b4fcbd188","d6f3a05d4124ae9c1f2f74c599f80d091268ce0c"] | 2026-06-04 | 2026-03-18 | 2026-06-04 | 150 | 227 | 149 | d6f3a05d4124ae9c1f2f74c599f80d091268ce0c |
| react-router-7.18.4/.agents/skills/fix-bug/SKILL.md | Brooks Lybrand | 1 | ["4f8fff6cdb31c549fd011ac516fad5ad2e641b5f"] | 2026-05-29 | 2026-03-18 | 2026-06-04 | 156 | 227 | 149 | 4f8fff6cdb31c549fd011ac516fad5ad2e641b5f |
| react-router-7.18.4/.agents/skills/implement-rfc/SKILL.md | Matt Brophy | 4 | ["a6ab746a43675332ec3c190b1390724bf5c833db","fadd6c490cc84abc560a2413ee6fa0f2617d098d","522bc1b8cd0d7b3565bf9193789f2b7d5503856b","d6f3a05d4124ae9c1f2f74c599f80d091268ce0c"] | 2026-06-04 | 2026-05-07 | 2026-06-04 | 150 | 177 | 149 | fadd6c490cc84abc560a2413ee6fa0f2617d098d |
| react-router-7.18.4/.agents/skills/react-router/SKILL.md | Brooks Lybrand | 1 | ["8f364c820ef698952e4bed876d6c93c895357692"] | 2026-06-16 | 2026-06-16 | 2026-06-16 | 138 | 137 | 137 | 8f364c820ef698952e4bed876d6c93c895357692 |
| react-router-7.18.4/.agents/skills/react-router/references/data-mode.md | Brooks Lybrand | 1 | ["8f364c820ef698952e4bed876d6c93c895357692"] | 2026-06-16 | 2026-06-16 | 2026-06-16 | 138 | 137 | 137 | 8f364c820ef698952e4bed876d6c93c895357692 |
| react-router-7.18.4/.agents/skills/react-router/references/declarative-mode.md | Brooks Lybrand | 1 | ["8f364c820ef698952e4bed876d6c93c895357692"] | 2026-06-16 | 2026-06-16 | 2026-06-16 | 138 | 137 | 137 | 8f364c820ef698952e4bed876d6c93c895357692 |
| react-router-7.18.4/.agents/skills/react-router/references/framework-mode.md | Brooks Lybrand | 1 | ["8f364c820ef698952e4bed876d6c93c895357692"] | 2026-06-16 | 2026-06-16 | 2026-06-16 | 138 | 137 | 137 | 8f364c820ef698952e4bed876d6c93c895357692 |
| react-router-7.18.4/.agents/skills/react-router/references/rsc.md | Brooks Lybrand | 1 | ["8f364c820ef698952e4bed876d6c93c895357692"] | 2026-06-16 | 2026-06-16 | 2026-06-16 | 138 | 137 | 137 | 8f364c820ef698952e4bed876d6c93c895357692 |
| react-router-7.18.4/.browserslistrc | Michael Jackson | 3 | ["82c500c4a1a5d53a608faee25f8322c661b242a1","b3f728487ae6fe7d5ef4ddc759fb2a4ca0df712e","f6df0697e1b2064a2b3a12e8b39577326fdd945b"] | 2021-09-09 | 2018-10-30 | 2021-09-09 | 1879 | 2923 | 1878 | f6df0697e1b2064a2b3a12e8b39577326fdd945b |
| react-router-7.18.4/.browserslistrc | Matt Brophy | 1 | ["4fa24c1b12c7c2ff8f32bb611b8b5b3ac4678c61"] | 2024-03-27 | 2018-10-30 | 2021-09-09 | 949 | 2923 | 1878 | 4fa24c1b12c7c2ff8f32bb611b8b5b3ac4678c61 |

[Full data](./List_git_files_with_commit_statistics_by_author.csv)

---

## 7. Data Quality

Files in git log that are unresolved (not found in codebase) or ambiguous (multiple matches). Affects reliability of co-change metrics.

### 7.1 File Resolution Summary

Resolved vs. ambiguous vs. unresolved files by extension.

| resolved | extension | gitFileCount | fileLabels | gitFileExamples |
| --- | --- | --- | --- | --- |
| false | md | 1890 | ["File","Git"] | ["packages/react-router-fs-routes/CHANGELOG.md","packages/react-router-node/CHANGELOG.md","packages/react-router-remix-routes-option-adapter/CHANGELOG.md","packages/react-router-serve/CHANGELOG.md","packages/react-router/.changes/patch.rsc-meta-redirect-escaping.md","packages/react-router/.changes/patch.skip-view-transitions-on-revalidation-and-hydration.md","packages/react-router/CHANGELOG.md","packages/react-router-node/.changes/patch.streaming-client-disconnect.md","packages/react-router/.changes/patch.linear-route-matching.md"] |
| false | js | 1744 | ["File","Git"] | ["examples/multi-app/inbox/messages.js","examples/multi-app/server.js","examples/multi-app/vite.config.js","examples/notes/src/notes.js","examples/ssr-data-router/server.js","examples/ssr-data-router/vite.config.js","examples/ssr/server.js","examples/ssr/vite.config.js","scripts/constants.js"] |
| false | ts | 1133 | ["File","Git"] | ["packages/react-router/__tests__/router/view-transition-test.ts","scripts/changes/pr.ts","scripts/changes/publish.ts","packages/react-router-node/__tests__/stream-test.ts","packages/react-router/__tests__/router/utils/data-router-setup.ts","packages/react-router/__tests__/router/browser-test.ts","packages/react-router/__tests__/router/redirects-test.ts","packages/react-router/__tests__/rsc/server-test.ts","packages/react-router/lib/rsc/redirect.ts"] |
| false | tsx | 489 | ["File","Git"] | ["packages/react-router/lib/rsc/server.ssr.tsx","packages/react-router/__tests__/external-navigation-test.tsx","packages/react-router/__tests__/useNavigate-test.tsx","packages/react-router/lib/components.tsx","packages/react-router/lib/hooks.tsx","packages/react-router/lib/rsc/browser.tsx","packages/react-router/__tests__/dom/link-href-test.tsx","packages/react-router/lib/dom/lib.tsx","packages/react-router/lib/dom/server.tsx"] |
| false | json | 272 | ["File","Git"] | ["examples/auth-router-provider/package-lock.json","examples/auth-router-provider/package.json","examples/auth-router-provider/tsconfig.json","examples/auth/package-lock.json","examples/auth/package.json","examples/auth/tsconfig.json","examples/basic-data-router/package-lock.json","examples/basic-data-router/package.json","examples/basic-data-router/tsconfig.json"] |
| false | css | 85 | ["File","Git"] | ["examples/auth-router-provider/src/index.css","examples/auth/src/index.css","examples/basic-data-router/src/index.css","examples/basic/src/index.css","examples/custom-filter-link/src/index.css","examples/custom-link/src/index.css","examples/custom-query-parsing/src/index.css","examples/data-router/src/index.css","examples/error-boundaries/src/index.css"] |
| false | gitignore | 83 | ["File","Git"] | [".gitignore","examples/auth-router-provider/.gitignore","examples/auth/.gitignore","examples/basic-data-router/.gitignore","examples/basic/.gitignore","examples/custom-filter-link/.gitignore","examples/custom-link/.gitignore","examples/custom-query-parsing/.gitignore","examples/data-router/.gitignore"] |
| false | html | 64 | ["File","Git"] | ["examples/auth-router-provider/index.html","examples/auth/index.html","examples/basic-data-router/index.html","examples/basic/index.html","examples/custom-filter-link/index.html","examples/custom-link/index.html","examples/custom-query-parsing/index.html","examples/data-router/index.html","examples/error-boundaries/index.html"] |
| false | ico | 50 | ["File","Git"] | ["playground/performance/public/favicon.ico","integration/helpers/vite-8-template/public/favicon.ico","integration/helpers/vite-rolldown-template/public/favicon.ico","playground/framework-rolldown-vite/public/favicon.ico","playground/framework/public/favicon.ico","playground/framework-vite-6/public/favicon.ico","playground/rsc-vite-7-framework/public/favicon.ico","integration/helpers/rsc-parcel/public/favicon.ico","integration/helpers/rsc-parcel-framework/public/favicon.ico"] |
| false | yml | 44 | ["File","Git"] | [".github/workflows/release.yml","contributors.yml",".github/workflows/format.yml",".github/ISSUE_TEMPLATE/bug_report.yml",".github/workflows/deduplicate-lock-file.yml",".github/workflows/docs.yml",".github/workflows/integration-full.yml",".github/workflows/preview.yml",".github/workflows/test.yml"] |

[Full data](./List_git_files_by_resolved_label_and_extension.csv)

### 7.2 Ambiguous Git Files

Match multiple codebase files — excluded from co-change analysis.

⚠️ _No data available — git history not imported for this codebase._

### 7.3 Unresolved Git Files

Not found in scanned codebase. May indicate deleted files, renames, or out-of-scope paths.

| codeFileExtension | firstThreeCodeFileLabels | codeFileCount | codeFileExamples |
| --- | --- | --- | --- |
| json | ["File","NPM"] | 1 | ["./package.json"] |
| tsx | ["File","NPM"] | 3 | ["./dist/config/default-rsc-entries/entry.rsc.tsx","./dist/config/default-rsc-entries/entry.ssr.tsx","./dist/config/default-rsc-entries/entry.client.tsx"] |
| ts | ["File","NPM"] | 1 | ["./rsc-types.d.ts"] |
| json | ["File","TS"] | 13 | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.4/./source/react-router-7.18.4/packages/react-router-cloudflare/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.4/./source/react-router-7.18.4/packages/react-router-architect/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.4/./source/react-router-7.18.4/packages/react-router-dom/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.4/./source/react-router-7.18.4/packages/create-react-router/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.4/./source/react-router-7.18.4/packages/create-react-router/__tests__/fixtures/with-ignored-dir/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.4/./source/react-router-7.18.4/packages/create-react-router/__tests__/fixtures/blank/.reports/jqa/ts-output.json"] |

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
