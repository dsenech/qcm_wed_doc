.. include:: options_intro.txt

Boolean options
=========================
.. csv-table::
    :header: "name", "default", "description"
    :widths: 15, 10, 50

    "verb_Hilbert", "false", "prints progress information on bases and operators in the Hilbert space"
    "verb_ED", "false", "prints ED information and progress"
    "verb_integrals", "false", "prints information and progress about integrals"
    "CSR_sym_store", "false", "stores CSR matrices fully for openMP application"
    "strip_anomalous_self", "false", "sets to zero the anomalous part of the self-energy"
    "print_Hamiltonian", "false", "Prints the Hamiltonian on the screen, if small enough"
    "SEF_calc", "false", "Calculates the Self-energy functional, even when not performing VCA"
    "periodized_averages", "false", "computes lattice averages using the periodized Green function"
    "continued_fraction", "false", "Uses the continued fraction solver for the Green function instead of the band Lanczos method"
    "dual_basis", "false", "uses the dual basis for wavevector computations"
    "nosym", "false", "does not take cluster symmetries into account"
    "modified_Lanczos", "false", "Uses the modified Lanczos method for the ground state instead of the usual Lanczos method"
    "periodic", "false", "considers the cluster(s) as periodic"
    "zero_dim", "false", "sets the spatial dimension to zero, on any model"
    "print_all", "false", "prints dependent parameters as well"
    "check_lanczos_residual", "false", "checks the Lanczos residual at the end of the eigenvector computation"
    "no_degenerate_BL", "false", "forbids band lanczos to proceed when the eigenstates have degenerate energies"
    "potential_energy", "false", "Calculates the potential energy with Tr(Sigma*G) when computing averages"
    "one_body_solution", "false", "Only solves the one-body part of the problem, for the Green function"



Integer-valued options
=========================
.. csv-table::
    :header: "name", "default", "description"
    :widths: 15, 10, 50

    "max_iter_lanczos", "600", "Maximum number of iterations in the Lanczos procedure"
    "max_iter_QN", "60", "maximum number of iterations in the quasi-Newton method"
    "cuba3D_mineval", "16000", "minimum number of integrand evaluations in CUBA (3D)"
    "seed", "0", "seed of the random number generator"
    "kgrid_side", "32", "number of wavevectors on the side in a fixed wavevector grid"
    "print_precision", "8", "precision of printed output"
    "cuba2D_mineval", "1024", "minimum number of integrand evaluations in CUBA (2D)"
    "dim_max_print", "64", "Maximum dimension for printing vectors and matrices"
    "max_iter_CF", "400", "Maximum number of iterations in the continuous fraction Lanczos procedure"
    "GK_min_regions", "8", "minimum number of regions in the Gauss-Kronrod method"
    "Davidson_states", "1", "Number of states requested in the Davidson-Liu algorithm"
    "max_dim_full", "256", "Maximum dimension for using full diagonalization"
    "max_iter_BL", "600", "Maximum number of iterations in the band Lanczos procedure"



Real-valued options
=========================
.. csv-table::
    :header: "name", "default", "description"
    :widths: 15, 10, 50

    "Qmatrix_vtol", "1e-10", "minimum value of a Qmatrix contribution"
    "Qmatrix_wtol", "1e-05", "maximum difference in frequencies in Q-matrix"
    "band_lanczos_minimum_gap", "1e-05", "gap between the lowest two states in BL below which the method fails"
    "accur_Q_matrix", "1e-05", "tolerance in the normalization of the Q matrix"
    "minimum_weight", "0.01", "minimum weight in the density matrix"
    "cutoff_scale", "1e+12", "high-frequency cutoff in integrals"
    "large_scale", "20", "high-frequency region for imaginary frequency axis integrals"
    "eta", "0.0001", "value of the imaginary part of the frequency in Chern number/Berry phase computations"
    "temperature", "0", "Temperature of the system."
    "accur_OP", "0.0001", "accuracy of lattice averages"
    "small_scale", "0.5", "low-frequency region for imaginary frequency axis integrals"
    "accur_SEF", "5e-08", "Accuracy of the Potthoff functional"
    "accur_continued_fraction", "0.01", "value of beta below which the simple Lanczos process stops"
    "accur_Davidson", "1e-05", "maximum norm of residuals in the Davidson-Liu algorithm"
    "accur_lanczos", "1e-12", "tolerance of the Ritz residual estimate in the Lanczos method"
    "accur_band_lanczos", "1e-12", "energy difference tolerance for stopping the BL process"
    "accur_deflation", "1e-07", "norm below which a vector is deflated in the Band Lanczos method"



Char-valued options
=========================
.. csv-table::
    :header: "name", "default", "description"
    :widths: 15, 10, 50

    "Hamiltonian_format", "S", "Desired Hamiltonian format: S (CSR matrix), O (individual operators), F (factorized), N (none = on the fly)"
    "periodization", "G", "periodization scheme: G, S, M, C or N (None)"



