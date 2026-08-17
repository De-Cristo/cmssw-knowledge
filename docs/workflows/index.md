---
title: Workflows
status: draft
---

# Workflows

A workflow note follows real execution across package boundaries. Prefer a
traceable chain such as:

```text
configuration fragment
→ configured module label and plugin type
→ C++ plugin
→ consumed data products and EventSetup records
→ algorithm implementation
→ produced data products
→ downstream consumer or output
```

Initial workflow candidates:

- RAW input to local detector reconstruction
- Pixel digis to reconstructed tracks
- Reconstructed objects to analysis-level candidates
- Simulation through digitization
- L1 decisions into HLT processing
- Conditions retrieval during event processing
