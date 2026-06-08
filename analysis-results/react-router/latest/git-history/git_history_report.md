---
title: "Git History Report"
generated: "2026-06-08"
model_version: "v4.0.1"
dataset: "react-router-7.16.0"
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
| react-router-7.16.0 | react-router-7.16.0 |  |  | Matt Brophy | github-actions[bot] | Mark Dalgleish | 592 | 1473 | 4947 | 2026-05-26 | 2026-05-28 | 2026-05-28 | 11 | 12 | 10 | fff84b5f20f35c347c9d6313dfc603db0eac6e19 | react-router-7.16.0/typedoc.mjs | 1 | 1 |
| react-router-7.16.0/.agents/skills | .agents/skills | react-router-7.16.0 | react-router-7.16.0 | Matt Brophy | null | null | 1 | 2 | 8 | 2026-05-07 | 2026-05-07 | 2026-05-14 | 25 | 31 | 31 | fadd6c490cc84abc560a2413ee6fa0f2617d098d | react-router-7.16.0/.agents/skills/implement-rfc/SKILL.md | 3 | 2 |
| react-router-7.16.0/.agents/skills/fix-bug | fix-bug | react-router-7.16.0/.agents/skills | skills | Matt Brophy | null | null | 1 | 1 | 5 | 2026-03-18 | 2026-04-14 | 2026-04-14 | 55 | 81 | 54 | a842fca719e81505f454a8e6a8c728cdaed22067 | react-router-7.16.0/.agents/skills/fix-bug/SKILL.md | 4 | 1 |
| react-router-7.16.0/.agents/skills/implement-rfc | implement-rfc | react-router-7.16.0/.agents/skills | skills | Matt Brophy | null | null | 1 | 1 | 3 | 2026-05-07 | 2026-05-07 | 2026-05-14 | 25 | 31 | 31 | fadd6c490cc84abc560a2413ee6fa0f2617d098d | react-router-7.16.0/.agents/skills/implement-rfc/SKILL.md | 4 | 1 |
| react-router-7.16.0/.github | .github | react-router-7.16.0 | react-router-7.16.0 | Matt Brophy | Michael Jackson | Michaël De Boey | 21 | 19 | 216 | 2026-05-26 | 2026-05-27 | 2026-05-27 | 12 | 12 | 11 | ff67b74a33c9f13fac28afc4923d0bf5628998ec | react-router-7.16.0/.github/workflows/test.yml | 2 | 1 |
| react-router-7.16.0/.github/ISSUE_TEMPLATE | ISSUE_TEMPLATE | react-router-7.16.0/.github | .github | Matt Brophy | Pedro Cattori | Tim Dorr | 13 | 3 | 50 | 2023-01-11 | 2025-07-16 | 2025-07-16 | 327 | 1243 | 326 | ff67b74a33c9f13fac28afc4923d0bf5628998ec | react-router-7.16.0/.github/ISSUE_TEMPLATE/documentation_isse.yml | 3 | 1 |
| react-router-7.16.0/.github/workflows | workflows | react-router-7.16.0/.github | .github | Matt Brophy | dependabot[bot] | Michael Jackson | 15 | 14 | 177 | 2026-05-26 | 2026-05-27 | 2026-05-27 | 12 | 12 | 11 | ff4c0712f7b24d38f51f7b967d7c31aeac531bed | react-router-7.16.0/.github/workflows/test.yml | 3 | 1 |
| react-router-7.16.0/decisions | decisions | react-router-7.16.0 | react-router-7.16.0 | Matt Brophy | Pedro Cattori | Michael Jackson | 9 | 20 | 67 | 2026-02-19 | 2026-05-05 | 2026-05-05 | 34 | 108 | 33 | ff67b74a33c9f13fac28afc4923d0bf5628998ec | react-router-7.16.0/decisions/template.md | 2 | 1 |
| react-router-7.16.0/docs | docs | react-router-7.16.0 | react-router-7.16.0 | Matt Brophy | Remix Run Bot | Ryan Florence | 121 | 197 | 688 | 2026-05-07 | 2026-05-27 | 2026-05-27 | 12 | 31 | 11 | ff6a4fea561d67b1e61002522096797afb9ff55e | react-router-7.16.0/docs/upgrading/v6.md | 2 | 1 |
| react-router-7.16.0/docs/api | api | react-router-7.16.0/docs | docs | Matt Brophy | Remix Run Bot | Brooks Lybrand | 22 | 109 | 193 | 2026-05-07 | 2026-05-27 | 2026-05-27 | 12 | 31 | 11 | fed3b6300c8b8db90d9779a8f9c3304e91d719d3 | react-router-7.16.0/docs/api/utils/resolvePath.md | 3 | 1 |

