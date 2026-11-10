---
title: "Git History Report"
generated: "2026-11-09"
model_version: "v5.0.1"
dataset: "react-router-7.18.5"
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
| react-router-7.18.5 | react-router-7.18.5 |  |  | Matt Brophy | github-actions[bot] | Remix Run Bot | 603 | 1188 | 4933 | 2026-10-27 | 2026-10-27 | 2026-10-27 | 13 | 13 | 12 | fff84b5f20f35c347c9d6313dfc603db0eac6e19 | react-router-7.18.5/typedoc.mjs | 1 | 1 |
| react-router-7.18.5/.agents/skills | .agents/skills | react-router-7.18.5 | react-router-7.18.5 | Matt Brophy | Brooks Lybrand | null | 2 | 7 | 12 | 2026-06-16 | 2026-06-16 | 2026-06-16 | 146 | 145 | 145 | fadd6c490cc84abc560a2413ee6fa0f2617d098d | react-router-7.18.5/.agents/skills/react-router/references/rsc.md | 3 | 2 |
| react-router-7.18.5/.agents/skills/fix-bug | fix-bug | react-router-7.18.5/.agents/skills | skills | Matt Brophy | Brooks Lybrand | null | 2 | 1 | 8 | 2026-03-18 | 2026-06-04 | 2026-06-04 | 158 | 236 | 158 | d6f3a05d4124ae9c1f2f74c599f80d091268ce0c | react-router-7.18.5/.agents/skills/fix-bug/SKILL.md | 4 | 1 |
| react-router-7.18.5/.agents/skills/implement-rfc | implement-rfc | react-router-7.18.5/.agents/skills | skills | Matt Brophy | null | null | 1 | 1 | 4 | 2026-05-07 | 2026-06-04 | 2026-06-04 | 158 | 186 | 158 | fadd6c490cc84abc560a2413ee6fa0f2617d098d | react-router-7.18.5/.agents/skills/implement-rfc/SKILL.md | 4 | 1 |
| react-router-7.18.5/.agents/skills/react-router | react-router | react-router-7.18.5/.agents/skills | skills | Brooks Lybrand | null | null | 1 | 5 | 1 | 2026-06-16 | 2026-06-16 | 2026-06-16 | 146 | 145 | 145 | 8f364c820ef698952e4bed876d6c93c895357692 | react-router-7.18.5/.agents/skills/react-router/references/rsc.md | 4 | 1 |
| react-router-7.18.5/.agents/skills/react-router/references | references | react-router-7.18.5/.agents/skills/react-router | react-router | Brooks Lybrand | null | null | 1 | 4 | 1 | 2026-06-16 | 2026-06-16 | 2026-06-16 | 146 | 145 | 145 | 8f364c820ef698952e4bed876d6c93c895357692 | react-router-7.18.5/.agents/skills/react-router/references/rsc.md | 5 | 1 |
| react-router-7.18.5/.github | .github | react-router-7.18.5 | react-router-7.18.5 | Matt Brophy | Michael Jackson | Michaël De Boey | 22 | 19 | 221 | 2026-05-26 | 2026-06-16 | 2026-06-16 | 146 | 167 | 146 | ff67b74a33c9f13fac28afc4923d0bf5628998ec | react-router-7.18.5/.github/workflows/test.yml | 2 | 1 |
| react-router-7.18.5/.github/ISSUE_TEMPLATE | ISSUE_TEMPLATE | react-router-7.18.5/.github | .github | Matt Brophy | Pedro Cattori | Tim Dorr | 13 | 3 | 51 | 2023-01-11 | 2026-06-04 | 2026-06-04 | 158 | 1398 | 158 | ff67b74a33c9f13fac28afc4923d0bf5628998ec | react-router-7.18.5/.github/ISSUE_TEMPLATE/documentation_isse.yml | 3 | 1 |
| react-router-7.18.5/.github/workflows | workflows | react-router-7.18.5/.github | .github | Matt Brophy | dependabot[bot] | Michael Jackson | 16 | 14 | 182 | 2026-05-26 | 2026-06-16 | 2026-06-16 | 146 | 167 | 146 | ff4c0712f7b24d38f51f7b967d7c31aeac531bed | react-router-7.18.5/.github/workflows/test.yml | 3 | 1 |
| react-router-7.18.5/decisions | decisions | react-router-7.18.5 | react-router-7.18.5 | Matt Brophy | Pedro Cattori | Michael Jackson | 10 | 20 | 69 | 2026-02-19 | 2026-06-04 | 2026-06-04 | 158 | 263 | 158 | ff67b74a33c9f13fac28afc4923d0bf5628998ec | react-router-7.18.5/decisions/template.md | 2 | 1 |

