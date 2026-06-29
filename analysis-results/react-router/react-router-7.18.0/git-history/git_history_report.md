---
title: "Git History Report"
generated: "2026-06-29"
model_version: "v4.0.1"
dataset: "react-router-7.18.0"
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
| react-router-7.18.0 | react-router-7.18.0 |  |  | Matt Brophy | github-actions[bot] | Remix Run Bot | 601 | 1176 | 4907 | 2026-06-15 | 2026-06-16 | 2026-06-16 | 13 | 13 | 12 | fff84b5f20f35c347c9d6313dfc603db0eac6e19 | react-router-7.18.0/typedoc.mjs | 1 | 1 |
| react-router-7.18.0/.agents/skills | .agents/skills | react-router-7.18.0 | react-router-7.18.0 | Matt Brophy | Brooks Lybrand | null | 2 | 2 | 11 | 2026-05-07 | 2026-06-04 | 2026-06-04 | 25 | 52 | 24 | fadd6c490cc84abc560a2413ee6fa0f2617d098d | react-router-7.18.0/.agents/skills/implement-rfc/SKILL.md | 3 | 2 |
| react-router-7.18.0/.agents/skills/fix-bug | fix-bug | react-router-7.18.0/.agents/skills | skills | Matt Brophy | Brooks Lybrand | null | 2 | 1 | 8 | 2026-03-18 | 2026-06-04 | 2026-06-04 | 25 | 102 | 24 | d6f3a05d4124ae9c1f2f74c599f80d091268ce0c | react-router-7.18.0/.agents/skills/fix-bug/SKILL.md | 4 | 1 |
| react-router-7.18.0/.agents/skills/implement-rfc | implement-rfc | react-router-7.18.0/.agents/skills | skills | Matt Brophy | null | null | 1 | 1 | 4 | 2026-05-07 | 2026-06-04 | 2026-06-04 | 25 | 52 | 24 | fadd6c490cc84abc560a2413ee6fa0f2617d098d | react-router-7.18.0/.agents/skills/implement-rfc/SKILL.md | 4 | 1 |
| react-router-7.18.0/.github | .github | react-router-7.18.0 | react-router-7.18.0 | Matt Brophy | Michael Jackson | Michaël De Boey | 22 | 19 | 220 | 2026-05-26 | 2026-06-04 | 2026-06-04 | 25 | 33 | 24 | ff67b74a33c9f13fac28afc4923d0bf5628998ec | react-router-7.18.0/.github/workflows/test.yml | 2 | 1 |
| react-router-7.18.0/.github/ISSUE_TEMPLATE | ISSUE_TEMPLATE | react-router-7.18.0/.github | .github | Matt Brophy | Pedro Cattori | Tim Dorr | 13 | 3 | 51 | 2023-01-11 | 2026-06-04 | 2026-06-04 | 25 | 1264 | 24 | ff67b74a33c9f13fac28afc4923d0bf5628998ec | react-router-7.18.0/.github/ISSUE_TEMPLATE/documentation_isse.yml | 3 | 1 |
| react-router-7.18.0/.github/workflows | workflows | react-router-7.18.0/.github | .github | Matt Brophy | dependabot[bot] | Michael Jackson | 16 | 14 | 181 | 2026-05-26 | 2026-06-04 | 2026-06-04 | 25 | 33 | 24 | ff4c0712f7b24d38f51f7b967d7c31aeac531bed | react-router-7.18.0/.github/workflows/test.yml | 3 | 1 |
| react-router-7.18.0/decisions | decisions | react-router-7.18.0 | react-router-7.18.0 | Matt Brophy | Pedro Cattori | Michael Jackson | 10 | 20 | 69 | 2026-02-19 | 2026-06-04 | 2026-06-04 | 25 | 129 | 24 | ff67b74a33c9f13fac28afc4923d0bf5628998ec | react-router-7.18.0/decisions/template.md | 2 | 1 |
| react-router-7.18.0/docs | docs | react-router-7.18.0 | react-router-7.18.0 | Matt Brophy | Remix Run Bot | Ryan Florence | 124 | 197 | 703 | 2026-05-07 | 2026-06-15 | 2026-06-15 | 14 | 52 | 13 | ff6a4fea561d67b1e61002522096797afb9ff55e | react-router-7.18.0/docs/upgrading/v6.md | 2 | 1 |
| react-router-7.18.0/docs/api | api | react-router-7.18.0/docs | docs | Matt Brophy | Remix Run Bot | Brooks Lybrand | 23 | 109 | 200 | 2026-05-07 | 2026-06-15 | 2026-06-15 | 14 | 52 | 13 | fed3b6300c8b8db90d9779a8f9c3304e91d719d3 | react-router-7.18.0/docs/api/utils/resolvePath.md | 3 | 1 |

