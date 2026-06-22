---
title: "Git History Report"
generated: "2026-06-22"
model_version: "v4.0.1"
dataset: "react-router-7.17.0"
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
| react-router-7.17.0 | react-router-7.17.0 |  |  | Matt Brophy | github-actions[bot] | Mark Dalgleish | 595 | 1174 | 4882 | 2026-06-01 | 2026-06-04 | 2026-06-04 | 18 | 20 | 17 | fff84b5f20f35c347c9d6313dfc603db0eac6e19 | react-router-7.17.0/typedoc.mjs | 1 | 1 |
| react-router-7.17.0/.agents/skills | .agents/skills | react-router-7.17.0 | react-router-7.17.0 | Matt Brophy | Brooks Lybrand | null | 2 | 2 | 10 | 2026-05-07 | 2026-06-04 | 2026-06-04 | 18 | 45 | 17 | fadd6c490cc84abc560a2413ee6fa0f2617d098d | react-router-7.17.0/.agents/skills/implement-rfc/SKILL.md | 3 | 2 |
| react-router-7.17.0/.agents/skills/fix-bug | fix-bug | react-router-7.17.0/.agents/skills | skills | Matt Brophy | Brooks Lybrand | null | 2 | 1 | 7 | 2026-03-18 | 2026-06-04 | 2026-06-04 | 18 | 95 | 17 | a842fca719e81505f454a8e6a8c728cdaed22067 | react-router-7.17.0/.agents/skills/fix-bug/SKILL.md | 4 | 1 |
| react-router-7.17.0/.agents/skills/implement-rfc | implement-rfc | react-router-7.17.0/.agents/skills | skills | Matt Brophy | null | null | 1 | 1 | 3 | 2026-05-07 | 2026-05-07 | 2026-05-14 | 39 | 45 | 45 | fadd6c490cc84abc560a2413ee6fa0f2617d098d | react-router-7.17.0/.agents/skills/implement-rfc/SKILL.md | 4 | 1 |
| react-router-7.17.0/.github | .github | react-router-7.17.0 | react-router-7.17.0 | Matt Brophy | Michael Jackson | Michaël De Boey | 21 | 19 | 217 | 2026-05-26 | 2026-05-28 | 2026-05-28 | 25 | 26 | 24 | ff67b74a33c9f13fac28afc4923d0bf5628998ec | react-router-7.17.0/.github/workflows/test.yml | 2 | 1 |
| react-router-7.17.0/.github/ISSUE_TEMPLATE | ISSUE_TEMPLATE | react-router-7.17.0/.github | .github | Matt Brophy | Pedro Cattori | Tim Dorr | 13 | 3 | 50 | 2023-01-11 | 2025-07-16 | 2025-07-16 | 341 | 1257 | 340 | ff67b74a33c9f13fac28afc4923d0bf5628998ec | react-router-7.17.0/.github/ISSUE_TEMPLATE/documentation_isse.yml | 3 | 1 |
| react-router-7.17.0/.github/workflows | workflows | react-router-7.17.0/.github | .github | Matt Brophy | dependabot[bot] | Michael Jackson | 15 | 14 | 178 | 2026-05-26 | 2026-05-28 | 2026-05-28 | 25 | 26 | 24 | ff4c0712f7b24d38f51f7b967d7c31aeac531bed | react-router-7.17.0/.github/workflows/test.yml | 3 | 1 |
| react-router-7.17.0/decisions | decisions | react-router-7.17.0 | react-router-7.17.0 | Matt Brophy | Pedro Cattori | Michael Jackson | 10 | 20 | 69 | 2026-02-19 | 2026-06-04 | 2026-06-04 | 18 | 122 | 17 | ff67b74a33c9f13fac28afc4923d0bf5628998ec | react-router-7.17.0/decisions/template.md | 2 | 1 |
| react-router-7.17.0/docs | docs | react-router-7.17.0 | react-router-7.17.0 | Matt Brophy | Remix Run Bot | Ryan Florence | 122 | 197 | 695 | 2026-05-07 | 2026-06-04 | 2026-06-04 | 18 | 45 | 17 | ff6a4fea561d67b1e61002522096797afb9ff55e | react-router-7.17.0/docs/upgrading/v6.md | 2 | 1 |
| react-router-7.17.0/docs/api | api | react-router-7.17.0/docs | docs | Matt Brophy | Remix Run Bot | Brooks Lybrand | 23 | 109 | 196 | 2026-05-07 | 2026-06-04 | 2026-06-04 | 18 | 45 | 17 | fed3b6300c8b8db90d9779a8f9c3304e91d719d3 | react-router-7.17.0/docs/api/utils/resolvePath.md | 3 | 1 |

