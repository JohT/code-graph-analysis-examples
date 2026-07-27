---
title: "Git History Report"
generated: "2026-07-27"
model_version: "v4.0.2"
dataset: "react-router-7.18.1"
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
| react-router-7.18.1 | react-router-7.18.1 |  |  | Matt Brophy | github-actions[bot] | Remix Run Bot | 602 | 1181 | 4915 | 2026-06-16 | 2026-06-29 | 2026-06-29 | 28 | 40 | 27 | fff84b5f20f35c347c9d6313dfc603db0eac6e19 | react-router-7.18.1/typedoc.mjs | 1 | 1 |
| react-router-7.18.1/.agents/skills | .agents/skills | react-router-7.18.1 | react-router-7.18.1 | Matt Brophy | Brooks Lybrand | null | 2 | 7 | 12 | 2026-06-16 | 2026-06-16 | 2026-06-16 | 41 | 40 | 40 | fadd6c490cc84abc560a2413ee6fa0f2617d098d | react-router-7.18.1/.agents/skills/react-router/references/rsc.md | 3 | 2 |
| react-router-7.18.1/.agents/skills/fix-bug | fix-bug | react-router-7.18.1/.agents/skills | skills | Matt Brophy | Brooks Lybrand | null | 2 | 1 | 8 | 2026-03-18 | 2026-06-04 | 2026-06-04 | 53 | 130 | 52 | d6f3a05d4124ae9c1f2f74c599f80d091268ce0c | react-router-7.18.1/.agents/skills/fix-bug/SKILL.md | 4 | 1 |
| react-router-7.18.1/.agents/skills/implement-rfc | implement-rfc | react-router-7.18.1/.agents/skills | skills | Matt Brophy | null | null | 1 | 1 | 4 | 2026-05-07 | 2026-06-04 | 2026-06-04 | 53 | 81 | 52 | fadd6c490cc84abc560a2413ee6fa0f2617d098d | react-router-7.18.1/.agents/skills/implement-rfc/SKILL.md | 4 | 1 |
| react-router-7.18.1/.agents/skills/react-router | react-router | react-router-7.18.1/.agents/skills | skills | Brooks Lybrand | null | null | 1 | 5 | 1 | 2026-06-16 | 2026-06-16 | 2026-06-16 | 41 | 40 | 40 | 8f364c820ef698952e4bed876d6c93c895357692 | react-router-7.18.1/.agents/skills/react-router/references/rsc.md | 4 | 1 |
| react-router-7.18.1/.agents/skills/react-router/references | references | react-router-7.18.1/.agents/skills/react-router | react-router | Brooks Lybrand | null | null | 1 | 4 | 1 | 2026-06-16 | 2026-06-16 | 2026-06-16 | 41 | 40 | 40 | 8f364c820ef698952e4bed876d6c93c895357692 | react-router-7.18.1/.agents/skills/react-router/references/rsc.md | 5 | 1 |
| react-router-7.18.1/.github | .github | react-router-7.18.1 | react-router-7.18.1 | Matt Brophy | Michael Jackson | Michaël De Boey | 22 | 19 | 221 | 2026-05-26 | 2026-06-16 | 2026-06-16 | 41 | 62 | 41 | ff67b74a33c9f13fac28afc4923d0bf5628998ec | react-router-7.18.1/.github/workflows/test.yml | 2 | 1 |
| react-router-7.18.1/.github/ISSUE_TEMPLATE | ISSUE_TEMPLATE | react-router-7.18.1/.github | .github | Matt Brophy | Pedro Cattori | Tim Dorr | 13 | 3 | 51 | 2023-01-11 | 2026-06-04 | 2026-06-04 | 53 | 1292 | 52 | ff67b74a33c9f13fac28afc4923d0bf5628998ec | react-router-7.18.1/.github/ISSUE_TEMPLATE/documentation_isse.yml | 3 | 1 |
| react-router-7.18.1/.github/workflows | workflows | react-router-7.18.1/.github | .github | Matt Brophy | dependabot[bot] | Michael Jackson | 16 | 14 | 182 | 2026-05-26 | 2026-06-16 | 2026-06-16 | 41 | 62 | 41 | ff4c0712f7b24d38f51f7b967d7c31aeac531bed | react-router-7.18.1/.github/workflows/test.yml | 3 | 1 |
| react-router-7.18.1/decisions | decisions | react-router-7.18.1 | react-router-7.18.1 | Matt Brophy | Pedro Cattori | Michael Jackson | 10 | 20 | 69 | 2026-02-19 | 2026-06-04 | 2026-06-04 | 53 | 157 | 53 | ff67b74a33c9f13fac28afc4923d0bf5628998ec | react-router-7.18.1/decisions/template.md | 2 | 1 |