[Full data](./List_git_file_directories_with_commit_statistics.csv)

### 2.2 Directory Commit Statistics (Charts)



---

## 3. Co-Changed Files

Files committed together = logical coupling signal. May belong to the same conceptual unit or share a concern.

### 3.1 Co-Changed File Pairs

| firstFile | secondFile | commitCount |
| --- | --- | --- |
| react-router-7.18.0/packages/react-router-dom/package.json | react-router-7.18.0/packages/react-router/package.json | 350 |
| react-router-7.18.0/packages/react-router/CHANGELOG.md | react-router-7.18.0/packages/react-router/package.json | 181 |
| react-router-7.18.0/packages/react-router-dom/package.json | react-router-7.18.0/packages/react-router/CHANGELOG.md | 179 |
| react-router-7.18.0/contributors.yml | react-router-7.18.0/packages/react-router/package.json | 93 |
| react-router-7.18.0/contributors.yml | react-router-7.18.0/packages/react-router-dom/package.json | 91 |
| react-router-7.18.0/packages/react-router/lib/hooks.tsx | react-router-7.18.0/packages/react-router/lib/components.tsx | 90 |
| react-router-7.18.0/packages/react-router-node/CHANGELOG.md | react-router-7.18.0/packages/react-router-serve/CHANGELOG.md | 88 |
| react-router-7.18.0/packages/react-router-dev/CHANGELOG.md | react-router-7.18.0/packages/react-router-node/CHANGELOG.md | 88 |
| react-router-7.18.0/contributors.yml | react-router-7.18.0/packages/react-router/CHANGELOG.md | 86 |
| react-router-7.18.0/packages/react-router-dev/CHANGELOG.md | react-router-7.18.0/packages/react-router-serve/CHANGELOG.md | 86 |

### 3.2 Co-Changed File Pairs (All in One Commit)

Files changed together in a single large commit.

| firstFile | secondFile | commitCount |
| --- | --- | --- |
| react-router-7.18.0/packages/react-router-dom/package.json | react-router-7.18.0/packages/react-router/package.json | 600 |
| react-router-7.18.0/packages/react-router/CHANGELOG.md | react-router-7.18.0/packages/react-router/package.json | 426 |
| react-router-7.18.0/packages/react-router-dom/package.json | react-router-7.18.0/packages/react-router/CHANGELOG.md | 423 |
| react-router-7.18.0/packages/react-router-dev/CHANGELOG.md | react-router-7.18.0/packages/react-router-node/CHANGELOG.md | 237 |
| react-router-7.18.0/packages/react-router-node/CHANGELOG.md | react-router-7.18.0/packages/react-router-serve/CHANGELOG.md | 237 |
| react-router-7.18.0/packages/react-router-dev/CHANGELOG.md | react-router-7.18.0/packages/react-router-serve/CHANGELOG.md | 235 |
| react-router-7.18.0/packages/react-router-express/CHANGELOG.md | react-router-7.18.0/packages/react-router-node/CHANGELOG.md | 231 |
| react-router-7.18.0/packages/react-router-dev/CHANGELOG.md | react-router-7.18.0/packages/react-router-express/CHANGELOG.md | 230 |
| react-router-7.18.0/packages/react-router-dev/CHANGELOG.md | react-router-7.18.0/packages/react-router/CHANGELOG.md | 229 |
| react-router-7.18.0/packages/react-router-express/CHANGELOG.md | react-router-7.18.0/packages/react-router-serve/CHANGELOG.md | 229 |

### 3.3 Co-Changed With a Specific File

Shows all files that were changed together with another particular file.

