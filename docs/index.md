---
title: CMSSW Knowledge Base
description: A guided path through the architecture and code of CMSSW
---

# CMSSW Knowledge Base

Learn CMSSW as a connected system rather than as a collection of tens of
thousands of source files.

This knowledge base is organized around complementary views:

<div class="grid cards" markdown>

-   :material-school-outline:{ .lg .middle } **Learn**

    ---

    Follow a progressive path from the framework fundamentals to complete
    processing workflows.

    [:octicons-arrow-right-24: Start learning](learn/index.md)

-   :material-sitemap-outline:{ .lg .middle } **Architecture**

    ---

    Understand framework services, data flow, configuration, conditions, and
    the boundaries between major systems.

    [:octicons-arrow-right-24: Explore architecture](architecture/index.md)

-   :material-transit-connection-variant:{ .lg .middle } **Workflows**

    ---

    Trace concrete paths from configuration through plugins and data products.

    [:octicons-arrow-right-24: Follow workflows](workflows/index.md)

-   :material-package-variant-closed:{ .lg .middle } **Subsystems**

    ---

    Use concise package maps to find ownership, interfaces, configuration, and
    representative tests.

    [:octicons-arrow-right-24: Browse subsystems](subsystems/index.md)

-   :material-timer-outline:{ .lg .middle } **Timing**

    ---

    Trace BTL, ETL, and HGCAL time from simulated energy deposits through
    reconstruction, track association, TICL, persistence, and analysis-facing
    products.

    [:octicons-arrow-right-24: Follow the timing chain](timing/index.md)

</div>

!!! note "Source code remains authoritative"

    Notes are navigation aids. Technical conclusions should name the CMSSW
    release or commit where they were verified and link to concrete source,
    configuration, or tests.

## How to use this site

1. Begin with [The CMSSW big picture](learn/01-big-picture.md).
2. Follow the [timing curriculum](learn/timing-curriculum.md) for the focused
   BTL, ETL, and HGCAL study.
3. Use **Search** when investigating a symbol, package, data product, or error.
4. Follow source anchors to verify details in the relevant CMSSW checkout.
5. Record discoveries that would otherwise be expensive to reconstruct.

## Current status

The first source audit covers the Phase-II BTL, ETL, and HGCAL timing chain on
CMSSW `master` at commit
[`f1ac1dbe`](https://github.com/cms-sw/cmssw/commit/f1ac1dbe1f36762b14843b1fb906971de43a1044).
It identifies the principal timing products, transformations, and persistence
boundaries through MTD track extension and HGCAL TICL/PF reconstruction.

See the [verification snapshot](reference/verification-snapshot.md) for the
scope and known gaps of this audit.
