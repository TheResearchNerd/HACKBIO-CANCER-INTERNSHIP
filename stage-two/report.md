**GENE EXPRESSION ANALYSIS, VISUALISATION AND DOWNSTREAM FUNCTIONAL ENRICHMENT ANALYSIS OF GLIOBLASTOMA DATASET**
**Team: Biomarker Hunters and Data Scientists**
**Authors (@slack): Oluwatobi Ogundepo (@Oluwatobi), Abdulrahman Walid Elbagoury (@Willeau), Olabode Kaosara Omowunmi (@TheResearchNerd), Awoleke Ifeoluwa (@Ifeolu01), Henry Momanyi (@Henry), Benedict Orile Ajunku (@orile), Olajumoke Oladosu (@Jumblosu), Mary Dhevanayagam (@Shanu)**

Link to the code: hackbio-cancer-internship/stage-two/code.R at main · marydhevanayagam/hackbio-cancer-internship (github.com)

Link to the dataset: https://raw.githubusercontent.com/HackBio-Internship/public_datasets/main/Cancer2024/glioblastoma.csv

**GLIOBLASTOMA**
Glioblastoma is the most common and aggressive primary brain tumour in adults, characterised by necrosis and endothelial proliferation.1 It may arise from specific point mutations of the genes encoding IDH (isocitrate dehydrogenase).2 Typical molecular changes in glioblastoma include mutations in genes regulating receptor tyrosine kinase (RTK)/ RAS/phosphoinositide 3-kinase (PI3K), p53, and retinoblastoma protein signalling.3

In this task, a gene expression dataset for glioblastoma was visualized and interpreted to generate a heatmap and downstream functional enrichment analysis was performed. This helped to understand and interpret patterns of gene expression and the biological significance of differentially expressed genes (DEGs). The task involved data preprocessing, visualization, and interpretation of functional enrichment results.

