# DSWB Data Harmonization Models

This repository contains datasets, documentation, scripts, and reflective notes developed by the Data Harmonization Working Group for the DSWB Platform. These resources support collaborative efforts to harmonize population health data using FAIR principles and widely accepted standards like [Schema.org](https://schema.org/), JSON-LD, and model-based design.

---

### Folder Structure

#### `datasets/`
Schema.org-compliant JSON-LD translations of harmonized codebooks following [science-on-schema.org guidelines](https://github.com/ESIPFed/science-on-schema.org/blob/main/guides/Dataset.md).

- `tb_dataset.jsonld`  
  Translated representation of the tuberculosis (TB) dataset, derived from the DGH harmonized codebook.

- `DGH_TB_Codebook.xlsx`  
  The original harmonized Excel codebook for the TB dataset used for Schema.org translation.

#### `documentation/`
Technical guides, data models, and method-specific documentation.

- `FL-followedBy-NMA.md`  
  Combined approach of Federated Learning (FL) followed by Network Meta-Analysis (NMA).

- `MedicalRiskEstimator.md`  
  Description of the medical risk estimation model.

- `Using NMA after FL to adjust for heterogeneity.md`  
  Guide on applying NMA to account for population-level heterogeneity.

- `medicalobservationalstudy_v1.md`  
  Documentation of the medical observational study model.

- `medicalobservationalstudy_v1.html`  
  HTML version for web-based rendering.

#### `wiki/`
Collaborative blog-style reflections, internal notes, and working drafts on modeling and harmonization efforts.

---

