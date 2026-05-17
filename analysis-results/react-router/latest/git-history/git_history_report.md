---
title: "Git History Report"
generated: "2026-05-17"
model_version: "v4.0.1"
dataset: "react-router-7.13.2"
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
| react-router-7.13.2 | react-router-7.13.2 |  |  | Matt Brophy | github-actions[bot] | Michael Jackson | 580 | 1395 | 4870 | 2026-03-18 | 2026-03-23 | 2026-03-23 | 55 | 60 | 55 | fff84b5f20f35c347c9d6313dfc603db0eac6e19 | react-router-7.13.2/typedoc.mjs | 1 | 1 |
| react-router-7.13.2/.agents/skills/fix-bug | .agents/skills/fix-bug | react-router-7.13.2 | react-router-7.13.2 | Matt Brophy | null | null | 1 | 1 | 2 | 2026-03-18 | 2026-03-18 | 2026-03-18 | 60 | 60 | 60 | 2469dd6621fbcaec689571c3f003af5711bc54de | react-router-7.13.2/.agents/skills/fix-bug/SKILL.md | 4 | 3 |
| react-router-7.13.2/.changeset | .changeset | react-router-7.13.2 | react-router-7.13.2 | Matt Brophy | Chance Strickland | Michael Jackson | 5 | 2 | 31 | 2022-06-14 | 2024-11-22 | 2024-11-22 | 541 | 1432 | 541 | fd76ac8838c4b98cc6073fa987b6d30b08199c29 | react-router-7.13.2/.changeset/config.json | 2 | 1 |
| react-router-7.13.2/.github | .github | react-router-7.13.2 | react-router-7.13.2 | Matt Brophy | Michael Jackson | Tim Dorr | 21 | 20 | 225 | 2025-12-02 | 2025-12-11 | 2025-12-11 | 157 | 166 | 156 | ff67b74a33c9f13fac28afc4923d0bf5628998ec | react-router-7.13.2/.github/workflows/test.yml | 2 | 1 |
| react-router-7.13.2/.github/ISSUE_TEMPLATE | ISSUE_TEMPLATE | react-router-7.13.2/.github | .github | Matt Brophy | Pedro Cattori | Tim Dorr | 13 | 3 | 50 | 2023-01-11 | 2025-07-16 | 2025-07-16 | 305 | 1221 | 304 | ff67b74a33c9f13fac28afc4923d0bf5628998ec | react-router-7.13.2/.github/ISSUE_TEMPLATE/documentation_isse.yml | 3 | 1 |
| react-router-7.13.2/.github/workflows | workflows | react-router-7.13.2/.github | .github | Matt Brophy | dependabot[bot] | Michael Jackson | 15 | 15 | 189 | 2025-12-02 | 2025-12-11 | 2025-12-11 | 157 | 166 | 156 | fde69511bbfddf5a04e00d8c8bb9a7702a32b9bf | react-router-7.13.2/.github/workflows/test.yml | 3 | 1 |
| react-router-7.13.2/decisions | decisions | react-router-7.13.2 | react-router-7.13.2 | Matt Brophy | Pedro Cattori | Michael Jackson | 9 | 20 | 63 | 2026-02-19 | 2026-02-19 | 2026-03-18 | 60 | 87 | 87 | ff67b74a33c9f13fac28afc4923d0bf5628998ec | react-router-7.13.2/decisions/template.md | 2 | 1 |
| react-router-7.13.2/docs | docs | react-router-7.13.2 | react-router-7.13.2 | Matt Brophy | Ryan Florence | Remix Run Bot | 117 | 195 | 648 | 2025-11-26 | 2026-03-18 | 2026-03-18 | 60 | 171 | 60 | ff6a4fea561d67b1e61002522096797afb9ff55e | react-router-7.13.2/docs/upgrading/v6.md | 2 | 1 |
| react-router-7.13.2/docs/api | api | react-router-7.13.2/docs | docs | Matt Brophy | Remix Run Bot | Brooks Lybrand | 22 | 108 | 167 | 2025-08-13 | 2026-03-18 | 2026-03-18 | 60 | 277 | 60 | fed3b6300c8b8db90d9779a8f9c3304e91d719d3 | react-router-7.13.2/docs/api/utils/resolvePath.md | 3 | 1 |
| react-router-7.13.2/docs/api/components | components | react-router-7.13.2/docs/api | api | Matt Brophy | Remix Run Bot | Ryan Florence | 6 | 11 | 44 | 2025-03-14 | 2026-02-23 | 2026-02-23 | 83 | 429 | 83 | f153b191e1c52bc8fb0e485bfd5d8ec2a8752104 | react-router-7.13.2/docs/api/components/index.md | 4 | 1 |