[Full data](./List_git_file_directories_with_commit_statistics.csv)

### 2.2 Directory Commit Statistics (Charts)



---

## 3. Co-Changed Files

Files committed together = logical coupling signal. May belong to the same conceptual unit or share a concern.

### 3.1 Co-Changed File Pairs

| firstFile | secondFile | commitCount |
| --- | --- | --- |
| react-router-7.18.1/packages/react-router-dom/package.json | react-router-7.18.1/packages/react-router/package.json | 351 |
| react-router-7.18.1/packages/react-router/CHANGELOG.md | react-router-7.18.1/packages/react-router/package.json | 182 |
| react-router-7.18.1/packages/react-router-dom/package.json | react-router-7.18.1/packages/react-router/CHANGELOG.md | 180 |
| react-router-7.18.1/packages/react-router/package.json | react-router-7.18.1/contributors.yml | 93 |
| react-router-7.18.1/packages/react-router-dom/package.json | react-router-7.18.1/contributors.yml | 92 |
| react-router-7.18.1/packages/react-router/lib/components.tsx | react-router-7.18.1/packages/react-router/lib/hooks.tsx | 90 |
| react-router-7.18.1/packages/react-router-node/CHANGELOG.md | react-router-7.18.1/packages/react-router-serve/CHANGELOG.md | 89 |
| react-router-7.18.1/packages/react-router-dev/CHANGELOG.md | react-router-7.18.1/packages/react-router-node/CHANGELOG.md | 89 |
| react-router-7.18.1/packages/react-router-dev/CHANGELOG.md | react-router-7.18.1/packages/react-router-serve/CHANGELOG.md | 87 |
| react-router-7.18.1/packages/react-router/CHANGELOG.md | react-router-7.18.1/contributors.yml | 86 |

### 3.2 Co-Changed File Pairs (All in One Commit)

Files changed together in a single large commit.

| firstFile | secondFile | commitCount |
| --- | --- | --- |
| react-router-7.18.1/packages/react-router-dom/package.json | react-router-7.18.1/packages/react-router/package.json | 601 |
| react-router-7.18.1/packages/react-router/CHANGELOG.md | react-router-7.18.1/packages/react-router/package.json | 427 |
| react-router-7.18.1/packages/react-router-dom/package.json | react-router-7.18.1/packages/react-router/CHANGELOG.md | 424 |
| react-router-7.18.1/packages/react-router-dev/CHANGELOG.md | react-router-7.18.1/packages/react-router-node/CHANGELOG.md | 238 |
| react-router-7.18.1/packages/react-router-node/CHANGELOG.md | react-router-7.18.1/packages/react-router-serve/CHANGELOG.md | 238 |
| react-router-7.18.1/packages/react-router-dev/CHANGELOG.md | react-router-7.18.1/packages/react-router-serve/CHANGELOG.md | 236 |
| react-router-7.18.1/packages/react-router-express/CHANGELOG.md | react-router-7.18.1/packages/react-router-node/CHANGELOG.md | 232 |
| react-router-7.18.1/packages/react-router-dev/CHANGELOG.md | react-router-7.18.1/packages/react-router-express/CHANGELOG.md | 231 |
| react-router-7.18.1/packages/react-router-express/CHANGELOG.md | react-router-7.18.1/packages/react-router-serve/CHANGELOG.md | 230 |
| react-router-7.18.1/packages/react-router-dev/CHANGELOG.md | react-router-7.18.1/packages/react-router/CHANGELOG.md | 230 |

### 3.3 Co-Changed With a Specific File

Shows all files that were changed together with another particular file.