[Full data](./List_git_file_directories_with_commit_statistics.csv)

### 2.2 Directory Commit Statistics (Charts)



---

## 3. Co-Changed Files

Files committed together = logical coupling signal. May belong to the same conceptual unit or share a concern.

### 3.1 Co-Changed File Pairs

| firstFile | secondFile | commitCount |
| --- | --- | --- |
| react-router-7.17.0/packages/react-router-dom/package.json | react-router-7.17.0/packages/react-router/package.json | 349 |
| react-router-7.17.0/packages/react-router/CHANGELOG.md | react-router-7.17.0/packages/react-router/package.json | 180 |
| react-router-7.17.0/packages/react-router-dom/package.json | react-router-7.17.0/packages/react-router/CHANGELOG.md | 178 |
| react-router-7.17.0/packages/react-router/package.json | react-router-7.17.0/contributors.yml | 93 |
| react-router-7.17.0/packages/react-router-dom/package.json | react-router-7.17.0/contributors.yml | 91 |
| react-router-7.17.0/packages/react-router/lib/components.tsx | react-router-7.17.0/packages/react-router/lib/hooks.tsx | 90 |
| react-router-7.17.0/packages/react-router-node/CHANGELOG.md | react-router-7.17.0/packages/react-router-serve/CHANGELOG.md | 87 |
| react-router-7.17.0/packages/react-router-dev/CHANGELOG.md | react-router-7.17.0/packages/react-router-node/CHANGELOG.md | 87 |
| react-router-7.17.0/packages/react-router/CHANGELOG.md | react-router-7.17.0/contributors.yml | 86 |
| react-router-7.17.0/packages/react-router-dev/CHANGELOG.md | react-router-7.17.0/packages/react-router-serve/CHANGELOG.md | 85 |

### 3.2 Co-Changed File Pairs (All in One Commit)

Files changed together in a single large commit.

| firstFile | secondFile | commitCount |
| --- | --- | --- |
| react-router-7.17.0/packages/react-router-dom/package.json | react-router-7.17.0/packages/react-router/package.json | 598 |
| react-router-7.17.0/packages/react-router/CHANGELOG.md | react-router-7.17.0/packages/react-router/package.json | 424 |
| react-router-7.17.0/packages/react-router-dom/package.json | react-router-7.17.0/packages/react-router/CHANGELOG.md | 421 |
| react-router-7.17.0/packages/react-router-node/CHANGELOG.md | react-router-7.17.0/packages/react-router-serve/CHANGELOG.md | 235 |
| react-router-7.17.0/packages/react-router-dev/CHANGELOG.md | react-router-7.17.0/packages/react-router-node/CHANGELOG.md | 235 |
| react-router-7.17.0/packages/react-router-dev/CHANGELOG.md | react-router-7.17.0/packages/react-router-serve/CHANGELOG.md | 233 |
| react-router-7.17.0/packages/react-router-express/CHANGELOG.md | react-router-7.17.0/packages/react-router-node/CHANGELOG.md | 229 |
| react-router-7.17.0/packages/react-router-express/CHANGELOG.md | react-router-7.17.0/packages/react-router-serve/CHANGELOG.md | 227 |
| react-router-7.17.0/packages/react-router-dev/CHANGELOG.md | react-router-7.17.0/packages/react-router-express/CHANGELOG.md | 227 |
| react-router-7.17.0/packages/react-router-dev/CHANGELOG.md | react-router-7.17.0/packages/react-router/CHANGELOG.md | 226 |

### 3.3 Co-Changed With a Specific File

Shows all files that were changed together with another particular file.

