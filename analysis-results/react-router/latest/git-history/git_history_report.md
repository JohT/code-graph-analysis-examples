---
title: "Git History Report"
generated: "2026-05-25"
model_version: "v4.0.1"
dataset: "react-router-7.15.1"
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
| react-router-7.15.1 | react-router-7.15.1 |  |  | Matt Brophy | github-actions[bot] | Mark Dalgleish | 590 | 1481 | 4958 | 2026-05-07 | 2026-05-14 | 2026-05-14 | 11 | 17 | 10 | fff84b5f20f35c347c9d6313dfc603db0eac6e19 | react-router-7.15.1/typedoc.mjs | 1 | 1 |
| react-router-7.15.1/.agents/skills | .agents/skills | react-router-7.15.1 | react-router-7.15.1 | Matt Brophy | null | null | 1 | 2 | 7 | 2026-05-07 | 2026-05-07 | 2026-05-13 | 12 | 17 | 17 | fadd6c490cc84abc560a2413ee6fa0f2617d098d | react-router-7.15.1/.agents/skills/implement-rfc/SKILL.md | 3 | 2 |
| react-router-7.15.1/.agents/skills/fix-bug | fix-bug | react-router-7.15.1/.agents/skills | skills | Matt Brophy | null | null | 1 | 1 | 5 | 2026-03-18 | 2026-04-14 | 2026-04-14 | 41 | 67 | 40 | a842fca719e81505f454a8e6a8c728cdaed22067 | react-router-7.15.1/.agents/skills/fix-bug/SKILL.md | 4 | 1 |
| react-router-7.15.1/.agents/skills/implement-rfc | implement-rfc | react-router-7.15.1/.agents/skills | skills | Matt Brophy | null | null | 1 | 1 | 2 | 2026-05-07 | 2026-05-07 | 2026-05-13 | 12 | 17 | 17 | fadd6c490cc84abc560a2413ee6fa0f2617d098d | react-router-7.15.1/.agents/skills/implement-rfc/SKILL.md | 4 | 1 |
| react-router-7.15.1/.github | .github | react-router-7.15.1 | react-router-7.15.1 | Matt Brophy | Michael Jackson | Tim Dorr | 21 | 22 | 241 | 2026-04-14 | 2026-04-28 | 2026-04-28 | 27 | 40 | 26 | ff67b74a33c9f13fac28afc4923d0bf5628998ec | react-router-7.15.1/.github/workflows/test.yml | 2 | 1 |
| react-router-7.15.1/.github/ISSUE_TEMPLATE | ISSUE_TEMPLATE | react-router-7.15.1/.github | .github | Matt Brophy | Pedro Cattori | Tim Dorr | 13 | 3 | 50 | 2023-01-11 | 2025-07-16 | 2025-07-16 | 313 | 1229 | 312 | ff67b74a33c9f13fac28afc4923d0bf5628998ec | react-router-7.15.1/.github/ISSUE_TEMPLATE/documentation_isse.yml | 3 | 1 |
| react-router-7.15.1/.github/workflows | workflows | react-router-7.15.1/.github | .github | Matt Brophy | dependabot[bot] | Michael Jackson | 15 | 17 | 205 | 2026-04-14 | 2026-04-28 | 2026-04-28 | 27 | 40 | 26 | fde69511bbfddf5a04e00d8c8bb9a7702a32b9bf | react-router-7.15.1/.github/workflows/test.yml | 3 | 1 |
| react-router-7.15.1/decisions | decisions | react-router-7.15.1 | react-router-7.15.1 | Matt Brophy | Pedro Cattori | Michael Jackson | 9 | 20 | 67 | 2026-02-19 | 2026-05-05 | 2026-05-05 | 20 | 94 | 19 | ff67b74a33c9f13fac28afc4923d0bf5628998ec | react-router-7.15.1/decisions/template.md | 2 | 1 |
| react-router-7.15.1/docs | docs | react-router-7.15.1 | react-router-7.15.1 | Matt Brophy | Remix Run Bot | Ryan Florence | 121 | 197 | 684 | 2026-05-07 | 2026-05-13 | 2026-05-13 | 12 | 17 | 11 | ff6a4fea561d67b1e61002522096797afb9ff55e | react-router-7.15.1/docs/upgrading/v6.md | 2 | 1 |
| react-router-7.15.1/docs/api | api | react-router-7.15.1/docs | docs | Matt Brophy | Remix Run Bot | Brooks Lybrand | 22 | 109 | 189 | 2026-05-07 | 2026-05-13 | 2026-05-13 | 12 | 17 | 11 | fed3b6300c8b8db90d9779a8f9c3304e91d719d3 | react-router-7.15.1/docs/api/utils/resolvePath.md | 3 | 1 |

