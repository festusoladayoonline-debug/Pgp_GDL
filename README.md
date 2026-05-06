# Research Data Availability: Graph-Based De Novo Design and Ensemble Learning for P-gp Inhibitors

This documentation outlines the repository and data architecture for the discovery of novel P-glycoprotein (P-gp) inhibitors. Developed for highly impactful scientific research, this project integrates Geometric Deep Learning and consensus Machine Learning to address multi-drug resistance (MDR) and enhance drug delivery across the Blood-Brain Barrier (BBB).

---

## 1. Project Overview & Impact
The efflux transporter P-glycoprotein (P-gp) remains a formidable challenge in neuro-pharmacology, often preventing therapeutic concentrations of drugs from reaching the central nervous system. This study utilizes a sophisticated computational pipeline to identify inhibitors that are both structurally novel and synthetically accessible.

### Key Objectives
*   **De Novo Molecular Generation:** Employing Graph Neural Networks (GNN) for atom-by-atom assembly of novel chemical entities.
*   **Predictive Modeling:** Utilizing a high-fidelity ensemble (RF, SVM, XGBoost, CatBoost, and MLP) to classify inhibition activity.
*   **Mechanistic Clarity:** Prioritizing explainable AI (SHAP) to understand the physicochemical drivers of P-gp modulation.



---

## 2. The Scientific Contract
To maintain the highest standards of scientific integrity and reproducibility, this research adheres to a strict foundational contract:

*   **Anti-Randomness Clause:** We reject random data splitting in favor of **Bemis-Murcko Scaffold Splitting**, ensuring the model generalizes to truly novel chemical spaces rather than simple analogs.
*   **No-Dummy Coding:** Every data point utilized is experimentally derived; no manipulative or placeholder codes are permitted.
*   **Temporal Integrity:** Model robustness is validated against a **"Time-Machine" set** comprising experimental data from **2024–2026**.
*   **Target Specificity:** All workflows are optimized for the unique challenges of P-gp, specifically distinguishing between inhibitors and substrates.

---

## 3. Data Repository & Directory Structure
All computational artifacts, raw data, and visual results are systematically organized to support transparency and peer review.

### The `/Data` Directory
The project utilizes a centralized `/Data` directory which houses all generated outputs:

| File Type | File Format | Description |
| :--- | :--- | :--- |
| **Figures** | `.png` | Visualizations including SHAP feature importance, ROC curves, and generated molecular structures. |
| **Tables** | `.csv` | Quantitative outputs, including lead candidate metrics, scaffold analysis results, and predictive scores. |
| **Metadata** | `.json`/`.md` | Detailed descriptions of features and experimental conditions used in the models. |

> **Note:** All figures and tables obtained from the execution of the research codes are automatically exported to this directory to ensure a unified data stream.

---

## 4. Methodology & Validation Phase Descriptions
Each phase of this research is documented within the Jupyter Notebook environment using markdown cells to maintain clear formatting and technical context.

### Phase 1: Data Curation & Standardization
*   Retrieval of human ABCB1 (P-gp) data from ChEMBL.
*   Rigorous standardization of SMILES (neutralization, salt removal, and tautomer canonization).

### Phase 2: Generative Graph Modeling
*   Implementation of GNNs for *de novo* design.
*   Application of **Multi-Parameter Optimization (MPO)**, including QED and Synthetic Accessibility (SA) scores.

### Phase 3: Ensemble Predictive Framework
*   Training five distinct architectures to create a consensus voting mechanism.
*   Validation via Bemis-Murcko scaffold partitioning to test "out-of-distribution" performance.

### Phase 4: Temporal & Scaffolding Validation
*   Final assessment using the 2024–2026 validation set to ensure the model remains predictive of the latest experimental trends.

---

## 5. Contact & Institutional Affiliation
**Authors:** Festus Ogungbemiro and Jane Anebi
**Institution:** CBIOS — Universidade Lusófona's Research Center for Biosciences & Health Technologies
**Date of Current Version:** April 28, 2026[cite: 1]

How would you like to proceed with the specific phase descriptions or the validation of the `/Data` directory outputs?