[Full data](./List_git_file_directories_with_commit_statistics.csv)

### 2.2 Directory Commit Statistics (Charts)



---

## 3. Co-Changed Files

Files committed together = logical coupling signal. May belong to the same conceptual unit or share a concern.

### 3.1 Co-Changed File Pairs

| firstFile | secondFile | commitCount |
| --- | --- | --- |
| react-router-7.16.0/packages/react-router-dom/package.json | react-router-7.16.0/packages/react-router/package.json | 345 |
| react-router-7.16.0/packages/react-router/CHANGELOG.md | react-router-7.16.0/packages/react-router/package.json | 180 |
| react-router-7.16.0/packages/react-router-dom/package.json | react-router-7.16.0/packages/react-router/CHANGELOG.md | 178 |
| react-router-7.16.0/packages/react-router-node/CHANGELOG.md | react-router-7.16.0/packages/react-router-serve/CHANGELOG.md | 93 |
| react-router-7.16.0/packages/react-router/package.json | react-router-7.16.0/contributors.yml | 92 |
| react-router-7.16.0/packages/react-router-dom/package.json | react-router-7.16.0/contributors.yml | 91 |
| react-router-7.16.0/packages/react-router-dev/CHANGELOG.md | react-router-7.16.0/packages/react-router-serve/CHANGELOG.md | 91 |
| react-router-7.16.0/packages/react-router-dev/CHANGELOG.md | react-router-7.16.0/packages/react-router-node/CHANGELOG.md | 91 |
| react-router-7.16.0/packages/react-router/CHANGELOG.md | react-router-7.16.0/contributors.yml | 88 |
| react-router-7.16.0/packages/react-router-express/CHANGELOG.md | react-router-7.16.0/packages/react-router-serve/CHANGELOG.md | 85 |

### 3.2 Co-Changed File Pairs (All in One Commit)

Files changed together in a single large commit.

| firstFile | secondFile | commitCount |
| --- | --- | --- |
| react-router-7.16.0/packages/react-router-dom/package.json | react-router-7.16.0/packages/react-router/package.json | 583 |
| react-router-7.16.0/packages/react-router/CHANGELOG.md | react-router-7.16.0/packages/react-router/package.json | 414 |
| react-router-7.16.0/packages/react-router-dom/package.json | react-router-7.16.0/packages/react-router/CHANGELOG.md | 411 |
| react-router-7.16.0/packages/react-router-node/CHANGELOG.md | react-router-7.16.0/packages/react-router-serve/CHANGELOG.md | 233 |
| react-router-7.16.0/packages/react-router-dev/CHANGELOG.md | react-router-7.16.0/packages/react-router-serve/CHANGELOG.md | 231 |
| react-router-7.16.0/packages/react-router-dev/CHANGELOG.md | react-router-7.16.0/packages/react-router-node/CHANGELOG.md | 231 |
| react-router-7.16.0/packages/react-router-express/CHANGELOG.md | react-router-7.16.0/packages/react-router-serve/CHANGELOG.md | 225 |
| react-router-7.16.0/packages/react-router-express/CHANGELOG.md | react-router-7.16.0/packages/react-router-node/CHANGELOG.md | 225 |
| react-router-7.16.0/packages/react-router-dev/CHANGELOG.md | react-router-7.16.0/packages/react-router-express/CHANGELOG.md | 223 |
| react-router-7.16.0/packages/react-router-dev/CHANGELOG.md | react-router-7.16.0/packages/react-router/CHANGELOG.md | 222 |

