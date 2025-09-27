# UCD FYP 2025: Explainable Artificial Intelligence (XAI) for Time Series Data Reduction

**Title:** Time Series Data Reduction using Explainable AI (XAI)

This research project addresses the challenge of managing large-scale and noisy time-series data, especially **multivariate** datasets where only a fraction of channels are relevant. The goal is to develop and evaluate an approach for **data reduction** without compromising predictive performance.

We will apply **XAI techniques (e.g., SHAP, LIME)** to identify unimportant or noisy channels and selectively remove them, reducing dimensionality and improving training/inference efficiency while aiming to preserve accuracy.

Students (me!) will gain hands-on experience with time-series classification/regression (UCR datasets like *GunPoint*, *Coffee*), and implement multiple XAI techniques. The main objective is to show that **XAI-driven reduction** yields more efficient models with minimal performance loss.

---

##  Project Structure
FYP-2025-XAI-TimeSeries-DataReduction/
├── src/
│ ├── baseline/ # first experiments (GunPoint, Coffee)
│ └── xai/ # SHAP/LIME/Ablation explanations
├── report/ # drafts, Overleaf exports
├── presentations/ # slides for Trimester 1 + 2
├── data/ # (optional) small datasets or links to UCR archive
├── README.md # project overview 
└── requirements.txt # Python packages (aeon, shap, sklearn, etc.)


##  Setup (Windows / PowerShell)
python -m venv .venv
.\.venv\Scripts\activate
pip install -r requirements.txt


##  Quick start
- Open the folder in **VS Code**.
- Use the **Jupyter** & **Python** extensions.
- Run `src/baseline/quickstart.ipynb` to verify the environment.

##  Datasets
- UCR Archive: http://www.timeseriesclassification.com/dataset.php  
  (Keep large datasets out of Git; place small samples in `data/`.)

##  Reading
- Bake off redux: Time Series Classification algorithms — https://arxiv.org/abs/2304.13029
- Improving the Evaluation and Actionability of Explanation Methods for Multivariate TSC — https://arxiv.org/abs/2406.12507
- KDD24: Hands-on intro to TSC/TSR — https://aeon-tutorials.github.io/KDD-2024/
- XAI books — https://christophmolnar.com/books


##  Research plan (high-level)
1. Baselines on UCR (GunPoint, Coffee): 1NN, RF, SVM.
2. Train model(s) on multivariate data.
3. Use SHAP/LIME to rank channels/time-points.
4. Define reduction policy (e.g., top-k channels; threshold).
5. Retrain & evaluate efficiency vs accuracy trade-off.
6. Ablation & robustness checks; report.


