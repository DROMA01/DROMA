# DROMA
Drug Response Omics association MAp (DROMA, 卓玛)  

<img src="https://github.com/user-attachments/assets/000473aa-7869-41c8-9352-e8481ba922fa" alt="image" style="zoom:50%;" />

DROMA-DB is a comprehensive database and analysis tool that integrates the largest published studies investigating cancer response to chemical compounds and the associations between drug sensitivity and multi-omics data (mRNA, CNV, protein, mutation, etc.) across various cancer models including PDC (Patient-Derived Cells), PDO (Patient-Derived Organoids), and PDX, human data are under development. 

![image](https://github.com/user-attachments/assets/89b385e0-f5e4-4d8e-a33b-5f30bed039b2)



## Main components

- Projects about data:

DROMA_DB: [mugpeng/DROMA_DB: Sqlite db and DromaSet obj for Drug Response Omics association MAp. (DROMA)](https://github.com/mugpeng/DROMA_DB)

DROMA_Set: [mugpeng/DROMA_Set: DROMASet is a comprehensive R package for managing and analyzing drug response and omics data across multiple projects. It provides a robust framework for handling complex multi-omics datasets with integrated drug sensitivity information, enabling seamless cross-project comparisons and analyses.](https://github.com/mugpeng/DROMA_set)

- Projects about analysis:

DROMA_R: [mugpeng/DROMA_R: R package for DROMA.](https://github.com/mugpeng/DROMA_R)

DROMA_Web: [mugpeng/DROMA_Web: Shiny website for Drug Response Omics association MAp. (DROMA)](https://github.com/mugpeng/DROMA_web)

- Under development:

DROMA_MCP, DROMA_AI, DROMA_Augur, DROMA_py



## Statistics Info

Include 17 datasets now(11 cell line, 2 PDC, 3 PDO, 1 PDX), totally 2599 unique samples and 56398 unique drugs.

![](https://raw.githubusercontent.com/mugpeng/mugpeng-my-gallery-02/main/img20250513115037.png)

![](https://raw.githubusercontent.com/mugpeng/mugpeng-my-gallery-02/main/img20250513114926.png)







## Citation

If you use DROMA-DB in your research, please cite:

Li, S., Peng, Y., Chen, M. et al. Facilitating integrative and personalized oncology omics analysis with UCSCXenaShiny. Commun Biol 7, 1200 (2024). https://doi.org/10.1038/s42003-024-06891-2



## Milestone

### 0513 v0.3

Refactor App.R and Modules: Update version to 0.3.

- add new datasets, now have in vivo data now(Xeva PDX dataset), totally include 17 datasets now(11 cell line, 2 PDC, 3 PDO, 1 PDX)

![](https://raw.githubusercontent.com/mugpeng/mugpeng-my-gallery-02/main/img20250513115037.png)

- add new module, and enhance drug feature analysis. 
- Remove deprecated Rmd files and adjust data loading paths. 
- Update BatchFeature and DrugOmicPair modules for improved functionality and user experience.
- Functionize all functions in modules and put them under `Package_Function/` preparing for making DROMA R package.
- fix some bugs.





### 0319

I will attend UM PhD seminar, welcome!
<img width="446" alt="image" src="https://github.com/user-attachments/assets/72adc553-f807-48f8-afa8-bb4009eef963" />



### 0318 v0.2

The stable version v0.2 is online now in UM network: http://fscpo.fhs.um.edu.mo/DROMA_DB/
Btw, please be patient, it may take 10-20s when first time start it. :)

This update includes:

1) Add denglab three PDO data(deng1(breast), deng2(colon), deng3(nasopharynx)) with paired RNAseq, IC50 and annotation data;
2) Harmonize cell line drug and cell names also the annotation data;
3) Add choice to filter data for a specific tumor type(Breast, lung..) or data type(cell line, PDO), and a global setting page to set data. Now all continous data is transformed to by z-score in default, which allow to add a merged result for visualization ;
4) Add several figures and some visualization-related improvement.

