# ISRUC-Sleep Dataset Repository

This repository provides resources for working with the ISRUC-Sleep dataset, a comprehensive polysomnographic (PSG) dataset designed to aid sleep research. It is organized into two main folders: `raw/` and `processed/`, catering to different stages of analysis.

## Folder Structure

### **1. `raw/`**

This folder contains references and metadata for the raw ISRUC-Sleep dataset. The actual dataset files are not included due to licensing restrictions. Instead, it provides documentation and guidelines for accessing the original data.

- **Contents**:
  - `README.md`: Instructions for accessing and citing the ISRUC-Sleep dataset.
  - Link to the official ISRUC-Sleep dataset: [ISRUC-Sleep Dataset](https://sleeptight.isr.uc.pt/).

- **Dataset Information**:
  - Includes original PSG recordings from multiple subjects.
  - Contains data for 100+ subjects, including healthy individuals and those with sleep disorders.

---

### **2. `processed/`**

This folder contains the preprocessed version of the ISRUC-Sleep dataset, optimized for machine learning applications.

- **Contents**:
  - Preprocessed data categorized into `Events/` (apnea events) and `Non Events/` (normal respiration periods).
  - Files are stored in `.csv` format, labeled and segmented for easy use in training and testing models.

- **Preprocessing Steps**:
  - Signal extraction (e.g., SpO2, abdominal flow, nasal airflow).
  - Signal filtering, segmentation, and normalization.
  - Event and non-event labeling for supervised learning tasks.

---

## Applications

This dataset repository is designed to support:

- **Sleep Research**: Analysis of sleep disorders, including apnea.
- **Deep Learning Models**: Training and validation for apnea event classification.
- **Signal Processing**: Feature extraction and analysis of physiological signals.

## Citation

If you use this repository or the ISRUC-Sleep dataset in your work, please cite the original publication:

Khalighi Sirvan, Teresa Sousa, José Moutinho Santos, and Urbano Nunes.  
**"ISRUC-Sleep: A comprehensive public dataset for sleep researchers."**  
*Computer Methods and Programs in Biomedicine* 124 (2016): 180-192.

## License

This repository is governed by the licensing terms of the original ISRUC-Sleep dataset. Users must comply with the dataset’s terms and conditions. For more details, refer to the licensing information in the `raw/` and `processed/` folders.

## Acknowledgments

The ISRUC-Sleep dataset was developed with support from:

- Portuguese Foundation for Science and Technology (FCT).
- QREN-funded project SLEEPTIGHT.
- Sleep Medicine Centre of the Hospital of Coimbra University (CHUC).

For more details, visit the [ISRUC-Sleep Dataset website](https://sleeptight.isr.uc.pt/).