[Full data](./List_git_file_directories_with_commit_statistics.csv)

### 2.2 Directory Commit Statistics (Charts)



---

## 3. Co-Changed Files

Files committed together = logical coupling signal. May belong to the same conceptual unit or share a concern.

### 3.1 Co-Changed File Pairs

| firstFile | secondFile | commitCount |
| --- | --- | --- |
| react-router-7.13.2/packages/react-router-dom/package.json | react-router-7.13.2/packages/react-router/package.json | 329 |
| react-router-7.13.2/packages/react-router/CHANGELOG.md | react-router-7.13.2/packages/react-router/package.json | 164 |
| react-router-7.13.2/packages/react-router-dom/package.json | react-router-7.13.2/packages/react-router/CHANGELOG.md | 162 |
| react-router-7.13.2/packages/react-router/package.json | react-router-7.13.2/contributors.yml | 84 |
| react-router-7.13.2/packages/react-router-dom/package.json | react-router-7.13.2/contributors.yml | 82 |
| react-router-7.13.2/packages/react-router/lib/components.tsx | react-router-7.13.2/packages/react-router/lib/hooks.tsx | 81 |
| react-router-7.13.2/packages/react-router/CHANGELOG.md | react-router-7.13.2/contributors.yml | 80 |
| react-router-7.13.2/packages/react-router-node/CHANGELOG.md | react-router-7.13.2/packages/react-router-serve/CHANGELOG.md | 75 |
| react-router-7.13.2/packages/react-router-dev/CHANGELOG.md | react-router-7.13.2/packages/react-router-node/CHANGELOG.md | 73 |
| react-router-7.13.2/packages/react-router-dev/CHANGELOG.md | react-router-7.13.2/packages/react-router-serve/CHANGELOG.md | 73 |

### 3.2 Co-Changed File Pairs (All in One Commit)

Files changed together in a single large commit.

| firstFile | secondFile | commitCount |
| --- | --- | --- |
| react-router-7.13.2/packages/react-router-dom/package.json | react-router-7.13.2/packages/react-router/package.json | 570 |
| react-router-7.13.2/packages/react-router/CHANGELOG.md | react-router-7.13.2/packages/react-router/package.json | 401 |
| react-router-7.13.2/packages/react-router-dom/package.json | react-router-7.13.2/packages/react-router/CHANGELOG.md | 398 |
| react-router-7.13.2/packages/react-router-node/CHANGELOG.md | react-router-7.13.2/packages/react-router-serve/CHANGELOG.md | 216 |
| react-router-7.13.2/packages/react-router-dev/CHANGELOG.md | react-router-7.13.2/packages/react-router-node/CHANGELOG.md | 214 |
| react-router-7.13.2/packages/react-router-dev/CHANGELOG.md | react-router-7.13.2/packages/react-router-serve/CHANGELOG.md | 214 |
| react-router-7.13.2/packages/react-router-express/CHANGELOG.md | react-router-7.13.2/packages/react-router-node/CHANGELOG.md | 208 |
| react-router-7.13.2/packages/react-router-express/CHANGELOG.md | react-router-7.13.2/packages/react-router-serve/CHANGELOG.md | 208 |
| react-router-7.13.2/packages/react-router-dev/CHANGELOG.md | react-router-7.13.2/packages/react-router-express/CHANGELOG.md | 206 |
| react-router-7.13.2/packages/react-router-dev/CHANGELOG.md | react-router-7.13.2/packages/react-router/CHANGELOG.md | 201 |

