# DROMA
**药物反应组学关联图谱** (DROMA, 卓玛)  

[![Website](https://img.shields.io/website?url=https%3A//droma01.github.io/DROMA)](https://droma01.github.io/DROMA)
[![GitHub Stars](https://img.shields.io/github/stars/DROMA01/DROMA?style=social)](https://github.com/DROMA01/DROMA)
[![License: MPL-2.0](https://img.shields.io/badge/License-MPL--2.0-yellow.svg)](https://opensource.org/licenses/MPL-2.0)
[![R](https://img.shields.io/badge/R-%3E%3D4.0.0-blue.svg)](https://www.r-project.org/)
[![Python](https://img.shields.io/badge/Python-3.10+-green.svg)](https://www.python.org/)
[![DOI](https://zenodo.org/badge/DOI/10.1038/s42003-024-06891-2.svg)](https://doi.org/10.1038/s42003-024-06891-2)

<div align="center">
  <img src="https://github.com/user-attachments/assets/000473aa-7869-41c8-9352-e8481ba922fa" alt="DROMA Logo" width="400"/>
</div>

## 🌐 官方网站
**访问DROMA官方网站：[https://droma01.github.io/DROMA/](https://droma01.github.io/DROMA/)**

探索交互式网页界面，包含完整文档、组件详情和实时示例。

## 🌟 项目概述

**DROMA** 是一个综合性精准肿瘤学平台，整合了世界上最大的药物反应和多组学数据集合。通过先进的分析方法、AI驱动的工具和用户友好的界面，它架起了癌症药物基因组学数据与可操作见解之间的桥梁。

### 🚀 核心亮点

- **🗄️ 海量数据集**: **20个项目**包含**2,600+样本**和**56,000+药物** - 世界最大开源整合药敏数据集
- **🧬 多组学支持**: mRNA、CNV、突变、甲基化、蛋白质组学等
- **🏥 多样模型系统**: 细胞系、PDO（患者来源类器官）、PDX（患者来源异种移植）、PDC（患者来源细胞）
- **🤖 AI驱动**: 通过MCP（模型上下文协议）服务器支持自然语言交互
- **📊 高级分析**: 元分析、生物标志物发现和统计建模
- **🌐 网页界面**: 直观分析的交互式Shiny应用程序

## 🏗️ DROMA生态系统

DROMA平台由相互连接的组件组成，共同提供完整的药物反应分析解决方案：

<div align="center">
  <img src="https://raw.githubusercontent.com/mugpeng/mugpeng-my-gallery-02/main/img20250619145856.png" alt="DROMA架构" width="600"/>
</div>

### 📊 数据基础设施

#### **[DROMA_DB](https://github.com/mugpeng/DROMA_DB)** - 数据库基础
- **用途**: SQLite数据库创建和管理
- **特性**: 面向项目的结构、高效查询、优化索引
- **内容**: 20个项目的综合组学和药物反应数据
- **集成**: 所有其他DROMA组件的基础

#### **[DROMA_Set](https://github.com/mugpeng/DROMA_Set)** - 数据管理
- **用途**: 多项目数据管理和分析的R包
- **特性**: S4类（DromaSet、MultiDromaSet）、跨项目比较、样本重叠检测
- **核心类**:
  - `DromaSet`: 单项目分析
  - `MultiDromaSet`: 跨项目比较
- **功能**: 灵活的数据加载、元数据管理、数据库连接

### 🔬 分析引擎

#### **[DROMA_R](https://github.com/mugpeng/DROMA_R)** - 高级分析
- **用途**: 药物-组学关联的统计分析和可视化
- **特性**: 元分析、批处理、全面可视化
- **方法**: Spearman相关性、Wilcoxon检验、Cliff's Delta效应量
- **输出**: 森林图、火山图、比较可视化
- **性能**: Z-score标准化、并行处理支持

### 🌐 用户界面

#### **[DROMA_Web](https://github.com/mugpeng/DROMA_web)** - 网页应用
- **用途**: 交互式Shiny网页界面
- **特性**: 实时分析、动态可视化、用户友好界面
- **模块**: 药物特征分析、批量分析、药物-组学配对
- **访问**: 基于浏览器，无需安装

#### **[DROMA_MCP](https://github.com/mugpeng/DROMA_MCP)** - AI界面
- **用途**: 自然语言交互的模型上下文协议服务器
- **特性**: AI助手集成、自然语言查询、自动化分析
- **功能**: 数据集管理、数据加载、数据库探索
- **集成**: 与ChatGPT、Claude和其他AI助手配合使用

### 🐍 Python接口

#### **[DROMA_Py](https://github.com/mugpeng/DROMA_Py)** - Python访问层
- **用途**: 数据库操作和数据访问的Python包
- **特性**: 完整DROMA生态系统集成、Python化API、无缝R-Python桥接
- **功能**: 数据库查询、数据协调、批处理、跨平台兼容性
- **安装**: PyPI可用 (`pip install droma-py`)
- **目标用户**: Python数据科学家、生物信息学家、计算生物学家

### 🚀 未来组件

- **DROMA_AI**: 自动化分析和假设生成的多智能体系统
- **DROMA_Augur**: 药物反应预测的机器学习模型

## 📈 数据库统计

我们的综合数据库包含：

| **指标** | **数量** | **描述** |
|----------|----------|----------|
| **项目** | 18 | 独立研究数据集 |
| **样本** | 2,600+ | 独特生物样本 |
| **药物** | 56,000+ | 独特化学化合物 |
| **模型系统** | 4类型 | 细胞系、PDO、PDX、PDC |

### 📊 项目分布

<div align="center">
  <img src="https://raw.githubusercontent.com/mugpeng/mugpeng-my-gallery-02/main/img20250513115037.png" alt="项目分布" width="500"/>
</div>

<div align="center">
  <img src="https://raw.githubusercontent.com/mugpeng/mugpeng-my-gallery-02/main/img20250513114926.png" alt="数据类型" width="500"/>
</div>

### 🏥 模型系统覆盖

- **细胞系** (11个项目): CCLE、GDSC1、GDSC2、CTRP1、CTRP2、gCSI、NCI60、FIMM、GRAY、Prism、UHNBreast
- **PDO** (3个项目): UMPDO1、UMPDO2、UMPDO3
- **PDC** (2个项目): PDTXBreast、Tavor  
- **PDX** (1个项目): Xeva
- **临床** (1个项目): CTR-DB（开发中）

## 🚀 快速开始

### 1. **数据库设置**
```r
# 安装DROMA.Set
devtools::install_github("mugpeng/DROMA_Set")

# 从Zenodo下载数据
# https://zenodo.org/records/15742800

# 创建数据库
library(DROMA.Set)
createDROMADatabase("droma.sqlite", "data/")
```

### 2. **基本分析**
```r
# 加载数据集
gCSI <- createDromaSetFromDatabase("gCSI", "droma.sqlite")

# 加载带标准化的分子谱
gCSI <- loadMolecularProfilesNormalized(gCSI, 
                                       molecular_type = "mRNA", 
                                       features = "ABCB1")

# 加载药物反应
gCSI <- loadTreatmentResponseNormalized(gCSI, drugs = "Paclitaxel")

# 分析药物-基因关联
library(DROMA.R)
result <- analyzeDrugOmicPair(gCSI, "mRNA", "ABCB1", "Paclitaxel")
```

### 3. **AI驱动分析**
```bash
# 安装DROMA MCP
pip install droma-mcp

# 启动AI服务器
droma-mcp run --db-path droma.sqlite

# 与AI助手使用
"加载CCLE数据集并分析BRCA1表达与他莫昔芬反应的关系"
```

### 4. **Python接口**
```python
# 安装并使用DROMA_Py
import droma_py as dp

# 连接数据库
db = dp.DROMADatabase("droma.sqlite")

# 加载和协调数据
data = db.load_molecular_profiles("CCLE", "mRNA", features=["BRCA1", "TP53"])
harmonized = dp.harmonize_gene_names(data)

# 查询药物反应
drug_data = db.load_treatment_response("CCLE", drugs=["Tamoxifen"])
```

### 5. **网页界面**
访问我们的交互式网页应用程序进行基于浏览器的分析（请联系获取访问权限）。

## 🛠️ 安装

### 前提条件
- **R** ≥ 4.0.0
- **Python** ≥ 3.10 (用于DROMA_MCP)
- **SQLite** 数据库

### 核心组件
```r
# 安装DROMA包
devtools::install_github("mugpeng/DROMA_Set")
devtools::install_github("mugpeng/DROMA_R")
```

```bash
# 安装Python组件
pip install droma-py      # Python访问层
pip install droma-mcp     # AI界面
```

### 数据下载
```bash
# 从Zenodo下载 (15.5 GB)
wget https://zenodo.org/records/15742800/files/droma-data.zip
unzip droma-data.zip
```

## 📚 文档

每个组件都有全面的文档：

- **[DROMA_DB文档](https://github.com/mugpeng/DROMA_DB#readme)**: 数据库创建和管理
- **[DROMA_Set文档](https://github.com/mugpeng/DROMA_Set#readme)**: 数据管理和S4类
- **[DROMA_R文档](https://github.com/mugpeng/DROMA_R#readme)**: 统计分析和可视化
- **[DROMA_MCP文档](https://github.com/mugpeng/DROMA_MCP#readme)**: AI界面和自然语言查询

## 🎯 应用场景

### 🔬 生物标志物发现
- 识别与多个数据集中药物敏感性相关的基因
- 执行元分析以增强统计能力
- 在不同模型系统中验证发现

### 💊 药物重定位
- 探索跨癌症类型的药物反应模式
- 识别具有相似反应谱的化合物
- 在新环境中预测药物疗效

### 🏥 精准医学
- 分析患者来源模型（PDO、PDX）
- 将分子谱与治疗结果相关联
- 开发个性化治疗策略

### 📊 比较分析
- 比较细胞系与患者模型的药物反应
- 评估生物标志物在研究间的一致性
- 整合多组学数据获得全面见解

## 🌟 核心特性

### 🔄 **无缝集成**
所有组件通过标准化接口和数据格式协同工作。

### ⚡ **高性能**
- 优化的SQLite数据库与索引
- 大规模分析的并行处理
- 内存高效的数据处理

### 🎨 **丰富可视化**
- 交互式图表和仪表板
- 出版就绪的图形
- 可定制的主题和布局

### 🔍 **灵活查询**
- 按肿瘤类型、数据类型或特定特征过滤
- 跨项目样本匹配
- 高级统计过滤

### 🤖 **AI增强**
- 自然语言查询
- 自动化分析工作流
- 智能数据探索

## 🏆 影响与应用

DROMA已被用于：
- **学术研究**: 在高影响因子期刊发表
- **药物发现**: 产业合作
- **临床转化**: 生物标志物验证研究
- **教育**: 计算药物基因组学培训

## 📈 版本历史

### **v0.4 (当前版本)** - "陆地"
- **新增**: DROMA_MCP AI界面
- **增强**: 多项目分析能力
- **添加**: 默认Z-score标准化
- **改进**: 性能优化

### **v0.3** - 数据扩展
- **新增**: 体内数据（Xeva PDX数据集）
- **总计**: 18个数据集（11个细胞系、2个PDC、3个PDO、1个PDX、1个临床）
- **增强**: 药物特征分析模块
- **改进**: 可视化和用户体验

### **v0.2** - 网页界面
- **推出**: 交互式Shiny网页应用
- **新增**: PDO数据集（乳腺、结肠、鼻咽）
- **增强**: 数据协调和注释
- **特性**: 肿瘤类型和数据类型过滤

## 📄 引用

如果您在研究中使用DROMA，请引用：

```bibtex
@article{li2024facilitating,
  title={Facilitating integrative and personalized oncology omics analysis with UCSCXenaShiny},
  author={Li, Shixiang and Peng, Yu and Chen, Miaozun and others},
  journal={Communications Biology},
  volume={7},
  number={1},
  pages={1200},
  year={2024},
  publisher={Nature Publishing Group},
  doi={10.1038/s42003-024-06891-2}
}
```

## 🤝 贡献

我们欢迎对DROMA生态系统的贡献！

### 如何贡献
1. **Fork** 相关仓库
2. **创建** 功能分支
3. **进行** 更改并添加测试
4. **提交** 拉取请求

### 贡献领域
- **新数据集**: 额外的癌症药物基因组学研究
- **分析方法**: 新的统计方法
- **可视化**: 增强的绘图功能
- **文档**: 教程和示例
- **错误报告**: 问题和功能请求

## 🔗 链接与资源

### **官方仓库**
- **主项目**: [github.com/mugpeng/DROMA](https://github.com/mugpeng/DROMA)
- **数据库**: [github.com/mugpeng/DROMA_DB](https://github.com/mugpeng/DROMA_DB)
- **数据管理**: [github.com/mugpeng/DROMA_Set](https://github.com/mugpeng/DROMA_Set)
- **分析**: [github.com/mugpeng/DROMA_R](https://github.com/mugpeng/DROMA_R)
- **Python接口**: [github.com/mugpeng/DROMA_Py](https://github.com/mugpeng/DROMA_Py)
- **AI界面**: [github.com/mugpeng/DROMA_MCP](https://github.com/mugpeng/DROMA_MCP)

### **数据与资源**
- **数据仓库**: [Zenodo记录](https://zenodo.org/records/15742800)
- **文档**: 组件特定的README文件
- **示例**: 每个仓库中的全面使用示例

### **支持与社区**
- **问题**: 仓库特定的GitHub Issues
- **讨论**: GitHub Discussions
- **联系**: yc47680@um.edu.mo

## 📜 许可证

DROMA在**Mozilla Public License 2.0** (MPL-2.0)下许可。详情请参见[LICENSE](LICENSE)。

## 🙏 致谢

DROMA由澳门大学精准肿瘤学研究团队开发。我们感谢所有贡献者、合作者以及更广泛的癌症研究社区的支持和反馈。

---

<div align="center">

**🧬 DROMA - 连接癌症药物基因组学与AI 💊**

*通过全面数据集成和智能分析赋能精准医学*

</div> 