| filePath | commitCount | coChangeRate | maxLift | avgLift |
| --- | --- | --- | --- | --- |
| react-router-7.18.1/packages/react-router-dom/package.json | 354 | 0.0004945308243577386 | 2.320969825948165 | 1.3642038215376235 |
| react-router-7.18.1/packages/react-router/CHANGELOG.md | 192 | 0.0008438929838209893 | 1.6150276243093924 | 1.0913500040856614 |
| react-router-7.18.1/packages/react-router/lib/components.tsx | 171 | 0.0007035647279549719 | 6.34008097165992 | 2.720108313909902 |
| react-router-7.18.1/contributors.yml | 152 | 0.0005924193705544188 | 1.1646433493011352 | 0.6855000280774831 |
| react-router-7.18.1/pnpm-lock.yaml | 151 | 0.0007409042957729202 | 5.965714285714285 | 1.549357277017951 |
| react-router-7.18.1/packages/react-router/package.json | 133 | 0.0006411368851352654 | 1.297627118644068 | 0.6769338092771102 |
| react-router-7.18.1/packages/react-router-dev/vite/plugin.ts | 124 | 0.0007628891349821583 | 4.2021466905187825 | 1.66032886192991 |
| react-router-7.18.1/packages/react-router/lib/hooks.tsx | 102 | 0.0022900763358778627 | 5.36719115126967 | 2.82387159928131 |
| react-router-7.18.1/packages/react-router-dev/CHANGELOG.md | 96 | 0.0005136106831022085 | 3.43218085106383 | 2.096345083989764 |
| react-router-7.18.1/packages/react-router-node/CHANGELOG.md | 92 | 0.0009916143913427753 | 3.5556405939078526 | 1.8930597753952887 |

[Full data](./List_git_files_that_were_changed_together_with_another_file.csv)

### 3.4 Co-Changed With a Specific File (All in One)

| filePath | commitCount |
| --- | --- |
| react-router-7.18.1/packages/react-router/package.json | 635 |
| react-router-7.18.1/packages/react-router-dom/package.json | 607 |
| react-router-7.18.1/packages/react-router/CHANGELOG.md | 490 |
| react-router-7.18.1/contributors.yml | 438 |
| react-router-7.18.1/packages/react-router-dev/package.json | 256 |
| react-router-7.18.1/packages/react-router-dev/CHANGELOG.md | 245 |
| react-router-7.18.1/packages/react-router-node/CHANGELOG.md | 241 |
| react-router-7.18.1/packages/react-router-serve/CHANGELOG.md | 238 |
| react-router-7.18.1/packages/react-router-express/CHANGELOG.md | 233 |
| react-router-7.18.1/packages/react-router-architect/CHANGELOG.md | 209 |

### 3.5 Co-Changed Files (Charts)



---

## 4. File Change Distribution

Files changed per commit. High proportion of large commits = low commit granularity.

### 4.1 Files per Commit Distribution

| filesPerCommit | commitCount |
| --- | --- |
| 1 | 4666 |
| 2 | 1806 |
| 3 | 917 |
| 4 | 577 |
| 5 | 476 |
| 6 | 288 |
| 7 | 198 |
| 8 | 164 |
| 9 | 103 |
| 10 | 131 |

[Full data](./List_git_files_per_commit_distribution.csv)

### 4.2 Files per Commit Chart



---

## 5. Pairwise Changed Files

Commit overlap counts and dependency info between file pairs.

### 5.1 Pairwise Changed Files

| firstFileName | secondFileName | filePairLineBreak | filePairWithRelativePathLineBreak | filePair | filePairWithRelativePath | firstFileExtension | secondFileExtension | fileExtensionPair | updateCommitCount | updateCommitMinConfidence | updateCommitSupport | updateCommitLift | updateCommitJaccardSimilarity |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| integration/CHANGELOG.md | packages/create-react-router/CHANGELOG.md | CHANGELOG<br>CHANGELOG | integration/CHANGELOG.md<br>packages/create-react-router/CHANGELOG.md | CHANGELOG↔CHANGELOG | integration/CHANGELOG.md↔packages/create-react-router/CHANGELOG.md | md | md | md↔md | 6 | 0.061855670103092786 | 0.0019157088122605363 | 0.9450339451848125 | 0.02027027027027027 |
| packages/react-router-remix-routes-option-adapter/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-remix-routes-option-adapter/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-remix-routes-option-adapter/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 28 | 0.13658536585365855 | 0.008939974457215836 | 1.9804878048780483 | 0.07124681933842239 |
| packages/react-router-dom/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-dom/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-dom/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 28 | 0.13658536585365855 | 0.008939974457215836 | 0.6394400087498632 | 0.03309692671394799 |
| packages/react-router-dev/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-dev/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-dev/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 28 | 0.13658536585365855 | 0.008939974457215836 | 1.3979913916786226 | 0.057971014492753624 |
| packages/react-router/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 28 | 0.13658536585365855 | 0.008939974457215836 | 0.6042166184373707 | 0.031638418079096044 |
| packages/react-router-node/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-node/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-node/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 28 | 0.13658536585365855 | 0.008939974457215836 | 1.8126498553121122 | 0.06779661016949153 |
| packages/react-router-serve/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-serve/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-serve/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 28 | 0.13658536585365855 | 0.008939974457215836 | 1.8518847006651882 | 0.06862745098039216 |
| packages/react-router-fs-routes/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-fs-routes/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-fs-routes/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 28 | 0.13658536585365855 | 0.008939974457215836 | 1.892855601122383 | 0.06947890818858561 |
| packages/react-router-cloudflare/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-cloudflare/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-cloudflare/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 28 | 0.13658536585365855 | 0.008939974457215836 | 1.8281425891181986 | 0.0681265206812652 |
| packages/react-router-express/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-express/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-express/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 28 | 0.13658536585365855 | 0.008939974457215836 | 1.8439024390243903 | 0.06845965770171149 |

