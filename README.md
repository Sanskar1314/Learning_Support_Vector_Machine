# Learning Support Vector Machines

Notebook exercises covering support vector classification and regression with scikit-learn.

## Contents

- `learning_svc.ipynb`: generates a synthetic binary classification dataset, compares linear, RBF, and polynomial kernels, and tunes an RBF SVC with five-fold GridSearchCV. Evaluation uses classification reports and confusion matrices.
- `learning_svr.ipynb`: predicts `total_bill` from the Seaborn tips dataset using categorical encoding, SVR, and hyperparameter search. Evaluation uses R² and mean absolute error.

## Run locally

Use Python 3 and run Jupyter from the repository directory.

```bash
git clone https://github.com/Sanskar1314/Learning_Support_Vector_Machine.git
cd Learning_Support_Vector_Machine
python -m venv .venv
source .venv/bin/activate
python -m pip install jupyterlab numpy pandas matplotlib seaborn scikit-learn
jupyter lab
```

On Windows, activate the environment with `.venv\Scripts\activate`. Open the notebook listed above and run its cells in order. Results and visualizations appear in the notebook.

## Reproduction notes

The classification dataset is generated locally; loading the tips dataset may require internet access. In the regression notebook, the test-data encoding section is incomplete: apply the fitted `sex` encoder to `X_test['sex']` before the column transformation. Review the cell mentioning an already transformed test array when running from a fresh kernel.
