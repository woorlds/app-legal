# Lorumi Legal Pages Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Publish Lorumi-specific privacy and support pages using the existing Putly page structure.

**Architecture:** Add two static HTML documents under a new `lorumi` directory and connect them from the existing site index and README. Reuse the shared stylesheet and describe only behavior evidenced by the Lorumi implementation.

**Tech Stack:** Static HTML, CSS, GitHub Pages, shell-based structural validation

## Global Constraints

- Preserve Putly's directory structure, HTML layout, shared stylesheet, navigation pattern, and English-language tone.
- Reuse `shared/style.css` without modification.
- Use `woorlds@gmail.com` for contact.
- Describe local recording, transcription, Apple on-device Foundation Models feedback, protected backup-excluded storage, and in-app deletion accurately.
- Do not claim accounts, analytics, advertising, developer-operated servers, or sale of user data.

---

### Task 1: Lorumi Privacy, Support, and Navigation

**Files:**
- Create: `lorumi/privacy/index.html`
- Create: `lorumi/support/index.html`
- Modify: `index.html`
- Modify: `README.md`
- Test: shell structural and link checks

**Interfaces:**
- Consumes: `shared/style.css` and existing Putly HTML structure
- Produces: `/lorumi/privacy/` and `/lorumi/support/` GitHub Pages routes

- [ ] **Step 1: Run a failing structural check**

```bash
test -f lorumi/privacy/index.html && test -f lorumi/support/index.html
```

Expected: FAIL because neither Lorumi page exists.

- [ ] **Step 2: Create the privacy and support pages**

Create semantic English HTML pages with `../../shared/style.css`, Lorumi-specific data handling, microphone and runtime troubleshooting, deletion guidance, contact email, and the public privacy URL.

- [ ] **Step 3: Add navigation and README links**

Add a Lorumi app item to `index.html` and these exact URLs to `README.md`:

```text
https://woorlds.github.io/app-legal/lorumi/privacy/
https://woorlds.github.io/app-legal/lorumi/support/
```

- [ ] **Step 4: Run structural and content verification**

```bash
test -f lorumi/privacy/index.html
test -f lorumi/support/index.html
rg -q './lorumi/privacy/' index.html
rg -q './lorumi/support/' index.html
rg -q 'app-legal/lorumi/privacy/' README.md
rg -q 'app-legal/lorumi/support/' README.md
rg -q '../../shared/style.css' lorumi/privacy/index.html
rg -q '../../shared/style.css' lorumi/support/index.html
rg -q 'on-device' lorumi/privacy/index.html
rg -q 'Apple Intelligence' lorumi/support/index.html
git diff --check
```

Expected: every command exits successfully with no output from `git diff --check`.

- [ ] **Step 5: Inspect links and commit**

Use an HTML parser to confirm that every local link target exists, inspect the final diff for unrelated changes, and commit the four page changes plus this plan.

- [ ] **Step 6: Push and verify remote state**

Push the current branch to its configured upstream and verify the remote branch resolves to the new commit.