### 3.3 Co-Changed With a Specific File

Shows all files that were changed together with another particular file.

| filePath | commitCount | coChangeRate | maxLift | avgLift |
| --- | --- | --- | --- | --- |
| react-router-7.13.2/packages/react-router-dom/package.json | 333 | 0.0005372293485327831 | 2.3829953198127924 | 1.3428434024427154 |
| react-router-7.13.2/contributors.yml | 220 | 0.0005630515345713642 | 1.329185520361991 | 0.6221928060645834 |
| react-router-7.13.2/packages/react-router/CHANGELOG.md | 173 | 0.0007991168142492228 | 1.4511088519899094 | 1.0013305294713213 |
| react-router-7.13.2/packages/react-router/package.json | 155 | 0.0006201810928791207 | 2.24302496328928 | 0.6564867917952943 |
| react-router-7.13.2/packages/react-router/index.ts | 123 | 0.001426252319109462 | 4.471879815100155 | 2.7457378157432673 |
| react-router-7.13.2/packages/react-router/lib/components.tsx | 123 | 0.00165567371113205 | 5.853352984524688 | 3.3923301996870627 |
| react-router-7.13.2/packages/react-router-dev/package.json | 82 | 0.0006607787519339866 | 2.5451263537906135 | 1.0921966752978978 |
| react-router-7.13.2/packages/react-router-node/CHANGELOG.md | 76 | 0.0011556826130592135 | 3.6660586569385107 | 1.7802396737522803 |
| react-router-7.13.2/packages/react-router-dev/CHANGELOG.md | 74 | 0.0006065076633062864 | 3.596958113578813 | 2.0974422710295975 |
| react-router-7.13.2/packages/react-router-dev/vite/plugin.ts | 70 | 0.00150324270927286 | 4.487847222222221 | 1.8197446080923507 |

[Full data](./List_git_files_that_were_changed_together_with_another_file.csv)

### 3.4 Co-Changed With a Specific File (All in One)

| filePath | commitCount |
| --- | --- |
| react-router-7.13.2/packages/react-router/package.json | 603 |
| react-router-7.13.2/packages/react-router-dom/package.json | 574 |
| react-router-7.13.2/packages/react-router/CHANGELOG.md | 455 |
| react-router-7.13.2/contributors.yml | 399 |
| react-router-7.13.2/packages/react-router-dev/package.json | 234 |
| react-router-7.13.2/packages/react-router-node/CHANGELOG.md | 217 |
| react-router-7.13.2/packages/react-router-serve/CHANGELOG.md | 216 |
| react-router-7.13.2/packages/react-router-dev/CHANGELOG.md | 215 |
| react-router-7.13.2/packages/react-router-express/CHANGELOG.md | 208 |
| react-router-7.13.2/packages/react-router-cloudflare/CHANGELOG.md | 187 |

### 3.5 Co-Changed Files (Charts)



---

## 4. File Change Distribution

Files changed per commit. High proportion of large commits = low commit granularity.

### 4.1 Files per Commit Distribution

| filesPerCommit | commitCount |
| --- | --- |
| 1 | 4578 |
| 2 | 1767 |
| 3 | 882 |
| 4 | 556 |
| 5 | 470 |
| 6 | 282 |
| 7 | 194 |
| 8 | 157 |
| 9 | 99 |
| 10 | 130 |

[Full data](./List_git_files_per_commit_distribution.csv)

### 4.2 Files per Commit Chart



---

## 5. Pairwise Changed Files

Commit overlap counts and dependency info between file pairs.

### 5.1 Pairwise Changed Files

