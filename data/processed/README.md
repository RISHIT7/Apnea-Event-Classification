# Processed ISRUC Dataset

This folder contains the **processed ISRUC-Sleep dataset**, prepared for use in deep learning models for apnea event classification. The raw ISRUC-Sleep data has been preprocessed to extract relevant features and ensure consistency across subjects and recording sessions.

## Dataset Overview

The processed dataset is derived from the raw ISRUC-Sleep dataset and includes the following improvements:

1. **Signal Extraction**: Relevant signals (e.g., SpO2, abdominal flow, nasal airflow) have been extracted and standardized across all recordings.
2. **Preprocessing**: Signals have been filtered, normalized, and segmented into event-based and non-event-based data.
3. **Annotations**: Event labels (e.g., apnea events, sleep stages) are included for supervised learning tasks.

## Structure

The folder structure is as follows:

- **`Events/`**
  - Contains processed data for apnea events.
  - Files are named as:
    `S1_p100_1_Stagen1_Event102_Session_1.csv`
    - **S1**: Subject ID
    - **p100**: Patient ID
    - **1**: Sequence number of the segment
    - **Stagen1**: Sleep stage
    - **Event102**: Event identifier
    - **Session_1**: Recording session number

- **`Non Events/`**
  - Contains processed data for non-apnea (normal) events.
  - Files are named using the same convention as in the `Events/` directory.

## Preprocessing Steps

The following preprocessing steps were applied to the raw ISRUC-Sleep data:

1. **Signal Filtering**: Applied bandpass filters to remove noise and irrelevant frequency components.
2. **Segmentation**: Signals were divided into fixed-length segments for event and non-event classification.
3. **Normalization**: Data was normalized for consistency across patients and sessions.
4. **Labeling**: Each segment was labeled based on the corresponding apnea or non-apnea events.

## Usage

This dataset can be directly used for:

- Deep Learning
  - Access through this link: [ISRUC-Processed](https://www.kaggle.com/datasets/rishitjakharia/isruc-processed)
  - Can be used to train Time-Series Applications.
- Machine Learning
  - Access through this link: [ISRUC-Signal-Features](https://www.kaggle.com/datasets/rishitjakharia/isurc-signal-features)
  - These are signal features extracted using the `TSFEL` library.
  - It can be used to train machine-learning applications.

## Acknowledgments

This processed dataset is based on the publicly available ISRUC-Sleep dataset. Please ensure that any use of this processed data complies with the licensing and usage terms of the original ISRUC-Sleep dataset.

For more information about the ISRUC-Sleep dataset, visit:  
[ISRUC-Sleep Dataset](https://sleeptight.isr.uc.pt/)

If you use this processed dataset in your research, please cite the original dataset publication:

Khalighi Sirvan, Teresa Sousa, José Moutinho Santos, and Urbano Nunes.  
**"ISRUC-Sleep: A comprehensive public dataset for sleep researchers."**  
*Computer Methods and Programs in Biomedicine* 124 (2016): 180-192.

## License

This dataset inherits the licensing terms of the ISRUC-Sleep dataset.
