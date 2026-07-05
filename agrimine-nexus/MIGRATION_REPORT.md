# AgriMine Nexus — Repository Migration Report (ACT-005, Part A)

> **Goal:** separate the AgriMine Nexus project from the hydrology repository into a dedicated repository (`agrimine-nexus-research`), preserving commit history, folder structure, and all governance/engine/knowledge assets, and make it the single source of truth.

---

## 1. Status & environment constraint

**Automated remote-repo creation is not possible from this cloud-agent environment.** The GitHub CLI here is **read-only** (it can view but not create/modify GitHub resources), and the available PR tooling only operates on the *current* repository. Creating a new GitHub repository and pushing to it therefore requires a step run by a maintainer (or a write-enabled environment).

What has been done here to make that final step trivial and safe:
- Verified a **history-preserving extraction** of the `agrimine-nexus/` subtree (validated below).
- Confirmed the `agrimine-nexus/` tree is **fully self-contained** (all internal links are relative and stay valid when the folder becomes the repository root).
- Prepared a ready-to-push **export branch** and exact commands (below).

## 2. What migrates

Everything under `agrimine-nexus/` becomes the root of the new repo:

```
CITATION_STANDARD.md · ROM_Internalisation.md · MREP_Internalisation.md · README.md
research-engine/ · knowledge-repository/ · templates/ · activity-log/ · source/
MIGRATION_REPORT.md
```

Governance documents, templates, knowledge repository, research engine, work-package tracker, activity logs, and citation standard are all included. The hydrology files at the current repo root (`revisio_summaries`, `hydrology_2026_smart_notebook.ipynb`, etc.) are **not** part of AgriMine Nexus and stay in the hydrology repo.

## 3. History-preservation validation (already run)

Using `git subtree split --prefix=agrimine-nexus`:
- **11 commits** touch `agrimine-nexus/`; the split produced a rewritten history of **11 commits** with the project contents at the tree root — history preserved.
- Verified split-tree root contains all project folders (`research-engine`, `knowledge-repository`, `templates`, `activity-log`, `source`, and the governance docs).

## 4. Migration procedure (run by a maintainer with GitHub write access)

### Path A — `git subtree split` (recommended, no extra tooling)
```bash
# 1. From a clone of the hydrology repo, on the branch that holds the AgriMine Nexus work:
git checkout cursor/agrimine-rom-internalisation-9a65   # or main once merged

# 2. Extract the project into a standalone branch with preserved history:
git subtree split --prefix=agrimine-nexus -b agrimine-nexus-main

# 3. Create the new EMPTY GitHub repo named 'agrimine-nexus-research'
#    (via GitHub UI or:  gh repo create agrimine-nexus-research --private )

# 4. Push the extracted history as 'main' of the new repo:
git push git@github.com:<owner>/agrimine-nexus-research.git agrimine-nexus-main:main
```

### Path B — `git filter-repo` (cleanest full-history rewrite)
```bash
git clone <hydrology-repo-url> agrimine-nexus-research && cd agrimine-nexus-research
git filter-repo --subdirectory-filter agrimine-nexus
git remote add origin git@github.com:<owner>/agrimine-nexus-research.git
git push -u origin main
```

> A ready-made export branch **`cursor/agrimine-nexus-export-9a65`** (produced by Path A from the latest project commit) has been pushed to the current remote as a convenience — a maintainer can push it straight to the new repo's `main` (step 4 above) without re-running the split.

## 5. Cleanup of the hydrology repository (after the new repo is confirmed)
```bash
# On the hydrology repo, remove the AgriMine Nexus folder:
git rm -r agrimine-nexus
git commit -m "Move AgriMine Nexus to dedicated agrimine-nexus-research repository"
git push
```
Add a pointer to the hydrology `README.md`: *"AgriMine Nexus has moved to the `agrimine-nexus-research` repository."*

## 6. Internal links & README
- All internal links within `agrimine-nexus/` are **relative** (`../…`, `source/…`, `knowledge-repository/…`) and remain valid once the folder is the repo root.
- `agrimine-nexus/README.md` is written to serve as the **root README** of the new repository (project overview, governance, engine, knowledge repo, activity log, current position).
- No links point outside `agrimine-nexus/`, so nothing breaks on extraction.

## 7. Single source of truth
Once Path A/B completes and cleanup is done, `agrimine-nexus-research` is the **sole** home of the project. All future activity records, work packages, and commits target that repository.

## 8. Outstanding action (requires write access)
- [ ] Create GitHub repo `agrimine-nexus-research`.
- [ ] Push extracted history to its `main` (use the prepared export branch).
- [ ] Remove `agrimine-nexus/` from the hydrology repo and add a pointer.
- [ ] Confirm links render on the new repo and update any absolute references if introduced later.