[Full data](./List_pairwise_changed_files.csv)

### 5.2 Pairwise Changed Files (Top by Lift)

File pairs that co-change more often than random chance (lift > 1).

| fileExtensionPair | firstFileNameShort | secondFileNameShort | updateCommitCount | updateCommitMinConfidence | updateCommitLift | updateCommitJaccardSimilarity | updateCommitSupport | firstFileName | secondFileName |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ts↔ts | vite-dev-custom-entry-test | vite-absolute-base-test | 3 | 1 | 156.6 | 0.15 | 0.0009578544061302681 | integration/vite-dev-custom-entry-test.ts | integration/vite-absolute-base-test.ts |
| ts↔ts | vite-loader-context-test | vite-node-env-test | 4 | 0.8 | 147.3882352941176 | 0.2222222222222222 | 0.001277139208173691 | integration/vite-loader-context-test.ts | integration/vite-node-env-test.ts |
| ts↔ts | sessions-test | sessions | 3 | 0.375 | 117.44999999999999 | 0.2 | 0.0009578544061302681 | packages/react-router/__tests__/server-runtime/sessions-test.ts | packages/react-router/lib/server-runtime/sessions.ts |
| ts↔ts | remove-exports-test | remove-exports | 4 | 0.36363636363636365 | 103.53719008264463 | 0.2222222222222222 | 0.001277139208173691 | packages/react-router-dev/vite/remove-exports-test.ts | packages/react-router-dev/vite/remove-exports.ts |
| ts↔ts | vite-dotenv-test | vite-node-env-test | 4 | 0.8 | 92.8 | 0.14285714285714285 | 0.001277139208173691 | integration/vite-dotenv-test.ts | integration/vite-node-env-test.ts |
| ts↔ts | fileStorage | sessions-test | 3 | 0.3 | 85.41818181818181 | 0.16666666666666666 | 0.0009578544061302681 | packages/react-router-node/sessions/fileStorage.ts | packages/react-router-node/__tests__/sessions-test.ts |
| ts↔ts | routes | routes | 3 | 0.75 | 81 | 0.1 | 0.0009578544061302681 | packages/react-router-dev/config/routes.ts | packages/react-router-dev/routes.ts |
| ts↔ts | vite-server-bundles-test | vite-node-env-test | 5 | 1 | 74.57142857142856 | 0.11904761904761904 | 0.0015964240102171138 | integration/vite-server-bundles-test.ts | integration/vite-node-env-test.ts |
| ts↔ts | vite-dot-server-test | vite-node-env-test | 5 | 1 | 72.83720930232558 | 0.11627906976744186 | 0.0015964240102171138 | integration/vite-dot-server-test.ts | integration/vite-node-env-test.ts |
| ts↔ts | vite-dot-client-test | vite-dev-custom-entry-test | 3 | 0.42857142857142855 | 67.11428571428571 | 0.125 | 0.0009578544061302681 | integration/vite-dot-client-test.ts | integration/vite-dev-custom-entry-test.ts |

[Full data](./List_pairwise_changed_files_top_lift.csv)

### 5.3 Pairwise Changed Files With Dependencies

Files that are co-changed and also have a structural dependency relationship between them.

