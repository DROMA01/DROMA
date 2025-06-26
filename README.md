# DROMA
Drug Response Omics association MAp (DROMA, 卓玛)  

<img src="https://github.com/user-attachments/assets/000473aa-7869-41c8-9352-e8481ba922fa" alt="image" style="zoom:50%;" />

DROMA is a comprehensive database and analysis tool that integrates the largest published studies investigating cancer response to chemical compounds and the associations between drug sensitivity and multi-omics data (mRNA, CNV, protein, mutation, etc.) across various cancer models including PDC (Patient-Derived Cells), PDO (Patient-Derived Organoids), and PDX, human data are under development. 

# Integration with DROMA Ecosystem

The DROMA_DB serves as the foundation for the broader DROMA ecosystem:

1. **[DROMA_DB](https://github.com/mugpeng/DROMA_DB)**: Database creation and management, the backbone for DROMA project.
2. **[DROMA_Set](https://github.com/mugpeng/DROMA_Set)**: R package  for managing and analyzing drug response and omics data across multiple projects, interact with the sqldb dataset producing from DROMA_DB.
3. **[DROMA_R](https://github.com/mugpeng/DROMA_R)**: R package provides advanced analysis functions for drug-omics associations using DromaSet and MultiDromaSet objects from the DROMA.Set package.
4. **[DROMA_Web](https://github.com/mugpeng/DROMA_web)**: Shiny website for Drug Response Omics association MAp based on DROMA_DB, DROMA_Set and DROMA_R.
5. **[DROMA_MCP](https://github.com/mugpeng/DROMA_MCP)**: A Model Context Protocol (MCP) server for DROMA (Drug Response Omics association MAp) - enabling natural language interactions with drug-omics association analysis.

Other components including DROMA_AI, DROMA_Augur, DROMA_py are underdevelopment now.


```
我们开发的DROMA（Drug Response Omics association MAp, 药物反应组学关联图谱）是一个精准肿瘤学领域的综合性药物反应分析平台。它的核心目标是解决当前分析工具在直观可视化、全面数据整合和透明统计模型方面的不足，从而更好地进行生物学解读和假设生成。

DROMA平台的核心功能主要包括三个紧密相关的组成部分：
1.  DROMA-DB（数据库和分析工具）：该组件致力于实现药物反应模式的动态可视化和元分析，支持高通量生物标志物的发现和个性化分析。DROMA-DB整合了来自癌细胞系和患者来源类器官的多维组学数据（如基因表达、拷贝数变异、DNA甲基化等）与药物敏感性信息，目前已包含超过55000种药物和2500个样本（世界最大开源的整合高通量药敏数据集），并且仍在不断更新中。
2.  DROMA-Augur（预测建模）：此组件专注于药物反应的预测建模。目标是开发机器学习方法提高药物反应预测的准确性，特别是针对像患者来源类器官（PDOs）这样的小型数据集。同时，改进一些已发表的先进方法或可解释性算法，例如TxGNN、TabPFN、TCRP，以及一些强效的机器学习模型，如随机森林和XGBoost。
3.  DROMA-AI（AI辅助工作流）：旨在创建一个用户友好的网页界面，提供AI辅助的分析工作流。这包括开发多智能体系统进行代码生成和报告验证，以及利用大语言模型（LLM）的能力，根据不同层面的证据来生成科学假设。同时开发一个DROMA-MCP 工具以满足不同agent 或llm 的需求。

对于DROMA-AI，开发一个由不同类型的大语言模型驱动的多智能体系统，这些智能体可能扮演团队领导、工具使用者、总结者和指导者的角色 。利用LLM的能力来自动生成分析报告，并引导用户完成复杂的数据分析任务 。结合LLM进行假设生成，使其能够基于不同层面的证据提出新的科学见解 。
```



## Main components

![](https://raw.githubusercontent.com/mugpeng/mugpeng-my-gallery-02/main/img20250619145856.png)



- Projects about data:

DROMA_DB: [mugpeng/DROMA_DB: Sqlite db and DromaSet obj for Drug Response Omics association MAp. (DROMA)](https://github.com/mugpeng/DROMA_DB)

DROMA_Set: [mugpeng/DROMA_Set: DROMASet is a comprehensive R package for managing and analyzing drug response and omics data across multiple projects. It provides a robust framework for handling complex multi-omics datasets with integrated drug sensitivity information, enabling seamless cross-project comparisons and analyses.](https://github.com/mugpeng/DROMA_set)

- Projects about analysis:

DROMA_R: [mugpeng/DROMA_R: R package for DROMA.](https://github.com/mugpeng/DROMA_R)

DROMA_Web: [mugpeng/DROMA_Web: Shiny website for Drug Response Omics association MAp. (DROMA)](https://github.com/mugpeng/DROMA_web)

- AI and AI agent:

DROMA_MCP: [mugpeng/DROMA_MCP: DROMA MCP Server bridges the gap between AI assistants and cancer pharmacogenomics analysis by providing a natural language interface to the [DROMA.R](https://github.com/mugpeng/DROMA_R) and [DROMA.Set](https://github.com/mugpeng/DROMA_Set) packages.](https://github.com/mugpeng/DROMA_MCP)



- Under development:

DROMA_MCP, DROMA_AI, DROMA_Augur, DROMA_py



## Statistics Info

Include 17 datasets now(11 cell line, 2 PDC, 3 PDO, 1 PDX), totally 2599 unique samples and 56398 unique drugs.

![](https://raw.githubusercontent.com/mugpeng/mugpeng-my-gallery-02/main/img20250513115037.png)

![](https://raw.githubusercontent.com/mugpeng/mugpeng-my-gallery-02/main/img20250513114926.png)







## Citation

If you use DROMA or any subprojects(DB, R, web..) in your research, please cite:

Li, S., Peng, Y., Chen, M. et al. Facilitating integrative and personalized oncology omics analysis with UCSCXenaShiny. Commun Biol 7, 1200 (2024). https://doi.org/10.1038/s42003-024-06891-2



## Milestone

### 0526 v0.4 andata

坂本龍一:【氛围感｜andata (Electric Youth Remix)】 https://www.bilibili.com/video/BV1v7kAY7Eoi/?share_source=copy_web&vd_source=bd40fa636d7a7f4f2a51596fed85e2b0



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