### 3.3 Co-Changed With a Specific File

Shows all files that were changed together with another particular file.

| filePath | commitCount | coChangeRate | maxLift | avgLift |
| --- | --- | --- | --- | --- |
| react-router-7.16.0/packages/react-router-dom/package.json | 347 | 0.00047479092779894043 | 2.3466551575312904 | 1.342786342445529 |
| react-router-7.16.0/packages/react-router/CHANGELOG.md | 189 | 0.0008136381247578458 | 1.517817014446228 | 1.0546647967257463 |
| react-router-7.16.0/contributors.yml | 181 | 0.000544069640914037 | 1.5243622294764843 | 0.6102795913130418 |
| react-router-7.16.0/pnpm-lock.yaml | 154 | 0.000565189466923571 | 6.003809523809523 | 1.4174673725542495 |
| react-router-7.16.0/packages/react-router/package.json | 137 | 0.0006021978021978022 | 1.0006349206349208 | 0.5556365556999152 |
| react-router-7.16.0/packages/react-router/lib/hooks.tsx | 119 | 0.0018757881462799495 | 4.173518284993696 | 2.8083550140282365 |
| react-router-7.16.0/packages/react-router/lib/components.tsx | 97 | 0.0023663153786104606 | 4.0973496064129415 | 3.1179917574983778 |
| react-router-7.16.0/packages/react-router-dev/CHANGELOG.md | 96 | 0.0004816230697450408 | 3.7932712653406693 | 2.267036974337175 |
| react-router-7.16.0/packages/react-router-node/CHANGELOG.md | 94 | 0.0009004348908941127 | 3.933233147273508 | 2.008891165734653 |
| react-router-7.16.0/packages/react-router-dev/package.json | 86 | 0.00042722305017386985 | 1.9990560471976402 | 1.2426220089479487 |

[Full data](./List_git_files_that_were_changed_together_with_another_file.csv)

### 3.4 Co-Changed With a Specific File (All in One)

| filePath | commitCount |
| --- | --- |
| react-router-7.16.0/packages/react-router/package.json | 616 |
| react-router-7.16.0/packages/react-router-dom/package.json | 588 |
| react-router-7.16.0/packages/react-router/CHANGELOG.md | 475 |
| react-router-7.16.0/contributors.yml | 424 |
| react-router-7.16.0/packages/react-router-dev/package.json | 250 |
| react-router-7.16.0/packages/react-router-dev/CHANGELOG.md | 236 |
| react-router-7.16.0/packages/react-router-node/CHANGELOG.md | 234 |
| react-router-7.16.0/packages/react-router-serve/CHANGELOG.md | 233 |
| react-router-7.16.0/packages/react-router-express/CHANGELOG.md | 225 |
| react-router-7.16.0/packages/react-router-cloudflare/CHANGELOG.md | 204 |

### 3.5 Co-Changed Files (Charts)



---

## 4. File Change Distribution

Files changed per commit. High proportion of large commits = low commit granularity.

### 4.1 Files per Commit Distribution

| filesPerCommit | commitCount |
| --- | --- |
| 1 | 4648 |
| 2 | 1796 |
| 3 | 907 |
| 4 | 574 |
| 5 | 473 |
| 6 | 287 |
| 7 | 195 |
| 8 | 163 |
| 9 | 103 |
| 10 | 130 |

[Full data](./List_git_files_per_commit_distribution.csv)

### 4.2 Files per Commit Chart



---

## 5. Pairwise Changed Files

Commit overlap counts and dependency info between file pairs.

### 5.1 Pairwise Changed Files

