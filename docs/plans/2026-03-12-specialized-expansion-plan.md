# Specialized Expansion Implementation Plan

> **For Claude:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task.

**Goal:** Expand the repository with three additional high-value specialized prompt guides for Docker, CI/CD, and infrastructure-as-code workflows.

**Architecture:** Keep the current documentation-first structure. Add three new Markdown files under `docs/specialized/`, then update the homepage and the general guide to point to them. Refresh repository metadata only if the new topics meaningfully improve discoverability.

**Tech Stack:** Markdown, GitHub repository conventions

---

### Task 1: Record the expansion design

**Files:**
- Create: `docs/plans/2026-03-12-specialized-expansion-design.md`
- Create: `docs/plans/2026-03-12-specialized-expansion-plan.md`

**Step 1: Document the gap**

Explain why infrastructure and delivery topics are the next best additions.

**Step 2: Lock the scope**

Choose Docker, CI/CD, and Terraform/Ansible as the next three specialized guides.

### Task 2: Add the Docker specialized guide

**Files:**
- Create: `docs/specialized/docker-compose.md`

**Step 1: Cover production-safe Docker design**

Include image design, container runtime assumptions, and configuration hygiene.

**Step 2: Cover troubleshooting and delivery**

Include compose usage, debugging, and production-minded rollout guidance.

### Task 3: Add the CI/CD specialized guide

**Files:**
- Create: `docs/specialized/cicd-github-actions.md`

**Step 1: Cover pipeline design**

Explain how to reason about reliability, secrets, validation, and rollback.

**Step 2: Cover debugging and maintenance**

Include prompts for flaky pipelines, failing checks, and release flow review.

### Task 4: Add the Terraform/Ansible specialized guide

**Files:**
- Create: `docs/specialized/terraform-ansible.md`

**Step 1: Cover IaC structure**

Focus on semantics, state safety, drift, and maintainability.

**Step 2: Cover operational review**

Include prompts for plan review, module design, and rollback-aware execution.

### Task 5: Update repository navigation

**Files:**
- Modify: `README.md`
- Modify: `docs/general/core-prompt-list.md`

**Step 1: Add quick links**

Expose the new specialized guides from the homepage and general overview.

**Step 2: Update examples**

Add examples showing when a user should choose the new guides.

### Task 6: Verify and publish

**Files:**
- Check: `README.md`
- Check: `docs/general/core-prompt-list.md`
- Check: `docs/specialized/*.md`

**Step 1: Run link validation**

Verify all relative Markdown links resolve.

**Step 2: Optionally refresh repo topics**

Add only the tags that clearly improve discoverability.

**Step 3: Commit and push**

Publish the expansion changes.
