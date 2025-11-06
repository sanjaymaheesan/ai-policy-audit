# AI Privacy Policy Audit — Replication Code

This repository contains the code for the paper on auditing AI privacy policies (topics, rights, and modality across EU/US).

## What this code does

- Converts 8 official privacy policy HTML files (Google, Meta, OpenAI, xAI; EU and US) into clean text
- Splits text into paragraphs (blank lines, ≥30 characters)
- Builds baseline and brand-ablated TF–IDF features
- Runs NMF topics and checks stability after brand ablation
- Trains a brand-independent classifier (company as target) with LOGO by document
- Computes:
  - rights and consent references per 1,000 words (with bootstrap intervals)
  - a neutral US state-appendix diagnostic
  - modality markers (organisational discretion, user agency, user constraints) per 1,000 words

## How to run (Google Colab)

1. Open the notebook `ai_policy_audit_onecell.ipynb` in Google Colab.
2. Upload these 8 HTML files into the Colab environment with *exactly* these names:

   - `google_eu.html`
   - `google_us.html`
   - `meta_eu.html`
   - `meta_us.html`
   - `openai_eu.html`
   - `openai_us.html`
   - `xai_eu.html`
   - `xai_us.html`

3. Run the notebook from top to bottom.
4. The script will create an `outputs/` folder containing:
   - all figures (PNG + captions)
   - all tables (CSV)
   - an environment file
   - a ZIP bundle (`supplement_bundle_tp_robustness.zip`) for the supplement.

## Inputs

The HTML files are not redistributed here. They are the official privacy policies downloaded from the companies’ websites (Google, Meta, OpenAI, xAI; EU and US variants). The notebook explains exactly which filenames are expected.
