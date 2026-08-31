---
title: "Git History Report"
generated: "2026-08-31"
model_version: "v4.0.2"
dataset: "react-router-7.18.3"
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
| react-router-7.18.3 | react-router-7.18.3 |  |  | Matt Brophy | github-actions[bot] | Remix Run Bot | 602 | 1187 | 4926 | 2026-08-27 | 2026-08-28 | 2026-08-28 | 3 | 3 | 2 | fff84b5f20f35c347c9d6313dfc603db0eac6e19 | react-router-7.18.3/typedoc.mjs | 1 | 1 |
| react-router-7.18.3/.agents/skills | .agents/skills | react-router-7.18.3 | react-router-7.18.3 | Matt Brophy | Brooks Lybrand | null | 2 | 7 | 12 | 2026-06-16 | 2026-06-16 | 2026-06-16 | 76 | 75 | 75 | fadd6c490cc84abc560a2413ee6fa0f2617d098d | react-router-7.18.3/.agents/skills/react-router/references/rsc.md | 3 | 2 |
| react-router-7.18.3/.agents/skills/fix-bug | fix-bug | react-router-7.18.3/.agents/skills | skills | Matt Brophy | Brooks Lybrand | null | 2 | 1 | 8 | 2026-03-18 | 2026-06-04 | 2026-06-04 | 88 | 165 | 87 | d6f3a05d4124ae9c1f2f74c599f80d091268ce0c | react-router-7.18.3/.agents/skills/fix-bug/SKILL.md | 4 | 1 |
| react-router-7.18.3/.agents/skills/implement-rfc | implement-rfc | react-router-7.18.3/.agents/skills | skills | Matt Brophy | null | null | 1 | 1 | 4 | 2026-05-07 | 2026-06-04 | 2026-06-04 | 88 | 115 | 87 | fadd6c490cc84abc560a2413ee6fa0f2617d098d | react-router-7.18.3/.agents/skills/implement-rfc/SKILL.md | 4 | 1 |
| react-router-7.18.3/.agents/skills/react-router | react-router | react-router-7.18.3/.agents/skills | skills | Brooks Lybrand | null | null | 1 | 5 | 1 | 2026-06-16 | 2026-06-16 | 2026-06-16 | 76 | 75 | 75 | 8f364c820ef698952e4bed876d6c93c895357692 | react-router-7.18.3/.agents/skills/react-router/references/rsc.md | 4 | 1 |
| react-router-7.18.3/.agents/skills/react-router/references | references | react-router-7.18.3/.agents/skills/react-router | react-router | Brooks Lybrand | null | null | 1 | 4 | 1 | 2026-06-16 | 2026-06-16 | 2026-06-16 | 76 | 75 | 75 | 8f364c820ef698952e4bed876d6c93c895357692 | react-router-7.18.3/.agents/skills/react-router/references/rsc.md | 5 | 1 |
| react-router-7.18.3/.github | .github | react-router-7.18.3 | react-router-7.18.3 | Matt Brophy | Michael Jackson | Michaël De Boey | 22 | 19 | 221 | 2026-05-26 | 2026-06-16 | 2026-06-16 | 76 | 96 | 75 | ff67b74a33c9f13fac28afc4923d0bf5628998ec | react-router-7.18.3/.github/workflows/test.yml | 2 | 1 |
| react-router-7.18.3/.github/ISSUE_TEMPLATE | ISSUE_TEMPLATE | react-router-7.18.3/.github | .github | Matt Brophy | Pedro Cattori | Tim Dorr | 13 | 3 | 51 | 2023-01-11 | 2026-06-04 | 2026-06-04 | 88 | 1327 | 87 | ff67b74a33c9f13fac28afc4923d0bf5628998ec | react-router-7.18.3/.github/ISSUE_TEMPLATE/documentation_isse.yml | 3 | 1 |
| react-router-7.18.3/.github/workflows | workflows | react-router-7.18.3/.github | .github | Matt Brophy | dependabot[bot] | Michael Jackson | 16 | 14 | 182 | 2026-05-26 | 2026-06-16 | 2026-06-16 | 76 | 96 | 75 | ff4c0712f7b24d38f51f7b967d7c31aeac531bed | react-router-7.18.3/.github/workflows/test.yml | 3 | 1 |
| react-router-7.18.3/decisions | decisions | react-router-7.18.3 | react-router-7.18.3 | Matt Brophy | Pedro Cattori | Michael Jackson | 10 | 20 | 69 | 2026-02-19 | 2026-06-04 | 2026-06-04 | 88 | 192 | 88 | ff67b74a33c9f13fac28afc4923d0bf5628998ec | react-router-7.18.3/decisions/template.md | 2 | 1 |