| filePath | commitCount | coChangeRate | maxLift | avgLift |
| --- | --- | --- | --- | --- |
| react-router-7.18.0/packages/react-router-dom/package.json | 350 | 0.0006352755825477092 | 2.318642658868586 | 1.561543814824198 |
| react-router-7.18.0/contributors.yml | 303 | 0.00028172209370653297 | 1.6759656652360515 | 0.5878028410718673 |
| react-router-7.18.0/packages/react-router/CHANGELOG.md | 184 | 0.0016089260418670538 | 1.6138745387453872 | 1.433901314996745 |
| react-router-7.18.0/packages/react-router/lib/hooks.tsx | 172 | 0.0007409577309461858 | 6.09431721798134 | 2.6500866683814133 |
| react-router-7.18.0/packages/react-router/lib/components.tsx | 150 | 0.0010121457489878543 | 6.323886639676114 | 2.4943302382233163 |
| react-router-7.18.0/packages/react-router/index.ts | 148 | 0.0008290201877618695 | 9.134502923976608 | 2.3996280133898535 |
| react-router-7.18.0/pnpm-lock.yaml | 146 | 0.0008599110639926967 | 5.950476190476191 | 1.7279408113310002 |
| react-router-7.18.0/packages/react-router/lib/router/router.ts | 128 | 0.0010232959723710088 | 7.067873303167422 | 2.4141621097602832 |
| react-router-7.18.0/packages/react-router-dev/vite/plugin.ts | 122 | 0.0008209517657192075 | 4.191413237924866 | 1.731476273223016 |
| react-router-7.18.0/packages/react-router-dev/CHANGELOG.md | 95 | 0.0003840028456631931 | 3.4088310786514073 | 2.1312769709730963 |

[Full data](./List_git_files_that_were_changed_together_with_another_file.csv)

### 3.4 Co-Changed With a Specific File (All in One)

| filePath | commitCount |
| --- | --- |
| react-router-7.18.0/packages/react-router/package.json | 634 |
| react-router-7.18.0/packages/react-router-dom/package.json | 605 |
| react-router-7.18.0/packages/react-router/CHANGELOG.md | 489 |
| react-router-7.18.0/contributors.yml | 437 |
| react-router-7.18.0/packages/react-router-dev/package.json | 255 |
| react-router-7.18.0/packages/react-router-dev/CHANGELOG.md | 244 |
| react-router-7.18.0/packages/react-router-node/CHANGELOG.md | 240 |
| react-router-7.18.0/packages/react-router-serve/CHANGELOG.md | 237 |
| react-router-7.18.0/packages/react-router-express/CHANGELOG.md | 232 |
| react-router-7.18.0/packages/react-router-cloudflare/CHANGELOG.md | 208 |

### 3.5 Co-Changed Files (Charts)



---

## 4. File Change Distribution

Files changed per commit. High proportion of large commits = low commit granularity.

### 4.1 Files per Commit Distribution