| filePath | commitCount | coChangeRate | maxLift | avgLift |
| --- | --- | --- | --- | --- |
| react-router-7.17.0/packages/react-router-dom/package.json | 351 | 0.0005787495053423031 | 2.3069396896496563 | 1.4201920949881344 |
| react-router-7.17.0/packages/react-router/CHANGELOG.md | 183 | 0.0012763820497440261 | 1.467966683772155 | 1.1661858257319553 |
| react-router-7.17.0/packages/react-router/lib/components.tsx | 170 | 0.0006910569105691057 | 6.298780487804878 | 2.6863206877382853 |
| react-router-7.17.0/packages/react-router/lib/hooks.tsx | 168 | 0.0008616842850328517 | 6.068710089399744 | 2.507796868122065 |
| react-router-7.17.0/pnpm-lock.yaml | 148 | 0.0008214008214008214 | 5.902857142857143 | 1.6528267152547893 |
| react-router-7.17.0/packages/react-router/index.ts | 138 | 0.0010081749841102856 | 9.101321585903083 | 2.263558931257244 |
| react-router-7.17.0/packages/react-router/lib/router/router.ts | 126 | 0.0012346404844494091 | 7.075342465753426 | 2.472573538193864 |
| react-router-7.17.0/packages/react-router-dev/vite/plugin.ts | 121 | 0.0007971014492753623 | 4.240042566129522 | 1.7089803110496067 |
| react-router-7.17.0/packages/react-router/package.json | 93 | 0.0014184397163120568 | 0.44195054629097186 | 0.44195054629097186 |
| react-router-7.17.0/packages/react-router-dev/CHANGELOG.md | 92 | 0.0005277408104263228 | 3.4146814088681183 | 2.0795880811592116 |

[Full data](./List_git_files_that_were_changed_together_with_another_file.csv)

### 3.4 Co-Changed With a Specific File (All in One)

| filePath | commitCount |
| --- | --- |
| react-router-7.17.0/packages/react-router/package.json | 632 |
| react-router-7.17.0/packages/react-router-dom/package.json | 603 |
| react-router-7.17.0/packages/react-router/CHANGELOG.md | 486 |
| react-router-7.17.0/contributors.yml | 430 |
| react-router-7.17.0/packages/react-router-dev/package.json | 253 |
| react-router-7.17.0/packages/react-router-dev/CHANGELOG.md | 240 |
| react-router-7.17.0/packages/react-router-node/CHANGELOG.md | 238 |
| react-router-7.17.0/packages/react-router-serve/CHANGELOG.md | 235 |
| react-router-7.17.0/packages/react-router-express/CHANGELOG.md | 229 |
| react-router-7.17.0/packages/react-router-architect/CHANGELOG.md | 206 |

### 3.5 Co-Changed Files (Charts)



---

## 4. File Change Distribution

Files changed per commit. High proportion of large commits = low commit granularity.

### 4.1 Files per Commit Distribution

| filesPerCommit | commitCount |
| --- | --- |
| 1 | 4655 |
| 2 | 1799 |
| 3 | 909 |
| 4 | 575 |
| 5 | 476 |
| 6 | 287 |
| 7 | 196 |
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
| integration/CHANGELOG.md | packages/create-react-router/CHANGELOG.md | CHANGELOG<br>CHANGELOG | integration/CHANGELOG.md<br>packages/create-react-router/CHANGELOG.md | CHANGELOG↔CHANGELOG | integration/CHANGELOG.md↔packages/create-react-router/CHANGELOG.md | md | md | md↔md | 6 | 0.061855670103092786 | 0.001936108422071636 | 0.9489639685618046 | 0.020477815699658702 |
| packages/react-router-express/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-express/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-express/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 26 | 0.12871287128712872 | 0.008389803162310423 | 1.7418392494271262 | 0.06419753086419754 |
| packages/react-router-dev/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-dev/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-dev/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 26 | 0.12871287128712872 | 0.008389803162310423 | 1.3164395647485543 | 0.054279749478079335 |
| packages/create-react-router/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/create-react-router/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/create-react-router/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 26 | 0.12871287128712872 | 0.008389803162310423 | 1.7887048794565557 | 0.06516290726817042 |
| packages/react-router-remix-routes-option-adapter/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-remix-routes-option-adapter/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-remix-routes-option-adapter/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 26 | 0.12871287128712872 | 0.008389803162310423 | 1.8726816343606194 | 0.06683804627249357 |
| packages/react-router-cloudflare/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-cloudflare/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-cloudflare/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 26 | 0.12871287128712872 | 0.008389803162310423 | 1.726758390124727 | 0.06388206388206388 |
| packages/react-router-dom/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-dom/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-dom/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 26 | 0.12871287128712872 | 0.008389803162310423 | 0.5998213355170104 | 0.030915576694411414 |
| packages/react-router-serve/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-serve/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-serve/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 26 | 0.12871287128712872 | 0.008389803162310423 | 1.749478895257947 | 0.06435643564356436 |
| packages/react-router-architect/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-architect/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-architect/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 26 | 0.12871287128712872 | 0.008389803162310423 | 1.7418392494271262 | 0.06419753086419754 |
| packages/react-router-fs-routes/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-fs-routes/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-fs-routes/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 26 | 0.12871287128712872 | 0.008389803162310423 | 1.7887048794565557 | 0.06516290726817042 |

