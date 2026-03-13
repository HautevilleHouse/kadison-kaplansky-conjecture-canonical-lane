# Reviewer Map

    ## Claim Scope

    - Canonical-lane claim: inside the `manifold_constrained` lane, if the theorem chain in this repository holds and the guard certificate passes, the repository-level closure claim is satisfied.
    - Standard target claim: carried by the in-repo bridge theorems tying the lane to the target statement.

    ## Theorem Dependency Chain

    1. `EG1`: coercive response and active control floor.
    2. `EG2`: capture and admissible continuation.
    3. `EG3`: compactness and no-collapse spacing.
    4. `EG4`: rigidity and transfer.
    5. Identification bridge: strict coherence on the determining class.
    6. Scalar closure: `KK_G1, KK_G2, KK_G3, KK_G4, KK_G5, KK_G6, KK_GM` all `PASS`.

    Primary files:

    - `paper/KADISON_KAPLANSKY_CONJECTURE_PREPRINT.md`
    - `notes/EG1_public.md`
    - `notes/EG2_public.md`
    - `notes/EG3_public.md`
    - `notes/EG4_public.md`
    - `notes/IDENTIFICATION_BRIDGE.md`

    ## Closure Gates

    | Gate | Constant | Description |
    |------|----------|-------------|
    | `KK_G1` | `kappa_projection` | projected operator response has a strict positive floor |
| `KK_G2` | `sigma_trace` | trace defect stays above capture floor across admissible spectral losses |
| `KK_G3` | `kappa_compact` | normalized near-failure families are precompact and projection windows do not collapse |
| `KK_G4` | `rho_rigidity` | bad nontrivial-projection countermodels are excluded |
| `KK_G5` | `projection_transfer` | rigid limit transfers to the trivial-projection endpoint class |
| `KK_G6` | `eps_coh` | strict coherence / identification closure |
| `KK_GM` | derived | final strict margin |

    ## Falsification Conditions

    - `repro/certificate_runtime.json` has any non-`PASS` gate.
    - `lane.active_lane != "manifold_constrained"`.
    - `all_pass != true`.
    - Any manifest hash mismatch under `repro/repro_manifest.json`.
    - A verified counterexample to any EG theorem statement used in the paper.