[Full data](./List_git_file_directories_with_commit_statistics.csv)

### 2.2 Directory Commit Statistics (Charts)



---

## 3. Co-Changed Files

Files committed together = logical coupling signal. May belong to the same conceptual unit or share a concern.

### 3.1 Co-Changed File Pairs

| firstFile | secondFile | commitCount |
| --- | --- | --- |
| react-router-7.18.5/packages/react-router-dom/package.json | react-router-7.18.5/packages/react-router/package.json | 351 |
| react-router-7.18.5/packages/react-router/CHANGELOG.md | react-router-7.18.5/packages/react-router/package.json | 182 |
| react-router-7.18.5/packages/react-router-dom/package.json | react-router-7.18.5/packages/react-router/CHANGELOG.md | 180 |
| react-router-7.18.5/packages/react-router/lib/components.tsx | react-router-7.18.5/packages/react-router/lib/hooks.tsx | 91 |
| react-router-7.18.5/packages/react-router/package.json | react-router-7.18.5/contributors.yml | 91 |
| react-router-7.18.5/packages/react-router-dom/package.json | react-router-7.18.5/contributors.yml | 91 |
| react-router-7.18.5/packages/react-router-node/CHANGELOG.md | react-router-7.18.5/packages/react-router-serve/CHANGELOG.md | 89 |
| react-router-7.18.5/packages/react-router-dev/CHANGELOG.md | react-router-7.18.5/packages/react-router-node/CHANGELOG.md | 89 |
| react-router-7.18.5/packages/react-router-dev/CHANGELOG.md | react-router-7.18.5/packages/react-router-serve/CHANGELOG.md | 87 |
| react-router-7.18.5/packages/react-router/CHANGELOG.md | react-router-7.18.5/contributors.yml | 85 |

### 3.2 Co-Changed File Pairs (All in One Commit)

Files changed together in a single large commit.

| firstFile | secondFile | commitCount |
| --- | --- | --- |
| react-router-7.18.5/packages/react-router-dom/package.json | react-router-7.18.5/packages/react-router/package.json | 605 |
| react-router-7.18.5/packages/react-router/CHANGELOG.md | react-router-7.18.5/packages/react-router/package.json | 431 |
| react-router-7.18.5/packages/react-router-dom/package.json | react-router-7.18.5/packages/react-router/CHANGELOG.md | 428 |
| react-router-7.18.5/packages/react-router-node/CHANGELOG.md | react-router-7.18.5/packages/react-router-serve/CHANGELOG.md | 242 |
| react-router-7.18.5/packages/react-router-dev/CHANGELOG.md | react-router-7.18.5/packages/react-router-node/CHANGELOG.md | 242 |
| react-router-7.18.5/packages/react-router-dev/CHANGELOG.md | react-router-7.18.5/packages/react-router-serve/CHANGELOG.md | 240 |
| react-router-7.18.5/packages/react-router-express/CHANGELOG.md | react-router-7.18.5/packages/react-router-node/CHANGELOG.md | 236 |
| react-router-7.18.5/packages/react-router-dev/CHANGELOG.md | react-router-7.18.5/packages/react-router-express/CHANGELOG.md | 235 |
| react-router-7.18.5/packages/react-router-dev/CHANGELOG.md | react-router-7.18.5/packages/react-router/CHANGELOG.md | 234 |
| react-router-7.18.5/packages/react-router-express/CHANGELOG.md | react-router-7.18.5/packages/react-router-serve/CHANGELOG.md | 234 |

### 3.3 Co-Changed With a Specific File

Shows all files that were changed together with another particular file.

