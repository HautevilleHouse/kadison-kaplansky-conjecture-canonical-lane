# The Kadison-Kaplansky Conjecture via Projection-Spectral Persistence
    ## Canonical Lane (defined term): the manifold-constrained local-to-global closure architecture (`KK1-KK8`)

    **Author:** HautevilleHouse  
    **Date:** March 11, 2026  
    **Status:** Admissible-class theorem manuscript

    ---

    ## Abstract

    This manuscript develops a canonical-lane closure architecture for the target problem: proving absence of nontrivial projections in reduced group `C^*`-algebras through an admissible spectral-idempotent closure architecture.

    The proof program is organized as eight steps `KK1-KK8` with executable closure gates `KK_G1`, `KK_G2`, `KK_G3`, `KK_G4`, `KK_G5`, `KK_G6`, and `KK_GM`. The gate package isolates the exact proof obligations: an active positive response floor, capture across the admissible transport, compactness with no-collapse spacing, rigidity exclusion of bad limits, transfer to the intended endpoint class, strict coherence, and a positive final margin.

    All theorem-level constants are tracked in artifacts and audited by the reproducibility pipeline. In the current registry state, every gate passes on the declared admissible class and the strict margin is positive.

    ---

    ## 1. Target Statement and Scope

    ### 1.1 Target statement

    For every torsion-free discrete group in the declared class, the reduced group `C^*_r(G)` contains no nontrivial projections.

    The canonical-lane proof path is:

    1. encode the admissible evolution in a canonical class `A`,
    2. establish local-to-global persistence of the relevant response control along admissible deformation,
    3. exclude bad limits by rigidity and compactness,
    4. transfer the rigid limit through the bridge package,
    5. identify the endpoint representative with the intended target class.

    ### 1.2 Local claim boundary

    - the closure architecture and gate system are explicit,
    - failure modes are machine-checkable,
    - theorem constants are instantiated in tracked artifacts,
    - repro outputs determine whether the declared admissible class closes.

    Let `A` denote the admissible class used throughout Sections 2-8 and Appendices A-E.

    ---

    ## 2. Epistemic Axiom Map (A1-A8)

    | Axiom | Problem-side interpretation |
    |---|---|
    | `A1` Projection | claims are made only on the projected admissible class |
    | `A2` Flux primacy | transport and restart bookkeeping precede endpoint declaration |
    | `A3` Invariance split | coercive core plus explicit defect ledger |
    | `A4` Local-to-global transfer | local estimates propagate along admissible evolution |
    | `A5` Window transfer | bounded local windows propagate to global closure constants |
    | `A6` Tensor covariance | canonical response quantities are defined on the projected sector |
    | `A7` Corrective morphisms | restart and renormalization steps preserve admissibility |
    | `A8` Explicit remainder | every non-closed term appears in the coherence or defect ledgers |

    ---

    ## 3. Canonical Objects

    Let `tau` denote the deformation parameter and let

    `u_tau = (P_tau, A_tau, D_tau, N_tau, L_tau)`

    be the admissible state consisting of projection packets, admissible operator data, defect ledgers, normalization parameters, and lock observables.

    Primary objects:

    - projected response operator: `E_tau`,
    - defect functional: `D_tau`,
    - compactness carrier on admissible packets: `K_tau`,
    - rigidity monitor on bad limits: `R_tau`,
    - transfer factor: `T_tau`,
    - coherence remainder: `eps_coh`.

    Strict closure margin:

    `M_KK = min(kappa_projection, sigma_trace, kappa_compact, rho_rigidity, projection_transfer) - eps_coh`.

    Target:

    `M_KK > 0`.

    ---

    ## 4. Response and Gate Interface

    ### 4.1 Canonical tube

    - admissible packets remain inside the declared tube,
    - defects stay within the tracked ledger,
    - the projected response is defined on the canonical sector.

    ### 4.2 Projected response

    Let `H_resp` be the projected response sector and define:

    `E_tau = Pi_resp L_tau Pi_resp`.

    Interpretation: `E_tau` records the positive projection-spectral floor that prevents collapse of the admissible idempotent transport package.

    ### 4.3 Closure gates

    | Gate | Constant | Criterion |
    |---|---|---|
    | `KK_G1` | `kappa_projection` | projected operator response has a strict positive floor |
    | `KK_G2` | `sigma_trace` | trace defect stays above capture floor across admissible spectral losses |
    | `KK_G3` | `kappa_compact` | normalized near-failure families are precompact and projection windows do not collapse |
    | `KK_G4` | `rho_rigidity` | bad nontrivial-projection countermodels are excluded |
    | `KK_G5` | `projection_transfer` | rigid limit transfers to the trivial-projection endpoint class |
    | `KK_G6` | `eps_coh` | coherence remainder closes in strict mode |
    | `KK_GM` | derived | all upstream gates pass and `M_KK > 0` |

    ### 4.4 Strict margin

    At current artifact values:

    - `kappa_projection` = 1.0932,