[Full data](./List_git_file_directories_with_commit_statistics.csv)

### 2.2 Directory Commit Statistics (Charts)



---

## 3. Co-Changed Files

Files committed together = logical coupling signal. May belong to the same conceptual unit or share a concern.

### 3.1 Co-Changed File Pairs

| firstFile | secondFile | commitCount |
| --- | --- | --- |
| react-router-7.15.1/packages/react-router-dom/package.json | react-router-7.15.1/packages/react-router/package.json | 341 |
| react-router-7.15.1/packages/react-router/CHANGELOG.md | react-router-7.15.1/packages/react-router/package.json | 176 |
| react-router-7.15.1/packages/react-router-dom/package.json | react-router-7.15.1/packages/react-router/CHANGELOG.md | 174 |
| react-router-7.15.1/packages/react-router/package.json | react-router-7.15.1/contributors.yml | 90 |
| react-router-7.15.1/packages/react-router-node/CHANGELOG.md | react-router-7.15.1/packages/react-router-serve/CHANGELOG.md | 89 |
| react-router-7.15.1/packages/react-router-dom/package.json | react-router-7.15.1/contributors.yml | 88 |
| react-router-7.15.1/packages/react-router-dev/CHANGELOG.md | react-router-7.15.1/packages/react-router-node/CHANGELOG.md | 87 |
| react-router-7.15.1/packages/react-router-dev/CHANGELOG.md | react-router-7.15.1/packages/react-router-serve/CHANGELOG.md | 87 |
| react-router-7.15.1/packages/react-router/CHANGELOG.md | react-router-7.15.1/contributors.yml | 86 |
| react-router-7.15.1/packages/react-router/lib/components.tsx | react-router-7.15.1/packages/react-router/lib/hooks.tsx | 84 |

### 3.2 Co-Changed File Pairs (All in One Commit)

Files changed together in a single large commit.

| firstFile | secondFile | commitCount |
| --- | --- | --- |
| react-router-7.15.1/packages/react-router-dom/package.json | react-router-7.15.1/packages/react-router/package.json | 581 |
| react-router-7.15.1/packages/react-router/CHANGELOG.md | react-router-7.15.1/packages/react-router/package.json | 412 |
| react-router-7.15.1/packages/react-router-dom/package.json | react-router-7.15.1/packages/react-router/CHANGELOG.md | 409 |
| react-router-7.15.1/packages/react-router-node/CHANGELOG.md | react-router-7.15.1/packages/react-router-serve/CHANGELOG.md | 231 |
| react-router-7.15.1/packages/react-router-dev/CHANGELOG.md | react-router-7.15.1/packages/react-router-node/CHANGELOG.md | 229 |
| react-router-7.15.1/packages/react-router-dev/CHANGELOG.md | react-router-7.15.1/packages/react-router-serve/CHANGELOG.md | 229 |
| react-router-7.15.1/packages/react-router-express/CHANGELOG.md | react-router-7.15.1/packages/react-router-node/CHANGELOG.md | 223 |
| react-router-7.15.1/packages/react-router-express/CHANGELOG.md | react-router-7.15.1/packages/react-router-serve/CHANGELOG.md | 223 |
| react-router-7.15.1/packages/react-router-dev/CHANGELOG.md | react-router-7.15.1/packages/react-router-express/CHANGELOG.md | 221 |
| react-router-7.15.1/packages/react-router-dev/CHANGELOG.md | react-router-7.15.1/packages/react-router/CHANGELOG.md | 218 |

