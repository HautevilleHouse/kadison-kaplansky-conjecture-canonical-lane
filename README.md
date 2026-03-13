# The Kadison-Kaplansky Conjecture via Projection-Spectral Persistence
## Canonical Lane (defined term): the manifold-constrained local-to-global closure architecture (`KK1-KK8`)

Canonical Lane research workspace for a flagship problem in operator algebras and noncommutative geometry:
proving absence of nontrivial projections in reduced group `C^*`-algebras through an admissible spectral-idempotent closure architecture.

## Main Manuscript

- [paper/KADISON_KAPLANSKY_CONJECTURE_PREPRINT.md](paper/KADISON_KAPLANSKY_CONJECTURE_PREPRINT.md)
- [paper/CANONICAL_ROUTING_INDEX.md](paper/CANONICAL_ROUTING_INDEX.md)

## Structure

- `paper/`
  - `KADISON_KAPLANSKY_CONJECTURE_PREPRINT.md`
  - `CANONICAL_ROUTING_INDEX.md`
  - `EXTRACTION_SPEC.md`

- `notes/`
  - `EG1_public.md`
  - `EG2_public.md`
  - `EG3_public.md`
  - `EG4_public.md`
  - `IDENTIFICATION_BRIDGE.md`

- `repro/`
  - `REPRO_PACK.md`
  - `THIRD_PARTY_RERUN_PROTOCOL.md`
  - `run_repro.sh`
  - `repro_manifest.json`
  - `certificate_baseline.json`

- `scripts/`
  - `kk_closure_guard.py`
  - `extract_constants.py`
  - `promote_constants.py`
  - `update_manifest.py`
  - `release_gate.py`
  - `README.md`

- `artifacts/`
  - `constants_extraction_inputs.json`
  - `constants_extracted.json`
  - `constants_registry.json`
  - `stitch_constants.json`
  - `promotion_report.json`

## Local Reproducibility Command

```bash
bash repro/run_repro.sh
```

This writes `repro/certificate_runtime.json`.

## How To Read This Professionally

1. Theorem chain first: read `paper/KADISON_KAPLANSKY_CONJECTURE_PREPRINT.md`.
2. Constants provenance second: audit `paper/EXTRACTION_SPEC.md`, `artifacts/constants_extraction_inputs.json`, `artifacts/constants_extracted.json`, and `artifacts/promotion_report.json`.
3. Pipeline third: run `bash repro/run_repro.sh` to audit hashes, provenance, and gates; it is reproducibility infrastructure, not theorem generation.

Release modes:

- `normalized`: `status=normalized_placeholder` allowed when explicitly labeled.
- `fully_extracted`: requires `status=derived_numeric` for all required constants and stitch keys.

Current KK runner policy:

- `repro/run_repro.sh` extracts, promotes, runs `scripts/kk_closure_guard.py`, updates `repro/repro_manifest.json`, and enforces `fully_extracted` release-gate mode.

## Routing Rule (inclusion discipline)

Every claim-bearing item must be routed through all three layers:

1. main preprint section/appendix,
2. mirror note under `notes/`,
3. artifact key consumed by `scripts/kk_closure_guard.py`.

Routing map: [paper/CANONICAL_ROUTING_INDEX.md](paper/CANONICAL_ROUTING_INDEX.md)

## Citation

- Metadata: [CITATION.cff](CITATION.cff)
- Manuscript target: [paper/KADISON_KAPLANSKY_CONJECTURE_PREPRINT.md](paper/KADISON_KAPLANSKY_CONJECTURE_PREPRINT.md)

## Authorship

- Program author: **HautevilleHouse**
- Canonical attribution source: [`CITATION.cff`](CITATION.cff)