[Full data](./List_git_file_directories_with_commit_statistics.csv)

### 2.2 Directory Commit Statistics (Charts)



---

## 3. Co-Changed Files

Files committed together = logical coupling signal. May belong to the same conceptual unit or share a concern.

### 3.1 Co-Changed File Pairs

| firstFile | secondFile | commitCount |
| --- | --- | --- |
| react-router-7.18.3/packages/react-router-dom/package.json | react-router-7.18.3/packages/react-router/package.json | 349 |
| react-router-7.18.3/packages/react-router/CHANGELOG.md | react-router-7.18.3/packages/react-router/package.json | 180 |
| react-router-7.18.3/packages/react-router-dom/package.json | react-router-7.18.3/packages/react-router/CHANGELOG.md | 178 |
| react-router-7.18.3/packages/react-router/lib/components.tsx | react-router-7.18.3/packages/react-router/lib/hooks.tsx | 91 |
| react-router-7.18.3/packages/react-router/package.json | react-router-7.18.3/contributors.yml | 91 |
| react-router-7.18.3/packages/react-router-dom/package.json | react-router-7.18.3/contributors.yml | 91 |
| react-router-7.18.3/packages/react-router-node/CHANGELOG.md | react-router-7.18.3/packages/react-router-serve/CHANGELOG.md | 87 |
| react-router-7.18.3/packages/react-router-dev/CHANGELOG.md | react-router-7.18.3/packages/react-router-node/CHANGELOG.md | 87 |
| react-router-7.18.3/packages/react-router-dev/CHANGELOG.md | react-router-7.18.3/packages/react-router-serve/CHANGELOG.md | 85 |
| react-router-7.18.3/packages/react-router/CHANGELOG.md | react-router-7.18.3/contributors.yml | 85 |

### 3.2 Co-Changed File Pairs (All in One Commit)

Files changed together in a single large commit.

| firstFile | secondFile | commitCount |
| --- | --- | --- |
| react-router-7.18.3/packages/react-router-dom/package.json | react-router-7.18.3/packages/react-router/package.json | 603 |
| react-router-7.18.3/packages/react-router/CHANGELOG.md | react-router-7.18.3/packages/react-router/package.json | 429 |
| react-router-7.18.3/packages/react-router-dom/package.json | react-router-7.18.3/packages/react-router/CHANGELOG.md | 426 |
| react-router-7.18.3/packages/react-router-node/CHANGELOG.md | react-router-7.18.3/packages/react-router-serve/CHANGELOG.md | 240 |
| react-router-7.18.3/packages/react-router-dev/CHANGELOG.md | react-router-7.18.3/packages/react-router-node/CHANGELOG.md | 240 |
| react-router-7.18.3/packages/react-router-dev/CHANGELOG.md | react-router-7.18.3/packages/react-router-serve/CHANGELOG.md | 238 |
| react-router-7.18.3/packages/react-router-express/CHANGELOG.md | react-router-7.18.3/packages/react-router-node/CHANGELOG.md | 234 |
| react-router-7.18.3/packages/react-router-dev/CHANGELOG.md | react-router-7.18.3/packages/react-router-express/CHANGELOG.md | 233 |
| react-router-7.18.3/packages/react-router-express/CHANGELOG.md | react-router-7.18.3/packages/react-router-serve/CHANGELOG.md | 232 |
| react-router-7.18.3/packages/react-router-dev/CHANGELOG.md | react-router-7.18.3/packages/react-router/CHANGELOG.md | 232 |