### 3.3 Co-Changed With a Specific File

Shows all files that were changed together with another particular file.

| filePath | commitCount | coChangeRate | maxLift | avgLift |
| --- | --- | --- | --- | --- |
| react-router-7.15.1/packages/react-router-dom/package.json | 344 | 0.00032360450261799807 | 2.831050228310502 | 1.4807287117649792 |
| react-router-7.15.1/contributors.yml | 295 | 0.0003570252894930483 | 2.3114035087719293 | 0.7602788153542583 |
| react-router-7.15.1/packages/react-router/CHANGELOG.md | 216 | 0.0005647546062797575 | 2.49054820415879 | 1.1460441748459123 |
| react-router-7.15.1/packages/react-router/package.json | 176 | 0.0002579272322795931 | 2.6685796269727398 | 1.1807341883842457 |
| react-router-7.15.1/packages/react-router/lib/components.tsx | 162 | 0.0007959827438802685 | 6.533057851239669 | 3.0336389597055327 |
| react-router-7.15.1/packages/react-router/lib/hooks.tsx | 155 | 0.0008969907407407407 | 6.17578125 | 2.736935716314863 |
| react-router-7.15.1/packages/react-router/lib/router/router.ts | 126 | 0.0012016021361815755 | 7.38785046728972 | 2.89288939255852 |
| react-router-7.15.1/packages/react-router/index.ts | 124 | 0.0009815251634556017 | 13.991150442477876 | 2.6039513219101855 |
| react-router-7.15.1/pnpm-lock.yaml | 110 | 0.0009754367296266737 | 6.022857142857143 | 2.181854358570139 |
| react-router-7.15.1/packages/react-router-dev/vite/plugin.ts | 105 | 0.0009241330751628235 | 4.923699781999377 | 2.144189089203039 |

[Full data](./List_git_files_that_were_changed_together_with_another_file.csv)

### 3.4 Co-Changed With a Specific File (All in One)

| filePath | commitCount |
| --- | --- |
| react-router-7.15.1/packages/react-router/package.json | 614 |
| react-router-7.15.1/packages/react-router-dom/package.json | 584 |
| react-router-7.15.1/packages/react-router/CHANGELOG.md | 471 |
| react-router-7.15.1/contributors.yml | 418 |
| react-router-7.15.1/packages/react-router-dev/package.json | 248 |
| react-router-7.15.1/packages/react-router-node/CHANGELOG.md | 232 |
| react-router-7.15.1/packages/react-router-dev/CHANGELOG.md | 232 |
| react-router-7.15.1/packages/react-router-serve/CHANGELOG.md | 231 |
| react-router-7.15.1/packages/react-router-express/CHANGELOG.md | 223 |
| react-router-7.15.1/packages/react-router-cloudflare/CHANGELOG.md | 202 |

### 3.5 Co-Changed Files (Charts)



---

## 4. File Change Distribution

Files changed per commit. High proportion of large commits = low commit granularity.

### 4.1 Files per Commit Distribution