| filePath | commitCount | coChangeRate | maxLift | avgLift |
| --- | --- | --- | --- | --- |
| react-router-7.18.5/packages/react-router-dom/package.json | 354 | 0.0004511174714993157 | 2.307398534150291 | 1.3188485198990727 |
| react-router-7.18.5/packages/react-router/CHANGELOG.md | 192 | 0.0006923185097844076 | 1.6124314442413166 | 1.0764629405818527 |
| react-router-7.18.5/contributors.yml | 172 | 0.000644585853589069 | 1.551229686277918 | 0.7068744721713336 |
| react-router-7.18.5/packages/react-router/lib/components.tsx | 156 | 0.0012605856875040403 | 6.0926435877262 | 3.246703512701848 |
| react-router-7.18.5/pnpm-lock.yaml | 150 | 0.0006697475051905432 | 6 | 1.5152910225418408 |
| react-router-7.18.5/packages/react-router/lib/hooks.tsx | 137 | 0.0016589571577341308 | 3.62467480488293 | 1.9980657419600456 |
| react-router-7.18.5/packages/react-router/package.json | 136 | 0.00045263326055700515 | 1.297752808988764 | 0.7106202073680374 |
| react-router-7.18.5/packages/react-router/lib/router/router.ts | 101 | 0.0012013512227614426 | 8.130530973451327 | 2.360833369970133 |
| react-router-7.18.5/packages/react-router-dev/CHANGELOG.md | 96 | 0.0005097164702134438 | 3.357002586454642 | 2.0618834978096037 |
| react-router-7.18.5/packages/react-router-node/CHANGELOG.md | 92 | 0.0009747827929646112 | 3.4760452313643806 | 1.8452901553705439 |

[Full data](./List_git_files_that_were_changed_together_with_another_file.csv)

### 3.4 Co-Changed With a Specific File (All in One)

| filePath | commitCount |
| --- | --- |
| react-router-7.18.5/packages/react-router/package.json | 639 |
| react-router-7.18.5/packages/react-router-dom/package.json | 611 |
| react-router-7.18.5/packages/react-router/CHANGELOG.md | 494 |
| react-router-7.18.5/contributors.yml | 438 |
| react-router-7.18.5/packages/react-router-dev/package.json | 260 |
| react-router-7.18.5/packages/react-router-dev/CHANGELOG.md | 249 |
| react-router-7.18.5/packages/react-router-node/CHANGELOG.md | 245 |
| react-router-7.18.5/packages/react-router-serve/CHANGELOG.md | 242 |
| react-router-7.18.5/packages/react-router-express/CHANGELOG.md | 237 |
| react-router-7.18.5/packages/react-router-architect/CHANGELOG.md | 213 |

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
| 5 | 479 |
| 6 | 289 |
| 7 | 198 |
| 8 | 164 |
| 9 | 104 |
| 10 | 133 |

[Full data](./List_git_files_per_commit_distribution.csv)

### 4.2 Files per Commit Chart



---

## 5. Pairwise Changed Files

Commit overlap counts and dependency info between file pairs.

### 5.1 Pairwise Changed Files

| firstFileName | secondFileName | filePairLineBreak | filePairWithRelativePathLineBreak | filePair | filePairWithRelativePath | firstFileExtension | secondFileExtension | fileExtensionPair | updateCommitCount | updateCommitMinConfidence | updateCommitSupport | updateCommitLift | updateCommitJaccardSimilarity |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| integration/CHANGELOG.md | packages/create-react-router/CHANGELOG.md | CHANGELOG<br>CHANGELOG | integration/CHANGELOG.md<br>packages/create-react-router/CHANGELOG.md | CHANGELOG↔CHANGELOG | integration/CHANGELOG.md↔packages/create-react-router/CHANGELOG.md | md | md | md↔md | 4 | 0.041237113402061855 | 0.0012698412698412698 | 0.6215163024712672 | 0.013245033112582781 |
| packages/react-router-serve/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-serve/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-serve/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 28 | 0.1339712918660287 | 0.008888888888888889 | 1.7957854016084698 | 0.0673076923076923 |
| packages/react-router-node/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-node/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-node/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 28 | 0.1339712918660287 | 0.008888888888888889 | 1.7583732057416266 | 0.0665083135391924 |
| packages/react-router-architect/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-architect/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-architect/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 28 | 0.1339712918660287 | 0.008888888888888889 | 1.788176141432163 | 0.0671462829736211 |
| packages/react-router-fs-routes/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-fs-routes/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-fs-routes/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 28 | 0.1339712918660287 | 0.008888888888888889 | 1.8348242146869147 | 0.0681265206812652 |
| packages/react-router-dev/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-dev/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-dev/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 28 | 0.1339712918660287 | 0.008888888888888889 | 1.3613211915419046 | 0.05702647657841141 |
| packages/react-router-cloudflare/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-cloudflare/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-cloudflare/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 28 | 0.1339712918660287 | 0.008888888888888889 | 1.7731494511680268 | 0.06682577565632458 |
| packages/create-react-router/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/create-react-router/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/create-react-router/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 28 | 0.1339712918660287 | 0.008888888888888889 | 1.8348242146869147 | 0.0681265206812652 |
| packages/react-router-dom/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-dom/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-dom/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 28 | 0.1339712918660287 | 0.008888888888888889 | 0.627057309625543 | 0.03278688524590164 |
| packages/react-router-express/package.json | packages/create-react-router/CHANGELOG.md | package<br>CHANGELOG | packages/react-router-express/package.json<br>packages/create-react-router/CHANGELOG.md | package↔CHANGELOG | packages/react-router-express/package.json↔packages/create-react-router/CHANGELOG.md | json | md | json↔md | 28 | 0.1339712918660287 | 0.008888888888888889 | 1.788176141432163 | 0.0671462829736211 |

