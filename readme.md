# The project involves evaluation of mutual exclusivity methods: Discover, Discover_strat, Fisher's Exact Test, MEGSA, MEMO and WExT. The results from these methods include pairwise mutual exclusivity p-values. Based on them, we apply our network centric epistatic evaluation.

# This is a concise repository for the epistasis project codes. We experimented with many ideas, factors and parameters. Some of them are not included for the final paper.

### Structure

#### 1. mutex_data: Includes all the input data such as mutual_exclusivity files, MLA files, PPI files etc. "{method}_mutation_filtered_ep_data" folder contains the MEX files.

	A. binary_matrices_all_genes_ep_mutation_filtered: includes binary matrices for mutation data.

	B. {method}_mutation_filtered_ep_data: inlcudes pairwise mutual exclusivity p-values.

	C. molecular_strat_patient_list: includes patient and subtype information for BRCA and COADREAD molecular stratification.

	D. MLA_ep_mutation_filtered_all_genes: Corresponding MLA.

	E. rare_genes: 2% or 3% rare genes.

	F: Census_allFri_Apr_26_12_49_57_2019.tsv: COSMIC file (Known driver genes)


#### 2. src_main: this includes the source code for the proposed evaluation and additional analysis

	A. evaluate_methods_on_permutations_version3_with_case_counts_rare.ipynb is the main source code for the evaluation. As output, you get tables with all analysis results.

	B. prep_table_for_latex.ipynb takes the evaluation results (A) and preps the result in Latex format. It is convenient for creating tables (check main paper and supplementary table formats, some &s may need to be removed).

	C. perc_sig_all_comb_rare.ipynb computes genewise percentage significance and save the file. I separated this since it takes a long time for t5. Relevant for plotting non-randomized plots quickly.

	D. plot_perc_sig_fig3_random_sampling_neighbors.ipynb takes the mutex files as input, and plots %sig.
	

#### 3. results_main: This contains the results from the scripts in src_main.