| filesPerCommit | commitCount |
| --- | --- |
| 1 | 4660 |
| 2 | 1806 |
| 3 | 915 |
| 4 | 576 |
| 5 | 476 |
| 6 | 287 |
| 7 | 198 |
| 8 | 163 |
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
| integration/CHANGELOG.md | packages/react-router-dev/CHANGELOG.md | CHANGELOG<br>CHANGELOG | integration/CHANGELOG.md<br>packages/react-router-dev/CHANGELOG.md | CHANGELOG↔CHANGELOG | integration/CHANGELOG.md↔packages/react-router-dev/CHANGELOG.md | md | md | md↔md | 43 | 0.44329896907216493 | 0.013764404609475032 | 4.825317001329071 | 0.12609970674486803 |
| packages/react-router-architect/package.json | packages/react-router-dev/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-architect/package.json<br>packages/react-router-dev/CHANGELOG.md | package↔CHANGELOG | packages/react-router-architect/package.json↔packages/react-router-dev/CHANGELOG.md | json | md | json↔md | 29 | 0.12554112554112554 | 0.009282970550576185 | 1.3665173386427742 | 0.05930470347648262 |
| packages/create-react-router/package.json | packages/react-router-dev/CHANGELOG.md | package<br>CHANGELOG | packages/create-react-router/package.json<br>packages/react-router-dev/CHANGELOG.md | package↔CHANGELOG | packages/create-react-router/package.json↔packages/react-router-dev/CHANGELOG.md | json | md | json↔md | 28 | 0.12444444444444444 | 0.008962868117797696 | 1.354579945799458 | 0.05785123966942149 |
| packages/react-router-cloudflare/package.json | packages/react-router-dev/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-cloudflare/package.json<br>packages/react-router-dev/CHANGELOG.md | package↔CHANGELOG | packages/react-router-cloudflare/package.json↔packages/react-router-dev/CHANGELOG.md | json | md | json↔md | 29 | 0.12446351931330472 | 0.009282970550576185 | 1.354787576079317 | 0.059063136456211814 |
| packages/react-router-dom/package.json | packages/react-router-dev/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-dom/package.json<br>packages/react-router-dev/CHANGELOG.md | package↔CHANGELOG | packages/react-router-dom/package.json↔packages/react-router-dev/CHANGELOG.md | json | md | json↔md | 29 | 0.10104529616724739 | 0.009282970550576185 | 0.4732616270262081 | 0.03135135135135135 |
| packages/react-router/package.json | packages/react-router-dev/CHANGELOG.md | package<br>CHANGELOG | packages/react-router/package.json<br>packages/react-router-dev/CHANGELOG.md | package↔CHANGELOG | packages/react-router/package.json↔packages/react-router-dev/CHANGELOG.md | json | md | json↔md | 29 | 0.10104529616724739 | 0.009282970550576185 | 0.4464858631209065 | 0.03005181347150259 |
| packages/react-router-dev/package.json | packages/react-router-dev/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-dev/package.json<br>packages/react-router-dev/CHANGELOG.md | package↔CHANGELOG | packages/react-router-dev/package.json↔packages/react-router-dev/CHANGELOG.md | json | md | json↔md | 29 | 0.10104529616724739 | 0.009282970550576185 | 1.0349688695950192 | 0.05150976909413854 |
| packages/react-router-fs-routes/package.json | packages/react-router-dev/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-fs-routes/package.json<br>packages/react-router-dev/CHANGELOG.md | package↔CHANGELOG | packages/react-router-fs-routes/package.json↔packages/react-router-dev/CHANGELOG.md | json | md | json↔md | 29 | 0.1288888888888889 | 0.009282970550576185 | 1.4029578010065815 | 0.060041407867494824 |
| packages/react-router-serve/package.json | packages/react-router-dev/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-serve/package.json<br>packages/react-router-dev/CHANGELOG.md | package↔CHANGELOG | packages/react-router-serve/package.json↔packages/react-router-dev/CHANGELOG.md | json | md | json↔md | 29 | 0.12608695652173912 | 0.009282970550576185 | 1.3724587183760035 | 0.05942622950819672 |
| packages/react-router-express/package.json | packages/react-router-dev/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-express/package.json<br>packages/react-router-dev/CHANGELOG.md | package↔CHANGELOG | packages/react-router-express/package.json↔packages/react-router-dev/CHANGELOG.md | json | md | json↔md | 29 | 0.12554112554112554 | 0.009282970550576185 | 1.3665173386427742 | 0.05930470347648262 |

[Full data](./List_pairwise_changed_files.csv)

### 5.2 Pairwise Changed Files (Top by Lift)

File pairs that co-change more often than random chance (lift > 1).

