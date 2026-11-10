=====================================================================
EXACT ARITHMETIC VERIFICATION OF INTER-UNIVERSAL TEICHMULLER THEORY IV
======================================================================
 
This repository contains the complete, reproducible codebase for the paper
"Exact Arithmetic Verification of Inter-Universal Teichmuller Theory IV".
 
It consists of 26 independent verification units (labeled A through Z).
Each unit verifies a specific numerical, algebraic, or p-adic identity
surrounding the proof of IUT IV, primarily focusing on the explicit
computations of Theorem 1.10 and the local data of the elliptic curve 11a1
at p=11. 
 
PREREQUISITES 
 
SageMath 9.5+ or 10.x is required. Many units rely on Sage's exact rational
arithmetic (QQ), p-adic fields (Qp), and elliptic curve databases.
Running these scripts in standard Python (without Sage) will result in errors. 
 
HOW TO RUN 
 
To run any unit, use the sage command in your terminal:
sage 01_procession_identity.sage
 
Each script is self-contained, prints its own detailed output, and ends with
a clear PASS or FAIL verdict along with a "Scope" section explaining what it
does NOT verify.
 
=====================================================================
UNIT DIRECTORY (A to Z)
=====================================================================
The 26 units are organized into six parts, matching the structure of the paper.
 
PART I: PROCESSION ARITHMETIC 
 
01_procession_identity.sage (Unit A)
Verifies the procession identity A_raw = (l^2-1)/48, A_norm = (l+1)/24,
and the constants chi = 12/(l(l+1)) and tau = 12/l^2 in exact rational
arithmetic for 12 primes.
 
02_propositions_2_3.sage (Unit B)
Verifies Propositions 2 and 3 of Urahigashi's fifth report, including the
H/(2l^2) rearrangement and the boundary failure at l=5.
 
12_procession_local_contributions.sage (Unit L)
Verifies that the procession-normalized sum of local log-volume
contributions equals (l+1)/24 * m * log(p).
 
23_spike_term.sage (Unit W)
Verifies the exact spike coefficients (l-j^2)/(2l) and their sum to -1/2.
 
24_corollary_3_12_numerical.sage (Unit X)
Symbolically verifies the numerical content of Corollary 3.12 for 11a1
at l=13, showing mu_Theta >= mu_q.
 
PART II: LOCAL P-ADIC DATA FOR 11a1 
 
03_log_unit_bounds.sage (Unit C)
Sample-checks IUT IV Proposition 1.2(i) for Q_11 and Q_11(sqrt 11).
 
07_theta_scaling.sage (Unit G)
Verifies the j^2-scaling of theta valuations in the Eisenstein extension
K = Q_11(pi).
 
11_log_volume_coefficient.sage (Unit K)
Verifies the log-volume coefficient formula for Q_11, Q_11(sqrt 11),
and Q_11(zeta_11).
 
14_ind2_log_volume.sage (Unit N)
Verifies that the log-volume is invariant under the (Ind2) automorphisms
(log-shell-preserving maps).
 
17_tate_parameter_root.sage (Unit Q)
Computes the explicit Tate parameter for 11a1 and verifies its 26th root
has valuation 5.
 
18_modular_j_invariant.sage (Unit R)
Verifies the Tate uniformization relation j(q_11) = j(11a1).
 
19_split_multiplicative.sage (Unit S)
Verifies that 11a1 has split multiplicative reduction at p=11
(Kodaira I_5, a_11=1, Tamagawa 5).
 
PART III: STRUCTURAL OBSTRUCTION & GLOBAL COMPARISON 
 
05_step_v_noncontainment.sage (Unit E)
Reproduces Urahigashi's explicit counterexample to Step (v) of Theorem 1.10,
showing the hull log-volume exceeds the bound.
 
08_cross_norm_lemma.sage (Unit H)
Verifies the cross-norm property for the projective tensor product of
p-adic Banach spaces.
 
09_global_szpiro.sage (Unit I)
Compares the local gap in Unit E to the global error term for the D_2 datum.
 
13_global_iut_inequality.sage (Unit M)
Instantiates the explicit global inequality of Theorem 1.10 for 11a1 over Q
at l=13.
 
PART IV: ALGEBRAIC DERIVATIONS 
 
15_szpiro_derivation.sage (Unit O)
Verifies the absorption step from C_Theta >= -1 to the explicit Szpiro
inequality. (Correctly uses log(q) in the second term).
 
16_log_q_substitution.sage (Unit P)
Verifies the substitution log(q_under) = (1/2l)log(q) and isolates the
sharp bound A >= (157/39)log(q_under) for l=13.
 
10_belyi_reduction.sage (Unit J)
Shows the proposed map is not Belyi, and verifies the corrected map
g(x) = (2/27)f(x) is Belyi of degree 6.
 
PART V: GALOIS & INITIAL DATA 
 
04_prop_1_8.sage (Unit D)
Checks IUT IV Proposition 1.8(i) for five curves and the verifiable
direction of 1.8(vii).
 
20_mod13_galois_representation.sage (Unit T)
Proves the mod-13 Galois representation of 11a1 is surjective onto GL_2(F_13).
 
21_global_torsion_failure.sage (Unit U)
Proves that 11a1 over Q fails the strict Initial Theta Data (since
E[30] is not a subset of E(Q) and sqrt(-1) is not in Q).
 
22_field_degree_bound.sage (Unit V)
Computes the field degree bound for F_tpd = Q(E[30], sqrt(-1)).
 
PART VI: ARCHIMEDEAN SCALING & COHERENCE 
 
06_archimedean_metric.sage (Unit F)
Verifies the 2^(|I|-1) bound for the archimedean metric on tensor products.
 
25_archimedean_scaling.sage (Unit Y)
Verifies the archimedean j^2-scaling of theta values over C to 200 bits
of precision.
 
26_arch_nonarch_coherence.sage (Unit Z)
The capstone unit. Shows that the archimedean and non-archimedean places
share the exact same (l+1)/24 coefficient, differing only in the base
quantity.
 
=====================================================================
WHAT IS NOT VERIFIED
=====================================================================
This repository verifies the exact numerical and algebraic arithmetic of IUT IV.
It does NOT verify:
1. The structural existence of the Theta-link.
2. The global possible-image hull.
3. The Scholze-Stix objection.
4. Corollary 3.12 or Theorem 1.10 as structural theorems.
5. The ABC conjecture. 
Please see Section 8 of the paper for full scope limitations.
 
=====================================================================
CITATION
=====================================================================
If you use this code in your research, please cite:
 
Chun Wing Lai, "Exact Arithmetic Verification of Inter-Universal Teichmuller
Theory IV", preprint, November 2026.
=====================================================================