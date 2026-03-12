# AI Prompt Template Repository Implementation Plan

> **For Claude:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task.

**Goal:** Build an open-source-ready GitHub template repository from the existing prompt list and expand it with six specialized prompt collections.

**Architecture:** Keep a lightweight Markdown-first repository. Use `README.md` as the main navigation hub, move long-form content into `docs/general/` and `docs/specialized/`, and add a few standard repository files for open-source collaboration.

**Tech Stack:** Markdown, GitHub repository conventions

---

### Task 1: Create the repository structure

**Files:**
- Create: `README.md`
- Create: `.gitignore`
- Create: `LICENSE`
- Create: `CONTRIBUTING.md`
- Create: `docs/general/core-prompt-list.md`
- Create: `docs/specialized/`

**Step 1: Define the file layout**

Create a root-level open-source repository structure with a documentation-first organization.

**Step 2: Add the basic repository files**

Write the minimal standard files needed for GitHub publishing and contribution guidance.

**Step 3: Verify the directory structure**

Confirm all planned directories and root files exist and are named consistently.

### Task 2: Normalize the main prompt collection

**Files:**
- Modify: `AI编程高频增强提示词清单_2026-03-10.md`
- Create: `docs/general/core-prompt-list.md`

**Step 1: Preserve the original source**

Keep the existing file intact as the original source material.

**Step 2: Create a repository-ready general document**

Move the main content into a clearer GitHub-facing document under `docs/general/`.

**Step 3: Align headings and navigation anchors**

Use predictable headings so README links are stable and easy to maintain.

### Task 3: Write the specialized prompt documents

**Files:**
- Create: `docs/specialized/kubernetes.md`
- Create: `docs/specialized/nginx.md`
- Create: `docs/specialized/shell-bash.md`
- Create: `docs/specialized/python-automation.md`
- Create: `docs/specialized/windows-server-automation.md`
- Create: `docs/specialized/agent-coding-clients.md`

**Step 1: Reuse the established writing format**

For each specialized file, use Chinese explanations and English prompts.

**Step 2: Focus on real engineering scenarios**

Include prompts that match operations, debugging, implementation, review, and documentation tasks relevant to the domain.

**Step 3: Keep the documents independently usable**

Each file should be readable on its own without requiring the main list for context.

### Task 4: Build the README navigation

**Files:**
- Create: `README.md`

**Step 1: Explain what the repository is**

State the purpose, target audience, and formatting rules.

**Step 2: Add quick navigation sections**

Provide direct links to the core list and every specialized document.

**Step 3: Add usage guidance**

Show the basic copy-paste usage pattern and explain how users can extend it.

### Task 5: Validate repository consistency

**Files:**
- Check: `README.md`
- Check: `docs/general/core-prompt-list.md`
- Check: `docs/specialized/*.md`

**Step 1: Check all internal links**

Verify that the README links point to existing files.

**Step 2: Check heading consistency**

Ensure the document titles and section styles match the current Markdown tone.

**Step 3: Review for release readiness**

Confirm the repository reads cleanly as a GitHub open-source starter.