[Full data](./List_pairwise_changed_files.csv)

### 5.2 Pairwise Changed Files (Top by Lift)

File pairs that co-change more often than random chance (lift > 1).

| fileExtensionPair | firstFileNameShort | secondFileNameShort | updateCommitCount | updateCommitMinConfidence | updateCommitLift | updateCommitJaccardSimilarity | updateCommitSupport | firstFileName | secondFileName |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ts↔ts | vite-dev-custom-entry-test | vite-absolute-base-test | 3 | 1 | 154.95000000000002 | 0.15 | 0.000968054211035818 | integration/vite-dev-custom-entry-test.ts | integration/vite-absolute-base-test.ts |
| ts↔ts | vite-loader-context-test | vite-node-env-test | 4 | 0.8 | 145.83529411764707 | 0.2222222222222222 | 0.0012907389480477573 | integration/vite-loader-context-test.ts | integration/vite-node-env-test.ts |
| ts↔ts | sessions-test | sessions | 3 | 0.375 | 116.2125 | 0.2 | 0.000968054211035818 | packages/react-router/__tests__/server-runtime/sessions-test.ts | packages/react-router/lib/server-runtime/sessions.ts |
| ts↔ts | remove-exports-test | remove-exports | 4 | 0.36363636363636365 | 102.44628099173553 | 0.2222222222222222 | 0.0012907389480477573 | packages/react-router-dev/vite/remove-exports-test.ts | packages/react-router-dev/vite/remove-exports.ts |
| ts↔ts | vite-dotenv-test | vite-node-env-test | 4 | 0.8 | 91.82222222222222 | 0.14285714285714285 | 0.0012907389480477573 | integration/vite-dotenv-test.ts | integration/vite-node-env-test.ts |
| ts↔ts | fileStorage | sessions-test | 3 | 0.3 | 84.51818181818182 | 0.16666666666666666 | 0.000968054211035818 | packages/react-router-node/sessions/fileStorage.ts | packages/react-router-node/__tests__/sessions-test.ts |
| ts↔ts | routes | routes | 3 | 0.75 | 80.14655172413794 | 0.1 | 0.000968054211035818 | packages/react-router-dev/config/routes.ts | packages/react-router-dev/routes.ts |
| ts↔ts | vite-server-bundles-test | vite-node-env-test | 5 | 1 | 73.78571428571429 | 0.11904761904761904 | 0.0016134236850596966 | integration/vite-server-bundles-test.ts | integration/vite-node-env-test.ts |
| ts↔ts | vite-dot-server-test | vite-node-env-test | 5 | 1 | 72.06976744186046 | 0.11627906976744186 | 0.0016134236850596966 | integration/vite-dot-server-test.ts | integration/vite-node-env-test.ts |
| ts↔ts | vite-dot-client-test | vite-dev-custom-entry-test | 3 | 0.42857142857142855 | 66.40714285714287 | 0.125 | 0.000968054211035818 | integration/vite-dot-client-test.ts | integration/vite-dev-custom-entry-test.ts |

[Full data](./List_pairwise_changed_files_top_lift.csv)

### 5.3 Pairwise Changed Files With Dependencies

Files that are co-changed and also have a structural dependency relationship between them.