[Full data](./List_pairwise_changed_files.csv)

### 5.2 Pairwise Changed Files (Top by Lift)

File pairs that co-change more often than random chance (lift > 1).

| fileExtensionPair | firstFileNameShort | secondFileNameShort | updateCommitCount | updateCommitMinConfidence | updateCommitLift | updateCommitJaccardSimilarity | updateCommitSupport | firstFileName | secondFileName |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ts↔ts | actions-test | actions | 3 | 0.5 | 175.00000000000003 | 0.25 | 0.0009523809523809524 | packages/react-router/__tests__/server-runtime/actions-test.ts | packages/react-router/lib/actions.ts |
| ts↔ts | vite-dev-custom-entry-test | vite-absolute-base-test | 3 | 1 | 157.5 | 0.15 | 0.0009523809523809524 | integration/vite-dev-custom-entry-test.ts | integration/vite-absolute-base-test.ts |
| ts↔ts | vite-loader-context-test | vite-node-env-test | 4 | 0.8 | 148.23529411764704 | 0.2222222222222222 | 0.0012698412698412698 | integration/vite-loader-context-test.ts | integration/vite-node-env-test.ts |
| ts↔ts | sessions-test | sessions | 3 | 0.375 | 118.12499999999999 | 0.2 | 0.0009523809523809524 | packages/react-router/__tests__/server-runtime/sessions-test.ts | packages/react-router/lib/server-runtime/sessions.ts |
| ts↔ts | remove-exports-test | remove-exports | 4 | 0.36363636363636365 | 104.13223140495867 | 0.2222222222222222 | 0.0012698412698412698 | packages/react-router-dev/vite/remove-exports-test.ts | packages/react-router-dev/vite/remove-exports.ts |
| ts↔ts | vite-dotenv-test | vite-node-env-test | 4 | 0.8 | 93.33333333333333 | 0.14285714285714285 | 0.0012698412698412698 | integration/vite-dotenv-test.ts | integration/vite-node-env-test.ts |
| ts↔ts | fileStorage | sessions-test | 3 | 0.3 | 85.9090909090909 | 0.16666666666666666 | 0.0009523809523809524 | packages/react-router-node/sessions/fileStorage.ts | packages/react-router-node/__tests__/sessions-test.ts |
| ts↔ts | routes | routes | 3 | 0.75 | 81.46551724137932 | 0.1 | 0.0009523809523809524 | packages/react-router-dev/config/routes.ts | packages/react-router-dev/routes.ts |
| ts↔ts | vite-server-bundles-test | vite-node-env-test | 5 | 1 | 75 | 0.11904761904761904 | 0.0015873015873015873 | integration/vite-server-bundles-test.ts | integration/vite-node-env-test.ts |
| ts↔ts | vite-dot-server-test | vite-node-env-test | 5 | 1 | 73.25581395348837 | 0.11627906976744186 | 0.0015873015873015873 | integration/vite-dot-server-test.ts | integration/vite-node-env-test.ts |

[Full data](./List_pairwise_changed_files_top_lift.csv)

### 5.3 Pairwise Changed Files With Dependencies

Files that are co-changed and also have a structural dependency relationship between them.