| fileExtensionPair | firstFileNameShort | secondFileNameShort | updateCommitCount | updateCommitMinConfidence | updateCommitLift | updateCommitJaccardSimilarity | updateCommitSupport | firstFileName | secondFileName |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ts↔ts | vite-dev-custom-entry-test | vite-absolute-base-test | 3 | 1 | 156.20000000000002 | 0.15 | 0.0009603072983354673 | integration/vite-dev-custom-entry-test.ts | integration/vite-absolute-base-test.ts |
| ts↔ts | vite-loader-context-test | vite-node-env-test | 4 | 0.8 | 147.01176470588234 | 0.2222222222222222 | 0.0012804097311139564 | integration/vite-loader-context-test.ts | integration/vite-node-env-test.ts |
| ts↔ts | sessions-test | sessions | 3 | 0.375 | 117.15 | 0.2 | 0.0009603072983354673 | packages/react-router/__tests__/server-runtime/sessions-test.ts | packages/react-router/lib/server-runtime/sessions.ts |
| ts↔ts | remove-exports-test | remove-exports | 4 | 0.36363636363636365 | 103.27272727272728 | 0.2222222222222222 | 0.0012804097311139564 | packages/react-router-dev/vite/remove-exports-test.ts | packages/react-router-dev/vite/remove-exports.ts |
| ts↔ts | vite-dotenv-test | vite-node-env-test | 4 | 0.8 | 92.56296296296296 | 0.14285714285714285 | 0.0012804097311139564 | integration/vite-dotenv-test.ts | integration/vite-node-env-test.ts |
| ts↔ts | fileStorage | sessions-test | 3 | 0.3 | 85.2 | 0.16666666666666666 | 0.0009603072983354673 | packages/react-router-node/sessions/fileStorage.ts | packages/react-router-node/__tests__/sessions-test.ts |
| ts↔ts | routes | routes | 3 | 0.75 | 80.79310344827586 | 0.1 | 0.0009603072983354673 | packages/react-router-dev/config/routes.ts | packages/react-router-dev/routes.ts |
| ts↔ts | vite-server-bundles-test | vite-node-env-test | 5 | 1 | 74.3809523809524 | 0.11904761904761904 | 0.0016005121638924455 | integration/vite-server-bundles-test.ts | integration/vite-node-env-test.ts |
| ts↔ts | vite-dot-server-test | vite-node-env-test | 5 | 1 | 72.65116279069768 | 0.11627906976744186 | 0.0016005121638924455 | integration/vite-dot-server-test.ts | integration/vite-node-env-test.ts |
| ts↔ts | vite-dot-client-test | vite-dev-custom-entry-test | 3 | 0.42857142857142855 | 66.94285714285714 | 0.125 | 0.0009603072983354673 | integration/vite-dot-client-test.ts | integration/vite-dev-custom-entry-test.ts |

[Full data](./List_pairwise_changed_files_top_lift.csv)

### 5.3 Pairwise Changed Files With Dependencies

Files that are co-changed and also have a structural dependency relationship between them.

| dependencyWeight | fileDistance | commitCount | updateCommitMinConfidence | updateCommitSupport | updateCommitLift | updateCommitJaccardSimilarity |
| --- | --- | --- | --- | --- | --- | --- |
| 5 | 4 | 4 | 0.16 | 0.0012804097311139564 | 2.192280701754386 | 0.01606425702811245 |
| 10 | 5 | 3 | 0.07317073170731707 | 0.0009603072983354673 | 1.0025673940949935 | 0.011278195488721804 |
| 10 | 5 | 9 | 0.14285714285714285 | 0.002880921895006402 | 1.957393483709273 | 0.031914893617021274 |
| 15 | 6 | 3 | 0.15 | 0.0009603072983354673 | 5.512941176470588 | 0.029411764705882353 |
| 15 | 4 | 9 | 0.0703125 | 0.002880921895006402 | 0.9634046052631579 | 0.025936599423631124 |
| 15 | 4 | 9 | 0.36 | 0.002880921895006402 | 37.48800000000001 | 0.1956521739130435 |
| 30 | 4 | 3 | 0.13636363636363635 | 0.0009603072983354673 | 1.8684210526315788 | 0.012145748987854251 |
| 30 | 5 | 3 | 0.07317073170731707 | 0.0009603072983354673 | 1.0343229224147445 | 0.011583011583011582 |
| 30 | 0 | 9 | 0.36 | 0.002880921895006402 | 8.78625 | 0.0625 |
| 45 | 0 | 3 | 0.058823529411764705 | 0.0009603072983354673 | 2.916900093370682 | 0.02702702702702703 |

[Full data](./List_pairwise_changed_files_with_dependencies.csv)

### 5.4 Pairwise Changed Files (Charts)



---

## 6. Files by Author

Per-author file commit stats. Useful for knowledge boundaries and bus-factor risk.