| dependencyWeight | fileDistance | commitCount | updateCommitMinConfidence | updateCommitSupport | updateCommitLift | updateCommitJaccardSimilarity |
| --- | --- | --- | --- | --- | --- | --- |
| 5 | 5 | 3 | 0.2727272727272727 | 0.000968054211035818 | 3.7232679215058067 | 0.01276595744680851 |
| 5 | 4 | 4 | 0.16 | 0.0012907389480477573 | 2.1843171806167403 | 0.016129032258064516 |
| 10 | 5 | 3 | 0.075 | 0.000968054211035818 | 1.023898678414097 | 0.011363636363636364 |
| 10 | 5 | 9 | 0.14516129032258066 | 0.002904162633107454 | 1.9817393775756715 | 0.03214285714285714 |
| 15 | 6 | 3 | 0.15789473684210525 | 0.000968054211035818 | 5.825187969924812 | 0.03 |
| 15 | 4 | 8 | 0.06451612903225806 | 0.0025814778960955146 | 0.8807730567002985 | 0.023323615160349854 |
| 15 | 4 | 9 | 0.36 | 0.002904162633107454 | 37.188 | 0.1956521739130435 |
| 30 | 4 | 3 | 0.13636363636363635 | 0.000968054211035818 | 1.8616339607529033 | 0.012195121951219513 |
| 30 | 5 | 3 | 0.075 | 0.000968054211035818 | 1.0613013698630138 | 0.01171875 |
| 30 | 0 | 9 | 0.36 | 0.002904162633107454 | 8.99709677419355 | 0.06428571428571428 |

[Full data](./List_pairwise_changed_files_with_dependencies.csv)

### 5.4 Pairwise Changed Files (Charts)



---

## 6. Files by Author

Per-author file commit stats. Useful for knowledge boundaries and bus-factor risk.

### 6.1 Files with Commit Statistics by Author