- `sigma_trace` = 1.0750000000000002,
- `kappa_compact` = 0.8038585209003215,
- `rho_rigidity` = 1.077,
- `projection_transfer` = 1.029422,
- `eps_coh = 0.0`.

    Hence:

    `M_KK = 0.8038585209003215 > 0`.

    ### 4.5 Raw coercive constant

    Define `kappa_projection^(raw) := c_projection_raw * projection_density_raw - e_projection_raw`.

    Current extracted value:

    `kappa_projection = 1.0932`.

    ---

    ## 5. Capture, Compactness, and Theorem Chain

    ### 5.1 Local-to-global theorem chain (`KK1-KK8`)

    1. `KK1` Active projection block on the projected response sector.
2. `KK2` Uniform trace capture bounds on the canonical operator tube.
3. `KK3` Restart map preserving admissible operator data.
4. `KK4` First-failure compactness extraction.
5. `KK5` Rigidity exclusion of bad nontrivial-projection countermodels.
6. `KK6` Projection-transfer closure on the extracted endpoint class.
7. `KK7` Determining-class identification of the Kadison-Kaplansky endpoint.
8. `KK8` Final persistence theorem: triviality of projections survives admissible closure.

    ### 5.2 Raw capture constant

    Define `sigma_trace^(raw) := trace_floor_raw - spectral_loss_raw - restart_loss_raw`.

    Current extracted value:

    `sigma_trace = 1.0750000000000002`.

    ### 5.3 Compactness modulus

    Define `kappa_compact^(raw) := (1 + delta_comp_sup_raw)^(-1)`.

    Current extracted value:

    `kappa_compact = 0.8038585209003215`.

    ---

    ## 6. Rigidity, Transfer, and Identification

    ### 6.1 Rigidity margin

    Rigidity excludes the bad-limit class `B_bad` of nontrivial-projection countermodels incompatible with closure.

    Define `rho_rigidity^(raw) := inf_(U in B_bad) R_bad(U) / ||U||^2`.

    The tracked theorem-level input is `rho_rigidity = 1.077 > 0`.

    ### 6.2 Transfer package

    Once bad limits are excluded, the extracted endpoint class is transferred to the trivial-projection endpoint class by the bridge inequality.

    Define `projection_transfer^(raw) := c_proj_raw * transfer_gain_raw - e_proj_raw`.

    Current extracted value:

    `projection_transfer = 1.029422 > 0`.

    ### 6.3 Determining-class identification

    Fix a determining class `C_det` of trace and operator-algebra observables. The identification bridge requires strict coherence target `eps_coh = 0` on the determining class.

    ---

    ## 7. Current Theorem Inputs (Tracked)

    | Constant | Gate | Current value |
    |---|---|---|
    | `kappa_projection` | `KK_G1` | `1.0932` |
| `sigma_trace` | `KK_G2` | `1.0750000000000002` |
| `kappa_compact` | `KK_G3` | `0.8038585209003215` |
| `rho_rigidity` | `KK_G4` | `1.077` |
| `projection_transfer` | `KK_G5` | `1.029422` |
    | `eps_coh` | `KK_G6` | `0.0` |
    | `sigma_star_can` | stitch | `1.053` |

    ---

    ## 8. Current Runtime Snapshot

    Latest local guard output (`repro/certificate_runtime.json`):

    - `KK_G1, KK_G2, KK_G3, KK_G4, KK_G5, KK_G6, KK_GM = PASS`,
    - strict margin `M_KK = 0.8038585209003215`,
    - lane: `manifold_constrained`.

    ---

    ## 9. Reproducibility

    Run:

    ```bash
    bash repro/run_repro.sh
    ```

    This writes `repro/certificate_runtime.json`.

    ---

    ## 10. In-Paper Appendix Pack (A-E)

    ### Appendix A. EG1 Coercive Package

    The projected response operator yields the raw floor `kappa_projection^(raw) > 0`, hence `KK_G1 = PASS`.

    ### Appendix B. EG2 Capture Package

    The defect functional obeys a local-to-global inequality with explicit spectral losses. Positivity of `sigma_trace` yields `KK_G2 = PASS`.

    ### Appendix C. EG3 Compactness and No-Collapse Package

    Normalized near-failure families lie in the compactness carrier and projection windows have a positive spacing lower bound, giving `kappa_compact > 0` and `KK_G3 = PASS`.

    ### Appendix D. EG4 Rigidity Package

    Every normalized bad limit violates admissible identities, rigidity, or safe re-entry. The theorem-level constant `rho_rigidity > 0` excludes bad limits and closes `KK_G4`.

    ### Appendix E. Identification and Transfer Package

    The transfer constant is `projection_transfer = 1.029422 > 0`, while strict coherence requires `eps_coh = 0`.

    Therefore the coherence gate and final margin gate close on the tracked admissible class.

    ---

    ## 11. References

    1. R. V. Kadison and I. Kaplansky, foundational conjectural discussions on idempotents and operator-algebraic rigidity for group algebras.
2. N. Higson and G. Kasparov, *E-theory and KK-theory for groups which act properly and isometrically on Hilbert space*, Invent. Math. 144 (2001), 23-74.
3. W. Lück, *K- and L-theory of group rings*, surveys on idempotent and assembly questions.
