# CUDA-DATA Status

**Updated:** 2026-09-06

**Architecture/ownership:** accepted independent columnar/table semantic owner under SPEC-0001.
**Production implementation/API:** not authorized / none.
**Provider/support:** none selected or claimed.

## Current work

- #1 ownership/bootstrap authority — completed.
- #2 repository-control/protected-main alignment — completed; `main` is protected and the selected CUDA-family settings were read back.
- #3 is the current consumer-backed columnar/relational activation roadmap; it remains planning/assessment authority, not a production specification.

## Next executable decision

Select one bounded consumer-backed column/table profile with explicit schema/nullability/material semantics and accept its contract before production implementation. Provider acceleration comes only after those reusable semantics exist.

Generic Tensor mathematics stays CUDA-JS-Tensor. CUDA-JS owns native memory/execution/provider mechanisms only. Generic reduce/scan/sort/map algorithm semantics do not become CUDA-JS-owned merely because multiple GPU consumers need them; an independently reusable algorithm layer would require a JavaScript/TypeScript owner above CUDA-JS. Storage/network mechanics stay with their own owners, and graph algorithms stay in `cuda-graph-analytics`.

`iteathen/CUDA-MM` is now the accepted **reserved architecture/ownership home** for reusable cross-domain physical memory-management policy. CUDA-MM is not a current CUDA-DATA dependency: production CUDA-MM remains gated by CUDA-MM #3/#4 and a separately accepted bounded contract. CUDA-DATA retains table/column semantic lifetimes, schema/material meaning and data-specific chunk/out-of-core policy; it may later project only generic physical constraints if CUDA-MM is activated.

## Governance

Protected-main and repository-setting alignment is complete. No local CI workflow currently exists, so no required status-check name is fabricated.

No roadmap entry, provider availability, CUDA-MM repository existence or completed governance bootstrap is production implementation authority.
