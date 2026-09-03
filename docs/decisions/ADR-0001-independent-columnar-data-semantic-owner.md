# ADR-0001: Independent Columnar/Data Semantic Owner

**Status:** Accepted
**Date:** 2026-09-02

## Context

GPU data analytics has reusable table/column/schema/join/grouping semantics that are neither generic Tensor mathematics nor CUDA runtime vocabulary. Encoding those semantics in CUDA-JS-Tensor would make Tensor a dataframe system; encoding them in CUDA-JS would make the runtime a data framework. A vendor dataframe library must not define the architecture merely because it is an accelerator candidate.

## Decision

`cuda-data` owns reusable provider-neutral columnar/table/dataframe semantics. CUDA-JS retains generic GPU/provider mechanisms; CUDA-JS-Tensor retains generic math; storage/network/graph/product meaning stays with natural owners.

## Deletion test

Deleting any one consumer/provider leaves CUDA-DATA coherent. Deleting CUDA-DATA leaves CUDA-JS and Tensor coherent general-purpose libraries.

## Implementation gate

Issue #3 selects a bounded consumer-backed semantic profile; an accepted spec and independent reference semantics are required before production source/API.

## Consequences

GPU data processing gets a dedicated semantic home without conflating tables with tensors or native CUDA mechanisms.