| filesPerCommit | commitCount |
| --- | --- |
| 1 | 4635 |
| 2 | 1795 |
| 3 | 901 |
| 4 | 567 |
| 5 | 472 |
| 6 | 287 |
| 7 | 195 |
| 8 | 161 |
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
| packages/react-router/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 27 | 0.1377551020408163 | 0.008538899430740038 | 0.6249377799900447 | 0.03117782909930716 |
| packages/react-router-cloudflare/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-cloudflare/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-cloudflare/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 27 | 0.1377551020408163 | 0.008538899430740038 | 1.9359183673469387 | 0.06852791878172589 |
| packages/react-router-express/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-express/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-express/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 27 | 0.1377551020408163 | 0.008538899430740038 | 1.9532808639150725 | 0.06887755102040816 |
| packages/react-router-node/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-node/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-node/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 27 | 0.1377551020408163 | 0.008538899430740038 | 1.918861817854895 | 0.06818181818181818 |
| packages/react-router-serve/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-serve/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-serve/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 27 | 0.1377551020408163 | 0.008538899430740038 | 1.9620794263651407 | 0.06905370843989769 |
| packages/react-router-dev/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-dev/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-dev/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 27 | 0.1377551020408163 | 0.008538899430740038 | 1.466604823747681 | 0.05793991416309013 |
| packages/react-router-remix-routes-option-adapter/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-remix-routes-option-adapter/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-remix-routes-option-adapter/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 27 | 0.1377551020408163 | 0.008538899430740038 | 2.104259094942325 | 0.07180851063829788 |
| packages/create-react-router/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/create-react-router/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/create-react-router/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 27 | 0.1377551020408163 | 0.008538899430740038 | 2.007288629737609 | 0.06994818652849741 |
| packages/react-router-dom/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-dom/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-dom/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 27 | 0.1377551020408163 | 0.008538899430740038 | 0.6629857422421022 | 0.03268765133171913 |
| packages/react-router-architect/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-architect/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-architect/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 27 | 0.1377551020408163 | 0.008538899430740038 | 1.9532808639150725 | 0.06887755102040816 |

[Full data](./List_pairwise_changed_files.csv)

### 5.2 Pairwise Changed Files (Top by Lift)

File pairs that co-change more often than random chance (lift > 1).

| fileExtensionPair | firstFileNameShort | secondFileNameShort | updateCommitCount | updateCommitMinConfidence | updateCommitLift | updateCommitJaccardSimilarity | updateCommitSupport | firstFileName | secondFileName |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ts↔ts | vite-dev-custom-entry-test | vite-absolute-base-test | 3 | 1 | 158.1 | 0.15 | 0.0009487666034155598 | integration/vite-dev-custom-entry-test.ts | integration/vite-absolute-base-test.ts |
| ts↔ts | vite-loader-context-test | vite-node-env-test | 4 | 0.8 | 148.8 | 0.2222222222222222 | 0.001265022137887413 | integration/vite-loader-context-test.ts | integration/vite-node-env-test.ts |
| ts↔ts | sessions-test | sessions | 3 | 0.375 | 118.575 | 0.2 | 0.0009487666034155598 | packages/react-router/__tests__/server-runtime/sessions-test.ts | packages/react-router/lib/server-runtime/sessions.ts |
| ts↔ts | remove-exports-test | remove-exports | 4 | 0.36363636363636365 | 104.52892561983471 | 0.2222222222222222 | 0.001265022137887413 | packages/react-router-dev/vite/remove-exports-test.ts | packages/react-router-dev/vite/remove-exports.ts |
| ts↔ts | vite-dotenv-test | vite-node-env-test | 4 | 0.8 | 93.68888888888888 | 0.14285714285714285 | 0.001265022137887413 | integration/vite-dotenv-test.ts | integration/vite-node-env-test.ts |
| ts↔ts | fileStorage | sessions-test | 3 | 0.3 | 86.23636363636363 | 0.16666666666666666 | 0.0009487666034155598 | packages/react-router-node/sessions/fileStorage.ts | packages/react-router-node/__tests__/sessions-test.ts |
| ts↔ts | routes | routes | 3 | 0.75 | 84.69642857142857 | 0.10344827586206896 | 0.0009487666034155598 | packages/react-router-dev/config/routes.ts | packages/react-router-dev/routes.ts |
| ts↔ts | vite-server-bundles-test | vite-node-env-test | 5 | 1 | 75.28571428571429 | 0.11904761904761904 | 0.0015812776723592662 | integration/vite-server-bundles-test.ts | integration/vite-node-env-test.ts |
| ts↔ts | vite-dot-server-test | vite-node-env-test | 5 | 1 | 73.53488372093024 | 0.11627906976744186 | 0.0015812776723592662 | integration/vite-dot-server-test.ts | integration/vite-node-env-test.ts |
| ts↔ts | vite-dot-client-test | vite-dev-custom-entry-test | 3 | 0.42857142857142855 | 67.75714285714287 | 0.125 | 0.0009487666034155598 | integration/vite-dot-client-test.ts | integration/vite-dev-custom-entry-test.ts |