| filePath | author | commitCount | commitHashes | lastCommitDate | lastCreationDate | lastModificationDate | daysSinceLastCommit | daysSinceLastCreation | daysSinceLastModification | maxCommitSha |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| react-router-7.17.0/.agents/skills/fix-bug/SKILL.md | Matt Brophy | 6 | ["2469dd6621fbcaec689571c3f003af5711bc54de","06c1149bc0b4f50db0cc6fc10471b4ad963b8969","a842fca719e81505f454a8e6a8c728cdaed22067","46321cf2767cb820c1be8bbea3bafbc32c6c4ffd","1497c6ba52e55158e4f12b54617b1255935c75d5","963affeb924f2256bd20c0c5c87e4c4b4fcbd188"] | 2026-06-04 | 2026-03-18 | 2026-06-04 | 18 | 95 | 17 | a842fca719e81505f454a8e6a8c728cdaed22067 |
| react-router-7.17.0/.agents/skills/fix-bug/SKILL.md | Brooks Lybrand | 1 | ["4f8fff6cdb31c549fd011ac516fad5ad2e641b5f"] | 2026-05-29 | 2026-03-18 | 2026-06-04 | 24 | 95 | 17 | 4f8fff6cdb31c549fd011ac516fad5ad2e641b5f |
| react-router-7.17.0/.agents/skills/implement-rfc/SKILL.md | Matt Brophy | 3 | ["522bc1b8cd0d7b3565bf9193789f2b7d5503856b","fadd6c490cc84abc560a2413ee6fa0f2617d098d","a6ab746a43675332ec3c190b1390724bf5c833db"] | 2026-05-14 | 2026-05-07 | 2026-05-07 | 39 | 45 | 45 | fadd6c490cc84abc560a2413ee6fa0f2617d098d |
| react-router-7.17.0/.browserslistrc | Michael Jackson | 3 | ["82c500c4a1a5d53a608faee25f8322c661b242a1","b3f728487ae6fe7d5ef4ddc759fb2a4ca0df712e","f6df0697e1b2064a2b3a12e8b39577326fdd945b"] | 2021-09-09 | 2018-10-30 | 2021-09-09 | 1747 | 2791 | 1746 | f6df0697e1b2064a2b3a12e8b39577326fdd945b |
| react-router-7.17.0/.browserslistrc | Matt Brophy | 1 | ["4fa24c1b12c7c2ff8f32bb611b8b5b3ac4678c61"] | 2024-03-27 | 2018-10-30 | 2021-09-09 | 817 | 2791 | 1746 | 4fa24c1b12c7c2ff8f32bb611b8b5b3ac4678c61 |
| react-router-7.17.0/.github/FUNDING.yml | Michael Jackson | 1 | ["2679ebc9386c87a53da5c88f606d326ed6bba5bd"] | 2019-10-22 | 2019-10-22 | 2019-10-22 | 2435 | 2435 | 2435 | 2679ebc9386c87a53da5c88f606d326ed6bba5bd |
| react-router-7.17.0/.github/FUNDING.yml | Matt Brophy | 1 | ["4fa24c1b12c7c2ff8f32bb611b8b5b3ac4678c61"] | 2024-03-27 | 2019-10-22 | 2019-10-22 | 817 | 2435 | 2435 | 4fa24c1b12c7c2ff8f32bb611b8b5b3ac4678c61 |
| react-router-7.17.0/.github/ISSUE_TEMPLATE/bug_report.yml | Matt Brophy | 21 | ["5a43e19573c11d1469fd43ef1fddaf7be02abca5","721bee06b9085c57f20c9333cdd327ea81f0376a","12aa08a8756e5af0fdc2ae4eda0ae061cf713311","09024c8a82932bb8b2f1cd8bf3a08222523c9013","6585c8396085b75c7674e3dd1bacde3541b0f539","482b6a2902dc346b350a3c2d4fcac4e6048ee0cf","7b7498e4b7e1fff895d7aab512d11b57fecbdd37","953948ac3b53ac49fdd8028e10acab2587279355","15ad8d531fae7cd3e2d2038cf3c29595d7812ee1","14666ddd78070ffd6149f7e20371927b784eb054","f153b191e1c52bc8fb0e485bfd5d8ec2a8752104","4aa9298ab35483b1e21e357e7574aa3f0d727725","6d945608dc1981a2222cdae5d6a4698602cf852b","45a7b0e4636f45c910c074e5babb66975e8e8652","c5396bd94aacb97c57a6507b1397e08aa57da972","de0bf8345e6684a671474d992aaff5e7a4040a16","ac399b7b388fdf3474c74eecb363502cb4cc8c9e","cc0779ec9af43e3bfd61e09c0c2d0cb30500989f","4fa24c1b12c7c2ff8f32bb611b8b5b3ac4678c61","fdb90690cb74b1060f9e9de550520f30f9c2ef08","0252132bb7352d685609cb5d7b99fe632f731876"] | 2025-07-16 | 2021-11-05 | 2025-07-16 | 341 | 1689 | 340 | fdb90690cb74b1060f9e9de550520f30f9c2ef08 |
| react-router-7.17.0/.github/ISSUE_TEMPLATE/bug_report.yml | Pedro Cattori | 9 | ["c6c8c3bfe4bce8ce53e61cee5542d88363593a93","4e989f839a6af67a6f339f7726fd0ca58c93689a","f8c9a71581711d7f839fb3d76279a3cc2ed69b6f","d20ba30b1bfb5ea3b96c20af102dc54c8cd8b3b3","eb8be394f4897f0545fa70fe4b0d9c38dc877b85","b5f2e295f2e857edbfd15da236fd9497f1ec13b6","acf3f77a3076b55214e8985f7dc758535ac07c5e","6f313ec32d3078ea4b4e93fa3522325b6a979deb","d2710f8b0e8f17063c0fac9f1fbeeee4e0342479"] | 2025-06-03 | 2021-11-05 | 2025-07-16 | 384 | 1689 | 340 | f8c9a71581711d7f839fb3d76279a3cc2ed69b6f |
| react-router-7.17.0/.github/ISSUE_TEMPLATE/bug_report.yml | Tim Dorr | 3 | ["129b49aa293f2c084d1c455b4c6f1a87ac4ec552","2375e7956873a311edf8985714e104cdbc0ecb80","c299d29c7eeb1b3fc3c1726a5d6ebebdfb74ea4a"] | 2022-03-17 | 2021-11-05 | 2025-07-16 | 1558 | 1689 | 340 | c299d29c7eeb1b3fc3c1726a5d6ebebdfb74ea4a |

[Full data](./List_git_files_with_commit_statistics_by_author.csv)

---

## 7. Data Quality

Files in git log that are unresolved (not found in codebase) or ambiguous (multiple matches). Affects reliability of co-change metrics.

### 7.1 File Resolution Summary

Resolved vs. ambiguous vs. unresolved files by extension.

