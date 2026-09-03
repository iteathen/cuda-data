# CUDA-DATA Project Charter

**Status:** Accepted architecture after bootstrap integration; production implementation not authorized.

## Purpose

Own reusable provider-neutral columnar/table/dataframe semantics without turning CUDA-JS into a data framework or CUDA-JS-Tensor into a dataframe library.

## Owns, when separately accepted

- columns/tables/schema/nullability/string/categorical meaning;
- selection/filter/sort/partition/shuffle;
- join/group-by/aggregation/window and related relational-table operations;
- versioned table plans/material/liveness/buffer roles;
- explicit columnar interchange semantics when lifetime/device ownership is specified.

## Does not own

Generic Tensor dtype/shape/math; generic CUDA sort/scan/reduce primitives; CUDA memory/provider lifecycle; graph analytics; filesystem/storage-engine/database-server policy; or downstream dataset/business meaning.

## Composition

CUDA-JS owns lower GPU/provider mechanisms. CUDA-JS-Tensor owns generic math. `cuda-io` and `cuda-comm` may be optional dependencies for out-of-core/multi-GPU profiles, but their semantics remain independently owned.

No vendor library is selected by the architecture bootstrap.

## Dependency direction

Base dependency is `cuda-data -> public cuda-js`; other semantic dependencies are optional and profile-selected.

## Activation gate

Issue #3 must prove a reusable bounded table/column profile before production source/API. Reference semantics precede provider acceleration.

## Non-goals

SQL server, database/storage engine, arbitrary cuDF passthrough, graph analytics, or provider-driven public vocabulary.