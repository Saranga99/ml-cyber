# Cybersecurity and Machine Learning Assignment

## How to Run the Notebooks

The assignment contains four Jupyter notebooks:

* `task_1_email_spam_detection.ipynb`
* `task_2_network_intrusion_detection.ipynb`
* `task_3_anomaly_detection.ipynb`
* `task_4_ransomware_detection.ipynb`

## Running the Notebooks in Google Colab

1. Upload all `.ipynb` files to Google Drive.

2. Right-click the required notebook and select:

   **Open with → Google Colaboratory**

3. In Google Colab, go to:

   **Runtime → Change runtime type**

4. Select **GPU** as the hardware accelerator.

   GPU is recommended because the notebooks contain deep learning models such as LSTM, CNN, and Autoencoder.

5. Click **Save** and wait for the runtime to connect.

6. Run the notebook using:

   **Runtime → Run all**

   This will execute all cells from top to bottom.

7. The notebook can also be executed manually by clicking the **Run** button beside each cell.

   When running cell by cell, always follow the notebook order because later cells depend on variables created in previous cells.

8. Wait until model training is complete before running evaluation cells.

9. After execution, check the final:

   * accuracy;
   * precision;
   * recall;
   * F1-score;
   * classification reports;
   * confusion matrices;
   * training graphs;
   * model comparison results.

10. Save the completed notebook to Google Drive or download it as an `.ipynb` file for submission.

---

# Task 1 – Email Spam / Phishing Detection

This task detects whether an email is legitimate or spam/phishing.

The **Enron Spam Dataset** is used.

The main steps are:

* clean and preprocess email text;
* convert text into numerical features using TF-IDF;
* train Logistic Regression;
* train Random Forest;
* tokenize and pad text sequences;
* train an LSTM neural network;
* evaluate the models using accuracy, precision, recall, F1-score, confusion matrix, and ROC curve.

The notebook compares traditional machine learning methods with an LSTM deep learning model.

---

# Task 2 – Network Intrusion Detection

This task detects different types of network attacks using the **NSL-KDD Dataset**.

The attacks are grouped into five classes:

* Normal
* DoS
* Probe
* R2L
* U2R

The main steps are:

* preprocess numerical and categorical network features;
* apply one-hot encoding;
* scale numerical features;
* use PCA for dimensionality reduction;
* train a Random Forest classifier;
* train a 1D CNN deep learning model;
* evaluate both models using accuracy, precision, recall, F1-score, confusion matrices, and ROC curves.

The final results are used to compare the Random Forest and CNN models.

---

# Task 3 – Anomaly Detection

This task detects unusual network behaviour using the **UNSW-NB15 Dataset**.

The main idea is to train models using normal network traffic and identify unusual traffic as possible attacks.

Two models are used:

* Isolation Forest
* Autoencoder

The main steps are:

* remove duplicate records;
* preprocess network features;
* encode categorical variables;
* scale numerical features;
* train Isolation Forest using normal traffic;
* train Autoencoder using normal traffic;
* calculate anomaly scores;
* select anomaly thresholds;
* classify unusual traffic as attacks;
* compare both models using precision, recall, F1-score, false positive rate, and Precision-Recall curves.

The task demonstrates how unsupervised and deep learning methods can detect abnormal network behaviour.

---

# Task 4 – Ransomware Detection

This task detects ransomware activity using the **CIC-AndMal2017 Dataset**.

The notebook performs binary classification between:

* Benign
* Ransomware

The main steps are:

* load and filter the dataset;
* create additional behavioural features;
* separate training and testing data;
* remove constant features;
* remove highly correlated features;
* standardize numerical features;
* create sequences of network flows;
* train a Linear SVM;
* train an LSTM model;
* evaluate both models using accuracy, precision, recall, F1-score, confusion matrices, and training curves.

The final comparison shows how traditional machine learning and deep learning perform for ransomware detection.

---

# General Notes

All notebooks should be executed from the first cell to the last cell.

Do not skip preprocessing cells because the model-training and evaluation sections depend on them.

A GPU runtime is recommended for the deep learning models.

If the Colab runtime disconnects, reconnect and run the notebook again from the beginning.

Some results may change slightly between runs because deep learning models can be affected by random initialization and GPU operations.

Always save the final notebook after all outputs, plots, and evaluation results have been generated.
