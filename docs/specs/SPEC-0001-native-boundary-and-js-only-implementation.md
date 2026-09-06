# SPEC-0001: Native Boundary and JavaScript/TypeScript Implementation

**Status:** Accepted architecture/ownership authority; production data profiles remain separately gated.

**Version:** 1.0.0

**Owner:** CUDA-DATA

**Lower authority:** `iteathen/CUDA-JS` SPEC-0032

## Purpose

CUDA-DATA owns reusable provider-neutral columnar/table/dataframe semantics. CUDA-JS is the sole native CUDA/provider integration owner.

## Repository implementation rule

Maintained CUDA-DATA source is JavaScript/TypeScript. Restricted Device-JS generation is permitted only through public CUDA-JS contracts.

CUDA-DATA does not maintain C, C++, CUDA C++, PTX, direct native FFI, native addons, cuDF/provider bindings, native handles/pointers, ABI structs or platform discovery code. Native evidence may be produced externally and recorded, but native oracle/provider source is not maintained here.

A missing native mechanism routes to CUDA-JS before any local workaround.

## CUDA-DATA owns

- column/table/schema/nullability/string/categorical meaning;
- relational selection/filter/sort/partition/join/group/aggregation semantics;
- table material/liveness/buffer-role semantics;
- columnar interchange meaning and lifetime requirements;
- data-specific execution/provider eligibility/equivalence;
- JavaScript/TypeScript reference and conformance evidence.

## Lower boundaries

CUDA-JS-Tensor owns generic Tensor mathematics. CUDA-IO owns reusable source/sink/storage semantics. CUDA-COMM owns reusable communication semantics.

CUDA-JS owns native allocation/view/transfer/registered/mapped/managed/peer-memory mechanisms, compiler/operation resources and native provider integrations. Generic flat-buffer GPU primitives may be CUDA-JS-owned only when their semantics are genuinely consumer-neutral and independently justified.

## Memory-policy boundary

CUDA-DATA owns semantic lifetimes of columns/tables and data-specific out-of-core/chunking policy. It may project generic byte/alignment/access/lifetime/placement constraints downward.

Generic cross-domain arena/pool/placement/fragmentation/spill/migration policy is not CUDA-DATA-owned merely because data workloads motivate it. If independently justified, it requires a JavaScript/TypeScript owner above CUDA-JS and must remain free of table vocabulary.

## Activation gate preservation

This specification does not authorize a table/dataframe API, provider, generic algorithm library or production execution path. Existing consumer-backed semantic activation remains required.

## Non-goals

No native dataframe backend, no arbitrary cuDF/provider passthrough, no database engine, no generic GPU memory manager, no production capability or support claim.