| dependencyWeight | fileDistance | commitCount | updateCommitMinConfidence | updateCommitSupport | updateCommitLift | updateCommitJaccardSimilarity |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | 5 | 3 | 0.07317073170731707 | 0.0009523809523809524 | 1.0198575437081803 | 0.011363636363636364 |
| 1 | 6 | 3 | 0.15 | 0.0009523809523809524 | 5.558823529411764 | 0.029411764705882353 |
| 1 | 4 | 4 | 0.16 | 0.0012698412698412698 | 2.2105263157894735 | 0.01606425702811245 |
| 1 | 4 | 9 | 0.36 | 0.002857142857142857 | 37.800000000000004 | 0.1956521739130435 |
| 2 | 5 | 3 | 0.07317073170731707 | 0.0009523809523809524 | 1.0109114249037228 | 0.011278195488721804 |
| 2 | 5 | 9 | 0.140625 | 0.002857142857142857 | 1.9428453947368423 | 0.03180212014134275 |
| 2 | 0 | 9 | 0.36 | 0.002857142857142857 | 8.790697674418604 | 0.06206896551724138 |
| 3 | 0 | 3 | 0.058823529411764705 | 0.0009523809523809524 | 2.8952205882352944 | 0.026785714285714284 |
| 3 | 4 | 9 | 0.06976744186046512 | 0.002857142857142857 | 0.9638922888616892 | 0.02586206896551724 |
| 6 | 4 | 3 | 0.13636363636363635 | 0.0009523809523809524 | 1.8839712918660285 | 0.012145748987854251 |

[Full data](./List_pairwise_changed_files_with_dependencies.csv)

### 5.4 Pairwise Changed Files (Charts)



---

## 6. Files by Author

Per-author file commit stats. Useful for knowledge boundaries and bus-factor risk.

### 6.1 Files with Commit Statistics by Author

| filePath | author | commitCount | commitHashes | lastCommitDate | lastCreationDate | lastModificationDate | daysSinceLastCommit | daysSinceLastCreation | daysSinceLastModification | maxCommitSha |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| react-router-7.18.5/.agents/skills/fix-bug/SKILL.md | Matt Brophy | 7 | ["2469dd6621fbcaec689571c3f003af5711bc54de","a842fca719e81505f454a8e6a8c728cdaed22067","06c1149bc0b4f50db0cc6fc10471b4ad963b8969","1497c6ba52e55158e4f12b54617b1255935c75d5","46321cf2767cb820c1be8bbea3bafbc32c6c4ffd","d6f3a05d4124ae9c1f2f74c599f80d091268ce0c","963affeb924f2256bd20c0c5c87e4c4b4fcbd188"] | 2026-06-04 | 2026-03-18 | 2026-06-04 | 158 | 236 | 158 | d6f3a05d4124ae9c1f2f74c599f80d091268ce0c |
| react-router-7.18.5/.agents/skills/fix-bug/SKILL.md | Brooks Lybrand | 1 | ["4f8fff6cdb31c549fd011ac516fad5ad2e641b5f"] | 2026-05-29 | 2026-03-18 | 2026-06-04 | 164 | 236 | 158 | 4f8fff6cdb31c549fd011ac516fad5ad2e641b5f |
| react-router-7.18.5/.agents/skills/implement-rfc/SKILL.md | Matt Brophy | 4 | ["522bc1b8cd0d7b3565bf9193789f2b7d5503856b","fadd6c490cc84abc560a2413ee6fa0f2617d098d","a6ab746a43675332ec3c190b1390724bf5c833db","d6f3a05d4124ae9c1f2f74c599f80d091268ce0c"] | 2026-06-04 | 2026-05-07 | 2026-06-04 | 158 | 186 | 158 | fadd6c490cc84abc560a2413ee6fa0f2617d098d |
| react-router-7.18.5/.agents/skills/react-router/SKILL.md | Brooks Lybrand | 1 | ["8f364c820ef698952e4bed876d6c93c895357692"] | 2026-06-16 | 2026-06-16 | 2026-06-16 | 146 | 145 | 145 | 8f364c820ef698952e4bed876d6c93c895357692 |
| react-router-7.18.5/.agents/skills/react-router/references/data-mode.md | Brooks Lybrand | 1 | ["8f364c820ef698952e4bed876d6c93c895357692"] | 2026-06-16 | 2026-06-16 | 2026-06-16 | 146 | 145 | 145 | 8f364c820ef698952e4bed876d6c93c895357692 |
| react-router-7.18.5/.agents/skills/react-router/references/declarative-mode.md | Brooks Lybrand | 1 | ["8f364c820ef698952e4bed876d6c93c895357692"] | 2026-06-16 | 2026-06-16 | 2026-06-16 | 146 | 145 | 145 | 8f364c820ef698952e4bed876d6c93c895357692 |
| react-router-7.18.5/.agents/skills/react-router/references/framework-mode.md | Brooks Lybrand | 1 | ["8f364c820ef698952e4bed876d6c93c895357692"] | 2026-06-16 | 2026-06-16 | 2026-06-16 | 146 | 145 | 145 | 8f364c820ef698952e4bed876d6c93c895357692 |
| react-router-7.18.5/.agents/skills/react-router/references/rsc.md | Brooks Lybrand | 1 | ["8f364c820ef698952e4bed876d6c93c895357692"] | 2026-06-16 | 2026-06-16 | 2026-06-16 | 146 | 145 | 145 | 8f364c820ef698952e4bed876d6c93c895357692 |
| react-router-7.18.5/.browserslistrc | Michael Jackson | 3 | ["82c500c4a1a5d53a608faee25f8322c661b242a1","b3f728487ae6fe7d5ef4ddc759fb2a4ca0df712e","f6df0697e1b2064a2b3a12e8b39577326fdd945b"] | 2021-09-09 | 2018-10-30 | 2021-09-09 | 1887 | 2931 | 1886 | f6df0697e1b2064a2b3a12e8b39577326fdd945b |
| react-router-7.18.5/.browserslistrc | Matt Brophy | 1 | ["4fa24c1b12c7c2ff8f32bb611b8b5b3ac4678c61"] | 2024-03-27 | 2018-10-30 | 2021-09-09 | 957 | 2931 | 1886 | 4fa24c1b12c7c2ff8f32bb611b8b5b3ac4678c61 |

