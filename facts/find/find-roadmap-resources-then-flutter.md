---
name: find-roadmap-resources-then-flutter
description: NOBAD Find plan: RAM/CPU/GPU first, then a named-pipe engine service and a Flutter UI, then features; resume from ROADMAP.md in nobad-studio/find
type: decision
date: 2026-11-18
---

The maintainer's main aim for NOBAD Find is to optimize RAM, CPU and GPU first, then add in-app features, and
that it must not "bug out". The full plan, architecture, feature inventory and a status table live in
`ROADMAP.md in nobad-studio/find` in nobad-studio/Nobad-VPN.

Order: measure (tools/measure.py, docs/measurements.md) → engine diet (ONNX arenas, worker imports, EcoQoS,
job memory limit) → engine as a service over a private named pipe (rpc.py, contract tests) → Flutter UI
(Qt/QML fallback if the prototype misses its budget) → 0.8.0 multilingual model tiers.

**Why:** measured 0.7.0 on the maintainer's PC: WebView2 used 425 MB in 7 processes; the engine had 549 MB working
set but 3.98 GB committed. NOBAD VPN's mini window was seen showing a raw `{"ok": false}` API page, a bug class of
URL/local-server UIs that a native UI over a pipe can't have.
**How to apply:** read the roadmap's status table before any NOBAD Find work; don't start features ahead of the
resource and stability phases unless the table says they were parked; update the table when you finish a step.
