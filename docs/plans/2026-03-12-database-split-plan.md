# Database Split Implementation Plan

> **For Claude:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task.

**Goal:** Add dedicated SQL and NoSQL specialized prompt guides and expose them from the repository navigation.

**Architecture:** Keep the current docs-first repository structure. Add two new specialized Markdown files for SQL and NoSQL workflows, then update `README.md` and `docs/general/core-prompt-list.md` to link to them. Refresh repository topics only if they materially improve discoverability.

**Tech Stack:** Markdown, GitHub repository conventions

---

### Task 1: Record the split rationale

**Files:**
- Create: `docs/plans/2026-03-12-database-split-design.md`
- Create: `docs/plans/2026-03-12-database-split-plan.md`

**Step 1: Document why one database guide is too broad**

Explain the practical difference between SQL and NoSQL engineering concerns.

**Step 2: Lock the chosen scope**

Choose two specialized files: one for SQL and one for NoSQL.

### Task 2: Add the SQL specialized guide

**Files:**
- Create: `docs/specialized/sql-database.md`

**Step 1: Cover schema and query design**

Include prompts for table design, indexing, transactions, and query correctness.

**Step 2: Cover performance and operational work**

Include prompts for slow queries, migrations, and production-safe changes.

### Task 3: Add the NoSQL specialized guide

**Files:**
- Create: `docs/specialized/nosql-database.md`

**Step 1: Cover data modeling and scaling**

Include prompts for partitioning, replication, consistency, and access-pattern design.

**Step 2: Cover debugging and operations**

Include prompts for hotspots, capacity, backup, and recovery-minded execution.

### Task 4: Update repository navigation

**Files:**
- Modify: `README.md`
- Modify: `docs/general/core-prompt-list.md`

**Step 1: Add quick links**

Expose both new guides from the homepage and general overview.

**Step 2: Update usage cues**

Show when a user should choose SQL versus NoSQL.

### Task 5: Verify and publish

**Files:**
- Check: `README.md`
- Check: `docs/general/core-prompt-list.md`
- Check: `docs/specialized/*.md`

**Step 1: Run link validation**

Verify all relative Markdown links resolve.

**Step 2: Refresh repository topics if useful**

Add `database`, `sql`, and `nosql` only if they improve searchability.

**Step 3: Commit and push**

Publish the changes to GitHub.