| dependencyWeight | fileDistance | commitCount | updateCommitMinConfidence | updateCommitSupport | updateCommitLift | updateCommitJaccardSimilarity |
| --- | --- | --- | --- | --- | --- | --- |
| 7 | 4 | 4 | 0.16 | 0.001277139208173691 | 2.197894736842105 | 0.01606425702811245 |
| 14 | 5 | 3 | 0.07317073170731707 | 0.0009578544061302681 | 1.005134788189987 | 0.011278195488721804 |
| 14 | 5 | 9 | 0.14285714285714285 | 0.0028735632183908046 | 1.962406015037594 | 0.031914893617021274 |
| 21 | 4 | 9 | 0.0703125 | 0.0028735632183908046 | 0.9658717105263157 | 0.025936599423631124 |
| 28 | 6 | 3 | 0.15 | 0.0009578544061302681 | 5.527058823529412 | 0.029411764705882353 |
| 28 | 4 | 9 | 0.36 | 0.0028735632183908046 | 37.584 | 0.1956521739130435 |
| 42 | 4 | 3 | 0.13636363636363635 | 0.0009578544061302681 | 1.8732057416267942 | 0.012145748987854251 |
| 56 | 0 | 9 | 0.36 | 0.0028735632183908046 | 8.80875 | 0.0625 |
| 70 | 5 | 3 | 0.07317073170731707 | 0.0009578544061302681 | 1.0369716366846926 | 0.011583011583011582 |
| 70 | 3 | 44 | 0.36065573770491804 | 0.0140485312899106 | 4.954270923209663 | 0.1437908496732026 |

[Full data](./List_pairwise_changed_files_with_dependencies.csv)

### 5.4 Pairwise Changed Files (Charts)



---

## 6. Files by Author

Per-author file commit stats. Useful for knowledge boundaries and bus-factor risk.

### 6.1 Files with Commit Statistics by Author

| filePath | author | commitCount | commitHashes | lastCommitDate | lastCreationDate | lastModificationDate | daysSinceLastCommit | daysSinceLastCreation | daysSinceLastModification | maxCommitSha |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| react-router-7.18.1/.agents/skills/fix-bug/SKILL.md | Matt Brophy | 7 | ["2469dd6621fbcaec689571c3f003af5711bc54de","06c1149bc0b4f50db0cc6fc10471b4ad963b8969","a842fca719e81505f454a8e6a8c728cdaed22067","1497c6ba52e55158e4f12b54617b1255935c75d5","46321cf2767cb820c1be8bbea3bafbc32c6c4ffd","d6f3a05d4124ae9c1f2f74c599f80d091268ce0c","963affeb924f2256bd20c0c5c87e4c4b4fcbd188"] | 2026-06-04 | 2026-03-18 | 2026-06-04 | 53 | 130 | 52 | d6f3a05d4124ae9c1f2f74c599f80d091268ce0c |
| react-router-7.18.1/.agents/skills/fix-bug/SKILL.md | Brooks Lybrand | 1 | ["4f8fff6cdb31c549fd011ac516fad5ad2e641b5f"] | 2026-05-29 | 2026-03-18 | 2026-06-04 | 59 | 130 | 52 | 4f8fff6cdb31c549fd011ac516fad5ad2e641b5f |
| react-router-7.18.1/.agents/skills/implement-rfc/SKILL.md | Matt Brophy | 4 | ["fadd6c490cc84abc560a2413ee6fa0f2617d098d","a6ab746a43675332ec3c190b1390724bf5c833db","522bc1b8cd0d7b3565bf9193789f2b7d5503856b","d6f3a05d4124ae9c1f2f74c599f80d091268ce0c"] | 2026-06-04 | 2026-05-07 | 2026-06-04 | 53 | 81 | 52 | fadd6c490cc84abc560a2413ee6fa0f2617d098d |
| react-router-7.18.1/.agents/skills/react-router/SKILL.md | Brooks Lybrand | 1 | ["8f364c820ef698952e4bed876d6c93c895357692"] | 2026-06-16 | 2026-06-16 | 2026-06-16 | 41 | 40 | 40 | 8f364c820ef698952e4bed876d6c93c895357692 |
| react-router-7.18.1/.agents/skills/react-router/references/data-mode.md | Brooks Lybrand | 1 | ["8f364c820ef698952e4bed876d6c93c895357692"] | 2026-06-16 | 2026-06-16 | 2026-06-16 | 41 | 40 | 40 | 8f364c820ef698952e4bed876d6c93c895357692 |
| react-router-7.18.1/.agents/skills/react-router/references/declarative-mode.md | Brooks Lybrand | 1 | ["8f364c820ef698952e4bed876d6c93c895357692"] | 2026-06-16 | 2026-06-16 | 2026-06-16 | 41 | 40 | 40 | 8f364c820ef698952e4bed876d6c93c895357692 |
| react-router-7.18.1/.agents/skills/react-router/references/framework-mode.md | Brooks Lybrand | 1 | ["8f364c820ef698952e4bed876d6c93c895357692"] | 2026-06-16 | 2026-06-16 | 2026-06-16 | 41 | 40 | 40 | 8f364c820ef698952e4bed876d6c93c895357692 |
| react-router-7.18.1/.agents/skills/react-router/references/rsc.md | Brooks Lybrand | 1 | ["8f364c820ef698952e4bed876d6c93c895357692"] | 2026-06-16 | 2026-06-16 | 2026-06-16 | 41 | 40 | 40 | 8f364c820ef698952e4bed876d6c93c895357692 |
| react-router-7.18.1/.browserslistrc | Michael Jackson | 3 | ["82c500c4a1a5d53a608faee25f8322c661b242a1","b3f728487ae6fe7d5ef4ddc759fb2a4ca0df712e","f6df0697e1b2064a2b3a12e8b39577326fdd945b"] | 2021-09-09 | 2018-10-30 | 2021-09-09 | 1782 | 2826 | 1781 | f6df0697e1b2064a2b3a12e8b39577326fdd945b |
| react-router-7.18.1/.browserslistrc | Matt Brophy | 1 | ["4fa24c1b12c7c2ff8f32bb611b8b5b3ac4678c61"] | 2024-03-27 | 2018-10-30 | 2021-09-09 | 852 | 2826 | 1781 | 4fa24c1b12c7c2ff8f32bb611b8b5b3ac4678c61 |

