# TODO

## Major

- [ ] Accelerate batchFindSignificantFeatures (too slow now)
- [ ] Add enrichment methods
- [ ] add raw dose viability part, recomputeAUC using PharmacoGx method,



## Middle

- [ ] single data compare, find cell line, compare types(CXP)
  - [ ] Try Co_Occurence(like maftools) part for drugs
- [x] Harmonized drug and cell names
  - [x] how to build a name checker agent?
- [ ] How to allow user analysis data without loading all datasets locally
- [ ] reload normalization will cause process dead
- [ ] Add combintation drugs results parts
  - [ ] in house
  - [ ] synergy prediction
- [ ] server check2 (make shiny load faster)
  - Preloading noticed screen
  - options(shiny.idle_timeout = 0)
  - Using the future and promises packages to run computations asynchronously
- [ ] Add data ranking check(allow user highlight interested features), drug rank(select a cell) and cell rank(select a feature)
- [ ] Add PDO WES
- [ ] add chemical structure info 
- [ ] https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-014-0367-1/figures/1 seems better to use rank based method (how to solve the direction problem, seems ok, smaller means another direction, and the median rank is to devide into two parts)
  - try to see the performance of rank method
- [ ] more detailed cellline data
  - [ ] [Cellosaurus cell line MDA-MB-361 (CVCL_0620)](https://www.cellosaurus.org/CVCL_0620)
- [ ] [Integrating heterogeneous drug sensitivity data from cancer pharmacogenomic studies - PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC5239501/) calculate other matric

- [ ] Add ecDNA predict method
  - MYC ecDNA promotes intratumour heterogeneity and plasticity in PDAC, AmpliconArchitect
- [ ] 



## Minor

- [ ] what para orchestra official used for calculate AAC
- [ ] recheck cellline WES results
- [ ] Add drug annotation for drug screen in batch mode
- [x] volcano plot seems a bug wrongly highlight top5
- [ ] Add compare methods
- [ ] Add user counts
- [ ] adapt to mobile user



# DB

- 标准化omics, drug data 纳入过程 (对象)
  - Assessment of modelling strategies for drug response prediction in cell lines and xenografts，重新计算一些药敏相关的指标

- 直接比一下global 和drug level 的，看看区别大不大



# Tools

- clinicalgenome
- oncomx expression

- Tdc, datasets for Txgemma/txagent, Marinka Zitnik



# agent

- 开发agent
  - 安全性考量，MCP 能否解决？
  - 给予操纵环境能力？
  - 直接用camel.ai 实例一个小模型做agent，通过MCP 调用DROMA-DB 方法



# Augur

- 预测方法
  - [TxGNN Explorer](http://txgnn.org/)
    - [Nature Medicine | AI指导 “旧药新用”](https://mp.weixin.qq.com/s/hSxcWXPWwWT5S1lmx_zBXw)
  - https://www.perplexity.ai/search/it-is-recommanded-to-use-z-sco-sOgK4n2xRz2dOl1GESf7cw#5
    - 预测还是用global z-score 吧
    - https://www.perplexity.ai/search/it-is-recommanded-to-use-z-sco-sOgK4n2xRz2dOl1GESf7cw#10 并不是很能信服



解卷积方法有无应用空间：https://github.com/Huber-group-EMBL/DepInfeR



# V1

DB:

- data
  - Denglab pdo data, add NCI60 PDC, PDX data
  - perturbation results
  - add before after treatment data
- analysis
  - similarity part
  - Ref:
    - PDX: [bioconductor.org/packages/release/bioc/vignettes/Xeva/inst/doc/Xeva.pdf#page=11.17](https://bioconductor.org/packages/release/bioc/vignettes/Xeva/inst/doc/Xeva.pdf#page=11.17)
    - others: [Bioconductor - PharmacoGx](https://www.bioconductor.org/packages/release/bioc/html/PharmacoGx.html)
- package result
- handle big raw data
  - Sql?
- outside API
  - TDC
  - **PGxDB**



Augur:

- algorithm try
  - TxGNN
  - TabFNN
  - machine learning methods
  - chemical info?
- Explainable?



agent:

- AI interface
  - camel
- multiagent
  - Collect
  - Reason
  - instruct
- tools
  - MCP
  - toolRAGs?



# 竞争对手

- Haibe-Kains
- https://www.cancermodels.org/ jackson lab
- [Therapeutics Data Commons - TDC](https://tdcommons.ai/) harvord google 
- [pgx-db.org/drug_lookup/](https://pgx-db.org/drug_lookup/) university of Copenhagen