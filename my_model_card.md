---
{}
---

language: en
license: cc-by-4.0
tags:

- text-classification
  repo: https://github.com/azibbrrrrr/Bi-LSTM

---

# Model Card for AzibIqbal-WanteLin-ED

<!-- Provide a quick summary of what the model is/does. -->

The biLSTM model is designed to address the problem of evidence detection in text data. It processes and identifies relevant information that can be considered as evidence within a given claim.

## Model Details

### Model Description

<!-- Provide a longer summary of what this model is. -->

A bi-directional Long Short-Term Memory (biLSTM) network trained to detect and classify textual evidence. The model was developed to process and identify relevant information in text data that can be used as evidence in various domains.

- **Developed by:** Azib Iqbal and Wante Lin
- **Language(s):** English
- **Model type:** Classification
- **Model architecture:** BiLSTM
- **Finetuned from model [optional]:** N/A

### Model Resources

<!-- Provide links where applicable. -->

- **Repository:** https://github.com/azibbrrrrr/Bi-LSTM
- **Paper or documentation:** N/A

## Training Details

### Training Data

<!-- This is a short stub of information on the training data that was used, and documentation related to data pre-processing or additional filtering (if applicable). -->

The model was trained on a dataset comprising over 23,000 examples. A set of over 5,000 instances was used for testing.

### Training Procedure

<!-- This relates heavily to the Technical Specifications. Content here should link to that section when it is relevant to the training procedure. -->

#### Training Hyperparameters

<!-- This is a summary of the values of hyperparameters used in training the model. -->

      - learning_rate: 0.001
      - batch_size: 256
      - num_epochs: 3
      - validation_split=0.2
      - droput = 0.1

#### Speeds, Sizes, Times

<!-- This section provides information about how roughly how long it takes to train the model and the size of the resulting model. -->

      - overall training time: 22.33 seconds
      - duration per training epoch: 7.44 seconds
      - model size: 9.91 MB

## Evaluation

<!-- This section describes the evaluation protocols and provides the results. -->

### Testing Data & Metrics

#### Testing Data

<!-- This should describe any evaluation data used (e.g., the development/validation set provided). -->

The model was tested using over 5,000+ instances from the development set.

#### Metrics

<!-- These are the evaluation metrics being used. -->

      - Precision
      - Recall
      - F1-score
      - Support
      - Accuracy
      - ROC AUC Score

### Results

        The model achieved the following results on the test set:
        - Accuracy: 81.31%
        - ROC AUC Score: 0.73

        Class-wise metrics:
        - Class 0 (Precision: 0.85, Recall: 0.91, F1-Score: 0.88, Support: 4327)
        - Class 1 (Precision: 0.69, Recall: 0.61, F1-Score: 0.61, Support: 1599)

## Technical Specifications

### Hardware

      - RAM: at least 16 GB
      - Storage: at least 2GB
      - GPU: V100 (recommended)

### Software

      - TensorFlow 2.x
      - Keras (compatible version with TensorFlow 2.x)

## Bias, Risks, and Limitations

<!-- This section is meant to convey both technical and sociotechnical limitations. -->

The model may exhibit lower recall for class 1, indicating a potential bias towards class 0. It's recommended to further investigate the data distribution and consider additional measures to balance the classes.

## Additional Information

<!-- Any other information that would be useful for other people to know. -->

The hyperparameters were selected based on preliminary experiments optimizing for model performance and training efficiency.
