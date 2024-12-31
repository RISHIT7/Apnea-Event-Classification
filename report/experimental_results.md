# Experimental Results

This document summarizes the key experimental results from the project **Apnea Event Classification Using Deep Learning**. It includes results from different model architectures, datasets, and evaluation strategies.

---

## 1. Train-Test Split Using PatientID

### 1.1. Bi-LSTM + Attention Model

- **Model:** Bi-LSTM with Attention Mechanism
- **Loss Function:** KL Divergence
- **Dataset:** UnderSampled Dataset
- **Observation:** Bi-LSTM models were heavily biased due to the extreme class imbalance in the dataset, resulting in poor generalization. Simpler models performed better on this imbalanced dataset.

| Experiment                                | Train Accuracy | Validation Accuracy |
| ----------------------------------------- | -------------- | ------------------- |
| KL Divergence Loss (UnderSampled Dataset) | 52.41%         | 51.58%              |

### 1.2. Temporal Convolutional Network (TCN)

- **Model Architecture:** TCN with layers of increasing and then decreasing filters
- **Loss Function:** KL Divergence
- **Dataset:** Complete Dataset

#### Results:

| Configuration                                                                                    | Train Accuracy | Validation Accuracy |
| ------------------------------------------------------------------------------------------------ | -------------- | ------------------- |
| TCN (64, 128, 256, 64) (250k parameters)                                                         | 94.61%         | 79.75%              |
| TCN (32, 64, 128, 32) (63k parameters)                                                           | 88.97%         | 73.78%              |
| TCN (32, 64, 128, 32) (63k parameters) + Selected Patients with High Inter-Annotator Reliability | 87.83%         | 76.83%              |

### 1.3. Machine Learning Model

- **Model:** LightGBM
- **Dataset:** Processed Features

#### Results:

| Metric   | Train Accuracy | Test Accuracy |
| -------- | -------------- | ------------- |
| LightGBM | 99%            | 77%           |

---

## 2. Two-Class Classification

### 2.1. Temporal Convolutional Network (TCN)

- **Model Architecture:** TCN with layers (32, 64, 128, 256)
- **Loss Function:** KL Divergence
- **Dataset:** Selected Patients with High Inter-Annotator Reliability

#### Results:

| Experiment                          | Train Accuracy | Validation Accuracy |
| ----------------------------------- | -------------- | ------------------- |
| Initial TCN Model (218k parameters) | 93.04%         | 90.36%              |
| Hyperparameter Tuning               | 95.04%         | 90.89%              |

---

## Observations and Key Findings

1. **Bi-LSTM with Attention**:

   - Bi-LSTM models were heavily biased due to the extreme class imbalance in the dataset, resulting in poor performance on validation data.
   - Simpler models like LightGBM performed better under these conditions.

2. **TCN Models**:

   - Achieve significantly higher performance compared to Bi-LSTM models, especially in two-class classification tasks.
   - Larger TCN models (e.g., 250k parameters) show better performance but require more training time.
   - Downscaled TCN architectures (e.g., 63k parameters) achieve good results with faster training times.
   - Using patients with high inter-annotator reliability further improves validation accuracy, showing the importance of dataset quality.

3. **LightGBM**:

   - Machine learning models perform well on feature-engineered data but may lack the robustness of deep learning models for raw signal-based classification.

4. **Two-Class Classification**:

   - TCN models achieve high validation accuracy (90.89%) with hyperparameter tuning, demonstrating their effectiveness for binary classification tasks.

---

## Conclusion

Temporal Convolutional Networks (TCNs) outperform Bi-LSTM models in this task, particularly when used with datasets of higher quality (e.g., selected patients). The experiments demonstrate the potential of deep learning approaches in apnea event classification while highlighting the need for robust preprocessing and dataset curation to achieve optimal results.