### 6.1 Files with Commit Statistics by Author

| filePath | author | commitCount | commitHashes | lastCommitDate | lastCreationDate | lastModificationDate | daysSinceLastCommit | daysSinceLastCreation | daysSinceLastModification | maxCommitSha |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| react-router-7.18.0/.agents/skills/fix-bug/SKILL.md | Matt Brophy | 7 | ["2469dd6621fbcaec689571c3f003af5711bc54de","06c1149bc0b4f50db0cc6fc10471b4ad963b8969","a842fca719e81505f454a8e6a8c728cdaed22067","46321cf2767cb820c1be8bbea3bafbc32c6c4ffd","1497c6ba52e55158e4f12b54617b1255935c75d5","963affeb924f2256bd20c0c5c87e4c4b4fcbd188","d6f3a05d4124ae9c1f2f74c599f80d091268ce0c"] | 2026-06-04 | 2026-03-18 | 2026-06-04 | 25 | 102 | 24 | d6f3a05d4124ae9c1f2f74c599f80d091268ce0c |
| react-router-7.18.0/.agents/skills/fix-bug/SKILL.md | Brooks Lybrand | 1 | ["4f8fff6cdb31c549fd011ac516fad5ad2e641b5f"] | 2026-05-29 | 2026-03-18 | 2026-06-04 | 31 | 102 | 24 | 4f8fff6cdb31c549fd011ac516fad5ad2e641b5f |
| react-router-7.18.0/.agents/skills/implement-rfc/SKILL.md | Matt Brophy | 4 | ["a6ab746a43675332ec3c190b1390724bf5c833db","522bc1b8cd0d7b3565bf9193789f2b7d5503856b","fadd6c490cc84abc560a2413ee6fa0f2617d098d","d6f3a05d4124ae9c1f2f74c599f80d091268ce0c"] | 2026-06-04 | 2026-05-07 | 2026-06-04 | 25 | 52 | 24 | fadd6c490cc84abc560a2413ee6fa0f2617d098d |
| react-router-7.18.0/.browserslistrc | Michael Jackson | 3 | ["82c500c4a1a5d53a608faee25f8322c661b242a1","b3f728487ae6fe7d5ef4ddc759fb2a4ca0df712e","f6df0697e1b2064a2b3a12e8b39577326fdd945b"] | 2021-09-09 | 2018-10-30 | 2021-09-09 | 1754 | 2798 | 1753 | f6df0697e1b2064a2b3a12e8b39577326fdd945b |
| react-router-7.18.0/.browserslistrc | Matt Brophy | 1 | ["4fa24c1b12c7c2ff8f32bb611b8b5b3ac4678c61"] | 2024-03-27 | 2018-10-30 | 2021-09-09 | 824 | 2798 | 1753 | 4fa24c1b12c7c2ff8f32bb611b8b5b3ac4678c61 |
| react-router-7.18.0/.github/FUNDING.yml | Michael Jackson | 1 | ["2679ebc9386c87a53da5c88f606d326ed6bba5bd"] | 2019-10-22 | 2019-10-22 | 2019-10-22 | 2442 | 2441 | 2441 | 2679ebc9386c87a53da5c88f606d326ed6bba5bd |
| react-router-7.18.0/.github/FUNDING.yml | Matt Brophy | 1 | ["4fa24c1b12c7c2ff8f32bb611b8b5b3ac4678c61"] | 2024-03-27 | 2019-10-22 | 2019-10-22 | 824 | 2441 | 2441 | 4fa24c1b12c7c2ff8f32bb611b8b5b3ac4678c61 |
| react-router-7.18.0/.github/ISSUE_TEMPLATE/bug_report.yml | Matt Brophy | 22 | ["0252132bb7352d685609cb5d7b99fe632f731876","721bee06b9085c57f20c9333cdd327ea81f0376a","12aa08a8756e5af0fdc2ae4eda0ae061cf713311","09024c8a82932bb8b2f1cd8bf3a08222523c9013","482b6a2902dc346b350a3c2d4fcac4e6048ee0cf","6585c8396085b75c7674e3dd1bacde3541b0f539","7b7498e4b7e1fff895d7aab512d11b57fecbdd37","953948ac3b53ac49fdd8028e10acab2587279355","15ad8d531fae7cd3e2d2038cf3c29595d7812ee1","5a43e19573c11d1469fd43ef1fddaf7be02abca5","d6f3a05d4124ae9c1f2f74c599f80d091268ce0c","14666ddd78070ffd6149f7e20371927b784eb054","4aa9298ab35483b1e21e357e7574aa3f0d727725","f153b191e1c52bc8fb0e485bfd5d8ec2a8752104","de0bf8345e6684a671474d992aaff5e7a4040a16","6d945608dc1981a2222cdae5d6a4698602cf852b","45a7b0e4636f45c910c074e5babb66975e8e8652","c5396bd94aacb97c57a6507b1397e08aa57da972","ac399b7b388fdf3474c74eecb363502cb4cc8c9e","cc0779ec9af43e3bfd61e09c0c2d0cb30500989f","4fa24c1b12c7c2ff8f32bb611b8b5b3ac4678c61","fdb90690cb74b1060f9e9de550520f30f9c2ef08"] | 2026-06-04 | 2021-11-05 | 2026-06-04 | 25 | 1696 | 24 | fdb90690cb74b1060f9e9de550520f30f9c2ef08 |
| react-router-7.18.0/.github/ISSUE_TEMPLATE/bug_report.yml | Pedro Cattori | 9 | ["c6c8c3bfe4bce8ce53e61cee5542d88363593a93","4e989f839a6af67a6f339f7726fd0ca58c93689a","f8c9a71581711d7f839fb3d76279a3cc2ed69b6f","acf3f77a3076b55214e8985f7dc758535ac07c5e","d20ba30b1bfb5ea3b96c20af102dc54c8cd8b3b3","eb8be394f4897f0545fa70fe4b0d9c38dc877b85","d2710f8b0e8f17063c0fac9f1fbeeee4e0342479","b5f2e295f2e857edbfd15da236fd9497f1ec13b6","6f313ec32d3078ea4b4e93fa3522325b6a979deb"] | 2025-06-03 | 2021-11-05 | 2026-06-04 | 391 | 1696 | 24 | f8c9a71581711d7f839fb3d76279a3cc2ed69b6f |
| react-router-7.18.0/.github/ISSUE_TEMPLATE/bug_report.yml | Tim Dorr | 3 | ["2375e7956873a311edf8985714e104cdbc0ecb80","129b49aa293f2c084d1c455b4c6f1a87ac4ec552","c299d29c7eeb1b3fc3c1726a5d6ebebdfb74ea4a"] | 2022-03-17 | 2021-11-05 | 2026-06-04 | 1565 | 1696 | 24 | c299d29c7eeb1b3fc3c1726a5d6ebebdfb74ea4a |