| firstFileName | secondFileName | filePairLineBreak | filePairWithRelativePathLineBreak | filePair | filePairWithRelativePath | firstFileExtension | secondFileExtension | fileExtensionPair | updateCommitCount | updateCommitMinConfidence | updateCommitSupport | updateCommitLift | updateCommitJaccardSimilarity |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| packages/react-router-dom/package.json | integration/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-dom/package.json<br>integration/CHANGELOG.md | package↔CHANGELOG | packages/react-router-dom/package.json↔integration/CHANGELOG.md | json | md | json↔md | 6 | 0.06818181818181818 | 0.0019639934533551553 | 0.324953907247199 | 0.008298755186721992 |
| packages/react-router/package.json | integration/CHANGELOG.md | package<br>CHANGELOG | packages/react-router/package.json<br>integration/CHANGELOG.md | package↔CHANGELOG | packages/react-router/package.json↔integration/CHANGELOG.md | json | md | json↔md | 6 | 0.06818181818181818 | 0.0019639934533551553 | 0.3058670404485382 | 0.007863695937090432 |
| packages/react-router-serve/package.json | integration/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-serve/package.json<br>integration/CHANGELOG.md | package↔CHANGELOG | packages/react-router-serve/package.json↔integration/CHANGELOG.md | json | md | json↔md | 6 | 0.06818181818181818 | 0.0019639934533551553 | 1.0111429832303618 | 0.020833333333333332 |
| packages/react-router-remix-routes-option-adapter/package.json | integration/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-remix-routes-option-adapter/package.json<br>integration/CHANGELOG.md | package↔CHANGELOG | packages/react-router-remix-routes-option-adapter/package.json↔integration/CHANGELOG.md | json | md | json↔md | 6 | 0.06818181818181818 | 0.0019639934533551553 | 1.102092352092352 | 0.02214022140221402 |
| packages/react-router-express/package.json | integration/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-express/package.json<br>integration/CHANGELOG.md | package↔CHANGELOG | packages/react-router-express/package.json↔integration/CHANGELOG.md | json | md | json↔md | 6 | 0.06818181818181818 | 0.0019639934533551553 | 1.0160753880266074 | 0.020905923344947737 |
| packages/react-router-cloudflare/package.json | integration/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-cloudflare/package.json<br>integration/CHANGELOG.md | package↔CHANGELOG | packages/react-router-cloudflare/package.json↔integration/CHANGELOG.md | json | md | json↔md | 6 | 0.06818181818181818 | 0.0019639934533551553 | 1.006258234519104 | 0.020761245674740483 |
| packages/react-router-architect/package.json | integration/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-architect/package.json<br>integration/CHANGELOG.md | package↔CHANGELOG | packages/react-router-architect/package.json↔integration/CHANGELOG.md | json | md | json↔md | 6 | 0.06818181818181818 | 0.0019639934533551553 | 1.0160753880266074 | 0.020905923344947737 |
| packages/react-router-dev/package.json | integration/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-dev/package.json<br>integration/CHANGELOG.md | package↔CHANGELOG | packages/react-router-dev/package.json↔integration/CHANGELOG.md | json | md | json↔md | 6 | 0.06818181818181818 | 0.0019639934533551553 | 0.7519691499835903 | 0.016713091922005572 |
| packages/create-react-router/package.json | integration/CHANGELOG.md | package<br>CHANGELOG | packages/create-react-router/package.json<br>integration/CHANGELOG.md | package↔CHANGELOG | packages/create-react-router/package.json↔integration/CHANGELOG.md | json | md | json↔md | 6 | 0.06818181818181818 | 0.0019639934533551553 | 1.0362957937584802 | 0.02120141342756184 |
| packages/react-router-fs-routes/package.json | integration/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-fs-routes/package.json<br>integration/CHANGELOG.md | package↔CHANGELOG | packages/react-router-fs-routes/package.json↔integration/CHANGELOG.md | json | md | json↔md | 6 | 0.06818181818181818 | 0.0019639934533551553 | 1.0467108268615806 | 0.021352313167259787 |

[Full data](./List_pairwise_changed_files.csv)

### 5.2 Pairwise Changed Files (Top by Lift)

File pairs that co-change more often than random chance (lift > 1).