**Task 1** - Generate a heatmap for the entire dataset. Use a diverging and sequential color palette to generate two color variants of the same heatmap. 

 
Figure 1. Task 1 output 1 - heatmap with diverging colour palette.
![image](https://github.com/user-attachments/assets/0219e4ce-fd05-4041-ae10-4c333244f833)

 
Figure 2. Task 1 output 2 - heatmap with sequential colour palette.
![image](https://github.com/user-attachments/assets/75250732-38de-4b9b-b943-2a29e5f4365a)

Colour selection is important for visualising and interpreting datasets using plots such as heatmaps as it enhances contrast using colour palettes to differentiate between different values in the plot and to emphasize on significant differences in the data.4 Sequential colour palette does not consist of a neutral central value, while a diverging colour palette consists of two different colours with a neutral central value, which is useful for observing deviations from the midpoint. The plots can also be easier to interpret by people with colour blindness when specific colour palettes are used.5 

Task 2 - With the same heatmap, generate a variant of your heatmap where you
a.	Cluster your genes (rows) alone
b.	Cluster your samples (columns) alone
c.	Cluster both genes and sample together.

 
Figure 3. Task 2 output 1 - clustering genes (rows) alone.
![image](https://github.com/user-attachments/assets/c3be2047-8ea0-41a1-abeb-f5f3164f0c2c)

 
Figure 4. Task 2 output 2 - clustering samples (columns) alone.
![image](https://github.com/user-attachments/assets/32b59089-0dda-4c1b-9924-b91999bd24db)

 
Figure 5. Task 2 output 3 - clustering both genes and sample together.
![image](https://github.com/user-attachments/assets/b795db04-f5eb-4498-9b8d-ad8594bfbf6a)

Clustering rows (genes) and columns (samples) in the heatmap is important for data analysis as it helps to identify patterns or relationships within the dataset, providing a better visual representation of the genes and samples with similar characteristics.6

 
Tasks 3 & 4 - Subset genes that are significantly upregulated and significantly downregulated. (Setup your own cut-offs for the fold change and p-values).
 
Figure 6. Tasks 3 & 4 output 1 – volcano plot of glioblastoma data.
![image](https://github.com/user-attachments/assets/112f9c17-66f8-4771-aa20-39fa2ad775dc)

 
Figure 7. Tasks 3 & 4 output 2 – volcano plot of glioblastoma data.
![image](https://github.com/user-attachments/assets/4059f05a-6ed6-4982-bd8e-465eadf40103)

- The p-value cut-off was set as 0.05, with log2fold-change of 21 to 3 for significantly upregulated genes and -22 to -3 for significantly downregulated genes.
 
 
 

Task 5 - Perform functional enrichment analysis with either ShinyGO, GOrilla or PANTHER.
-	The gene IDs were submitted to ShinyGO
-	The p-value cutoff was set at 0.05.

 
Figure 8. Task 5 output – functional enrichment analysis.
![image](https://github.com/user-attachments/assets/e5548657-2aab-4c34-aa8c-118967f2f0e7)

Task 6 - Using the top 5 pathways, create a straightforward visualization (such as a lollipop plot, dot plot, line plot or bubble plot) that displays the number of genes associated with each pathway. The plot should also reflect the significance of each pathway by scaling the points according to the negative log10 of the p-value.

 
Figure 9. Task 6 output - top five enriched KEGG pathways.
![image](https://github.com/user-attachments/assets/7f742aec-ea6b-47ee-80cf-0162fff1bc57)


Task 7 - Describe the top 3 enriched pathways according to biological process.

 
Figure 10. Task 7 output - enriched pathways (according to biological process).
![image](https://github.com/user-attachments/assets/dfa14271-2df6-4894-82c5-aa25ad2e150f)

1)	Loop of Henle development – It is the process involved in the development of a part of the kidney called as Loop of Henle, which consists of a descending limb and an ascending limb. This structure is involved in regulating the concentration of urine.7 This developmental pathway is regulated by various signalling molecules, growth and transcription factors, including Wnt and Notch.8 Upregulation of these signalling mechanisms in glioblastoma is associated with resistance to apoptosis and increased cell survival, which can promote tumour growth.

2)	Proximal/distal pattern formation – It is the process which determines the formation of proximal-distal regions of developing tissues, which is mainly stimulated by FGF (Fibroblast Growth Factor) signalling.9 While FGF usually promotes the formation of distal structures, other elements such as retinoic acid promotes proximal features.10 Excess FGF signalling can facilitate tumour progression in glioblastoma.

3)	Lymphocyte chemotaxis – It is the process by which cells cross barriers such as the vascular endothelium and migrates within tissues, which is typically stimulated by chemokines via G-protein coupled receptors.11 Production of chemokines by glioblastoma cells can progress tumour formation by suppressing the body's immune response.12


References:
1.	Wirsching, H.-G., Galanis, E. and Weller, M. (2016) “Glioblastoma,” in Handbook of Clinical Neurology. Elsevier, pp. 381–397. Available at: https://www.sciencedirect.com/science/article/abs/pii/B9780128029978000232
2.	Han, S. et al. (2020) “IDH mutation in glioma: molecular mechanisms and potential therapeutic targets,” British journal of cancer, 122(11), pp. 1580–1589. DOI: 10.1038/s41416-020-0814-x.
3.	Davis, M. (2016) “Glioblastoma: Overview of disease and treatment,” Clinical journal of oncology nursing, 20(5), pp. S2–S8. DOI: 10.1188/16.cjon.s1.2-8.
4.	Nakić, J., Kosović, I. N. and Franić, A. (2022) “User-centered design as a method for engaging users in the development of geovisualization: A use case of temperature visualization,” Applied sciences (Basel, Switzerland), 12(17), p. 8754. DOI: 10.3390/app12178754.
5.	Crameri, F. and Hason, S. (2024) “Navigating color integrity in data visualization,” Patterns (New York, N.Y.), 5(5), p. 100972. DOI: 10.1016/j.patter.2024.100972.
6.	Engle, S. et al. (2017) “Unboxing cluster heatmaps,” BMC bioinformatics, 18(S2). DOI: 10.1186/s12859-016-1442-6.
7.	Chang, C.-H. and Davies, J. A. (2019) “In developing mouse kidneys, orientation of loop of Henle growth is adaptive and guided by long‐range cues from medullary collecting ducts,” Journal of anatomy, 235(2), pp. 262–270. DOI: 10.1111/joa.13012.
8.	Chai, O.-H. et al. (2013) “Molecular regulation of kidney development,” Anatomy & cell biology, 46(1), p. 19. DOI: 10.5115/acb.2013.46.1.19.
9.	Sheeba, C. J., Andrade, R. P. and Palmeirim, I. (2016) “Getting a handle on embryo limb development: Molecular interactions driving limb outgrowth and patterning,” Seminars in cell & developmental biology, 49, pp. 92–101. DOI: 10.1016/j.semcdb.2015.01.007.
10.	Feneck, E. and Logan, M. (2020) “The role of retinoic acid in establishing the early limb bud,” Biomolecules, 10(2), p. 312. DOI: 10.3390/biom10020312.
11.	Kim, B. et al. (2016) “Roles of the mitochondrial Na+-Ca2+ exchanger, NCLX, in B lymphocyte chemotaxis,” Scientific reports, 6(1), pp. 1–10. DOI: 10.1038/srep28378.
12.	Ardizzone, A. et al. (2023) “Recent emerging immunological treatments for primary brain tumors: Focus on chemokine-targeting immunotherapies,” Cells (Basel, Switzerland), 12(6), p. 841. DOI: 10.3390/cells12060841.


