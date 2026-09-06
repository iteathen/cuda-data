# CUDA-DATA Agent Entry Point

Read before changing the repository. Authority: owner instruction -> this file -> accepted ADRs -> accepted specs -> charter -> status/roadmap/issues.

Use `assess -> research -> reassess -> plan -> execute -> qualify -> review -> cleanup/document` and `LEGO -> SOLID -> CUPID -> KISS`.

LEGO is the outer architecture rule: ownership, universality, replaceability, scope containment, damage-limiting encapsulation, and context containment. A LEGO is too large when one agent cannot hold its complete authoritative working set—contract, implementation, invariants, lifecycle/resource/failure rules, tests/conformance, and immediate dependency/consumer interfaces—in focused attention with substantial headroom for reasoning and review. Context fit is a first-class boundary criterion alongside semantic, lifecycle, resource/failure, substitution, and change cohesion. When exceeded, recursively split at the strongest real seam or narrow scope; do not create arbitrary modules that duplicate truth or require cross-boundary internal knowledge. Inside a valid LEGO, SOLID structures responsibilities and dependency direction, CUPID shapes the implementation, and KISS removes remaining unjustified complexity; lower levels may not defeat higher ones.

CUDA-DATA owns reusable column/table/dataframe semantics when separately accepted: schema/column/nullability/string/categorical meaning, selection/filter/sort/partition/shuffle, joins/group-by/window/aggregation semantics, table plans/material roles, and explicit columnar interchange meaning.

CUDA-DATA does not own generic Tensor mathematics, generic CUDA sort/scan/reduce primitives, CUDA memory/provider lifecycle, graph analytics, filesystem/storage-engine/database-server policy, or downstream business/dataset semantics.

CUDA-JS owns generic GPU mechanisms and any bounded native provider mechanism selected later. CUDA-JS-Tensor owns generic Tensor mathematics. Optional `cuda-io`/`cuda-comm` composition does not transfer their semantics here.

No RAPIDS/cuDF provider is selected by repository creation. Vendor APIs are possible realizations, not semantic authority.

Direct native/FFI/CUDA C++/PTX/private imports or duplicated lower lifecycle are ownership-gap signals. Maintained code, when authorized, is JavaScript/ESM plus accepted restricted Device-JS; no Python/native escape path without a successor decision.

Repository creation authorizes no production API/source. #3 is the activation roadmap; #2 owns repository controls. Accepted bounded specs are required before implementation.