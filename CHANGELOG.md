# Changelog — maturity-model-technology

All notable changes to this repository are documented here. The format follows
[Keep a Changelog](https://keepachangelog.com/en/1.1.0/) and the project
adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Changed — BREAKING

- **Scale level renumbering adopted (dea-metamodel #214): `L-0 Not Assessed` + `L-1..L-5`.** Release 2.0.0 — blocked on upstream ratification of dea-metamodel #214; do not merge before the renumbered canonical scale instance is released and CI pins are bumped.
  - Mapping: old L0→new L-1 … old L4→new L-5; new L-0 is the Not Assessed sentinel (0 points, not a capability level).
  - Unchanged: level definitions/names, band instance `dea:maturity-bands-v2` v1.0.0 (ids, ranges, effort multipliers), band ids `level-1-emergent`…`level-5-self-optimising`, criteria and register content.
  - Comparability: historical index values and bands remain valid; only per-criterion level labels shift (+1).
  - Lockstep consuming-side changes: VERSION/model.yaml/standard.yaml declare 2.0.0 (standard.yaml drift from 1.0.0 resolved in lockstep); scripts/local_validate.py validates the six-level scale with the Not-Assessed first-entry rule; README presents the aligned numbering.

## [1.1.0] — 2026-11-19

### Added

- **CR-AM-13 Phase 4**: seeded criteria register draft
  (`maturity/model/technology-register-draft.yaml`) — five dimensions
  (Stack Fitness, Technical Debt, Lifecycle Management, Skill Coverage,
  Platform & Tooling Capability), 10 sub-dimensions, **14 criteria** with
  `TEC-*` criterion IDs as permanent benchmarking keys. Draft-by-design:
  model owners own refinement (questionnaire, weights) and the later stable
  promotion per CR-AM-13 §8.
- `touchpoints.yaml` **v0.1.0** mirror record `tp-technology-x-operations`
  (feeds): this model's platform and tooling capability maturity feeds
  operations D5 (effectiveness of tool use) — `TEC-D5-SD1-C01` ↔
  `OPS-D5-SD1-C01`.

### Changed

- `VERSION` and `model.yaml` 1.0.0 → 1.1.0 (minor, additive); model.yaml
  declares the touchpoints manifest and notes the seed register.

### Notes

- Reciprocity with the ecosystem is content-complete: the peer's
  `touchpoints.yaml` v0.2.0 ([maturity-model-operations release 2.0.0, PR #7]
  (https://github.com/Assessment-Models/maturity-model-operations/pull/7)) cites
  this `TEC` binding on its side. Bindings become citable once both releases
  are tagged (`v1.1.0` here, `v2.0.0` on the peer).
- Touchpoint declarations stay `status: draft` until
  `maturity-touchpoint-contract` publishes in `technehub-labs/dea-metamodel`
  (issue #213).

## [1.0.0] — 2026-11-13

### Added

- Initial release of the `dea:maturity-technology` maturity model as an
  independently versioned asset, per the Assessment-Models organisation
  taxonomy (CR-AM-11 §8).
- Model-owned scale conforming to the published `maturity-scale.schema.json`:
  five levels, ordinals 0–4, `ordering: ascending`, linear topology with
  exponential progression, scored against the canonical v2 band instance
  (`dea:maturity-bands-v2` v1.0.0) — non-linear widths 20/25/25/18/12 and
  per-level effort multipliers 1.0 → 6.0.
- CR-AM-11 §15 contract handshake (`model.yaml`) declaring conformance to
  `maturity-scale-contract`, `maturity-model-contract` and
  `conformance-contract` against `technehub-labs/dea-metamodel`.
- Level 1 local model CI and Level 2 contract conformance workflows.
- Worked scoring example demonstrating canonical v2 band resolution and the
  effort-adjusted value.

### Notes

- Level semantics are carried verbatim from the authoritative source; only the
  scoring fields differ between the frozen v1-alpha lineage and the canonical
  v2 scheme.
