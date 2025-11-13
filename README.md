# AI Policy Audit: Privacy Policies of Major AI Firms

This repository contains the **code** for the paper:

> *AI Privacy Policies: Topics, Rights and Agency across the EU and US*  
> (submitted to *Data & Policy*)

The goal of this repo is to provide a clean, minimal home for the **analysis code**.  
The full replication package (data, outputs, and notebook + manifest) is archived on Zenodo.

---

## Contents

- `ai_policy_audit_onecell.ipynb`  
  A single–notebook pipeline that:
  - converts the 8 HTML privacy policies into cleaned paragraph text;
  - builds baseline and brand–ablated TF–IDF representations;
  - runs NMF topic discovery and reports topic stability under brand ablation;
  - trains a brand–independent logistic classifier with leakage–aware validation (Leave-One-Group-Out);
  - computes rights/consent rates and modality indicators with bootstrap uncertainty;
  - generates all tables, figures, and the supplement bundle.

- `README.md`  
  This file.

All other artefacts (policies, outputs, supplement ZIP) are stored in the Zenodo replication package.

---

## Data and full replication package

The full replication package (including the 8 HTML and 8 TXT policy files, all outputs, and a manifest) is archived on Zenodo:

- **Zenodo DOI:** https://doi.org/10.5281/zenodo.17541990  

That ZIP contains:

- `policies_html/` – original HTML policy captures  
- `policies_text/` – cleaned TXT versions used as inputs  
- `Code/ai_policy_audit_onecell.ipynb` – the analysis notebook  
- `outputs/` – all tables, figures, and supplement bundle  
- `outputs/meta/env_versions.json` and `manifest.json` – environment and run metadata

---

## How to run the audit

1. Download the replication package ZIP from Zenodo:  
   https://doi.org/10.5281/zenodo.17541990  

2. Unzip it (you should see `ai_policy_audit_replication_package/` with `policies_html/`, `policies_text/`, `Code/`, `outputs/`, etc.).

3. Open `ai_policy_audit_onecell.ipynb` in:
   - Jupyter Notebook / JupyterLab, **or**
   - Google Colab (upload the notebook and the folder, or mount the folder in your environment).

4. Set the working directory so that the notebook “sees” the folder structure as:
   - `policies_html/`
   - `policies_text/`
   - `outputs/`
   - etc.

5. Run all cells.  
   This will regenerate all tables and figures into `outputs/` deterministically.

---

## License and reuse

The code in this repository may be reused for research and regulatory audit purposes.  
Please cite the associated paper and the Zenodo record when using or adapting the pipeline.

---

## Citation

If you use this code or the replication package, please cite:

- The paper (once published), and  
- The Zenodo archive:  
  > Sanjay M. (2025). *AI policy audit replication package* (v1). Zenodo. https://doi.org/10.5281/zenodo.17541990