### 3.3 Co-Changed With a Specific File

Shows all files that were changed together with another particular file.

| filePath | commitCount | coChangeRate | maxLift | avgLift |
| --- | --- | --- | --- | --- |
| react-router-7.18.3/packages/react-router-dom/package.json | 352 | 0.00046300985342844327 | 2.3024432736508467 | 1.3188771487573363 |
| react-router-7.18.3/packages/react-router/CHANGELOG.md | 190 | 0.0007014564450925738 | 1.614752293577982 | 1.0693595298730991 |
| react-router-7.18.3/contributors.yml | 167 | 0.0006438579040304734 | 1.3015443827340931 | 0.643676060640473 |
| react-router-7.18.3/packages/react-router/lib/components.tsx | 157 | 0.0011788910914879557 | 6.079104379753475 | 3.079922704357124 |
| react-router-7.18.3/pnpm-lock.yaml | 150 | 0.0006851661527920521 | 5.986666666666667 | 1.5290736748268359 |
| react-router-7.18.3/packages/react-router/lib/hooks.tsx | 139 | 0.0015408662106885123 | 3.61661997198319 | 1.8584262518639025 |
| react-router-7.18.3/packages/react-router/package.json | 135 | 0.00047654347135444246 | 1.2985164319248828 | 0.7131529643352874 |
| react-router-7.18.3/packages/react-router-dev/CHANGELOG.md | 94 | 0.0005253451070250936 | 3.3200704225352116 | 2.031431906627879 |
| react-router-7.18.3/packages/react-router/lib/router/router.ts | 91 | 0.0014057093425605537 | 8.184895833333334 | 2.5063186737082854 |
| react-router-7.18.3/packages/react-router-node/CHANGELOG.md | 90 | 0.0010028525583883046 | 3.4386443661971833 | 1.8094424029948144 |

[Full data](./List_git_files_that_were_changed_together_with_another_file.csv)

### 3.4 Co-Changed With a Specific File (All in One)

| filePath | commitCount |
| --- | --- |
| react-router-7.18.3/packages/react-router/package.json | 637 |
| react-router-7.18.3/packages/react-router-dom/package.json | 609 |
| react-router-7.18.3/packages/react-router/CHANGELOG.md | 492 |
| react-router-7.18.3/contributors.yml | 438 |
| react-router-7.18.3/packages/react-router-dev/package.json | 258 |
| react-router-7.18.3/packages/react-router-dev/CHANGELOG.md | 247 |
| react-router-7.18.3/packages/react-router-node/CHANGELOG.md | 243 |
| react-router-7.18.3/packages/react-router-serve/CHANGELOG.md | 240 |
| react-router-7.18.3/packages/react-router-express/CHANGELOG.md | 235 |
| react-router-7.18.3/packages/react-router-architect/CHANGELOG.md | 211 |

### 3.5 Co-Changed Files (Charts)



---

## 4. File Change Distribution

Files changed per commit. High proportion of large commits = low commit granularity.

### 4.1 Files per Commit Distribution

