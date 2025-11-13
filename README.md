# 🧬 Automated Molecular Docking Pipeline using Python

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://www.python.org/)
[![Framework](https://img.shields.io/badge/Framework-Streamlit-ff4b4b.svg)](https://streamlit.io/)
[![Docking Engine](https://img.shields.io/badge/Engine-AutoDock_Vina-green.svg)](https://vina.scripps.edu/)
[![Field](https://img.shields.io/badge/Domain-Bioinformatics-lightblue.svg)](#)

> **Automating Molecular Docking for Drug Discovery**  
> A complete end-to-end pipeline that automates receptor and ligand retrieval, validation, docking, and visualization using open-source bioinformatics tools.

---



### 🔬 About the Project

The **Automated Molecular Docking Pipeline** is a research-oriented Python application that integrates **AutoDock Vina**, **Open Babel**, **PyMOL**, and several bioinformatics APIs to automate the molecular docking process.  
Designed during a research internship at **IIT Mandi (CHCi Lab)**, the project aims to make molecular docking **faster, more reliable, and accessible** — reducing manual time by over **90%** while maintaining high reproducibility and interpretability.

> **Tagline:** “From sequence to docking — automated, reproducible, and researcher-friendly.”




## 📘 Abstract / Overview

The **Automated Molecular Docking Pipeline** is a research-driven project focused on simplifying and accelerating one of the most critical computational steps in modern drug discovery — *molecular docking*.  
Molecular docking predicts how small molecules (ligands) interact with receptor proteins to form stable complexes, helping researchers identify potential drug candidates.

Traditionally, this process involves multiple manual stages such as receptor and ligand preprocessing, grid generation, docking execution, and analysis — all of which are labor-intensive, time-consuming, and error-prone.

This project automates the **entire docking workflow** using Python and a collection of open-source bioinformatics tools including **AutoDock Vina**, **Open Babel**, **PyMOL**, and **Biopython**. The system handles receptor and ligand retrieval, structure preparation, validation via Ramachandran plots, docking execution, and result visualization — all through an intuitive **Streamlit web interface**.

The pipeline enables:
- **Batch docking** of multiple ligands with minimal user input.
- **Error-resilient execution** using robust logging and exception handling.
- **Consistent and reproducible results**, eliminating human bias in parameter setup.

By reducing the average docking time from **40–50 minutes to under 5 minutes**, this pipeline demonstrates a 90% efficiency improvement, making molecular docking accessible to **both experts and non-experts** in the field of computational biology.

> ⚡ *Developed as part of a Research Internship at the Centre for Human Computer Interaction (CHCi), Indian Institute of Technology, Mandi — under the guidance of Prof. (Dr.) Shubhajit Roy Chowdhury.*


## ⚙️ Key Features

The automated pipeline integrates multiple bioinformatics tools and scripting modules to deliver a seamless, fully reproducible molecular docking workflow.  
Below are its principal features:

### 1. End-to-End Automation  
Eliminates manual intervention by automating every stage of the docking process — from receptor and ligand acquisition to post-docking analysis.

### 2. Database Integration  
Directly fetches receptor and ligand structures from trusted biological databases such as **NCBI**, **PubChem**, and **SWISS-MODEL**, ensuring data accuracy and scientific validity.

### 3. Model Validation  
Performs automated structure validation using **Ramachandran plots** and stereochemical analysis to assess protein model reliability before docking.

### 4. Modular Design  
Implements a stepwise modular structure, allowing independent execution and testing of each phase — download, validation, preparation, configuration, docking, and visualization.

### 5. Streamlit-Based Interface  
Provides a clean, interactive web interface built using **Streamlit**, enabling users to perform docking experiments without command-line operations.

### 6. Batch Docking Support  
Capable of handling multiple ligands simultaneously against a single receptor, significantly enhancing throughput and reproducibility.

### 7. Visualization and Reporting  
Integrates **PyMOL** for three-dimensional visualization of binding poses and automatically generates structured reports in CSV format containing binding energies and interaction summaries.

### 8. Robust Logging and Error Handling  
Implements intermediate logs and exception-handling routines to maintain transparency, reproducibility, and reliability across runs.

### 9. Performance Efficiency  
Reduces average docking time from **40–50 minutes** (manual workflow) to **4–5 minutes**, achieving over **90% improvement** in time efficiency.

### 10. Accessibility  
Designed to be user-friendly for both researchers and students new to molecular docking, without requiring advanced domain knowledge.



## Screenshots and Demonstration

This section presents selected screenshots that illustrate the design, workflow, and functionality of the **Automated Molecular Docking Pipeline**.

All images are stored in the external `assets/` directory located at the same level as this project folder.

---

### 1. User Input Interface
Interface for receptor and ligand entry, built using **Streamlit**.  
Users can specify receptor names (e.g., OR1A1) and ligands (e.g., Citral), then initiate automated validation and docking.

![User Input Interface](https://github.com/Atirath-Pal/Automated-Molecular-Docking/blob/6c7b229871ed45bdf45398e4c1e4c190f8e8caad/ui_input.jpg)

---

### 2. Workflow Diagram of the Docking Pipeline
Flowchart showing the complete automation pipeline, including data retrieval, validation, docking, and visualization stages.

![Workflow Diagram](https://github.com/Atirath-Pal/Automated-Molecular-Docking/blob/397ca159e6a52fec18d65defd79f3d1d216dfaef/flowchart_pipeline.jpg)

---

### 3. Docking Results Output Interface
Output interface displaying binding energies, standard deviations, and ranking.  
Users can download results in `.csv` format or visualize binding poses interactively.

![Docking Results](https://github.com/Atirath-Pal/Automated-Molecular-Docking/blob/7ad212c99a1face5ec5862c380b18140be485388/output_interface.png)

---

### 4. PyMOL Visualization
Visualization of the docking result in **PyMOL**, showing the receptor–ligand complex after docking.  
Users can view binding interactions by clicking the *See Pose* button.

![PyMOL Visualization](https://github.com/Atirath-Pal/Automated-Molecular-Docking/blob/3fd195e811be2cda1528e24eaf16762887232290/pymol_visualization.png)

---

### 5. Ramachandran Plot for Model Validation
Automated receptor model validation using **SWISS-MODEL**.  
The Ramachandran plot confirms stereochemical quality before proceeding to docking.

![Ramachandran Plot](https://github.com/Atirath-Pal/Automated-Molecular-Docking/blob/534af0b55af7134241c276108938a21acb8df7d2/ramachandran_plot.png)

---

### 6. Docking Configuration: Random Seed Mode
Example of the random seed docking configuration.  
The system generates seed values automatically to enhance reproducibility and avoid bias.

![Random Seed Docking](https://github.com/Atirath-Pal/Automated-Molecular-Docking/blob/9328cf11647e2bc5d2b3c62f9dd7efc3bcee2f9c/random_seed_docking.png)

---

### 7. Docking Configuration: User-Defined Seed Mode
Interface for user-defined seed docking.  
Users can enter custom seed values for advanced control of stochastic docking runs.

![User Seed Docking](https://github.com/Atirath-Pal/Automated-Molecular-Docking/blob/d7dea41314ca7f9bc92cc076382ecf08cbb2e776/user_seed_docking.png)

---

### 8. Validation Results Table
Table summarizing receptor model validation parameters (e.g., QMEAN, GMQE) as retrieved from the SWISS-MODEL server.

![Validation Table](https://github.com/Atirath-Pal/Automated-Molecular-Docking/blob/b14de606190977be22089e2a22247d7305465d9e/validation_table.png)

---

### 9. Code Configuration Snapshot
Snippet of the `config.py` file showing customizable paths and automation parameters.

![Config.py Snapshot](https://github.com/Atirath-Pal/Automated-Molecular-Docking/blob/59af507e6fe0306df9562b9910b868518a922f04/config_snapshot.png)

---

### 10. Project Folder Structure
Overview of the organized folder structure, demonstrating modular design and code separation for maintainability.

![Folder Structure](https://github.com/Atirath-Pal/Automated-Molecular-Docking/blob/b61194545261a343f671a83a621b61d52432d7c9/folder_structure.png)

---

### 11. Demonstration Video
Watch a brief demonstration of the complete docking workflow:  
[▶️ **View Demo video**](https://vimeo.com/1136320708?share=copy&fl=sv&fe=ci)




## Workflow / Architecture

The **Automated Molecular Docking Pipeline** operates through a sequential, modular workflow that ensures automation, reproducibility, and high efficiency.  
Each stage in the process is managed by independent Python modules, allowing for flexibility and scalability.

### Step-by-Step Workflow

1. **User Input**  
   The user specifies the receptor and ligand names through the Streamlit web interface. Multiple ligands can be provided for batch docking.

2. **Data Retrieval**  
   - Receptor data is fetched from the **NCBI** protein database.  
   - Ligand data is downloaded from **PubChem**.  
   - Receptor modeling and validation data are retrieved from **SWISS-MODEL**.

3. **Receptor and Ligand Preparation**  
   Using **Open Babel**, molecular structures are cleaned, protonated, and converted into `.pdbqt` format suitable for AutoDock Vina.

4. **Model Validation**  
   The receptor model is validated using **Ramachandran plots** and stereochemical quality checks to ensure proper conformation and reliability.

5. **Docking Configuration**  
   The system automatically generates configuration files for **AutoDock Vina**, setting parameters such as exhaustiveness, grid box size, and seed values (random or user-defined).

6. **Docking Execution**  
   AutoDock Vina is executed through Python subprocess automation.  
   Docking runs are logged, and intermediate outputs (poses, energies) are stored for analysis.

7. **Results Analysis**  
   Binding affinities, RMSD values, and docking poses are analyzed and ranked.  
   Results are compiled into structured tables and CSV reports.

8. **Visualization**  
   The best receptor–ligand complexes are visualized using **PyMOL**, displaying 3D binding interactions and orientations.

9. **Report Generation**  
   The system automatically exports results in `.csv` format and generates graphical summaries for further interpretation.


![Workflow Diagram](https://github.com/Atirath-Pal/Automated-Molecular-Docking/blob/0963c2e06995658eb7d8179f18980b5f5bdbb0d0/workflow%20diagram.png)

> *Figure 1: Workflow diagram illustrating the complete automated molecular docking pipeline — from user input and data retrieval to docking execution, visualization, and report generation.*


---


## Tools and Technologies Used

The automated molecular docking pipeline integrates multiple open-source tools, scientific libraries, and frameworks to achieve complete automation of the docking process.  
The following table summarizes the major technologies and their respective roles in the system.

| Category | Tool / Library | Purpose / Function |
|-----------|----------------|--------------------|
| **Programming Language** | Python 3.10+ | Core scripting language used for automation, computation, and interface logic |
| **Docking Engine** | AutoDock Vina | Performs receptor–ligand docking and calculates binding affinities |
| **Structure Conversion** | Open Babel | Converts molecular file formats and prepares `.pdbqt` files for docking |
| **Visualization Tool** | PyMOL | Visualizes receptor–ligand binding poses in 3D |
| **User Interface Framework** | Streamlit | Builds the interactive graphical web interface |
| **Data Retrieval & Parsing** | Biopython (Entrez), BeautifulSoup, Requests | Automates downloading of biological data from NCBI, PubChem, and SWISS-MODEL |
| **Molecular Informatics** | RDKit | Handles ligand molecular structures and performs chemical property analysis |
| **Automation Tools** | Selenium, Subprocess | Automates web-based and local command-line operations |
| **Data Processing** | Pandas, NumPy | Processes numerical data and manages result tables and statistics |
| **Plotting & Reporting** | Matplotlib | Generates graphs and visual summaries of docking results |
| **System Utilities** | OS, Shutil, Threading | Manages file handling, task parallelization, and system-level operations |
| **Version Control** | Git & GitHub | Repository hosting and version management |

---

### Development Environment

- **Operating System:** Windows 10 / Linux (Ubuntu 22.04 tested)
- **Python Version:** 3.10 or higher
- **IDE / Editor:** VS Code or PyCharm
- **External Dependencies:** AutoDock Vina, Open Babel, PyMOL

> *All external tools must be correctly installed and their executable paths configured in `config.py` before running the pipeline.*

