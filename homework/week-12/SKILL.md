---
name: compare-clustering
description: Use only when explicitly invoked to explore unlabeled groups in tabular numeric data and report one selected clustering.
---

# Compare clustering methods

Use this skill only when explicitly named or supplied by path. Take the dataset, observation unit, feature columns, optional identifiers and known labels from the invocation. Keep identifiers for tracking rows. Set known labels aside until the model and cluster assignments are frozen.

1. **Prepare the features.** Check dimensions, row alignment, missing or infinite values, duplicates, and constant columns. Resolve data issues explicitly. Choose centering and scaling based on feature units and the meaning of variance. For many correlated features, consider PCA. Specify a variance target or component count before comparing fits. Use the same feature space for every candidate.

2. **Fit candidates.** Run at least three distinct algorithms, such as multistart K-means, Ward hierarchical clustering with Euclidean distance, and spectral clustering with an RBF affinity. For the RBF affinity, try the median nonzero squared distance as a starting bandwidth, with nearby bandwidths if tuning the affinity. Compare a small prespecified range of cluster counts (for example, 2 through 6 when the sample size allows). Record the settings and seed. Exclude failed fits and groups smaller than a prespecified minimum, unless finding rare groups is the stated goal.

3. **Select one fit.** Compare mean silhouette in the shared feature space. Estimate stability with repeated common subsamples drawn without replacement. Refit preprocessing and clustering on each subsample using the candidate's settings. If using a bandwidth multiplier, hold it fixed and recompute the reference distance in each subsample. Compute adjusted Rand index (ARI) against the full-data assignments for the retained rows and summarize it by the median. Assign a score of -1 to failed refits or refits returning fewer groups than requested, and record how often this happens. Set the selection rule before fitting. A default is to shortlist fits within 0.02 of the highest silhouette, then choose the highest median ARI, with silhouette, fewer clusters and a fixed candidate order breaking ties. Identify weak separation or instability even if a candidate ranks first. Keep full candidate scores in the working files.

4. **Interpret and check.** Verify assignment counts, chosen settings and scores. Use a readable plot of the chosen assignments, such as a scatterplot of the first two PCs with variance percentages on the axes. Explain what the plot shows and that projection can hide separation in the fitting space. Describe cluster sizes and observable patterns. If known labels are supplied, compare them with the frozen assignments using counts and limit that comparison to interpretation.

5. **Report.** Limit the generated analysis report to one printed page, including all text, figures and tables. Present clustering results from only the one selected method. Briefly name the other algorithms and explain the selection criteria without showing their scores, assignments, or plots. Include the most informative display, the selected fit's evidence, and a limitation. Print-preview the report to check its length and legibility. Keep code and any skill appendix after the analysis or in separate files, with the appendix starting on a new page if included.