| filesPerCommit | commitCount |
| --- | --- |
| 1 | 4666 |
| 2 | 1807 |
| 3 | 919 |
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
| integration/CHANGELOG.md | packages/create-react-router/CHANGELOG.md | CHANGELOG<br>CHANGELOG | integration/CHANGELOG.md<br>packages/create-react-router/CHANGELOG.md | CHANGELOG↔CHANGELOG | integration/CHANGELOG.md↔packages/create-react-router/CHANGELOG.md | md | md | md↔md | 4 | 0.041237113402061855 | 0.0012726694241170856 | 0.6261267991433838 | 0.013333333333333334 |
| packages/react-router-express/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-express/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-express/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 26 | 0.12560386473429952 | 0.008272351256761056 | 1.6870638754696727 | 0.06265060240963856 |
| packages/react-router-architect/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-architect/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-architect/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 26 | 0.12560386473429952 | 0.008272351256761056 | 1.6870638754696727 | 0.06265060240963856 |
| packages/react-router-dev/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-dev/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-dev/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 26 | 0.12560386473429952 | 0.008272351256761056 | 1.2817303469477384 | 0.053169734151329244 |
| packages/react-router-node/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-node/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-node/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 26 | 0.12560386473429952 | 0.008272351256761056 | 1.6587098607558968 | 0.06205250596658711 |
| packages/react-router-remix-routes-option-adapter/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-remix-routes-option-adapter/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-remix-routes-option-adapter/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 26 | 0.12560386473429952 | 0.008272351256761056 | 1.8108850773390066 | 0.06516290726817042 |
| packages/react-router/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 26 | 0.12560386473429952 | 0.008272351256761056 | 0.5560182350139484 | 0.029180695847362513 |
| packages/react-router-dom/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-dom/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-dom/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 26 | 0.12560386473429952 | 0.008272351256761056 | 0.5883352412219126 | 0.03051643192488263 |
| packages/react-router-fs-routes/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-fs-routes/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-fs-routes/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 26 | 0.12560386473429952 | 0.008272351256761056 | 1.7314602932451904 | 0.06356968215158924 |
| packages/create-react-router/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/create-react-router/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/create-react-router/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 26 | 0.12560386473429952 | 0.008272351256761056 | 1.7314602932451904 | 0.06356968215158924 |

[Full data](./List_pairwise_changed_files.csv)

### 5.2 Pairwise Changed Files (Top by Lift)

File pairs that co-change more often than random chance (lift > 1).

| fileExtensionPair | firstFileNameShort | secondFileNameShort | updateCommitCount | updateCommitMinConfidence | updateCommitLift | updateCommitJaccardSimilarity | updateCommitSupport | firstFileName | secondFileName |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ts↔ts | actions-test | actions | 3 | 0.5 | 174.61111111111111 | 0.25 | 0.0009545020680878142 | packages/react-router/__tests__/server-runtime/actions-test.ts | packages/react-router/lib/actions.ts |
| ts↔ts | vite-dev-custom-entry-test | vite-absolute-base-test | 3 | 1 | 157.15 | 0.15 | 0.0009545020680878142 | integration/vite-dev-custom-entry-test.ts | integration/vite-absolute-base-test.ts |
| ts↔ts | vite-loader-context-test | vite-node-env-test | 4 | 0.8 | 147.90588235294118 | 0.2222222222222222 | 0.0012726694241170856 | integration/vite-loader-context-test.ts | integration/vite-node-env-test.ts |
| ts↔ts | sessions-test | sessions | 3 | 0.375 | 117.86250000000001 | 0.2 | 0.0009545020680878142 | packages/react-router/__tests__/server-runtime/sessions-test.ts | packages/react-router/lib/server-runtime/sessions.ts |
| ts↔ts | remove-exports-test | remove-exports | 4 | 0.36363636363636365 | 103.90082644628099 | 0.2222222222222222 | 0.0012726694241170856 | packages/react-router-dev/vite/remove-exports-test.ts | packages/react-router-dev/vite/remove-exports.ts |
| ts↔ts | vite-dotenv-test | vite-node-env-test | 4 | 0.8 | 93.12592592592594 | 0.14285714285714285 | 0.0012726694241170856 | integration/vite-dotenv-test.ts | integration/vite-node-env-test.ts |
| ts↔ts | fileStorage | sessions-test | 3 | 0.3 | 85.71818181818182 | 0.16666666666666666 | 0.0009545020680878142 | packages/react-router-node/sessions/fileStorage.ts | packages/react-router-node/__tests__/sessions-test.ts |
| ts↔ts | routes | routes | 3 | 0.75 | 81.2844827586207 | 0.1 | 0.0009545020680878142 | packages/react-router-dev/config/routes.ts | packages/react-router-dev/routes.ts |
| ts↔ts | vite-server-bundles-test | vite-node-env-test | 5 | 1 | 74.83333333333333 | 0.11904761904761904 | 0.001590836780146357 | integration/vite-server-bundles-test.ts | integration/vite-node-env-test.ts |
| ts↔ts | vite-dot-server-test | vite-node-env-test | 5 | 1 | 73.09302325581396 | 0.11627906976744186 | 0.001590836780146357 | integration/vite-dot-server-test.ts | integration/vite-node-env-test.ts |