| fileExtensionPair | firstFileNameShort | secondFileNameShort | updateCommitCount | updateCommitMinConfidence | updateCommitLift | updateCommitJaccardSimilarity | updateCommitSupport | firstFileName | secondFileName |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ts↔ts | vite-dev-custom-entry-test | vite-absolute-base-test | 3 | 1 | 152.75 | 0.15 | 0.0009819967266775777 | integration/vite-dev-custom-entry-test.ts | integration/vite-absolute-base-test.ts |
| ts↔ts | vite-loader-context-test | vite-node-env-test | 4 | 0.8 | 143.76470588235293 | 0.2222222222222222 | 0.001309328968903437 | integration/vite-loader-context-test.ts | integration/vite-node-env-test.ts |
| ts↔ts | sessions-test | sessions | 3 | 0.375 | 114.56249999999999 | 0.2 | 0.0009819967266775777 | packages/react-router/__tests__/server-runtime/sessions-test.ts | packages/react-router/lib/server-runtime/sessions.ts |
| ts↔ts | remove-exports-test | remove-exports | 4 | 0.36363636363636365 | 100.99173553719007 | 0.2222222222222222 | 0.001309328968903437 | packages/react-router-dev/vite/remove-exports-test.ts | packages/react-router-dev/vite/remove-exports.ts |
| ts↔ts | vite-dotenv-test | vite-node-env-test | 4 | 0.8 | 90.51851851851852 | 0.14285714285714285 | 0.001309328968903437 | integration/vite-dotenv-test.ts | integration/vite-node-env-test.ts |
| ts↔ts | routes | routes | 3 | 0.75 | 88.12499999999999 | 0.1111111111111111 | 0.0009819967266775777 | packages/react-router-dev/config/routes.ts | packages/react-router-dev/routes.ts |
| ts↔ts | sessions-test | fileStorage | 3 | 0.3 | 83.31818181818181 | 0.16666666666666666 | 0.0009819967266775777 | packages/react-router-node/__tests__/sessions-test.ts | packages/react-router-node/sessions/fileStorage.ts |
| ts↔ts | vite-server-bundles-test | vite-node-env-test | 5 | 1 | 80.39473684210526 | 0.13157894736842105 | 0.0016366612111292963 | integration/vite-server-bundles-test.ts | integration/vite-node-env-test.ts |
| ts↔ts | virtual-route-config | virtual-route-modules | 3 | 0.375 | 76.37499999999999 | 0.15 | 0.0009819967266775777 | packages/react-router-dev/vite/rsc/virtual-route-config.ts | packages/react-router-dev/vite/rsc/virtual-route-modules.ts |
| ts↔ts | vite-dot-server-test | vite-node-env-test | 5 | 1 | 71.04651162790697 | 0.11627906976744186 | 0.0016366612111292963 | integration/vite-dot-server-test.ts | integration/vite-node-env-test.ts |

[Full data](./List_pairwise_changed_files_top_lift.csv)

### 5.3 Pairwise Changed Files With Dependencies

Files that are co-changed and also have a structural dependency relationship between them.

| dependencyWeight | fileDistance | commitCount | updateCommitMinConfidence | updateCommitSupport | updateCommitLift | updateCommitJaccardSimilarity |
| --- | --- | --- | --- | --- | --- | --- |
| 11 | 5 | 3 | 0.375 | 0.0009819967266775777 | 5.207386363636363 | 0.013333333333333334 |
| 11 | 4 | 4 | 0.19047619047619047 | 0.001309328968903437 | 2.6450216450216453 | 0.016877637130801686 |
| 22 | 5 | 3 | 0.09375 | 0.0009819967266775777 | 1.3018465909090908 | 0.012048192771084338 |
| 22 | 5 | 9 | 0.16666666666666666 | 0.0029459901800327334 | 2.3143939393939394 | 0.033962264150943396 |
| 33 | 4 | 8 | 0.07272727272727272 | 0.002618657937806874 | 1.0099173553719007 | 0.024844720496894408 |
| 66 | 4 | 3 | 0.1875 | 0.0009819967266775777 | 2.6036931818181817 | 0.012875536480686695 |
| 66 | 6 | 3 | 0.3333333333333333 | 0.0009819967266775777 | 14.143518518518517 | 0.038461538461538464 |
| 66 | 4 | 9 | 0.36 | 0.0029459901800327334 | 36.66 | 0.1956521739130435 |
| 91 | 0 | 3 | 0.375 | 0.0009819967266775777 | 26.64244186046512 | 0.0625 |
| 91 | 0 | 5 | 0.21739130434782608 | 0.0016366612111292963 | 16.603260869565215 | 0.08620689655172414 |