| firstFileName | secondFileName | filePairLineBreak | filePairWithRelativePathLineBreak | filePair | filePairWithRelativePath | firstFileExtension | secondFileExtension | fileExtensionPair | updateCommitCount | updateCommitMinConfidence | updateCommitSupport | updateCommitLift | updateCommitJaccardSimilarity |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| docs/how-to/middleware.md | packages/create-react-router/CHANGELOG.md | middleware<br>CHANGELOG | docs/how-to/middleware.md<br>packages/create-react-router/CHANGELOG.md | middleware↔CHANGELOG | docs/how-to/middleware.md↔packages/create-react-router/CHANGELOG.md | md | md | md↔md | 3 | 0.06382978723404255 | 0.0009517766497461929 | 1.011012509355287 | 0.012345679012345678 |
| integration/CHANGELOG.md | packages/create-react-router/CHANGELOG.md | CHANGELOG<br>CHANGELOG | integration/CHANGELOG.md<br>packages/create-react-router/CHANGELOG.md | CHANGELOG↔CHANGELOG | integration/CHANGELOG.md↔packages/create-react-router/CHANGELOG.md | md | md | md↔md | 9 | 0.09278350515463918 | 0.0028553299492385786 | 1.469616121846345 | 0.0313588850174216 |
| docs/start/framework/route-module.md | packages/create-react-router/CHANGELOG.md | route-module<br>CHANGELOG | docs/start/framework/route-module.md<br>packages/create-react-router/CHANGELOG.md | route-module↔CHANGELOG | docs/start/framework/route-module.md↔packages/create-react-router/CHANGELOG.md | md | md | md↔md | 3 | 0.05 | 0.0009517766497461929 | 0.7919597989949748 | 0.01171875 |
| packages/react-router/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 31 | 0.15577889447236182 | 0.00983502538071066 | 0.7014501076812635 | 0.03571428571428571 |
| packages/react-router-dom/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-dom/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-dom/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 31 | 0.15577889447236182 | 0.00983502538071066 | 0.7417146153729371 | 0.03734939759036145 |
| packages/create-react-router/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/create-react-router/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/create-react-router/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 31 | 0.15577889447236182 | 0.00983502538071066 | 2.2318867062585652 | 0.07989690721649484 |
| packages/react-router-remix-routes-option-adapter/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-remix-routes-option-adapter/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-remix-routes-option-adapter/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 31 | 0.15577889447236182 | 0.00983502538071066 | 2.338167025604211 | 0.082010582010582 |
| packages/react-router-fs-routes/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-fs-routes/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-fs-routes/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 31 | 0.15577889447236182 | 0.00983502538071066 | 2.2318867062585652 | 0.07989690721649484 |
| packages/react-router-cloudflare/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-cloudflare/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-cloudflare/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 31 | 0.15577889447236182 | 0.00983502538071066 | 2.153574892003879 | 0.07828282828282829 |
| packages/react-router-architect/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-architect/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-architect/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 31 | 0.15577889447236182 | 0.00983502538071066 | 2.172633076888869 | 0.07868020304568528 |

[Full data](./List_pairwise_changed_files.csv)

### 5.2 Pairwise Changed Files (Top by Lift)

File pairs that co-change more often than random chance (lift > 1).