[Full data](./List_pairwise_changed_files_top_lift.csv)

### 5.3 Pairwise Changed Files With Dependencies

Files that are co-changed and also have a structural dependency relationship between them.

| dependencyWeight | fileDistance | commitCount | updateCommitMinConfidence | updateCommitSupport | updateCommitLift | updateCommitJaccardSimilarity |
| --- | --- | --- | --- | --- | --- | --- |
| 25 | 4 | 4 | 0.16 | 0.0012726694241170856 | 2.205614035087719 | 0.01606425702811245 |
| 28 | 0 | 4 | 0.17391304347826086 | 0.0012726694241170856 | 12.711830131445904 | 0.06451612903225806 |
| 28 | 0 | 4 | 0.36363636363636365 | 0.0012726694241170856 | 19.048484848484847 | 0.05970149253731343 |
| 28 | 0 | 6 | 0.24 | 0.0019090041361756285 | 2.9237209302325584 | 0.021660649819494584 |
| 50 | 5 | 3 | 0.07317073170731707 | 0.0009545020680878142 | 1.0086649550706033 | 0.011278195488721804 |
| 50 | 5 | 9 | 0.14285714285714285 | 0.0028635062042634426 | 1.9692982456140349 | 0.031914893617021274 |
| 56 | 3 | 3 | 0.75 | 0.0009545020680878142 | 81.2844827586207 | 0.1 |
| 56 | 4 | 3 | 0.23076923076923078 | 0.0009545020680878142 | 7.18126428027418 | 0.02702702702702703 |
| 56 | 4 | 4 | 0.10256410256410256 | 0.0012726694241170856 | 6.715811965811965 | 0.04819277108433735 |
| 56 | 0 | 6 | 0.25 | 0.0019090041361756285 | 13.095833333333333 | 0.07692307692307693 |

[Full data](./List_pairwise_changed_files_with_dependencies.csv)

### 5.4 Pairwise Changed Files (Charts)



---

## 6. Files by Author

Per-author file commit stats. Useful for knowledge boundaries and bus-factor risk.

### 6.1 Files with Commit Statistics by Author

