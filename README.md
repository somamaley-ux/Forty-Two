# Forty Two Exhaustion, Closure, and Downstream Consequence

This repository is a standalone Lean package for the manuscript
`Forty Two Exhaustion, Closure, and Downstream Consequence`.

It is intended to be a buildable, auditable release of the capstone
formalization. The package includes the dedicated capstone theorem surface, the
supporting imported Lean islands needed by that surface, the dedicated axiom
check entrypoint, and the manuscript source tree.

## Repository layout

- `MaleyLean/UnifiedCapstonePaperStatements.lean`
  Main capstone formalization for the manuscript, including the paper-facing
  theorem layer, the bundled protocol system, and the concrete support-backed
  instantiation.
- `Checks/Axiom/UnifiedCapstoneAxiomCheck.lean`
  Dedicated audit target for theorem dependency checks.
- `paper/`
  Standalone manuscript source tree for the capstone.
- `reports/status/unified_capstone_status.md`
  Short package and status note.
- `reports/status/formalization_scope.md`
  Referee-facing scope note.
- `reports/audits/unified_capstone_axiom_audit.txt`
  Human-readable audit summary.

## Build

This package uses Lean `v4.28.0` via `lean-toolchain`.

Build the package:

```text
lake build
```

Run the dedicated axiom audit:

```text
lake env lean Checks\\Axiom\\UnifiedCapstoneAxiomCheck.lean
```

## What is formalized

The standalone package includes:

- a dedicated theorem surface for the unified capstone manuscript
- an integrated capstone protocol system with dependency, downstream, and
  closed-system audit layers
- constructor and witness-pack infrastructure for concrete instantiation
- a named concrete capstone instantiation
- a support-backed concrete capstone linked to real imported theorem surfaces

The strongest audited routes in this package are axiom-free, including the
support-backed concrete capstone path checked by the dedicated audit target.

## Boundary

This repository is a manuscript-oriented formalization, not an encyclopedic
mechanization of every surrounding application manuscript or every informal
motivation in the prose.

Its purpose is to provide a standalone Lean release that captures the capstone
proof spine in a buildable and auditable form.
