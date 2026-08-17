---
title: Contributing knowledge
---

# Contributing knowledge

## Capture, then distill

During an investigation, capture rough findings without interrupting the work.
Afterward, move durable conclusions into architecture, workflow, subsystem, or
debugging notes.

## Note metadata

Use front matter where applicable:

```yaml
---
title: Descriptive title
area: framework
cmssw_release: CMSSW_X_Y_Z
verified_commit: full-git-commit
last_verified: YYYY-MM-DD
status: draft
---
```

Recommended status values are `draft`, `verified`, `needs-review`, and
`obsolete`.

## Evidence standard

For a durable technical claim:

1. Link to or name the relevant file and symbol.
2. Record the CMSSW commit or release.
3. Prefer a representative test or configuration that demonstrates behavior.
4. Distinguish verified behavior from inference or an open question.

## Build check

Before publishing, run:

```bash
mkdocs build --strict
```
