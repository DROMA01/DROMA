# DROMA
**Drug Response Omics association MAp** (DROMA, 卓玛)  

[![Website](https://img.shields.io/website?url=https%3A//droma01.github.io/)](https://droma01.github.io/)
[![GitHub Stars](https://img.shields.io/github/stars/mugpeng/DROMA?style=social)](https://github.com/mugpeng/DROMA)
[![License: MPL-2.0](https://img.shields.io/badge/License-MPL--2.0-yellow.svg)](https://opensource.org/licenses/MPL-2.0)
[![R](https://img.shields.io/badge/R-%3E%3D4.0.0-blue.svg)](https://www.r-project.org/)
[![Python](https://img.shields.io/badge/Python-3.10+-green.svg)](https://www.python.org/)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.15742800.svg)](https://doi.org/10.5281/zenodo.15742800)

<div align="center">
  <img src="https://github.com/user-attachments/assets/000473aa-7869-41c8-9352-e8481ba922fa" alt="DROMA Logo" width="400"/>
</div>

## 🌐 Official Website
**Visit the DROMA website at: [https://droma01.github.io/](https://droma01.github.io/)**

Explore the interactive web interface with comprehensive documentation, component details, and live examples.

## 📋 Table of Contents
- [🌟 Overview](#-overview)
- [🎯 Key Features](#-key-features)
- [🏗️ DROMA Ecosystem](#️-droma-ecosystem)
- [📊 Dataset Overview](#-dataset-overview)
- [🚀 Quick Start](#-quick-start)
- [🔧 Installation](#-installation)
- [💻 Usage Examples](#-usage-examples)
- [🌐 Web Interface](#-web-interface)
- [🤖 AI Integration](#-ai-integration)
- [🖥️ Official Website](#️-official-website)
- [📖 Documentation](#-documentation)
- [🤝 Contributing](#-contributing)
- [📄 Citation](#-citation)
- [📧 Contact](#-contact)
- [📝 License](#-license)

## 🌟 Overview

**DROMA** is a comprehensive precision oncology platform that integrates the world's largest collection of drug response and multi-omics datasets. It bridges the gap between cancer pharmacogenomics data and actionable insights through advanced analytics, AI-powered tools, and user-friendly interfaces.

### 🚀 Key Highlights

- **🗄️ Massive Dataset**: **18 projects** with **2,600+ samples** and **56,000+ drugs** - the world's largest open-source integrated drug sensitivity dataset
- **🧬 Multi-Omics Support**: mRNA, CNV, mutations, methylation, proteomics, and more
- **🏥 Diverse Model Systems**: Cell lines, PDOs (Patient-Derived Organoids), PDXs (Patient-Derived Xenografts), and PDCs (Patient-Derived Cells)
- **🤖 AI-Powered**: Natural language interactions via MCP (Model Context Protocol) server
- **📊 Advanced Analytics**: Meta-analysis, biomarker discovery, and statistical modeling
- **🌐 Web Interface**: Interactive Shiny application for intuitive analysis

## 🏗️ DROMA Ecosystem

The DROMA platform consists of interconnected components that work together to provide a complete drug response analysis solution:

<div align="center">
  <img src="https://raw.githubusercontent.com/mugpeng/mugpeng-my-gallery-02/main/img20250619145856.png" alt="DROMA Architecture" width="600"/>
</div>

### 📊 Data Infrastructure

#### **[DROMA_DB](https://github.com/mugpeng/DROMA_DB)** - Database Foundation
- **Purpose**: SQLite database creation and management
- **Features**: Project-oriented structure, efficient querying, optimized indexing
- **Content**: 20 projects with comprehensive omics and drug response data
- **Integration**: Foundation for all other DROMA components

#### **[DROMA_Set](https://github.com/mugpeng/DROMA_Set)** - Data Management
- **Purpose**: R package for multi-project data management and analysis
- **Features**: S4 classes (DromaSet, MultiDromaSet), cross-project comparisons, sample overlap detection
- **Key Classes**:
  - `DromaSet`: Single-project analysis
  - `MultiDromaSet`: Cross-project comparisons
- **Capabilities**: Flexible data loading, metadata management, database connectivity

### 🔬 Analysis Engine

#### **[DROMA_R](https://github.com/mugpeng/DROMA_R)** - Advanced Analytics
- **Purpose**: Statistical analysis and visualization for drug-omics associations
- **Features**: Meta-analysis, batch processing, comprehensive visualization
- **Methods**: Spearman correlation, Wilcoxon tests, Cliff's Delta effect sizes
- **Outputs**: Forest plots, volcano plots, comparison visualizations
- **Performance**: Z-score normalization, parallel processing support

### 🌐 User Interfaces

#### **[DROMA_Web](https://github.com/mugpeng/DROMA_web)** - Web Application
- **Purpose**: Interactive Shiny web interface
- **Features**: Real-time analysis, dynamic visualization, user-friendly interface
- **Modules**: Drug feature analysis, batch analysis, drug-omics pairing
- **Access**: Browser-based, no installation required

#### **[DROMA_MCP](https://github.com/mugpeng/DROMA_MCP)** - AI Interface
- **Purpose**: Model Context Protocol server for natural language interactions
- **Features**: AI assistant integration, natural language queries, automated analysis
- **Capabilities**: Dataset management, data loading, database exploration
- **Integration**: Works with ChatGPT, Claude, and other AI assistants

### 🚀 Future Components

- **DROMA_AI**: Multi-agent systems for automated analysis and hypothesis generation
- **DROMA_Augur**: Machine learning models for drug response prediction
- **DROMA_py**: Python implementation for broader accessibility

## 📈 Database Statistics

Our comprehensive database includes:

| **Metric** | **Count** | **Description** |
|------------|-----------|-----------------|
| **Projects** | 20 | Independent research datasets |
| **Samples** | 2,600+ | Unique biological samples |
| **Drugs** | 56,000+ | Unique chemical compounds |
| **Model Systems** | 4 types | Cell lines, PDOs, PDXs, Clinical |

### 📊 Project Distribution

<div align="center">
  <img src="https://raw.githubusercontent.com/mugpeng/mugpeng-my-gallery-02/main/img20250513115037.png" alt="Project Distribution" width="500"/>
</div>

<div align="center">
  <img src="https://raw.githubusercontent.com/mugpeng/mugpeng-my-gallery-02/main/img20250513114926.png" alt="Data Types" width="500"/>
</div>

### 🏥 Model System Coverage

- **Cell Lines** (11 projects): CCLE, GDSC1, GDSC2, CTRP1, CTRP2, gCSI, NCI60, FIMM, GRAY, Prism, UHNBreast
- **PDOs** (5 projects): UMPDO1, UMPDO2, UMPDO3, HKPDO, LICOB
- **PDCs** (2 projects): PDTXBreast, Tavor  
- **PDXs** (1 project): Xeva
- **Clinical** (1 project): CTR-DB (under development)

## 🚀 Quick Start

### 1. **Database Setup**
```r
# Install DROMA.Set
devtools::install_github("mugpeng/DROMA_Set")

# Download data from Zenodo
# https://zenodo.org/records/15742800

# Connect database
library(DROMA.Set)
# Connect to your DROMA database
connectDROMADatabase("path/to/your/droma.sqlite")

# List available projects
projects <- listDROMAProjects()
print(projects)
```

### 2. **Basic Analysis**
```r
# Load dataset
gCSI <- createDromaSetFromDatabase("gCSI", "droma.sqlite")

# Load molecular profiles with normalization
gCSI <- loadMolecularProfilesNormalized(gCSI, 
                                       molecular_type = "mRNA", 
                                       features = "ABCB1")

# Load drug response
gCSI <- loadTreatmentResponseNormalized(gCSI, drugs = "Paclitaxel")

# Analyze drug-gene association
library(DROMA.R)
result <- analyzeDrugOmicPair(gCSI, "mRNA", "ABCB1", "Paclitaxel")
```

### 3. **AI-Powered Analysis**
```bash
# Install DROMA MCP
pip install droma-mcp

# Start AI server
droma-mcp run --db-path droma.sqlite

# Use with AI assistants
"Load CCLE dataset and analyze BRCA1 expression vs Tamoxifen response"
```

### 4. **Web Interface**
Visit our interactive web application for browser-based analysis (contact for access).

## 🛠️ Installation

### Prerequisites
- **R** ≥ 4.0.0
- **Python** ≥ 3.10 (for DROMA_MCP)
- **SQLite** database

### Core Components
```r
# Install DROMA packages
devtools::install_github("mugpeng/DROMA_Set")
devtools::install_github("mugpeng/DROMA_R")
```

```bash
# Install AI interface
pip install droma-mcp
```

### Data Download
```bash
# Download from Zenodo (15.5 GB)
wget https://zenodo.org/records/15742800/files/droma.sqlite
unzip droma-data.zip
```

## 📚 Documentation

Each component has comprehensive documentation:

- **[DROMA_DB Documentation](https://github.com/mugpeng/DROMA_DB#readme)**: Database creation and management
- **[DROMA_Set Documentation](https://github.com/mugpeng/DROMA_Set#readme)**: Data management and S4 classes
- **[DROMA_R Documentation](https://github.com/mugpeng/DROMA_R#readme)**: Statistical analysis and visualization
- **[DROMA_MCP Documentation](https://github.com/mugpeng/DROMA_MCP#readme)**: AI interface and natural language queries

## 🖥️ Official Website

**Visit [https://droma01.github.io/](https://droma01.github.io/)** for the complete DROMA experience:

### 🌟 Website Features
- **Interactive Homepage**: Animated DNA visualizations and ecosystem overview
- **Component Documentation**: Detailed information about each DROMA module  
- **Live Code Examples**: Copy-to-clipboard functionality for quick setup
- **Responsive Design**: Optimized for desktop, tablet, and mobile devices
- **Professional Theme**: Scientific color palette with modern animations

### 📱 User Experience
- **No Installation Required**: Access DROMA information instantly in your browser
- **Quick Navigation**: Jump between components, documentation, and examples
- **Mobile-Friendly**: Full functionality on all device sizes
- **Fast Loading**: Optimized performance with modern web technologies

### 🔗 Direct Links
- **Component Details**: Deep-dive into DROMA_DB, DROMA_Set, DROMA_R, DROMA_Web, and DROMA_MCP
- **Installation Guides**: Step-by-step setup instructions for each component
- **GitHub Integration**: Direct links to all source repositories
- **Data Access**: Links to Zenodo datasets and documentation

## 🎯 Use Cases

### 🔬 Biomarker Discovery
- Identify genes associated with drug sensitivity across multiple datasets
- Perform meta-analysis to strengthen statistical power
- Validate findings across different model systems

### 💊 Drug Repurposing
- Explore drug response patterns across cancer types
- Identify compounds with similar response profiles
- Predict drug efficacy in new contexts

### 🏥 Precision Medicine
- Analyze patient-derived models (PDOs, PDXs)
- Correlate molecular profiles with treatment outcomes
- Develop personalized treatment strategies

### 📊 Comparative Analysis
- Compare drug responses across cell lines vs patient models
- Evaluate consistency of biomarkers across studies
- Integrate multi-omics data for comprehensive insights

## 🌟 Key Features

### 🔄 **Seamless Integration**
All components work together through standardized interfaces and data formats.

### ⚡ **High Performance**
- Optimized SQLite database with indexing
- Parallel processing for large-scale analysis
- Memory-efficient data handling

### 🎨 **Rich Visualization**
- Interactive plots and dashboards
- Publication-ready figures
- Customizable themes and layouts

### 🔍 **Flexible Querying**
- Filter by tumor type, data type, or specific features
- Cross-project sample matching
- Advanced statistical filtering

### 🤖 **AI-Enhanced**
- Natural language queries
- Automated analysis workflows
- Intelligent data exploration

## 🏆 Impact & Applications

DROMA has been used for:
- **Academic Research**: Published in high-impact journals
- **Drug Discovery**: Industrial collaborations
- **Clinical Translation**: Biomarker validation studies
- **Educational**: Training in computational pharmacogenomics

## 📈 Version History

### **v0.4** - "Andata"
- **New**: DROMA_MCP AI interface
- **Enhanced**: Multi-project analysis capabilities
- **Added**: Z-score normalization by default
- **Improved**: Performance optimizations

<div align="center">
  <img src="https://raw.githubusercontent.com/mugpeng/mugpeng-my-gallery-02/main/imgoutdoor2.png" alt="DROMA Logo" width="400"/>
</div>



250620, I attended [11th Macau Symposium on Biomedical Sciences 2025 - 11th Macau Symposium on Biomedical Sciences 2025](https://msbs2025.fhs.um.edu.mo/):

<div align="center">
  <img src="https://raw.githubusercontent.com/mugpeng/mugpeng-my-gallery-02/main/img20250626174000.png" alt="DROMA Logo" width="400"/>
</div>

### **v0.3** - Data Expansion

- **Added**: In vivo data (Xeva PDX dataset)
- **Total**: 20 datasets (11 cell line, 2 PDC, 5 PDO, 1 PDX, 1 clinical)
- **Enhanced**: Drug feature analysis modules
- **Improved**: Visualization and user experience

250319 UM PhD seminar:

<div align="center">
  <img src="https://github.com/user-attachments/assets/72adc553-f807-48f8-afa8-bb4009eef963" alt="DROMA Logo" width="400"/>
</div>



### **v0.2** - Web Interface
- **Launch**: Interactive Shiny web application
- **Added**: PDO datasets (breast, colon, nasopharyngeal)
- **Enhanced**: Data harmonization and annotation
- **Features**: Tumor type and data type filtering

<div align="center">
  <img src="https://github.com/user-attachments/assets/89b385e0-f5e4-4d8e-a33b-5f30bed039b2" alt="DROMA Logo" width="400"/>
</div>



## 📄 Citation

If you use DROMA in your research, please cite:

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

## 🤝 Contributing

We welcome contributions to the DROMA ecosystem! 

### How to Contribute
1. **Fork** the relevant repository
2. **Create** a feature branch
3. **Make** your changes with tests
4. **Submit** a pull request

### Areas for Contribution
- **New datasets**: Additional cancer pharmacogenomics studies
- **Analysis methods**: Novel statistical approaches
- **Visualization**: Enhanced plotting functions
- **Documentation**: Tutorials and examples
- **Bug reports**: Issues and feature requests

## 🔗 Links & Resources

### **Official Repositories**
- **Main Project**: [github.com/mugpeng/DROMA](https://github.com/mugpeng/DROMA)
- **Database**: [github.com/mugpeng/DROMA_DB](https://github.com/mugpeng/DROMA_DB)
- **Data Management**: [github.com/mugpeng/DROMA_Set](https://github.com/mugpeng/DROMA_Set)
- **Analytics**: [github.com/mugpeng/DROMA_R](https://github.com/mugpeng/DROMA_R)
- **AI Interface**: [github.com/mugpeng/DROMA_MCP](https://github.com/mugpeng/DROMA_MCP)

### **Data & Resources**
- **Data Repository**: [Zenodo Record](https://zenodo.org/records/15742800)
- **Documentation**: Component-specific README files
- **Examples**: Comprehensive usage examples in each repository

### **Support & Community**
- **Issues**: Repository-specific GitHub Issues
- **Discussions**: GitHub Discussions
- **Contact**: yc47680@um.edu.mo

## 📜 License

DROMA is licensed under the **Mozilla Public License 2.0** (MPL-2.0). See [LICENSE](LICENSE) for details.

## 🙏 Acknowledgments

DROMA is developed by the precision oncology research team at the University of Macau. We thank all contributors, collaborators, and the broader cancer research community for their support and feedback.

---

<div align="center">
**🧬 DROMA - Bridging Cancer Pharmacogenomics and AI 💊**

*Empowering precision medicine through comprehensive data integration and intelligent analysis*

</div>