[Full data](./List_git_files_with_commit_statistics_by_author.csv)

---

## 7. Data Quality

Files in git log that are unresolved (not found in codebase) or ambiguous (multiple matches). Affects reliability of co-change metrics.

### 7.1 File Resolution Summary

Resolved vs. ambiguous vs. unresolved files by extension.

| resolved | extension | gitFileCount | fileLabels | gitFileExamples |
| --- | --- | --- | --- | --- |
| false | md | 1875 | ["File","Git"] | ["CHANGELOG.md","packages/react-router-dev/CHANGELOG.md","packages/react-router-express/CHANGELOG.md","packages/create-react-router/CHANGELOG.md","packages/react-router-architect/.changes/minor.request-context-domain-name.md","packages/react-router-architect/CHANGELOG.md","packages/react-router-cloudflare/CHANGELOG.md","packages/react-router-dev/.changes/patch.copy-server-watch-config.md","packages/react-router-dev/.changes/patch.ignore-external-server-environments-in-framework-mode-build-hooks.md"] |
| false | js | 1744 | ["File","Git"] | ["examples/multi-app/inbox/messages.js","examples/multi-app/server.js","examples/multi-app/vite.config.js","examples/notes/src/notes.js","examples/ssr-data-router/server.js","examples/ssr-data-router/vite.config.js","examples/ssr/server.js","examples/ssr/vite.config.js","scripts/constants.js"] |
| false | ts | 1131 | ["File","Git"] | ["integration/fog-of-war-test.ts","packages/react-router/__tests__/dom/ssr/fog-of-war-test.ts","packages/react-router/__tests__/rsc/server-test.ts","packages/react-router/__tests__/server-runtime/server-test.ts","scripts/changes/pr.ts","packages/react-router-express/__tests__/server-test.ts","packages/react-router/__tests__/server-runtime/actions-test.ts","integration/rsc/rsc-nojs-test.ts","integration/rsc/rsc-test.ts"] |
| false | tsx | 488 | ["File","Git"] | ["packages/react-router/lib/rsc/browser.tsx","packages/react-router/lib/hooks.tsx","packages/react-router/lib/rsc/server.ssr.tsx","packages/react-router/lib/dom-export/hydrated-router.tsx","packages/react-router/__tests__/dom/data-browser-router-test.tsx","packages/react-router/lib/dom/lib.tsx","packages/react-router/lib/dom/ssr/single-fetch.tsx","packages/react-router/__tests__/resolvePath-test.tsx","packages/react-router/__tests__/useNavigate-test.tsx"] |
| false | json | 272 | ["File","Git"] | ["examples/auth-router-provider/package-lock.json","examples/auth-router-provider/package.json","examples/auth-router-provider/tsconfig.json","examples/auth/package-lock.json","examples/auth/package.json","examples/auth/tsconfig.json","examples/basic-data-router/package-lock.json","examples/basic-data-router/package.json","examples/basic-data-router/tsconfig.json"] |
| false | css | 85 | ["File","Git"] | ["examples/auth-router-provider/src/index.css","examples/auth/src/index.css","examples/basic-data-router/src/index.css","examples/basic/src/index.css","examples/custom-filter-link/src/index.css","examples/custom-link/src/index.css","examples/custom-query-parsing/src/index.css","examples/data-router/src/index.css","examples/error-boundaries/src/index.css"] |
| false | gitignore | 83 | ["File","Git"] | [".gitignore","examples/auth-router-provider/.gitignore","examples/auth/.gitignore","examples/basic-data-router/.gitignore","examples/basic/.gitignore","examples/custom-filter-link/.gitignore","examples/custom-link/.gitignore","examples/custom-query-parsing/.gitignore","examples/data-router/.gitignore"] |
| false | html | 64 | ["File","Git"] | ["examples/auth-router-provider/index.html","examples/auth/index.html","examples/basic-data-router/index.html","examples/basic/index.html","examples/custom-filter-link/index.html","examples/custom-link/index.html","examples/custom-query-parsing/index.html","examples/data-router/index.html","examples/error-boundaries/index.html"] |
| false | ico | 50 | ["File","Git"] | ["playground/performance/public/favicon.ico","integration/helpers/vite-rolldown-template/public/favicon.ico","integration/helpers/vite-8-template/public/favicon.ico","playground/framework-rolldown-vite/public/favicon.ico","playground/framework-vite-6/public/favicon.ico","playground/framework/public/favicon.ico","playground/rsc-vite-7-framework/public/favicon.ico","integration/helpers/rsc-parcel/public/favicon.ico","integration/helpers/rsc-parcel-framework/public/favicon.ico"] |
| false | yml | 44 | ["File","Git"] | ["contributors.yml",".github/workflows/release.yml",".github/ISSUE_TEMPLATE/bug_report.yml",".github/workflows/deduplicate-lock-file.yml",".github/workflows/docs.yml",".github/workflows/format.yml",".github/workflows/integration-full.yml",".github/workflows/preview.yml",".github/workflows/test.yml"] |

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
| json | ["File","TS"] | 13 | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.0/./source/react-router-7.18.0/packages/react-router-serve/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.0/./source/react-router-7.18.0/packages/create-react-router/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.0/./source/react-router-7.18.0/packages/create-react-router/__tests__/fixtures/with-ignored-dir/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.0/./source/react-router-7.18.0/packages/create-react-router/__tests__/fixtures/blank/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.0/./source/react-router-7.18.0/packages/react-router-fs-routes/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.0/./source/react-router-7.18.0/packages/react-router-dev/.reports/jqa/ts-output.json"] |

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
