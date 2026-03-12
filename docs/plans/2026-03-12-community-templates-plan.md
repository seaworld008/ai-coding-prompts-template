# Community Templates Implementation Plan

> **For Claude:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task.

**Goal:** Add GitHub community collaboration templates so the repository is easier to contribute to and maintain as a public project.

**Architecture:** Use GitHub-native template files under `.github/ISSUE_TEMPLATE/`, add a root-level PR template, and complement them with simple support and maintainers documents. Update `README.md` with links to the new collaboration entry points.

**Tech Stack:** Markdown, YAML, GitHub repository conventions

---

### Task 1: Record the design

**Files:**
- Create: `docs/plans/2026-03-12-community-templates-design.md`
- Create: `docs/plans/2026-03-12-community-templates-plan.md`

**Step 1: Capture repository-specific needs**

Describe why this project needs content-oriented issue templates instead of only software bug forms.

**Step 2: Lock in the recommended scope**

Choose the smallest complete set of community templates.

### Task 2: Add GitHub issue templates

**Files:**
- Create: `.github/ISSUE_TEMPLATE/bug_report.yml`
- Create: `.github/ISSUE_TEMPLATE/feature_request.yml`
- Create: `.github/ISSUE_TEMPLATE/prompt_submission.yml`
- Create: `.github/ISSUE_TEMPLATE/config.yml`

**Step 1: Create a bug report form**

Collect practical information about broken content, broken links, or misleading guidance.

**Step 2: Create a feature request form**

Collect ideas for new prompt categories, specialized guides, or repository improvements.

**Step 3: Create a prompt submission form**

Make it easy for contributors to propose new prompt entries in the repository's style.

### Task 3: Add collaboration support files

**Files:**
- Create: `.github/pull_request_template.md`
- Create: `SUPPORT.md`
- Create: `MAINTAINERS.md`

**Step 1: Add a practical PR template**

Guide contributors to explain scope, affected docs, and validation.

**Step 2: Add support guidance**

Explain where users should ask for help and where they should file issues.

**Step 3: Add maintainers guidance**

Document the current ownership model in a lightweight way.

### Task 4: Update README and publish

**Files:**
- Modify: `README.md`

**Step 1: Add collaboration entry points**

Link the new support and maintainer docs from the homepage.

**Step 2: Verify links and push**

Run link validation, commit, and push the changes.
