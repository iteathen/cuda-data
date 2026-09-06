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

Generic cross-domain physical memory-management policy likewise requires its own JS/TS owner if independently justified; CUDA-DATA retains only table/column semantic lifetimes and data-specific chunk/out-of-core policy.

## Governance

Protected-main and repository-setting alignment is complete. No local CI workflow currently exists, so no required status-check name is fabricated.

No roadmap entry, provider availability, repository creation or completed governance bootstrap is production implementation authority.
