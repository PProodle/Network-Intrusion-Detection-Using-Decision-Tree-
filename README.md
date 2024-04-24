# KDD99 Network Intrusion Detection Project

## Overview
This project focuses on analyzing and classifying different types of network intrusions using the KDD99 dataset. The dataset is a benchmark for evaluating intrusion detection systems, containing a variety of network traffic with labeled attack types. The primary goal is to identify features that help detect various types of attacks and to train machine learning models to classify them accurately.

## Dataset
The dataset used in this project is the KDD Cup 1999 dataset. It contains both a training and a test set with multiple features describing network connections and labeled attack types. The dataset is structured as follows:

- **Training set**: Contains data to train models, with various attack types and normal traffic.
- **Test set**: Used to evaluate the models' performance, containing a mix of known and new attack types.

## Features
The dataset contains multiple features, including:

- `duration`: Duration of the connection.
- `protocol_type`: Type of network protocol (e.g., TCP, UDP).
- `service`: Network service on the destination port (e.g., HTTP, FTP).
- `flag`: Status of the connection.
- `src_bytes`, `dst_bytes`: Number of bytes from source and destination.
- And more...

Additionally, the dataset has a label column indicating whether a connection is normal or an attack, along with the type of attack.

## Preprocessing
To prepare the data for machine learning models, the following steps were taken:

- **Label Encoding**: Categorical features like `protocol_type`, `service`, and `flag` were converted into numeric form using label encoders.
- **One-Hot Encoding**: The same categorical features were transformed into a binary representation.
- **Feature Selection**: Statistical techniques like `SelectPercentile` and recursive feature elimination (RFE) were used to select the most relevant features for each attack type.
- **Normalization**: Features were normalized using a `StandardScaler` to ensure they are on a similar scale.

## Attack Categories
The project focuses on four primary categories of attacks:

1. **DoS (Denial of Service)**
2. **Probe (Information Gathering)**
3. **R2L (Remote to Local)**
4. **U2R (User to Root)**

These categories represent different types of malicious network activities, each requiring specific features and models for accurate detection.

## Model Training and Evaluation
Various models were trained to classify different attack categories. Decision trees were used extensively due to their interpretability and effectiveness in dealing with complex features. Models were evaluated using the following metrics:

- **Confusion Matrix**: To understand misclassifications.
- **Accuracy**: To measure overall model performance.
- **Feature Importance**: To identify which features contribute most to the model's predictions.

## Results and Findings
The project results include the following key outcomes:

- **Selected Features**: A list of the most important features for each attack category.
- **Performance Metrics**: Accuracy and confusion matrices for each model.
- **Insights**: Observations on which features are most indicative of specific attack types.

## Additional Considerations
To extend the project, consider the following:

- **Cross-Validation**: Implement cross-validation to ensure model robustness.
- **Model Diversity**: Explore other machine learning models like Random Forest, SVM, or Neural Networks.
- **Handling Imbalanced Data**: Investigate methods to deal with imbalanced attack categories.
- **Real-World Application**: Consider deploying the models in a real-world intrusion detection system.

## Contributing
Contributions are welcome. If you find a bug or want to add new features, feel free to open an issue or submit a pull request.
