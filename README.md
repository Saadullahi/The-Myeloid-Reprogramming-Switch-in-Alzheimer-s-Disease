# The-Myeloid-Reprogramming-Switch-in-Alzheimer-s-Disease
The Myeloid Reprogramming Switch in Alzheimer’s Disease: Sensory Transduction Silencing and Activation of the APOE-Innate Sentinel Module is an extension of the Neurodegenerative Disease Group project in the 2026 Biocoding Bootcamp Internship with Genomac Institute
This Jupyter Notebook outlines a comprehensive differential gene expression and systems biology pipeline analyzing transcriptomic profiles of brain-resident immune (myeloid) cells in Alzheimer's Disease (AD) compared to healthy controls.
Here is a high-level breakdown of the biological themes and computational steps executed in the notebook:
1. Computational & Statistical Framework
•	Differential Expression Analysis: Using PyDESeq2 (a Python implementation of the gold-standard DESeq2 framework), the pipeline models gene counts using a Negative Binomial distribution to control for overdispersion across $3\text{ AD}$$3\text{ AD}$ vs. $3\text{ Control}$$3\text{ Control}$ biological replicates.
•	Stringent Filtering: Identified 1,303 statistically significant differentially expressed genes using an FDR-corrected significance threshold ($P_{\text{adj}} < 0.05$$P_{\text{adj}} < 0.05$).
•	Visual Diagnostics: Explored global transcriptomic structures using MA Plots (expression-dependent bias) and Volcano Plots (significance vs. fold-change effect size).
2. Biological Revelations: The Transcriptomic "Switch"
The study reveals a clear, coordinated transition where myeloid cells trade their baseline environmental surveillance programs for an active defense and lipid-processing phenotype:
•	Sensory Silencing (Downregulated Signature): 
o	Key Pathway: Olfactory Transduction ($P_{\text{adj}} = 5.94 \times 10^{-10}$$P_{\text{adj}} = 5.94 \times 10^{-10}$) and GABAergic Synapses.
o	Implication: Healthy myeloid cells utilize membrane GPCRs and neuroimmune synaptic machinery to survey the brain. In the AD microenvironment, this sensory machinery is systematically silenced.
•	Active Disease-Associated Defense (Upregulated Signature):
o	Key Pathway: Complement and Coagulation Cascades and Fatty Acid Homeostasis.
o	Implication: Activation of a highly synchronized, dense functional module dominated by specialized metabolic and innate immune sensors.
3. Network Topology & Key Regulatory Hubs
By projecting the top enriched Biological Processes into a Gene-Concept Network Map, the study mathematically validated a highly centralized functional module governed by five key genes:
1.	NOD2 (Centrality: 0.231) & TLR2 (Centrality: 0.192): Extracellular and cytoplasmic pattern recognition sensors primed to coordinate defensive responses against neurotoxic $A\beta$$A\beta$ plaque aggregates.
2.	APOE (Centrality: 0.192): The master regulator of lipid clearance, dramatically upregulated in AD replicates ($>1,200$$>1,200$ normalized counts) compared to controls.
3.	XBP1 (Centrality: 0.154): Highly co-regulated with APOE ($r = 0.965$$r = 0.965$), driving endoplasmic reticulum stress management to support lipid-clearing protein folding demands.
4.	THBD (Centrality: 0.192): Exhibits a negative correlation with APOE ($r \approx -0.458$$r \approx -0.458$), indicating a functional partitioning at the neurovascular interface where vascular integrity (high-THBD) and aggressive lipid clearance (high-APOE) are mutually exclusive activation phases.
