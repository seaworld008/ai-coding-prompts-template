# README Structure Redesign Implementation Plan

> **For Claude:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task.

**Goal:** Reorganize the README into a clearer engineering homepage with a cleaner reading flow for new users and maintainers.

**Architecture:** Keep the README content largely intact, but reorder sections into a clearer path: overview, guide selection, getting started, examples, deeper navigation, and repository maintenance details. Add only small bridging edits where needed.

**Tech Stack:** Markdown, GitHub repository conventions

---

### Task 1: Record the redesign

**Files:**
- Create: `docs/plans/2026-03-12-readme-structure-design.md`
- Create: `docs/plans/2026-03-12-readme-structure-plan.md`

**Step 1: Capture the current weakness**

Describe why the README is already useful but not optimally ordered.

**Step 2: Lock the new structure**

Document the final reading sequence for the homepage.

### Task 2: Reorder the README

**Files:**
- Modify: `README.md`

**Step 1: Move choice guidance earlier**

Keep the selection matrix near the top so readers find the right guide quickly.

**Step 2: Move usage before repository mechanics**

Let readers learn how to use the repository before seeing maintenance and structure details.

**Step 3: Move maintenance material later**

Place installation, prerequisites, structure, contribution, and design records after the user-facing usage flow.

### Task 3: Verify and publish

**Files:**
- Check: `README.md`

**Step 1: Run Markdown link validation**

Ensure the reordered README does not break any links.

**Step 2: Commit and push**

Publish the README structure update to the remote repository.
