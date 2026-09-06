# CUDA-DATA

CUDA-DATA is a planned JavaScript library for reusable GPU columnar and relational data processing in the CUDA-JS ecosystem, intended for developers building GPU applications.

## Current state

This repository currently contains the project charter, architecture decision, development guidance, and planning records. **There is no production implementation, installable package, or public API yet.** No native-provider support or performance is claimed.

## Intended scope

The library aims to define columns, tables, schemas, filtering, sorting, joins, and aggregation through public CUDA-JS contracts.

Database-server and dataset-specific policy remain with applications. CUDA-JS supplies generic GPU mechanisms and CUDA-JS-Tensor supplies tensor mathematics. No cuDF provider has been selected.

Implementation depends on a concrete consumer need and an accepted specification. The [activation roadmap](https://github.com/iteathen/cuda-data/issues/3) describes candidate work; it is not a commitment that every proposed capability will ship.

## Start here

- [Current status](STATUS.md).
- [Project charter](docs/PROJECT_CHARTER.md) and [documentation](docs/README.md).
- [Development instructions](AGENTS.md) and [shared contribution guide](https://github.com/iteathen/.github/blob/main/CONTRIBUTING.md).
- [Private security reporting](https://github.com/iteathen/.github/blob/main/SECURITY.md).
- [License](LICENSE).