[Full data](./List_pairwise_changed_files_with_dependencies.csv)

### 5.4 Pairwise Changed Files (Charts)



---

## 6. Files by Author

Per-author file commit stats. Useful for knowledge boundaries and bus-factor risk.

### 6.1 Files with Commit Statistics by Author

| filePath | author | commitCount | commitHashes | lastCommitDate | lastCreationDate | lastModificationDate | daysSinceLastCommit | daysSinceLastCreation | daysSinceLastModification | maxCommitSha |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| react-router-7.13.2/.agents/skills/fix-bug/SKILL.md | Matt Brophy | 2 | ["2469dd6621fbcaec689571c3f003af5711bc54de","06c1149bc0b4f50db0cc6fc10471b4ad963b8969"] | 2026-03-18 | 2026-03-18 | 2026-03-18 | 60 | 60 | 60 | 2469dd6621fbcaec689571c3f003af5711bc54de |
| react-router-7.13.2/.browserslistrc | Michael Jackson | 3 | ["82c500c4a1a5d53a608faee25f8322c661b242a1","b3f728487ae6fe7d5ef4ddc759fb2a4ca0df712e","f6df0697e1b2064a2b3a12e8b39577326fdd945b"] | 2021-09-09 | 2018-10-30 | 2021-09-09 | 1711 | 2755 | 1710 | f6df0697e1b2064a2b3a12e8b39577326fdd945b |
| react-router-7.13.2/.browserslistrc | Matt Brophy | 1 | ["4fa24c1b12c7c2ff8f32bb611b8b5b3ac4678c61"] | 2024-03-27 | 2018-10-30 | 2021-09-09 | 781 | 2755 | 1710 | 4fa24c1b12c7c2ff8f32bb611b8b5b3ac4678c61 |
| react-router-7.13.2/.changeset/README.md | Matt Brophy | 2 | ["721bee06b9085c57f20c9333cdd327ea81f0376a","4fa24c1b12c7c2ff8f32bb611b8b5b3ac4678c61"] | 2024-03-27 | 2022-06-14 | 2022-06-14 | 781 | 1432 | 1432 | 721bee06b9085c57f20c9333cdd327ea81f0376a |
| react-router-7.13.2/.changeset/README.md | Chance Strickland | 1 | ["f264d828939e3ae74a6ca47e40d4c4b2fd027e8e"] | 2022-06-14 | 2022-06-14 | 2022-06-14 | 1433 | 1432 | 1432 | f264d828939e3ae74a6ca47e40d4c4b2fd027e8e |
| react-router-7.13.2/.changeset/config.json | Matt Brophy | 16 | ["721bee06b9085c57f20c9333cdd327ea81f0376a","bd7d7a1e5322e13b0cbe7e76f3e5afaef362996a","e3c67ede332794c64b2120d631864bb48d5523f7","eed3ebd417e2522f527eee4fba098785ceb3dcfb","7281167209fe8c76aa8e6b78bc5cc41fcbd5978d","ad761485a8278386fc296a4ad0dca6d5fabfa52a","7fe0cb95e04a60de9f81af5fec6985e98d2815ce","5e57ec92e2ad95955ab30e362f45b477e3b4a832","ea6d5beeb6895f72c0c1678dc79c457513c5e089","f8b1a47883109f968702ff272a370070577ca2ed","5ae997905b8362c3c5ba4361eb67f402d894f747","ec03b12c600ba899d1a35b6f63bc45bb594c1e88","a34b722b9b78b36575e6803e071650285036649a","2da4b9980517d541be54a7e1233eae141028714b","4fa24c1b12c7c2ff8f32bb611b8b5b3ac4678c61","b267a1cf1fe688809f3a57ef35f4467866fdada0"] | 2024-09-19 | 2022-06-14 | 2024-11-22 | 605 | 1432 | 541 | f8b1a47883109f968702ff272a370070577ca2ed |
| react-router-7.13.2/.changeset/config.json | Chance Strickland | 6 | ["f3009f5536b6bb3354bfe91d5ff02dd2fae91285","f264d828939e3ae74a6ca47e40d4c4b2fd027e8e","c143c9c1d7feb2a0035d52969d0a6e52ebdab7d0","aeceb7dcdf58c13eaf62e0657e79e8dba0122675","41c0491204272bb29f6275ab2acbb2d665b44ab5","558fb81772523191349d6fb5b504871c6457c605"] | 2022-10-06 | 2022-06-14 | 2024-11-22 | 1319 | 1432 | 541 | f3009f5536b6bb3354bfe91d5ff02dd2fae91285 |
| react-router-7.13.2/.changeset/config.json | Michael Jackson | 5 | ["d7dc44a9313be10227f93249de51efe30c771e44","70374283584e0b30ebcc60a84d1026c87ff31649","fd76ac8838c4b98cc6073fa987b6d30b08199c29","3f8f46da64df5210a33dd749ea30c69fa9e7c375","198dfa88851fd5eea9a3eed49f5e88eddc972d8b"] | 2024-11-22 | 2022-06-14 | 2024-11-22 | 541 | 1432 | 541 | fd76ac8838c4b98cc6073fa987b6d30b08199c29 |
| react-router-7.13.2/.changeset/config.json | Mark Dalgleish | 3 | ["559b0eba49a1c1667a40599af9d2324c1d2ace6b","0af95d49c5c5e0ccebabc73563ff627c760a524b","12afb2efdc8408bd9e87e03f8fd16dd21ef1b233"] | 2024-06-21 | 2022-06-14 | 2024-11-22 | 695 | 1432 | 541 | 559b0eba49a1c1667a40599af9d2324c1d2ace6b |
| react-router-7.13.2/.changeset/config.json | Jacob Ebey | 1 | ["aab4ea0e2b52ae91f93bd87653a2786e23252d49"] | 2024-05-09 | 2022-06-14 | 2024-11-22 | 738 | 1432 | 541 | aab4ea0e2b52ae91f93bd87653a2786e23252d49 |

