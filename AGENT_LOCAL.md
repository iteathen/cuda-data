# Repository context: cuda-data

Universal engineering and design guidance comes from the account-global `AGENTS.md`.

## Mission and ownership

CUDA-DATA owns reusable column/table/dataframe semantics when accepted: schema/column/nullability/string/categorical meaning, selection/filter/sort/partition/shuffle, joins/group-by/window/aggregation, table plans/material roles, and explicit columnar interchange meaning.

CUDA-JS owns generic GPU mechanisms. CUDA-JS-Tensor owns generic Tensor mathematics. Storage, communication, graph analytics, database-server, and downstream dataset/business semantics remain with their natural owners.

## Local routing

Accepted `docs/decisions/`, `docs/specs/`, repository status/roadmap, and current issues own local implementation/activation truth.

## Local constraints

Maintained code uses JavaScript/ESM plus accepted Device-JS through public lower contracts; no Python, direct native/provider escape path, or private lower imports.