[Full data](./List_pairwise_changed_files_top_lift.csv)

### 5.3 Pairwise Changed Files With Dependencies

Files that are co-changed and also have a structural dependency relationship between them.

| dependencyWeight | fileDistance | commitCount | updateCommitMinConfidence | updateCommitSupport | updateCommitLift | updateCommitJaccardSimilarity |
| --- | --- | --- | --- | --- | --- | --- |
| 11 | 5 | 3 | 0.3 | 0.0009487666034155598 | 4.197345132743363 | 0.012875536480686695 |
| 11 | 4 | 4 | 0.16 | 0.001265022137887413 | 2.23858407079646 | 0.016194331983805668 |
| 22 | 5 | 3 | 0.08108108108108109 | 0.0009487666034155598 | 1.1344176034441522 | 0.011538461538461539 |
| 22 | 5 | 9 | 0.14516129032258066 | 0.0028462998102466793 | 2.0309734513274336 | 0.03225806451612903 |
| 33 | 4 | 8 | 0.06666666666666667 | 0.002530044275774826 | 0.9327433628318584 | 0.023668639053254437 |
| 66 | 4 | 3 | 0.14285714285714285 | 0.0009487666034155598 | 1.9987357774968395 | 0.012295081967213115 |
| 66 | 6 | 3 | 0.16666666666666666 | 0.0009487666034155598 | 6.349397590361446 | 0.030612244897959183 |
| 66 | 4 | 9 | 0.36 | 0.0028462998102466793 | 37.944 | 0.1956521739130435 |
| 91 | 0 | 4 | 0.36363636363636365 | 0.001265022137887413 | 20.532467532467532 | 0.06349206349206349 |
| 91 | 0 | 5 | 0.21739130434782608 | 0.0015812776723592662 | 16.366459627329192 | 0.08333333333333333 |

[Full data](./List_pairwise_changed_files_with_dependencies.csv)

### 5.4 Pairwise Changed Files (Charts)



---

## 6. Files by Author

Per-author file commit stats. Useful for knowledge boundaries and bus-factor risk.

### 6.1 Files with Commit Statistics by Author

