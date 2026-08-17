---
title: Learning path
status: draft
---

# Learning path

The learning path favors concepts and executable workflows over a sequential
tour of packages. Each chapter should make the next layer of code easier to
read.

The general CMSSW foundations below run in parallel with a focused,
source-driven [timing curriculum](timing-curriculum.md). The two paths are
deliberately connected: timing provides a concrete case study for learning the
framework, while the framework chapters explain why timing data moves and
disappears as it does.

## Foundations

1. [The CMSSW big picture](01-big-picture.md)
2. Framework lifecycle and event processing
3. Python configuration and process construction
4. Event data products, provenance, and dependencies
5. EventSetup, conditions, and intervals of validity

## From concepts to execution

6. Plugin discovery and module construction
7. A complete reconstruction path
8. Geometry and detector description
9. Simulation and digitization
10. Trigger, monitoring, and validation

## What a completed chapter contains

- Learning objectives and prerequisite concepts
- A concise conceptual explanation
- A call-flow or data-flow diagram
- Important C++ symbols and Python configuration objects
- A small runnable or inspectable example
- Source anchors tied to a CMSSW revision
- Review questions and unresolved details