| filePath | author | commitCount | commitHashes | lastCommitDate | lastCreationDate | lastModificationDate | daysSinceLastCommit | daysSinceLastCreation | daysSinceLastModification | maxCommitSha |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| react-router-7.18.3/.agents/skills/fix-bug/SKILL.md | Matt Brophy | 7 | ["06c1149bc0b4f50db0cc6fc10471b4ad963b8969","a842fca719e81505f454a8e6a8c728cdaed22067","2469dd6621fbcaec689571c3f003af5711bc54de","46321cf2767cb820c1be8bbea3bafbc32c6c4ffd","1497c6ba52e55158e4f12b54617b1255935c75d5","963affeb924f2256bd20c0c5c87e4c4b4fcbd188","d6f3a05d4124ae9c1f2f74c599f80d091268ce0c"] | 2026-06-04 | 2026-03-18 | 2026-06-04 | 88 | 165 | 87 | d6f3a05d4124ae9c1f2f74c599f80d091268ce0c |
| react-router-7.18.3/.agents/skills/fix-bug/SKILL.md | Brooks Lybrand | 1 | ["4f8fff6cdb31c549fd011ac516fad5ad2e641b5f"] | 2026-05-29 | 2026-03-18 | 2026-06-04 | 94 | 165 | 87 | 4f8fff6cdb31c549fd011ac516fad5ad2e641b5f |
| react-router-7.18.3/.agents/skills/implement-rfc/SKILL.md | Matt Brophy | 4 | ["fadd6c490cc84abc560a2413ee6fa0f2617d098d","522bc1b8cd0d7b3565bf9193789f2b7d5503856b","a6ab746a43675332ec3c190b1390724bf5c833db","d6f3a05d4124ae9c1f2f74c599f80d091268ce0c"] | 2026-06-04 | 2026-05-07 | 2026-06-04 | 88 | 115 | 87 | fadd6c490cc84abc560a2413ee6fa0f2617d098d |
| react-router-7.18.3/.agents/skills/react-router/SKILL.md | Brooks Lybrand | 1 | ["8f364c820ef698952e4bed876d6c93c895357692"] | 2026-06-16 | 2026-06-16 | 2026-06-16 | 76 | 75 | 75 | 8f364c820ef698952e4bed876d6c93c895357692 |
| react-router-7.18.3/.agents/skills/react-router/references/data-mode.md | Brooks Lybrand | 1 | ["8f364c820ef698952e4bed876d6c93c895357692"] | 2026-06-16 | 2026-06-16 | 2026-06-16 | 76 | 75 | 75 | 8f364c820ef698952e4bed876d6c93c895357692 |
| react-router-7.18.3/.agents/skills/react-router/references/declarative-mode.md | Brooks Lybrand | 1 | ["8f364c820ef698952e4bed876d6c93c895357692"] | 2026-06-16 | 2026-06-16 | 2026-06-16 | 76 | 75 | 75 | 8f364c820ef698952e4bed876d6c93c895357692 |
| react-router-7.18.3/.agents/skills/react-router/references/framework-mode.md | Brooks Lybrand | 1 | ["8f364c820ef698952e4bed876d6c93c895357692"] | 2026-06-16 | 2026-06-16 | 2026-06-16 | 76 | 75 | 75 | 8f364c820ef698952e4bed876d6c93c895357692 |
| react-router-7.18.3/.agents/skills/react-router/references/rsc.md | Brooks Lybrand | 1 | ["8f364c820ef698952e4bed876d6c93c895357692"] | 2026-06-16 | 2026-06-16 | 2026-06-16 | 76 | 75 | 75 | 8f364c820ef698952e4bed876d6c93c895357692 |
| react-router-7.18.3/.browserslistrc | Michael Jackson | 3 | ["82c500c4a1a5d53a608faee25f8322c661b242a1","b3f728487ae6fe7d5ef4ddc759fb2a4ca0df712e","f6df0697e1b2064a2b3a12e8b39577326fdd945b"] | 2021-09-09 | 2018-10-30 | 2021-09-09 | 1817 | 2861 | 1816 | f6df0697e1b2064a2b3a12e8b39577326fdd945b |
| react-router-7.18.3/.browserslistrc | Matt Brophy | 1 | ["4fa24c1b12c7c2ff8f32bb611b8b5b3ac4678c61"] | 2024-03-27 | 2018-10-30 | 2021-09-09 | 887 | 2861 | 1816 | 4fa24c1b12c7c2ff8f32bb611b8b5b3ac4678c61 |

[Full data](./List_git_files_with_commit_statistics_by_author.csv)

---

## 7. Data Quality

Files in git log that are unresolved (not found in codebase) or ambiguous (multiple matches). Affects reliability of co-change metrics.

### 7.1 File Resolution Summary

Resolved vs. ambiguous vs. unresolved files by extension.

