# ALPS Projects
This repository contains analysis and file-organisation codes for the 2025 ALPS-related neuroimaging project.  
The project is focused on MRI-derived ALPS-related indices and conductivity-related imaging measures, including workflows for organising high-frequency conductivity and compartment-specific conductivity files, preparing image-derived variables, and supporting downstream analysis for dementia-related neuroimaging research.

# Project overview
The repository includes code used for organising and preparing neuroimaging-derived files for ALPS-related analysis.  
The main workflow includes:  
- extraction of compressed imaging-related files
- organisation of conductivity-derived files
- separation of imaging outputs into predefined folders
- preparation of high-frequency conductivity, extracellular conductivity, and intracellular conductivity data
- support for downstream ALPS-related ratio index analysis
- preparation of files for statistical and manuscript-related analysis
  
The repository currently includes code-only materials.

## Associated publication
This repository contains code and file-organisation workflows related to the following published article:

**Ahn J, Kim S-Y, Lee MB, Kwon O-I, Rhee HY, Jung YJ, Kim Y, Park S, Ryu C-W, Lee J, and Jahng G-H.**
**Evaluation of conductivity tensor image along the perivascular space in the brains of patients with cognitive impairments.**
*Frontiers in Aging Neuroscience*. 2026;18:1794175.
DOI: [10.3389/fnagi.2026.1794175](https://doi.org/10.3389/fnagi.2026.1794175)

This repository provides code used to organise and prepare MRI-derived files for the conductivity tensor imaging along the perivascular space (CTI-ALPS) analysis reported in the article.  
The associated study introduced the CTI-ALPS index and evaluated CTI-ALPS and DTI-ALPS in cognitively normal older adults, patients with amnestic mild cognitive impairment, and patients with Alzheimer’s disease.  
Please cite the associated article if you use or refer to this repository.

# Repository structure
```text
2025-ALPS/
│
├── Generate_Plottings.ipynb
│   └── Jupyter notebook for organising imaging-derived files and preparing project-level outputs
│
├── .gitignore
└── README.md
```

The current repository structure may be expanded as additional notebooks or scripts are added.

# Main analysis components
1. File extraction  
The notebook includes workflows for identifying compressed files and extracting them into the working directory. This is used to prepare imaging-derived files before folder-level organisation.

2. Conductivity file organisation  
The workflow organises conductivity-related files according to their filename prefixes.  
The main target groups include:  
- wConduct files for high-frequency conductivity-related outputs
- wsigma_e files for extracellular conductivity-related outputs
- wsigma_i files for intracellular conductivity-related outputs
  
These files are organised into corresponding project folders such as:  
- HFC
- EC
- IC
  
3. Subject-level folder handling  
The workflow includes procedures for identifying and handling subject-level folders, including NODDI-related folders used in the image-processing pipeline.

4. Downstream ALPS-related analysis support  
The repository is intended to support downstream analysis of ALPS-related indices and conductivity-based ratio indices. These codes are part of a broader neuroimaging workflow for dementia-related imaging research.

# Data availability
Raw and processed imaging data are not included in this repository.  
The following files and directories were excluded from version control:
- raw MRI data
- DICOM files
- NIfTI files
- compressed imaging archives
- subject-level image derivatives
- conductivity maps
- ALPS index maps
- generated figures
- statistical result files
- local path configuration files
- private data directories
  
This is to prevent accidental sharing of sensitive imaging data and unnecessary large files.

# Environment
The workflow was mainly developed using Python and Jupyter Notebook. Typical Python libraries used in the current workflow include:  
- os
- gzip
- shutil
- tarfile
- pathlib
- tqdm
  
Additional packages may be required for downstream statistical analysis, visualisation, or neuroimaging-specific processing depending on future notebooks.

# Notes
This repository is primarily for internal research code management and ALPS-related neuroimaging workflow organisation.  
The codes are not intended to provide a fully reproducible public analysis package because the original imaging datasets and generated derivatives are not included.

# Author
J. Ahn  
Ph.D. Candidate in AI for Healthcare and Medicine, Radiological Technologist  
AI-WM Lab, Department of Biomedical Engineering, Kyung Hee University
