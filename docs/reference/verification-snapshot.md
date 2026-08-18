---
title: Verification snapshot
description: Exact source revision, evidence policy, and known gaps
---

# Verification snapshot

## Current CMSSW baseline

| Item | Value |
| --- | --- |
| Repository | [`cms-sw/cmssw`](https://github.com/cms-sw/cmssw) |
| Branch | `master` |
| Commit | [`f1ac1dbe1f36762b14843b1fb906971de43a1044`](https://github.com/cms-sw/cmssw/commit/f1ac1dbe1f36762b14843b1fb906971de43a1044) |
| Commit subject | `Merge pull request #51708 from makortel/fixActivityRegistryDoc` |
| Checkout state | clean and aligned with `origin/master` when audited |
| Audit date | 17 August 2026 |

All CMSSW source links in the initial timing inventory are pinned to this
commit. The code—not this prose—is authoritative.

## External design references

- [CMS MIP Timing Detector Technical Design Report](https://cds.cern.ch/record/2667167)
  (`CERN-LHCC-2019-003`, `CMS-TDR-020`)
- [CMS High Granularity Calorimeter Technical Design Report](https://cds.cern.ch/record/2293646)
  (`CERN-LHCC-2017-023`, `CMS-TDR-019`)

These documents provide detector motivation and design context. They should not
be used to infer the exact behavior of current CMSSW without checking source and
configuration.

## Method used for the first audit

The initial trace followed data types, producer declarations, algorithm calls,
Python task composition, and event-content keep rules. It covered MTD device and
electronics simulation, local MTD reconstruction, track extension and TOF PID,
HGCAL digitization and local reconstruction, layer-cluster timing, trackster
timing, TICL candidate combination, and PF transfer.

## Known gaps

- no runtime event dump has yet validated the static source trace;
- standard DIGI output content has not yet been reduced to a workflow-specific
  product list;
- PAT, MiniAOD, NanoAOD, and tagger-input propagation remain unaudited;
- calibration and conditions records need a dedicated inventory;
- CPU and serialized-size costs have not yet been measured;
- HGCAL local-time naming and geometric-reference behavior need a small
  executable validation.

These are tracked gaps, not assumed absences.