| resolved | extension | gitFileCount | fileLabels | gitFileExamples |
| --- | --- | --- | --- | --- |
| false | md | 1862 | ["File","Git"] | ["CHANGELOG.md","packages/create-react-router/CHANGELOG.md","packages/react-router-architect/CHANGELOG.md","packages/react-router-cloudflare/CHANGELOG.md","packages/react-router-dev/.changes/patch.log-future-flags-once.md","packages/react-router-dev/.changes/unstable.rsc-optimize-deps-route-scan.md","packages/react-router-dev/CHANGELOG.md","packages/react-router-dom/CHANGELOG.md","packages/react-router-express/CHANGELOG.md"] |
| false | js | 1744 | ["File","Git"] | ["examples/multi-app/inbox/messages.js","examples/multi-app/server.js","examples/multi-app/vite.config.js","examples/notes/src/notes.js","examples/ssr-data-router/server.js","examples/ssr-data-router/vite.config.js","examples/ssr/server.js","examples/ssr/vite.config.js","scripts/constants.js"] |
| false | ts | 1127 | ["File","Git"] | ["examples/auth-router-provider/src/auth.ts","examples/auth-router-provider/src/vite-env.d.ts","examples/auth-router-provider/vite.config.ts","examples/auth/src/auth.ts","examples/auth/src/vite-env.d.ts","examples/auth/vite.config.ts","examples/basic-data-router/src/vite-env.d.ts","examples/basic-data-router/vite.config.ts","examples/basic/src/vite-env.d.ts"] |
| false | tsx | 488 | ["File","Git"] | ["examples/auth-router-provider/src/App.tsx","examples/auth-router-provider/src/main.tsx","examples/auth/src/App.tsx","examples/auth/src/main.tsx","examples/basic-data-router/src/app.tsx","examples/basic-data-router/src/main.tsx","examples/basic/src/App.tsx","examples/basic/src/main.tsx","examples/custom-filter-link/src/App.tsx"] |
| false | json | 272 | ["File","Git"] | ["examples/auth-router-provider/package-lock.json","examples/auth-router-provider/package.json","examples/auth-router-provider/tsconfig.json","examples/auth/package-lock.json","examples/auth/package.json","examples/auth/tsconfig.json","examples/basic-data-router/package-lock.json","examples/basic-data-router/package.json","examples/basic-data-router/tsconfig.json"] |
| false | css | 85 | ["File","Git"] | ["examples/auth-router-provider/src/index.css","examples/auth/src/index.css","examples/basic-data-router/src/index.css","examples/basic/src/index.css","examples/custom-filter-link/src/index.css","examples/custom-link/src/index.css","examples/custom-query-parsing/src/index.css","examples/data-router/src/index.css","examples/error-boundaries/src/index.css"] |
| false | gitignore | 83 | ["File","Git"] | ["examples/auth-router-provider/.gitignore","examples/auth/.gitignore","examples/basic-data-router/.gitignore","examples/basic/.gitignore","examples/custom-filter-link/.gitignore","examples/custom-link/.gitignore","examples/custom-query-parsing/.gitignore","examples/data-router/.gitignore","examples/error-boundaries/.gitignore"] |
| false | html | 64 | ["File","Git"] | ["examples/auth-router-provider/index.html","examples/auth/index.html","examples/basic-data-router/index.html","examples/basic/index.html","examples/custom-filter-link/index.html","examples/custom-link/index.html","examples/custom-query-parsing/index.html","examples/data-router/index.html","examples/error-boundaries/index.html"] |
| false | ico | 50 | ["File","Git"] | ["playground/performance/public/favicon.ico","integration/helpers/vite-rolldown-template/public/favicon.ico","integration/helpers/vite-8-template/public/favicon.ico","playground/framework-rolldown-vite/public/favicon.ico","playground/framework-vite-6/public/favicon.ico","playground/framework/public/favicon.ico","playground/rsc-vite-7-framework/public/favicon.ico","integration/helpers/rsc-parcel/public/favicon.ico","integration/helpers/rsc-parcel-framework/public/favicon.ico"] |
| false | yml | 44 | ["File","Git"] | ["contributors.yml",".github/workflows/issue-checks.yml",".github/workflows/pr-actions.yml",".github/workflows/pr-checks.yml",".github/workflows/close-no-repro-issue.yml",".github/workflows/support.yml",".github/workflows/close-no-repro-issues.yml",".github/workflows/delete-changeset-bot-comments.yml",".github/workflows/preview.yml"] |

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
| json | ["File","TS"] | 13 | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.17.0/./source/react-router-7.17.0/packages/react-router-serve/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.17.0/./source/react-router-7.17.0/packages/create-react-router/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.17.0/./source/react-router-7.17.0/packages/create-react-router/__tests__/fixtures/with-ignored-dir/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.17.0/./source/react-router-7.17.0/packages/create-react-router/__tests__/fixtures/blank/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.17.0/./source/react-router-7.17.0/packages/react-router-fs-routes/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.17.0/./source/react-router-7.17.0/packages/react-router-dev/.reports/jqa/ts-output.json"] |

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