[Full data](./List_git_files_with_commit_statistics_by_author.csv)

---

## 7. Data Quality

Files in git log that are unresolved (not found in codebase) or ambiguous (multiple matches). Affects reliability of co-change metrics.

### 7.1 File Resolution Summary

Resolved vs. ambiguous vs. unresolved files by extension.

| resolved | extension | gitFileCount | fileLabels | gitFileExamples |
| --- | --- | --- | --- | --- |
| false | md | 1881 | ["File","Git"] | ["CHANGELOG.md","packages/create-react-router/CHANGELOG.md","packages/react-router-architect/CHANGELOG.md","packages/react-router-cloudflare/CHANGELOG.md","packages/react-router-dev/CHANGELOG.md","packages/react-router-dom/.changes/patch.main-entry.md","packages/react-router-dom/CHANGELOG.md","packages/react-router-express/CHANGELOG.md","packages/react-router-fs-routes/CHANGELOG.md"] |
| false | js | 1744 | ["File","Git"] | ["examples/multi-app/inbox/messages.js","examples/multi-app/server.js","examples/multi-app/vite.config.js","examples/notes/src/notes.js","examples/ssr-data-router/server.js","examples/ssr-data-router/vite.config.js","examples/ssr/server.js","examples/ssr/vite.config.js","scripts/constants.js"] |
| false | ts | 1131 | ["File","Git"] | ["scripts/docs.ts","scripts/changes/publish.ts","scripts/changes/pr.ts","scripts/utils/github.ts","integration/fog-of-war-test.ts","packages/react-router/__tests__/dom/ssr/fog-of-war-test.ts","packages/react-router/__tests__/rsc/server-test.ts","packages/react-router/__tests__/server-runtime/server-test.ts","packages/react-router-express/__tests__/server-test.ts"] |
| false | tsx | 488 | ["File","Git"] | ["packages/react-router/lib/rsc/browser.tsx","packages/react-router/lib/hooks.tsx","packages/react-router/lib/rsc/server.ssr.tsx","packages/react-router/lib/dom-export/hydrated-router.tsx","packages/react-router/__tests__/dom/data-browser-router-test.tsx","packages/react-router/lib/dom/lib.tsx","packages/react-router/lib/dom/ssr/single-fetch.tsx","packages/react-router/__tests__/resolvePath-test.tsx","packages/react-router/__tests__/useNavigate-test.tsx"] |
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
| json | ["File","TS"] | 13 | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.1/./source/react-router-7.18.1/packages/react-router-node/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.1/./source/react-router-7.18.1/packages/create-react-router/__tests__/fixtures/blank/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.1/./source/react-router-7.18.1/packages/create-react-router/__tests__/fixtures/with-ignored-dir/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.1/./source/react-router-7.18.1/packages/create-react-router/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.1/./source/react-router-7.18.1/packages/react-router-express/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.1/./source/react-router-7.18.1/packages/react-router-dev/.reports/jqa/ts-output.json"] |

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
