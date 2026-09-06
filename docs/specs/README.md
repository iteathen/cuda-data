# CUDA-DATA specifications

**Architecture/ownership authority is accepted; no production data capability specification is accepted yet.**

- [`SPEC-0001-native-boundary-and-js-only-implementation.md`](SPEC-0001-native-boundary-and-js-only-implementation.md) — accepted cross-cutting rule that CUDA-DATA remains JavaScript/TypeScript, CUDA-JS owns native memory/execution/provider integration, and columnar/table/dataframe semantics remain here. This specification does not authorize a table API or provider profile.

The [activation roadmap](https://github.com/iteathen/cuda-data/issues/3) organizes assessment. Production implementation must first have a bounded, consumer-backed semantic contract accepted under the [development instructions](../../AGENTS.md).

Start with the [project charter](../PROJECT_CHARTER.md) and [architecture decision](../decisions/README.md) to understand the intended scope.