[Full data](./List_git_files_with_commit_statistics_by_author.csv)

---

## 7. Data Quality

Files in git log that are unresolved (not found in codebase) or ambiguous (multiple matches). Affects reliability of co-change metrics.

### 7.1 File Resolution Summary

Resolved vs. ambiguous vs. unresolved files by extension.

| resolved | extension | gitFileCount | fileLabels | gitFileExamples |
| --- | --- | --- | --- | --- |
| false | md | 1791 | ["File","Git"] | [".changeset/cold-schools-relate.md",".changeset/fix-createRoutesStub-component-type.md",".changeset/fix-dev-socket-file-crash.md",".changeset/gentle-doors-visit.md",".changeset/kind-shirts-turn.md",".changeset/passthrough-reqeusts.md",".changeset/remove-agnostic-types.md",".changeset/sweet-houses-kick.md",".changeset/twelve-snails-wait.md"] |
| false | js | 1742 | ["File","Git"] | ["scripts/playground.js","scripts/version.js","integration/helpers/rsc-vite-framework/start.js","integration/helpers/rsc-parcel-framework/start.js","integration/helpers/rsc-vite/server.js","playground/rsc-vite-framework/start-vite-middleware.js","playground/rsc-vite-framework/start.js","examples/multi-app/server.js","examples/multi-app/vite.config.js"] |
| false | ts | 1081 | ["File","Git"] | ["integration/passthrough-requests-test.ts","integration/vite-presets-test.ts","packages/create-react-router/__tests__/create-react-router-test.ts","packages/react-router-dev/__tests__/watcher-ignored-test.ts","packages/react-router/__tests__/router/fetchers-test.ts","packages/react-router/__tests__/router/router-test.ts","packages/react-router/__tests__/router/ssr-test.ts","packages/react-router/__tests__/router/submission-test.ts","scripts/docs.ts"] |
| false | tsx | 457 | ["File","Git"] | ["examples/modal/src/App.tsx","packages/react-router/__tests__/dom/data-browser-router-test.tsx","packages/react-router/__tests__/dom/partial-hydration-test.tsx","packages/react-router/__tests__/dom/special-characters-test.tsx","packages/react-router/lib/components.tsx","packages/react-router/lib/dom-export/hydrated-router.tsx","packages/react-router/lib/dom/lib.tsx","packages/react-router/lib/dom/server.tsx","packages/react-router/lib/dom/ssr/components.tsx"] |
| false | json | 241 | ["File","Git"] | [".changeset/pre.json","examples/modal/package-lock.json","examples/modal-data-router/package-lock.json","examples/modal-data-router/tsconfig.json","playground/data/tsconfig.json","integration/helpers/rsc-parcel/package.json","integration/helpers/rsc-parcel/tsconfig.json","playground/rsc-parcel/package.json","playground/rsc-parcel/tsconfig.json"] |
| false | gitignore | 79 | ["File","Git"] | [".gitignore","examples/modal-data-router/.gitignore","integration/helpers/rsc-parcel/.gitignore","playground/rsc-parcel/.gitignore","integration/helpers/rsc-parcel-framework/.gitignore","playground/rsc-parcel-framework/.gitignore","integration/helpers/rsc-vite-framework/.gitignore","playground/rsc-vite-framework/.gitignore","integration/helpers/rsc-vite/.gitignore"] |
| false | css | 77 | ["File","Git"] | ["examples/modal-data-router/src/index.css","playground/rsc-parcel-framework/app/root.css","playground/rsc-parcel-framework/app/routes/_index/styles.css","playground/rsc-parcel-framework/app/routes/client-loader-hydrate/styles.module.css","playground/rsc-parcel-framework/app/routes/client-loader-without-server-loader/styles.module.css","playground/rsc-parcel-framework/app/routes/client-loader/styles.module.css","playground/rsc-parcel-framework/app/routes/server-loader/styles.module.css","playground/rsc-vite-framework/app/routes/mdx-glob.$post/posts/hello/hello-component.module.css","playground/rsc-vite-framework/app/routes/mdx-glob.$post/posts/world/world-component.module.css"] |
| false | html | 64 | ["File","Git"] | ["examples/modal-data-router/index.html","playground/data/index.html","examples/auth-router-provider/index.html","examples/auth/index.html","examples/basic-data-router/index.html","examples/basic/index.html","examples/custom-filter-link/index.html","examples/custom-link/index.html","examples/custom-query-parsing/index.html"] |
| false | ico | 46 | ["File","Git"] | ["integration/helpers/rsc-parcel/public/favicon.ico","integration/helpers/rsc-parcel-framework/public/favicon.ico","integration/helpers/rsc-vite-framework/public/favicon.ico","playground/rsc-vite-framework/public/favicon.ico","integration/helpers/rsc-vite/public/favicon.ico","playground/rsc-vite/public/favicon.ico","integration/helpers/vite-7-beta-template/public/favicon.ico","playground/framework-vite-7-beta/public/favicon.ico","integration/helpers/vite-rolldown-template/public/favicon.ico"] |
| false | png | 37 | ["File","Git"] | ["templates/basic/public/logo-dark.png","templates/basic/public/logo-light.png","static/base-branch.png","integration/assets/image.png","fixtures/hello-cra/public/logo512.png","fixtures/hello-cra/public/logo192.png","website/modules/logo.png","website/static/apple-touch-icon.png","website/static/android-chrome-144x144.png"] |

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
| json | ["File","TS"] | 13 | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/create-react-router/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/create-react-router/__tests__/fixtures/blank/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/create-react-router/__tests__/fixtures/with-ignored-dir/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-architect/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-express/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-node/.reports/jqa/ts-output.json"] |

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
