# 🧬 Automated Molecular Docking Pipeline using Python

An end-to-end **automated molecular docking pipeline** built in **Python**, designed to simplify and accelerate the traditionally manual process of molecular docking — a crucial step in modern **drug discovery**.  
This project automates the preparation, execution, and analysis of receptor–ligand docking using open-source tools such as **AutoDock Vina**, **Open Babel**, and **PyMOL**, and provides an intuitive **Streamlit-based user interface** for both experts and non-experts.

---

## 📘 Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Tools & Technologies](#tools--technologies)
- [Pipeline Overview](#pipeline-overview)
- [Installation](#installation)
- [Usage](#usage)
- [Folder Structure](#folder-structure)
- [Results & Evaluation](#results--evaluation)
- [Future Enhancements](#future-enhancements)
- [Acknowledgements](#acknowledgements)
- [License](#license)

---

## 🔍 Introduction

**Molecular docking** is a computational method used to predict how small molecules (ligands) interact with receptor proteins to form stable complexes.  
However, manual docking is **time-consuming, error-prone**, and **difficult to scale** when dealing with large datasets.

This project automates the **entire molecular docking workflow**, including:
- Receptor and ligand retrieval from public databases.
- Structure preparation and validation.
- Configuration file generation.
- Docking execution.
- Result visualization and report generation.

> 🚀 Manual docking typically takes **40–50 minutes**, while this pipeline reduces the time to **4–5 minutes** — a **90% improvement**.

---

## ✨ Features

- 🔹 **Automatic Receptor & Ligand Download**  
  Fetches data from **NCBI**, **PubChem**, and **SWISS-MODEL** using Biopython and Selenium.

- 🔹 **Model Validation**  
  Generates and analyzes **Ramachandran plots** to ensure receptor reliability.

- 🔹 **Automated Docking Execution**  
  Performs docking using **AutoDock Vina** with dynamic configuration files.

- 🔹 **Batch Processing**  
  Supports **multiple ligands** in one run with automated folder management and logs.

- 🔹 **User-Friendly Web UI**  
  Built using **Streamlit** for simple input, configuration, and visualization.

- 🔹 **Result Visualization**  
  Integrated **PyMOL** interface for 3D visualization of docking poses.

- 🔹 **Comprehensive Outputs**  
  Exports results as **CSV** files and visual summaries with binding affinities and energy plots.

---

## 🧰 Tools & Technologies

| Category | Tools / Libraries |
|-----------|------------------|
| **Programming Language** | Python |
| **Docking Engine** | AutoDock Vina |
| **Structure Conversion** | Open Babel |
| **Visualization** | PyMOL |
| **UI Framework** | Streamlit |
| **Automation** | Selenium, BeautifulSoup |
| **Bioinformatics** | Biopython (Entrez), RDKit |
| **Data Handling** | Pandas, NumPy |
| **System Utilities** | os, subprocess, shutil, threading |

---

## ⚙️ Pipeline Overview

The complete automated docking pipeline includes:

1. **Input Collection** – User enters receptor and ligand names via UI.  
2. **Structure Generation** – Fetches receptor FASTA sequence (NCBI), models it via SWISS-MODEL, and downloads ligand structures from PubChem.  
3. **Validation** – Checks model quality via **Ramachandran plots** and stereochemistry analysis.  
4. **Preparation** – Cleans and converts receptor and ligand to **PDBQT** format using Open Babel.  
5. **Configuration Generation** – Creates config files based on docking parameters (exhaustiveness, seed, energy range).  
6. **Docking Execution** – Runs AutoDock Vina automatically and logs results.  
7. **Result Display** – Presents best binding poses, average energies, and provides CSV download and PyMOL visualization.

> **Flowchart of the Pipeline**
> ```
> User Input → Structure Generation → Validation → Preparation → Config Generation → Docking → Visualization & Report
> ```

---

## 🧩 Installation

### Prerequisites
Install the following software and ensure their paths are configured in `config.py`:
- [AutoDock Vina](https://vina.scripps.edu/)
- [Open Babel](https://openbabel.org/)
- [PyMOL](https://pymol.org/)
- [Google Chrome + ChromeDriver](https://chromedriver.chromium.org/)

### Python Dependencies
```bash
pip install biopython pandas numpy streamlit selenium beautifulsoup4 requests
```

---

## 🚀 Usage

1. **Run the Streamlit App**
   ```bash
   streamlit run app.py
   ```

2. **Input Details**
   - Enter receptor name (e.g., `OR1A1`)
   - Enter one or more ligands (comma-separated)

3. **Validate Model**
   - The system automatically validates the receptor using SWISS-MODEL.

4. **Set Docking Parameters**
   - Exhaustiveness (1–32)
   - Energy Range (1–10)
   - Number of Poses (1–20)
   - Choose **User-Defined Seed** or **Random Seed Docking**

5. **Run Docking**
   - Click **Start Docking** and wait for results.

6. **Visualize & Download**
   - View 3D docking poses via **PyMOL**.
   - Download results as `.csv`.

---

## 📁 Folder Structure

```
Automated_Molecular_Docking/
│
├── automation_code/
│   ├── step1_download.py
│   ├── step2_validate.py
│   ├── step3_prepare.py
│   ├── step4_config.py
│   ├── step5_dock.py
│   └── config.py
│
├── pages/
│   ├── About.py
│   └── Help.py
│
├── data/
│   ├── receptors/
│   ├── ligands/
│   ├── results/
│   └── logs/
│
├── app.py
└── README.md
```

---

## 📊 Results & Evaluation

- ⏱ **Time Efficiency:** Reduced docking time by ~90%.  
- ✅ **Accuracy:** Output validated against known ligand–receptor pairs.  
- 👥 **User Study:** 5 users (non-experts) successfully performed docking.  
- ⭐ **Average Rating:** 4.5 / 5 for usability and clarity.  

**Example Output:**
| Receptor | Ligand | Binding Energy (kcal/mol) | Std. Dev. | Remarks |
|-----------|---------|----------------------------|------------|----------|
| OR1A1 | Citral | -6.7 | 0.2 | Stable binding |
| OR6F1 | 4-Decenal | -7.1 | 0.3 | Strong affinity |

---

## 🔮 Future Enhancements

- Integrate **Machine Learning** for pre-screening ligands.  
- Deploy on **Cloud** for high-throughput virtual screening.  
- Support **Multi-Receptor Docking** and **ADMET prediction**.  
- Add **3D drag-and-drop UI** and collaborative features.  
- Integrate **Molecular Dynamics simulation** for pose refinement.

---

## 🙏 Acknowledgements

This project was carried out as part of a **Research Internship at IIT Mandi (CHCi Lab)**  
under the supervision of **Prof. (Dr.) Shubhajit Roy Chowdhury**, Chairperson, CHCi.

**Author:** *Atirath Pal*  
**Institution:** Government College of Engineering & Textile Technology, Serampore  
**Year:** August 2025  
**Supervisor:** Prof. (Dr.) Shubhajit Roy Chowdhury, IIT Mandi  

---

## 📜 License

This project is open-source under the **MIT License**.  
Feel free to use, modify, and build upon it with proper attribution.
