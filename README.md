# Apnea Event Classification Using Deep Learning

This project aims to classify apnea and non-apnea events from polysomnographic (PSG) signals using deep learning techniques. The dataset used for this project is derived from the **ISRUC-Sleep dataset**, a comprehensive collection of PSG recordings, which includes data from healthy individuals and subjects with sleep disorders. The project explores the use of Temporal Convolutional Networks (TCNs) for classifying apnea events based on respiratory signals.

## Project Structure

The project is organized into the following key components:

### **1. Dataset**

- **raw/**: Contains references to the original ISRUC-Sleep dataset. The raw data is not stored in this repository due to licensing restrictions. A `README.md` is provided to guide users in accessing and citing the dataset.
- **processed/**: Contains preprocessed versions of the ISRUC-Sleep dataset, including signal extraction, filtering, and segmentation into event-based and non-event-based data, ready for model training and evaluation.
- **ISRUC_Signal_Features/**: A folder containing feature-extracted data for further analysis or model refinement.

### **2. Source Code**

> to be created

- **src/**: Contains the main code for data preprocessing, model building, training, evaluation, and prediction. It includes:

  - `preprocessing/`: Scripts for filtering and extracting relevant signals from the raw data.
  - `models/`: Defines the Temporal Convolutional Network (TCN) architecture and other model components.
  - `train.py`: Script to train the deep learning model.
  - `evaluate.py`: Script to evaluate the trained model.
  - `predict.py`: Script for making predictions on new data.

### **3. Notebooks**

- **notebooks/**: Jupyter notebooks used for exploratory data analysis, visualization, and experimenting with various preprocessing techniques and model architectures.

### **4. Reports and Documentation**

> to be created

- **reports/**: Project reports, including the final documentation and figures used in the research.
- **README.md**: Provides an overview of the project, dataset, and instructions for usage.

### **5. Tests**

> to be created

- **tests/**: Unit tests to validate the integrity of the code and ensure the reliability of preprocessing, model, and evaluation scripts.

### **6. Miscellaneous**

- **requirements.txt**: A list of dependencies required to run the project.
- **LICENSE**: The project license, which is based on the original ISRUC-Sleep dataset license.

---

## Features of the Project

- **Signal Processing**: Extracting key signals like SpO2, abdominal flow, and nasal airflow from raw PSG data.
- **Deep Learning Model**: A Temporal Convolutional Network (TCN) model is used for classifying apnea and non-apnea events.
- **Preprocessing Pipeline**: Data is filtered, segmented, and normalized to ensure consistency across subjects.
- **Performance Evaluation**: The model is evaluated using a validation set, and the results are visualized to measure performance.

---

## Getting Started

### Prerequisites

To run this project, you need to have Python installed along with the necessary dependencies. You can install the required dependencies by running:

```bash
pip install -r requirements.txt
```

### Dataset Access

The project relies on the **ISRUC-Sleep dataset** for the raw and processed data. You can access the dataset via the official website:

[ISRUC-Sleep Dataset](https://sleeptight.isr.uc.pt/)

Please download the dataset manually, as it is not included in this repository due to licensing restrictions.

### Running the Code

1. **Preprocessing**: Run the `preprocessing/` scripts to extract and preprocess the signals from the raw dataset.
2. **Model Training**: Use the `train.py` script to train the Temporal Convolutional Network (TCN) model with the processed dataset.
3. **Model Evaluation**: After training, use the `evaluate.py` script to evaluate the model's performance on the validation set.
4. **Prediction**: To classify new apnea events, run the `predict.py` script with new data.

---

## Relevant Reading

|title|referenced paper|
|:---:|:---:|
|Inter Annotator Relibility|[Inter-Annotator Reliability of Medical Events, Coreferences and Temporal Relations in Clinical Narratives by Annotators with Varying Levels of Clinical Expertise](https://pubmed.ncbi.nlm.nih.gov/23304416/)|
|Automatic Home Based Apnea Estimation|[Towards automatic home-based sleep apnea estimation using deep learning](https://doi.org/10.1038/s41746-024-01139-z)|
|Deep Learning of OSA on Signal channel oximetry|[Deep learning for obstructive sleep apnea diagnosis based on single channel oximetry](https://doi.org/10.1038/s41467-023-40604-3)|
|Temporal Convolutional Networks|[Temporal Convolutional Networks: A Unified Approach to Action Segmentation](https://doi.org/10.48550/arXiv.1608.08242)|

---

## Citation

If you use this dataset or project in your research, please cite the original ISRUC-Sleep dataset:

Khalighi Sirvan, Teresa Sousa, José Moutinho Santos, and Urbano Nunes.  
**"ISRUC-Sleep: A comprehensive public dataset for sleep researchers."**  
*Computer Methods and Programs in Biomedicine* 124 (2016): 180-192.

---

## License

This project uses the **ISRUC-Sleep dataset**, which is governed by its original licensing terms. Please ensure you follow the terms specified by the authors when using the dataset.

For more information on the dataset's license, visit the [ISRUC-Sleep dataset website](https://sleeptight.isr.uc.pt/).

---

## Acknowledgments

- The ISRUC-Sleep dataset was developed with support from the Portuguese Foundation for Science and Technology (FCT).
- Thanks to the Sleep Medicine Centre of the Hospital of Coimbra University (CHUC) for their invaluable support in data acquisition and visual scoring.
- This project was made possible through the **SLEEPTIGHT** project (QREN, FEDER reference CENTRO-01-0202-FEDER-011530).