| fileExtensionPair | firstFileNameShort | secondFileNameShort | updateCommitCount | updateCommitMinConfidence | updateCommitLift | updateCommitJaccardSimilarity | updateCommitSupport | firstFileName | secondFileName |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ts↔ts | vite-dev-custom-entry-test | vite-absolute-base-test | 3 | 1 | 157.6 | 0.15 | 0.0009517766497461929 | integration/vite-dev-custom-entry-test.ts | integration/vite-absolute-base-test.ts |
| ts↔ts | vite-loader-context-test | vite-node-env-test | 4 | 0.8 | 148.32941176470587 | 0.2222222222222222 | 0.0012690355329949238 | integration/vite-loader-context-test.ts | integration/vite-node-env-test.ts |
| ts↔ts | sessions-test | sessions | 3 | 0.375 | 118.2 | 0.2 | 0.0009517766497461929 | packages/react-router/__tests__/server-runtime/sessions-test.ts | packages/react-router/lib/server-runtime/sessions.ts |
| ts↔ts | remove-exports-test | remove-exports | 4 | 0.36363636363636365 | 104.19834710743801 | 0.2222222222222222 | 0.0012690355329949238 | packages/react-router-dev/vite/remove-exports-test.ts | packages/react-router-dev/vite/remove-exports.ts |
| ts↔ts | vite-dotenv-test | vite-node-env-test | 4 | 0.8 | 93.3925925925926 | 0.14285714285714285 | 0.0012690355329949238 | integration/vite-dotenv-test.ts | integration/vite-node-env-test.ts |
| ts↔ts | fileStorage | sessions-test | 3 | 0.3 | 85.96363636363637 | 0.16666666666666666 | 0.0009517766497461929 | packages/react-router-node/sessions/fileStorage.ts | packages/react-router-node/__tests__/sessions-test.ts |
| ts↔ts | routes | routes | 3 | 0.75 | 81.51724137931035 | 0.1 | 0.0009517766497461929 | packages/react-router-dev/routes.ts | packages/react-router-dev/config/routes.ts |
| ts↔ts | vite-server-bundles-test | vite-node-env-test | 5 | 1 | 75.04761904761905 | 0.11904761904761904 | 0.0015862944162436548 | integration/vite-server-bundles-test.ts | integration/vite-node-env-test.ts |
| ts↔ts | vite-dot-server-test | vite-node-env-test | 5 | 1 | 73.30232558139535 | 0.11627906976744186 | 0.0015862944162436548 | integration/vite-dot-server-test.ts | integration/vite-node-env-test.ts |
| ts↔ts | vite-dot-client-test | vite-dev-custom-entry-test | 3 | 0.42857142857142855 | 67.54285714285714 | 0.125 | 0.0009517766497461929 | integration/vite-dot-client-test.ts | integration/vite-dev-custom-entry-test.ts |

[Full data](./List_pairwise_changed_files_top_lift.csv)

### 5.3 Pairwise Changed Files With Dependencies

Files that are co-changed and also have a structural dependency relationship between them.

| dependencyWeight | fileDistance | commitCount | updateCommitMinConfidence | updateCommitSupport | updateCommitLift | updateCommitJaccardSimilarity |
| --- | --- | --- | --- | --- | --- | --- |
| 11 | 5 | 3 | 0.2727272727272727 | 0.0009517766497461929 | 3.7869443331998394 | 0.01276595744680851 |
| 11 | 4 | 4 | 0.16 | 0.0012690355329949238 | 2.2216740088105724 | 0.016129032258064516 |
| 22 | 5 | 3 | 0.07692307692307693 | 0.0009517766497461929 | 1.0681125042358524 | 0.011406844106463879 |
| 22 | 5 | 9 | 0.14516129032258066 | 0.0028553299492385786 | 2.0156316612192695 | 0.03214285714285714 |
| 33 | 4 | 8 | 0.06504065040650407 | 0.0025380710659898475 | 0.9031195157766556 | 0.023391812865497075 |
| 66 | 4 | 3 | 0.13636363636363635 | 0.0009517766497461929 | 1.8934721665999197 | 0.012195121951219513 |
| 66 | 6 | 3 | 0.15789473684210525 | 0.0009517766497461929 | 5.924812030075188 | 0.03 |
| 66 | 4 | 9 | 0.36 | 0.0028553299492385786 | 37.824 | 0.1956521739130435 |
| 91 | 0 | 4 | 0.36363636363636365 | 0.0012690355329949238 | 20.108452950558217 | 0.0625 |
| 91 | 0 | 5 | 0.21739130434782608 | 0.0015862944162436548 | 15.935288169868555 | 0.08196721311475409 |

[Full data](./List_pairwise_changed_files_with_dependencies.csv)

### 5.4 Pairwise Changed Files (Charts)



---

## 6. Files by Author

Per-author file commit stats. Useful for knowledge boundaries and bus-factor risk.

### 6.1 Files with Commit Statistics by Author

