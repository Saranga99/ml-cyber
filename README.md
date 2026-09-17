# COMP70049 Assignment 1

## Status
All eight models are implemented. Default measurements are synthetic demonstrations, not real cybersecurity results. The brief is the only attached input. Real-data evaluation remains necessary before a benchmark submission.

## Run
Use Python 3.11+. Create a virtual environment, then run:

```sh
pip install numpy pandas scipy scikit-learn matplotlib seaborn torch nltk nbformat nbclient ipykernel jupyter
jupyter notebook COMP70049_Assignment1.ipynb
```

Run all cells in order. Alternatively: `python assignment.py` (figures display through your Matplotlib backend). CPU is supported. The notebook uses no downloaded pretrained model and no NLTK corpus download.

## Real data
Create `data/` beside the notebook. Supply emails.csv, network_train.csv, network_test.csv and ransomware.csv using the exact data contracts in the notebook. Set DEMO=False. Binary label 1 means malicious. UNSW official CSVs should use their train/test split. Convert Email Text to text and map Safe Email/Phishing Email to 0/1 explicitly. API files must contain confirmed ransomware and benign samples, ordered calls and executable sample_id. Do not execute malware.

The program deliberately raises an error if real files are absent or invalid. It writes metrics to results/metrics.csv. Real runs use up to 25 epochs, with validation checkpointing and early stopping. Adjust resource limits before running large datasets; dense one-hot arrays and PCA can require substantial memory.

## Files
- COMP70049_Assignment1.ipynb: main code, explanations, figures, comparisons and inline written report.
- assignment.py: equivalent executable Python code.
- REPORT.md: methodology/report text; includes the evaluation-pending limitation.
- README.md: these instructions.

## Submission
Re-run on real data, review outputs, and update the report with measured findings and exported figures. Follow institutional AI-use/disclosure requirements. This package does not claim a completed empirical evaluation from unavailable datasets.
