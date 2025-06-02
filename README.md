**PYTHON IMPLEMENTATION FOR THE MASTER PROJECT "Raf Signalling Pathway Reconstruction and
Robust Inference using Bayesian Coupled Model"**

*model.py*
- It contains the full implementation of the MCMC sampling scheme concerning the Bayesian coupled model with Gibbs prior distribution for DAGs as done by Werhli & Husmeier
- It extends the Werhli & Husmeier model by introducing a CPDAG coupling, skeleton coupling, Sequence Accumulating $k_{n}$-configuration Interactions (SAKI) algorithm, Enhanced Perfect Gas Approximation (EPGA), and additional meta-optimization techniques
- Input: see config.py
- Output: $I$ Averaged CPDAG networks sampled by the MCMC (heatmap); Mean CPDAG of the $I$ averaged CPDAGs (heatmap); Average of the sampled hypernetworks (heatmap); Parameter histograms; Parameter traceplots; PR curves; ROC curves; File containing all ROC and PR results for both CPDAG reconstruction and skeleton reconstruction of the true (CP)DAG 
- Remark: For serious experiments, launch on HPC such as Habrok. Multiprocessing is possible by modifying the launcher function plotMCMC()

*config.py*
- Configuration file for *model.py* containing all input networks/parameters (see the file itself for additional details)
- Remark: You might need to run this script before launching *model.py*

*Partition_function_empirical_analysis.ipynb*
- Source code for Section 4.1
- Empirical analysis of the CPU time when computing the partition function with EPGA and PGA
- Empirical analysis of the behavior of the Mismatch Energy Sums for each coupling scheme
- Remark/Warning: Computationally expensive

*StatisticalAnalysis.ipynb*
- Source code for the statistical analysis as described in Section 4.2
- Shapiro test, paired t-test, one-way ANOVA, Confidence Intervals

*data.py*
- It creates a .json file with the results of the numerous numerical experiments conducted on Habrok
- Remark: You might need to run this script before proceeding to *StatisticalAnalysis.ipynb*  