| filePath | author | commitCount | commitHashes | lastCommitDate | lastCreationDate | lastModificationDate | daysSinceLastCommit | daysSinceLastCreation | daysSinceLastModification | maxCommitSha |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| react-router-7.16.0/.agents/skills/fix-bug/SKILL.md | Matt Brophy | 5 | ["a842fca719e81505f454a8e6a8c728cdaed22067","2469dd6621fbcaec689571c3f003af5711bc54de","06c1149bc0b4f50db0cc6fc10471b4ad963b8969","46321cf2767cb820c1be8bbea3bafbc32c6c4ffd","1497c6ba52e55158e4f12b54617b1255935c75d5"] | 2026-04-14 | 2026-03-18 | 2026-04-14 | 55 | 81 | 54 | a842fca719e81505f454a8e6a8c728cdaed22067 |
| react-router-7.16.0/.agents/skills/implement-rfc/SKILL.md | Matt Brophy | 3 | ["fadd6c490cc84abc560a2413ee6fa0f2617d098d","522bc1b8cd0d7b3565bf9193789f2b7d5503856b","a6ab746a43675332ec3c190b1390724bf5c833db"] | 2026-05-14 | 2026-05-07 | 2026-05-07 | 25 | 31 | 31 | fadd6c490cc84abc560a2413ee6fa0f2617d098d |
| react-router-7.16.0/.browserslistrc | Michael Jackson | 3 | ["82c500c4a1a5d53a608faee25f8322c661b242a1","b3f728487ae6fe7d5ef4ddc759fb2a4ca0df712e","f6df0697e1b2064a2b3a12e8b39577326fdd945b"] | 2021-09-09 | 2018-10-30 | 2021-09-09 | 1733 | 2777 | 1732 | f6df0697e1b2064a2b3a12e8b39577326fdd945b |
| react-router-7.16.0/.browserslistrc | Matt Brophy | 1 | ["4fa24c1b12c7c2ff8f32bb611b8b5b3ac4678c61"] | 2024-03-27 | 2018-10-30 | 2021-09-09 | 803 | 2777 | 1732 | 4fa24c1b12c7c2ff8f32bb611b8b5b3ac4678c61 |
| react-router-7.16.0/.github/FUNDING.yml | Michael Jackson | 1 | ["2679ebc9386c87a53da5c88f606d326ed6bba5bd"] | 2019-10-22 | 2019-10-22 | 2019-10-22 | 2421 | 2420 | 2420 | 2679ebc9386c87a53da5c88f606d326ed6bba5bd |
| react-router-7.16.0/.github/FUNDING.yml | Matt Brophy | 1 | ["4fa24c1b12c7c2ff8f32bb611b8b5b3ac4678c61"] | 2024-03-27 | 2019-10-22 | 2019-10-22 | 803 | 2420 | 2420 | 4fa24c1b12c7c2ff8f32bb611b8b5b3ac4678c61 |
| react-router-7.16.0/.github/ISSUE_TEMPLATE/bug_report.yml | Matt Brophy | 21 | ["5a43e19573c11d1469fd43ef1fddaf7be02abca5","721bee06b9085c57f20c9333cdd327ea81f0376a","12aa08a8756e5af0fdc2ae4eda0ae061cf713311","09024c8a82932bb8b2f1cd8bf3a08222523c9013","953948ac3b53ac49fdd8028e10acab2587279355","6585c8396085b75c7674e3dd1bacde3541b0f539","7b7498e4b7e1fff895d7aab512d11b57fecbdd37","482b6a2902dc346b350a3c2d4fcac4e6048ee0cf","15ad8d531fae7cd3e2d2038cf3c29595d7812ee1","14666ddd78070ffd6149f7e20371927b784eb054","4aa9298ab35483b1e21e357e7574aa3f0d727725","f153b191e1c52bc8fb0e485bfd5d8ec2a8752104","45a7b0e4636f45c910c074e5babb66975e8e8652","de0bf8345e6684a671474d992aaff5e7a4040a16","c5396bd94aacb97c57a6507b1397e08aa57da972","6d945608dc1981a2222cdae5d6a4698602cf852b","cc0779ec9af43e3bfd61e09c0c2d0cb30500989f","ac399b7b388fdf3474c74eecb363502cb4cc8c9e","4fa24c1b12c7c2ff8f32bb611b8b5b3ac4678c61","0252132bb7352d685609cb5d7b99fe632f731876","fdb90690cb74b1060f9e9de550520f30f9c2ef08"] | 2025-07-16 | 2021-11-05 | 2025-07-16 | 327 | 1675 | 326 | fdb90690cb74b1060f9e9de550520f30f9c2ef08 |
| react-router-7.16.0/.github/ISSUE_TEMPLATE/bug_report.yml | Pedro Cattori | 9 | ["c6c8c3bfe4bce8ce53e61cee5542d88363593a93","f8c9a71581711d7f839fb3d76279a3cc2ed69b6f","4e989f839a6af67a6f339f7726fd0ca58c93689a","d2710f8b0e8f17063c0fac9f1fbeeee4e0342479","eb8be394f4897f0545fa70fe4b0d9c38dc877b85","d20ba30b1bfb5ea3b96c20af102dc54c8cd8b3b3","6f313ec32d3078ea4b4e93fa3522325b6a979deb","b5f2e295f2e857edbfd15da236fd9497f1ec13b6","acf3f77a3076b55214e8985f7dc758535ac07c5e"] | 2025-06-03 | 2021-11-05 | 2025-07-16 | 370 | 1675 | 326 | f8c9a71581711d7f839fb3d76279a3cc2ed69b6f |
| react-router-7.16.0/.github/ISSUE_TEMPLATE/bug_report.yml | Tim Dorr | 3 | ["2375e7956873a311edf8985714e104cdbc0ecb80","129b49aa293f2c084d1c455b4c6f1a87ac4ec552","c299d29c7eeb1b3fc3c1726a5d6ebebdfb74ea4a"] | 2022-03-17 | 2021-11-05 | 2025-07-16 | 1544 | 1675 | 326 | c299d29c7eeb1b3fc3c1726a5d6ebebdfb74ea4a |
| react-router-7.16.0/.github/ISSUE_TEMPLATE/bug_report.yml | Chance Strickland | 2 | ["91a52f822d292c4ef017e6c252b32b9ebd57c9c2","0079767bcc93ae543b5c2511f6c6f5f5b8c22f7c"] | 2023-01-13 | 2021-11-05 | 2025-07-16 | 1242 | 1675 | 326 | 91a52f822d292c4ef017e6c252b32b9ebd57c9c2 |

