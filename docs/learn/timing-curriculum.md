---
title: Timing curriculum
description: A layered learning path for Phase-II MTD and HGCAL timing in CMSSW
---

# Timing curriculum

This curriculum alternates between CMSSW foundations and repeated passes
through the timing chain. ETL and HGCAL receive first attention because the
initial use case is forward jets and track–calorimeter timing; BTL remains in
the comparison set so common and detector-specific behavior stay visible.

## Pass 1 — Build the map

**Goal:** recognize the major products and say which stage owns each value.

1. SIM hits and the meaning of detector arrival time
2. BTL/ETL and HGCAL digitization
3. Uncalibrated and calibrated rec hits
4. MTD clusters, tracks, and time-of-flight PID
5. HGCAL layer clusters, tracksters, TICL candidates, and PF candidates
6. Event content and the first persistence map

Start with [Timing in CMSSW](../timing/index.md), then keep the
[product inventory](../timing/inventory.md) beside the source tree.

## Pass 2 — Learn the framework through timing

**Goal:** understand why the chain is wired as it is.

1. `edm::EDProducer`, tokens, handles, and product provenance
2. Python `Task` and `Sequence` composition
3. data-product ownership and `ValueMap` associations
4. EventSetup records for geometry and calibration
5. era and process modifiers for Phase-II configurations
6. output commands, dropped products, and data-tier policy

Each topic should be tested against one MTD example and one HGCAL example.

## Pass 3 — Recover exact time semantics

**Goal:** attach a reference point and uncertainty model to every field.

1. simulation time, bunch crossing, and time-of-flight conventions
2. threshold crossing, ToA/ToT encoding, LSBs, saturation, and invalid codes
3. time walk, clock terms, smearing, and quantization
4. local rec-hit calibration and detector geometry corrections
5. cluster-time estimators and outlier rejection
6. track path length, mass hypotheses, beamline `t0`, and PID probabilities
7. HGCAL trackster time and origin correction in TICL

At the end of this pass, create a common-reference table. Do not align values
merely because they are measured in nanoseconds.

## Pass 4 — Audit information survival

**Goal:** know which measurements an analysis or tagger can actually consume.

1. compare SIM, DIGI, FEVT, RECO, and AOD event content;
2. trace associations needed to join time back to tracks and calorimeter
   objects;
3. audit MiniAOD and NanoAOD separately;
4. measure multiplicity, serialized size, and production CPU;
5. classify losses as compression, aggregation, missing association, or an
   output-command decision.

## Pass 5 — Prepare safe contributions

**Goal:** turn an information gap into a minimal, reviewable CMSSW change.

1. define the physics meaning and consumer before the storage type;
2. reuse an existing product or association where it preserves semantics;
3. specify invalid values, uncertainty, calibration provenance, and versioning;
4. estimate CPU and bytes per event;
5. add focused unit/integration tests and validation plots;
6. demonstrate synchronization across BTL, ETL, and HGCAL references;
7. document data-tier and backward-compatibility consequences.

## Chapter template

Every new timing chapter should contain:

- a one-paragraph physical model;
- a data-flow or call-flow diagram;
- a product-field table with units and invalid values;
- producer and configuration anchors pinned to a CMSSW commit;
- persistence and association status;
- one inspectable or runnable verification recipe;
- established facts, inferences, and open questions kept separate.
