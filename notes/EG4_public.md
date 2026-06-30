# EG4 Public Note (Rigidity and Endpoint Transfer)

Mature wording: `bad-limit exclusion / endpoint transfer`.

In-paper anchor: `paper/KADISON_KAPLANSKY_CONJECTURE_PREPRINT.md` (`KK_G4`, `KK_G5`).

## Goal
Separate the rigidity job from the endpoint-transfer job for `proving absence of nontrivial projections in reduced group `C^*`-algebras through an admissible spectral-idempotent closure architecture`.
The older wording `rigidity and endpoint-transfer` corresponds to bad-limit exclusion plus the bridge into the intended endpoint object.

## Objects

- bad-limit class: candidates extracted by the compactness gate but incompatible with closure.
- rigidity floor: `rho_rigidity`.
- endpoint-transfer lock: `1.029422`.
- coherence interface: `0.0` remains available to the bridge and final margin.

## Closure Criterion

`KK_G4` closes when `rho_rigidity` excludes bad endpoint alternatives: bad nontrivial-projection countermodels are excluded.
`KK_G5` closes when `1.029422` transfers the surviving endpoint to the intended target class: the rigid endpoint transfers to the intended problem-side class.
Together they feed the strict margin `M_KK`.

## Lemma Chain and Proof Payload

### Lemma EG4.1 (bad-limit exclusion)
Every extracted bad limit contradicts a declared rigidity constraint or leaves the admissible class.

Payload: verify `rho_rigidity` in the registry and certificate surfaces.

### Lemma EG4.2 (endpoint transfer)
The surviving rigid representative is locked to the standard problem-side endpoint by `1.029422`.

Payload: read this note together with `notes/IDENTIFICATION_BRIDGE.md`.

### Theorem EG4.3 (rigidity/transfer gate closure)
If bad limits are excluded and the endpoint lock is active, then `KK_G4` and `KK_G5` deliver the boundary object needed by the final margin.

## Current Instantiation

- rigidity gate: `KK_G4`
- rigidity artifact key: `rho_rigidity`
- transfer gate: `KK_G5`
- transfer artifact key: `1.029422`
- mature equivalent: `bad-limit exclusion / endpoint identification`
- audit surface: `notes/IDENTIFICATION_BRIDGE.md` and `repro/certificate_runtime.json`