[Full data](./List_git_files_with_commit_statistics_by_author.csv)

---

## 7. Data Quality

Files in git log that are unresolved (not found in codebase) or ambiguous (multiple matches). Affects reliability of co-change metrics.

### 7.1 File Resolution Summary

Resolved vs. ambiguous vs. unresolved files by extension.

| resolved | extension | gitFileCount | fileLabels | gitFileExamples |
| --- | --- | --- | --- | --- |
| false | md | 1859 | ["File","Git"] | ["CHANGELOG.md","packages/create-react-router/CHANGELOG.md","packages/react-router-architect/CHANGELOG.md","packages/react-router-cloudflare/CHANGELOG.md","packages/react-router-dev/.changes/minor.stabilize-trailing-slash-data-requests.md","packages/react-router-dev/.changes/minor.v8-future-flag-warnings.md","packages/react-router-dev/CHANGELOG.md","packages/react-router-dom/.changes/patch.remove-staleinvalid-unpkg-field-packagejson-removed.md","packages/react-router-dom/CHANGELOG.md"] |
| false | js | 1744 | ["File","Git"] | ["scripts/constants.js","scripts/utils.js","scripts/publish.js","scripts/version.js","scripts/find-release-from-changeset.js","packages/react-router/.eslintrc.js","packages/react-router/lib/dom/node-main.js","packages/react-router/lib/server-runtime/.eslintrc.js","packages/react-router/node-main-dom-export.js"] |
| false | ts | 1127 | ["File","Git"] | ["packages/react-router-express/__tests__/server-test.ts","scripts/release-comments.ts","integration/cli-test.ts","integration/fetcher-layout-test.ts","integration/single-fetch-test.ts","integration/vite-presets-test.ts","packages/react-router-dev/__tests__/future-flags-test.ts","packages/react-router-node/__tests__/stream-test.ts","packages/react-router/__tests__/router/browser-test.ts"] |
| false | tsx | 488 | ["File","Git"] | ["packages/react-router/__tests__/dom/ssr/meta-test.tsx","packages/react-router/__tests__/generatePath-test.tsx","packages/react-router/lib/dom-export/hydrated-router.tsx","packages/react-router/lib/dom/server.tsx","packages/react-router/lib/dom/ssr/components.tsx","packages/react-router/lib/dom/ssr/routes-test-stub.tsx","packages/react-router/lib/hooks.tsx","packages/react-router/lib/rsc/browser.tsx","packages/react-router/lib/rsc/server.ssr.tsx"] |
| false | json | 249 | ["File","Git"] | ["integration/helpers/cloudflare-dev-proxy-template/tsconfig.json","integration/helpers/rsc-vite-framework/tsconfig.json","playground/rsc-vite-framework/tsconfig.json",".changeset/config.json","playground/performance/public/.well-known/appspecific/com.chrome.devtools.json","playground/performance/tsconfig.json","scripts/tsconfig.json","integration/helpers/vite-rolldown-template/package.json","integration/helpers/vite-8-template/tsconfig.json"] |
| false | css | 85 | ["File","Git"] | ["playground/rsc-vite-7-framework/app/root.css","playground/rsc-vite-7-framework/app/routes/_index/styles.css","playground/rsc-vite-7-framework/app/routes/client-loader-hydrate/styles.module.css","playground/rsc-vite-7-framework/app/routes/client-loader-without-server-loader/styles.module.css","playground/rsc-vite-7-framework/app/routes/client-loader/styles.module.css","playground/rsc-vite-7-framework/app/routes/mdx-glob.$post/posts/hello/hello-component.module.css","playground/rsc-vite-7-framework/app/routes/mdx-glob.$post/posts/world/world-component.module.css","playground/rsc-vite-7-framework/app/routes/server-loader/styles.module.css","examples/modal-data-router/src/index.css"] |
| false | gitignore | 83 | ["File","Git"] | ["playground/performance/.gitignore","integration/helpers/vite-rolldown-template/.gitignore","integration/helpers/vite-8-template/.gitignore","playground/framework-rolldown-vite/.gitignore","playground/framework-vite-6/.gitignore","playground/framework/.gitignore","playground/rsc-vite-7-framework/.gitignore",".gitignore","examples/modal-data-router/.gitignore"] |
| false | html | 64 | ["File","Git"] | ["examples/modal-data-router/index.html","playground/data/index.html","examples/auth-router-provider/index.html","examples/auth/index.html","examples/basic-data-router/index.html","examples/basic/index.html","examples/custom-filter-link/index.html","examples/custom-link/index.html","examples/custom-query-parsing/index.html"] |
| false | ico | 50 | ["File","Git"] | ["playground/performance/public/favicon.ico","integration/helpers/vite-rolldown-template/public/favicon.ico","integration/helpers/vite-8-template/public/favicon.ico","playground/framework-rolldown-vite/public/favicon.ico","playground/framework/public/favicon.ico","playground/framework-vite-6/public/favicon.ico","playground/rsc-vite-7-framework/public/favicon.ico","integration/helpers/rsc-parcel/public/favicon.ico","integration/helpers/rsc-parcel-framework/public/favicon.ico"] |
| false | yml | 44 | ["File","Git"] | [".github/workflows/issue-checks.yml",".github/workflows/pr-actions.yml",".github/workflows/pr-checks.yml","contributors.yml",".github/workflows/close-no-repro-issue.yml",".github/workflows/support.yml",".github/workflows/close-no-repro-issues.yml",".github/workflows/delete-changeset-bot-comments.yml",".github/workflows/preview.yml"] |

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
| json | ["File","TS"] | 13 | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/create-react-router/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/create-react-router/__tests__/fixtures/blank/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/create-react-router/__tests__/fixtures/with-ignored-dir/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-architect/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-express/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-node/.reports/jqa/ts-output.json"] |

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
