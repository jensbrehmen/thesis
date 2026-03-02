# A Foundational Approach to Improve Causal Machine Learning and Uplift Modeling
Implementation and evaluation of **TabPFN** as a base learner in meta-learner frameworks (S, T, X, R, DR, Z) for causal effect estimation and uplift modeling. Benchmarked on semi-synthetic and real-world RCT datasets against LightGBM, linear models, Causal Forests, and CausalPFN.

## 📂 Repository Structure

The project is organized by experiment. Each experiment contains its own data and notebook to ensure modularity and reproducibility.

```
.
├── Experiment_Name/
│   ├── data/
│   │   ├── dataset_1.csv
│   │   ├── dataset_2.csv
│   │   └── ...
│   └── experiment.ipynb
├── Experiment_Name_2/
│   ├── data/
│   │   └── ...
│   └── experiment.ipynb
└── README.md
```

---

## 🔬 Per Experiment Structure

Each experiment is fully self-contained and follows the structure below.

```
Experiment/
├── data/
│   └── (CSV files used in the experiment)
└── experiment.ipynb
```

### 📁 `data/`

Contains all raw and/or processed CSV datasets used in the experiment.  
Ensures experiments remain self-contained and reproducible.

### 📓 `experiment.ipynb`
Jupyter Notebook containing:
- Data preprocessing  
- Model implementation (S-, T-, X-, R-, DR-, Z-learners)  
- Evaluation (PEHE, ATE error, AUQC)  
- Result visualization  
- Sensitivity analyses (if applicable)

This modular structure keeps experiments organized, reproducible, and easy to extend.