| filePath | author | commitCount | commitHashes | lastCommitDate | lastCreationDate | lastModificationDate | daysSinceLastCommit | daysSinceLastCreation | daysSinceLastModification | maxCommitSha |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| react-router-7.15.1/.agents/skills/fix-bug/SKILL.md | Matt Brophy | 5 | ["a842fca719e81505f454a8e6a8c728cdaed22067","06c1149bc0b4f50db0cc6fc10471b4ad963b8969","2469dd6621fbcaec689571c3f003af5711bc54de","1497c6ba52e55158e4f12b54617b1255935c75d5","46321cf2767cb820c1be8bbea3bafbc32c6c4ffd"] | 2026-04-14 | 2026-03-18 | 2026-04-14 | 41 | 67 | 40 | a842fca719e81505f454a8e6a8c728cdaed22067 |
| react-router-7.15.1/.agents/skills/implement-rfc/SKILL.md | Matt Brophy | 2 | ["522bc1b8cd0d7b3565bf9193789f2b7d5503856b","fadd6c490cc84abc560a2413ee6fa0f2617d098d"] | 2026-05-13 | 2026-05-07 | 2026-05-07 | 12 | 17 | 17 | fadd6c490cc84abc560a2413ee6fa0f2617d098d |
| react-router-7.15.1/.browserslistrc | Michael Jackson | 3 | ["82c500c4a1a5d53a608faee25f8322c661b242a1","b3f728487ae6fe7d5ef4ddc759fb2a4ca0df712e","f6df0697e1b2064a2b3a12e8b39577326fdd945b"] | 2021-09-09 | 2018-10-30 | 2021-09-09 | 1719 | 2763 | 1718 | f6df0697e1b2064a2b3a12e8b39577326fdd945b |
| react-router-7.15.1/.browserslistrc | Matt Brophy | 1 | ["4fa24c1b12c7c2ff8f32bb611b8b5b3ac4678c61"] | 2024-03-27 | 2018-10-30 | 2021-09-09 | 789 | 2763 | 1718 | 4fa24c1b12c7c2ff8f32bb611b8b5b3ac4678c61 |
| react-router-7.15.1/.github/FUNDING.yml | Michael Jackson | 1 | ["2679ebc9386c87a53da5c88f606d326ed6bba5bd"] | 2019-10-22 | 2019-10-22 | 2019-10-22 | 2407 | 2406 | 2406 | 2679ebc9386c87a53da5c88f606d326ed6bba5bd |
| react-router-7.15.1/.github/FUNDING.yml | Matt Brophy | 1 | ["4fa24c1b12c7c2ff8f32bb611b8b5b3ac4678c61"] | 2024-03-27 | 2019-10-22 | 2019-10-22 | 789 | 2406 | 2406 | 4fa24c1b12c7c2ff8f32bb611b8b5b3ac4678c61 |
| react-router-7.15.1/.github/ISSUE_TEMPLATE/bug_report.yml | Matt Brophy | 21 | ["5a43e19573c11d1469fd43ef1fddaf7be02abca5","721bee06b9085c57f20c9333cdd327ea81f0376a","09024c8a82932bb8b2f1cd8bf3a08222523c9013","12aa08a8756e5af0fdc2ae4eda0ae061cf713311","7b7498e4b7e1fff895d7aab512d11b57fecbdd37","953948ac3b53ac49fdd8028e10acab2587279355","15ad8d531fae7cd3e2d2038cf3c29595d7812ee1","6585c8396085b75c7674e3dd1bacde3541b0f539","482b6a2902dc346b350a3c2d4fcac4e6048ee0cf","14666ddd78070ffd6149f7e20371927b784eb054","4aa9298ab35483b1e21e357e7574aa3f0d727725","45a7b0e4636f45c910c074e5babb66975e8e8652","c5396bd94aacb97c57a6507b1397e08aa57da972","de0bf8345e6684a671474d992aaff5e7a4040a16","f153b191e1c52bc8fb0e485bfd5d8ec2a8752104","6d945608dc1981a2222cdae5d6a4698602cf852b","ac399b7b388fdf3474c74eecb363502cb4cc8c9e","cc0779ec9af43e3bfd61e09c0c2d0cb30500989f","4fa24c1b12c7c2ff8f32bb611b8b5b3ac4678c61","fdb90690cb74b1060f9e9de550520f30f9c2ef08","0252132bb7352d685609cb5d7b99fe632f731876"] | 2025-07-16 | 2021-11-05 | 2025-07-16 | 313 | 1661 | 312 | fdb90690cb74b1060f9e9de550520f30f9c2ef08 |
| react-router-7.15.1/.github/ISSUE_TEMPLATE/bug_report.yml | Pedro Cattori | 9 | ["c6c8c3bfe4bce8ce53e61cee5542d88363593a93","f8c9a71581711d7f839fb3d76279a3cc2ed69b6f","4e989f839a6af67a6f339f7726fd0ca58c93689a","b5f2e295f2e857edbfd15da236fd9497f1ec13b6","d2710f8b0e8f17063c0fac9f1fbeeee4e0342479","6f313ec32d3078ea4b4e93fa3522325b6a979deb","eb8be394f4897f0545fa70fe4b0d9c38dc877b85","d20ba30b1bfb5ea3b96c20af102dc54c8cd8b3b3","acf3f77a3076b55214e8985f7dc758535ac07c5e"] | 2025-06-03 | 2021-11-05 | 2025-07-16 | 356 | 1661 | 312 | f8c9a71581711d7f839fb3d76279a3cc2ed69b6f |
| react-router-7.15.1/.github/ISSUE_TEMPLATE/bug_report.yml | Tim Dorr | 3 | ["2375e7956873a311edf8985714e104cdbc0ecb80","129b49aa293f2c084d1c455b4c6f1a87ac4ec552","c299d29c7eeb1b3fc3c1726a5d6ebebdfb74ea4a"] | 2022-03-17 | 2021-11-05 | 2025-07-16 | 1530 | 1661 | 312 | c299d29c7eeb1b3fc3c1726a5d6ebebdfb74ea4a |
| react-router-7.15.1/.github/ISSUE_TEMPLATE/bug_report.yml | Chance Strickland | 2 | ["91a52f822d292c4ef017e6c252b32b9ebd57c9c2","0079767bcc93ae543b5c2511f6c6f5f5b8c22f7c"] | 2023-01-13 | 2021-11-05 | 2025-07-16 | 1228 | 1661 | 312 | 91a52f822d292c4ef017e6c252b32b9ebd57c9c2 |