[Full data](./List_git_files_with_commit_statistics_by_author.csv)

---

## 7. Data Quality

Files in git log that are unresolved (not found in codebase) or ambiguous (multiple matches). Affects reliability of co-change metrics.

### 7.1 File Resolution Summary

Resolved vs. ambiguous vs. unresolved files by extension.

| resolved | extension | gitFileCount | fileLabels | gitFileExamples |
| --- | --- | --- | --- | --- |
| false | md | 1892 | ["File","Git"] | ["CHANGELOG.md","packages/create-react-router/CHANGELOG.md","packages/react-router-architect/CHANGELOG.md","packages/react-router-cloudflare/CHANGELOG.md","packages/react-router-dev/CHANGELOG.md","packages/react-router-dom/CHANGELOG.md","packages/react-router-express/CHANGELOG.md","packages/react-router-fs-routes/CHANGELOG.md","packages/react-router-node/CHANGELOG.md"] |
| false | js | 1744 | ["File","Git"] | ["examples/multi-app/inbox/messages.js","examples/multi-app/server.js","examples/multi-app/vite.config.js","examples/notes/src/notes.js","examples/ssr-data-router/server.js","examples/ssr-data-router/vite.config.js","examples/ssr/server.js","examples/ssr/vite.config.js","scripts/constants.js"] |
| false | ts | 1134 | ["File","Git"] | ["integration/fog-of-war-test.ts","integration/rsc/route-discovery-test.ts","packages/react-router/__tests__/dom/ssr/fog-of-war-test.ts","packages/react-router/__tests__/rsc/server-test.ts","integration/rsc/rsc-nojs-test.ts","integration/rsc/rsc-test.ts","packages/react-router/__tests__/vendor/turbo-stream-test.ts","packages/react-router/__tests__/router/view-transition-test.ts","scripts/changes/pr.ts"] |
| false | tsx | 489 | ["File","Git"] | ["packages/react-router/lib/rsc/server.ssr.tsx","packages/react-router/__tests__/external-navigation-test.tsx","packages/react-router/__tests__/useNavigate-test.tsx","packages/react-router/lib/components.tsx","packages/react-router/lib/hooks.tsx","packages/react-router/lib/rsc/browser.tsx","packages/react-router/__tests__/dom/link-href-test.tsx","packages/react-router/lib/dom/lib.tsx","packages/react-router/lib/dom/server.tsx"] |
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
| json | ["File","TS"] | 13 | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.5/./source/react-router-7.18.5/packages/react-router-cloudflare/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.5/./source/react-router-7.18.5/packages/react-router-architect/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.5/./source/react-router-7.18.5/packages/react-router-dom/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.5/./source/react-router-7.18.5/packages/create-react-router/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.5/./source/react-router-7.18.5/packages/create-react-router/__tests__/fixtures/with-ignored-dir/.reports/jqa/ts-output.json","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.5/./source/react-router-7.18.5/packages/create-react-router/__tests__/fixtures/blank/.reports/jqa/ts-output.json"] |

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