| resolved | extension | gitFileCount | fileLabels | gitFileExamples |
| --- | --- | --- | --- | --- |
| false | md | 1888 | ["File","Git"] | ["CHANGELOG.md","packages/create-react-router/CHANGELOG.md","packages/react-router-architect/CHANGELOG.md","packages/react-router-cloudflare/CHANGELOG.md","packages/react-router-dev/CHANGELOG.md","packages/react-router-dom/CHANGELOG.md","packages/react-router-express/CHANGELOG.md","packages/react-router-fs-routes/CHANGELOG.md","packages/react-router-node/.changes/patch.streaming-client-disconnect.md"] |
| false | js | 1744 | ["File","Git"] | ["examples/multi-app/inbox/messages.js","examples/multi-app/server.js","examples/multi-app/vite.config.js","examples/notes/src/notes.js","examples/ssr-data-router/server.js","examples/ssr-data-router/vite.config.js","examples/ssr/server.js","examples/ssr/vite.config.js","scripts/constants.js"] |
| false | ts | 1133 | ["File","Git"] | ["packages/react-router-node/__tests__/stream-test.ts","packages/react-router/__tests__/router/utils/data-router-setup.ts","packages/react-router/__tests__/router/browser-test.ts","packages/react-router/__tests__/router/redirects-test.ts","packages/react-router/__tests__/rsc/server-test.ts","packages/react-router/lib/rsc/redirect.ts","packages/react-router/__tests__/server-runtime/actions-test.ts","integration/rsc-csrf-action-test.ts","scripts/docs.ts"] |
| false | tsx | 489 | ["File","Git"] | ["packages/react-router/__tests__/external-navigation-test.tsx","packages/react-router/__tests__/useNavigate-test.tsx","packages/react-router/lib/components.tsx","packages/react-router/lib/hooks.tsx","packages/react-router/lib/rsc/browser.tsx","packages/react-router/__tests__/dom/link-href-test.tsx","packages/react-router/lib/dom/lib.tsx","packages/react-router/lib/dom/server.tsx","packages/react-router/lib/rsc/server.ssr.tsx"] |
| false | json | 272 | ["File","Git"] | ["examples/auth-router-provider/package-lock.json","examples/auth-router-provider/package.json","examples/auth-router-provider/tsconfig.json","examples/auth/package-lock.json","examples/auth/package.json","examples/auth/tsconfig.json","examples/basic-data-router/package-lock.json","examples/basic-data-router/package.json","examples/basic-data-router/tsconfig.json"] |
| false | css | 85 | ["File","Git"] | ["examples/auth-router-provider/src/index.css","examples/auth/src/index.css","examples/basic-data-router/src/index.css","examples/basic/src/index.css","examples/custom-filter-link/src/index.css","examples/custom-link/src/index.css","examples/custom-query-parsing/src/index.css","examples/data-router/src/index.css","examples/error-boundaries/src/index.css"] |
| false | gitignore | 83 | ["File","Git"] | [".gitignore","examples/auth-router-provider/.gitignore","examples/auth/.gitignore","examples/basic-data-router/.gitignore","examples/basic/.gitignore","examples/custom-filter-link/.gitignore","examples/custom-link/.gitignore","examples/custom-query-parsing/.gitignore","examples/data-router/.gitignore"] |
| false | html | 64 | ["File","Git"] | ["examples/auth-router-provider/index.html","examples/auth/index.html","examples/basic-data-router/index.html","examples/basic/index.html","examples/custom-filter-link/index.html","examples/custom-link/index.html","examples/custom-query-parsing/index.html","examples/data-router/index.html","examples/error-boundaries/index.html"] |
| false | ico | 50 | ["File","Git"] | ["playground/performance/public/favicon.ico","integration/helpers/vite-rolldown-template/public/favicon.ico","integration/helpers/vite-8-template/public/favicon.ico","playground/framework-rolldown-vite/public/favicon.ico","playground/framework-vite-6/public/favicon.ico","playground/framework/public/favicon.ico","playground/rsc-vite-7-framework/public/favicon.ico","integration/helpers/rsc-parcel/public/favicon.ico","integration/helpers/rsc-parcel-framework/public/favicon.ico"] |
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
| json | ["File","TS"] | 13 | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-remix-routes-option-adapter/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-serve/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-dom/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-express/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-fs-routes/.reports/jqa/ts-output.json"] |

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
