# Network Connections ML

A Python cybersecurity machine-learning learning project analyzing synthetic network connections and preparing data for attack classification.

## Status

**Groups 1–4 complete; initial decision-tree experiment added.** Model evaluation and optimization are not yet implemented.

## Features

- Reproducible dataset generation: 350 benign and 150 attack-labelled connections.
- Data inspection, filtering, and descriptive statistics with pandas.
- Security feature engineering: total bytes, packet rate, byte ratio, and outbound-heavy indicator.
- Bar charts and histograms using matplotlib.
- One-hot protocol encoding and stratified 75/25 train/test split.
- Initial `DecisionTreeClassifier` training and predictions, without evaluation metrics yet.

## Technologies

Python, NumPy, pandas, matplotlib, scikit-learn, Jupyter Notebook.

## Run locally

```bash
python -m venv .venv
```

Activate the environment using `.venv\Scripts\Activate.ps1` in Windows PowerShell or `source .venv/bin/activate` on Linux/macOS, then:

```bash
pip install -r requirements.txt
jupyter notebook notebooks/Network-Connections-ML.ipynb
```

Run the cells from top to bottom. The notebook writes a generated `network_connections.csv` file into the current working directory.

## Roadmap

- [x] Group 1 — Synthetic network data generation
- [x] Group 2 — Exploratory analysis and filtering
- [x] Group 3 — Feature engineering and visualization
- [x] Group 4 — Machine-learning feature preparation and train/test split
- [x] Initial decision-tree model training and prediction
- [ ] Model evaluation: confusion matrix, precision, recall, F1 score
- [ ] Model comparison and optimization

## Limitations

This is a **synthetic educational dataset**, not evidence of real-world intrusion-detection performance. Benign and attack-labelled records are generated from distinct distributions, and the source IP ranges differ by class. The source IP is not included in the model feature list, but models could still learn unrealistic synthetic generation patterns. No validated detection performance is claimed.

## License

MIT — see [LICENSE](LICENSE).
