# A Foundational Approach to Improve Causal Machine Learning and Uplift Modeling
This repository contains the implementation and experimental evaluation for the thesis **“A Foundational Approach to Improve Causal Machine Learning and Uplift Modeling.”** The project studies **TabPFN** as a base learner within standard meta-learner frameworks for **conditional average treatment effect (CATE)** estimation and uplift modeling.

The evaluated meta-learners include **S-, T-, X-, R-, DR-, and Z-learners**. Their performance is benchmarked against established baselines, including **LightGBM**, **linear models**, **Causal Forests**, and **CausalPFN**, on **semi-synthetic** and **real-world randomized controlled trial (RCT)** datasets.

---

## 🎯 Experimental Scope

The experiments in this repository evaluate whether **TabPFN** can serve as an effective base learner within causal meta-learner frameworks for **conditional average treatment effect (CATE)** estimation and uplift modeling. The analysis focuses on performance across different meta-learner formulations, benchmark datasets, and sample sizes, with particular attention to small- and medium-scale tabular settings.

## 📊 Evaluation

Model performance is assessed using task-appropriate metrics for causal effect estimation and uplift modeling, including:
- **PEHE**
- **ATE error**
- **AUQC**
- standard classification or regression metrics where relevant for base-learner tuning

---

## 📂 Repository Structure

The repository is organized by experiment. Each experiment contains its own data and notebook to keep the workflow modular, transparent, and reproducible.
```
.
├── experiments/
│   ├── Experiment_Name/
│   │   ├── data/
│   │   │   ├── dataset_1.csv
│   │   │   ├── dataset_2.csv
│   │   │   └── ...
│   │   └── experiment.ipynb
├── README.md
```

### 📁 `data/`

Contains the datasets used in the corresponding experiment. Depending on the study, this may include raw input data, processed data, train/test splits, or semi-synthetic benchmark data.

### 📓 `experiment.ipynb`
Jupyter notebook containing the full experimental pipeline, including:
- Data preprocessing  
- Model implementation (S-, T-, X-, R-, DR-, Z-learners)  
- Evaluation (PEHE, ATE error, AUQC, )  
- Result visualization  
- Sensitivity analyses (if applicable)

This modular structure keeps experiments organized, reproducible, and easy to extend.