[Full data](./List_git_files_with_commit_statistics_by_author.csv)

---

## 7. Data Quality

Files in git log that are unresolved (not found in codebase) or ambiguous (multiple matches). Affects reliability of co-change metrics.

### 7.1 File Resolution Summary

Resolved vs. ambiguous vs. unresolved files by extension.

| resolved | extension | gitFileCount | fileLabels | gitFileExamples |
| --- | --- | --- | --- | --- |
| false | md | 1848 | ["File","Git"] | ["CHANGELOG.md","packages/create-react-router/CHANGELOG.md","packages/react-router-architect/CHANGELOG.md","packages/react-router-cloudflare/CHANGELOG.md","packages/react-router-dev/.changes/patch.fix-basename-app-directory-conflict.md","packages/react-router-dev/CHANGELOG.md","packages/react-router-dom/CHANGELOG.md","packages/react-router-express/CHANGELOG.md","packages/react-router-fs-routes/CHANGELOG.md"] |
| false | js | 1744 | ["File","Git"] | ["scripts/utils.js","scripts/publish.js","scripts/version.js","scripts/find-release-from-changeset.js","packages/react-router/.eslintrc.js","packages/react-router/lib/dom/node-main.js","packages/react-router/lib/server-runtime/.eslintrc.js","packages/react-router/node-main-dom-export.js","packages/react-router/node-main.js"] |
| false | ts | 1122 | ["File","Git"] | ["scripts/utils/git.ts","examples/data-router/src/todos.ts","integration/client-data-test.ts","integration/defer-test.ts","integration/helpers/vite.ts","integration/http-test.ts","integration/passthrough-requests-test.ts","integration/vite-basename-test.ts","packages/react-router/__tests__/router/fetchers-test.ts"] |
| false | tsx | 488 | ["File","Git"] | ["packages/react-router/__tests__/dom/client-on-error-test.tsx","packages/react-router/lib/components.tsx","packages/react-router/lib/hooks.tsx","packages/react-router/lib/dom/lib.tsx","examples/auth-router-provider/src/App.tsx","integration/helpers/rsc-vite/src/entry.rsc.tsx","packages/react-router/__tests__/dom/data-browser-router-test.tsx","packages/react-router/__tests__/dom/nav-link-active-test.tsx","packages/react-router/__tests__/dom/special-characters-test.tsx"] |
| false | json | 249 | ["File","Git"] | ["integration/helpers/cloudflare-dev-proxy-template/tsconfig.json","integration/helpers/rsc-vite-framework/tsconfig.json","playground/rsc-vite-framework/tsconfig.json",".changeset/config.json","playground/performance/public/.well-known/appspecific/com.chrome.devtools.json","playground/performance/tsconfig.json","scripts/tsconfig.json","integration/helpers/vite-rolldown-template/package.json","integration/helpers/vite-8-template/tsconfig.json"] |
| false | css | 85 | ["File","Git"] | ["playground/rsc-vite-7-framework/app/root.css","playground/rsc-vite-7-framework/app/routes/_index/styles.css","playground/rsc-vite-7-framework/app/routes/client-loader-hydrate/styles.module.css","playground/rsc-vite-7-framework/app/routes/client-loader-without-server-loader/styles.module.css","playground/rsc-vite-7-framework/app/routes/client-loader/styles.module.css","playground/rsc-vite-7-framework/app/routes/mdx-glob.$post/posts/hello/hello-component.module.css","playground/rsc-vite-7-framework/app/routes/mdx-glob.$post/posts/world/world-component.module.css","playground/rsc-vite-7-framework/app/routes/server-loader/styles.module.css","examples/modal-data-router/src/index.css"] |
| false | gitignore | 83 | ["File","Git"] | ["playground/performance/.gitignore","integration/helpers/vite-rolldown-template/.gitignore","integration/helpers/vite-8-template/.gitignore","playground/framework-rolldown-vite/.gitignore","playground/framework-vite-6/.gitignore","playground/framework/.gitignore","playground/rsc-vite-7-framework/.gitignore",".gitignore","examples/modal-data-router/.gitignore"] |
| false | html | 64 | ["File","Git"] | ["examples/modal-data-router/index.html","playground/data/index.html","examples/auth-router-provider/index.html","examples/auth/index.html","examples/basic-data-router/index.html","examples/basic/index.html","examples/custom-filter-link/index.html","examples/custom-link/index.html","examples/custom-query-parsing/index.html"] |
| false | ico | 50 | ["File","Git"] | ["playground/performance/public/favicon.ico","integration/helpers/vite-rolldown-template/public/favicon.ico","integration/helpers/vite-8-template/public/favicon.ico","playground/framework-rolldown-vite/public/favicon.ico","playground/framework/public/favicon.ico","playground/framework-vite-6/public/favicon.ico","playground/rsc-vite-7-framework/public/favicon.ico","integration/helpers/rsc-parcel/public/favicon.ico","integration/helpers/rsc-parcel-framework/public/favicon.ico"] |
| false | yml | 39 | ["File","Git"] | [".github/workflows/release.yml","contributors.yml",".github/workflows/release-comments.yml",".github/workflows/changes-file.yml",".github/workflows/close-no-repro-issues.yml",".github/workflows/deduplicate-lock-file.yml",".github/workflows/delete-changeset-bot-comments.yml",".github/workflows/docs.yml",".github/workflows/format.yml"] |

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
| json | ["File","TS"] | 13 | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.15.1/./source/react-router-7.15.1/packages/create-react-router/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.15.1/./source/react-router-7.15.1/packages/create-react-router/__tests__/fixtures/blank/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.15.1/./source/react-router-7.15.1/packages/create-react-router/__tests__/fixtures/with-ignored-dir/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.15.1/./source/react-router-7.15.1/packages/react-router-architect/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.15.1/./source/react-router-7.15.1/packages/react-router-express/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.15.1/./source/react-router-7.15.1/packages/react-router-node/.reports/jqa/ts-output.json"] |

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
