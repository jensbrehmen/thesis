# A Foundational Approach to Improve Causal Machine Learning and Uplift Modeling
This repository contains the implementation and experimental evaluation for the thesis _“A Foundational Approach to Improve Causal Machine Learning and Uplift Modeling.”_ The project studies **TabPFN** as a base learner within standard meta-learner frameworks for **conditional average treatment effect (CATE)** estimation and uplift modeling.

## 🎯 Experimental Scope

The experiments in this repository are organized to test **TabPFN as a base learner for causal meta-learners** under three complementary settings.

First, we evaluate the models on **semi-synthetic causal benchmarks** with known treatment effects, including datasets such as **IHDP-100**, **Twins**, **News**, and **ACIC2016**. These experiments allow direct assessment of how accurately each method recovers heterogeneous treatment effects.

Second, we evaluate the same methods on **real-world randomized controlled trial (RCT) data**, where treatment assignment is randomized but individual counterfactual outcomes are unobserved. In this setting, the focus shifts from direct error measurement to **treatment ranking and policy quality**, which is more relevant for practical uplift modeling.

Third, we conduct a **sensitivity analysis** to study robustness under challenging data conditions, including **treatment imbalance**, **weak overlap**, and **confounding**. This is intended to assess whether the relative performance of TabPFN-based meta-learners persists when the learning problem becomes less favorable.

Across these settings, the repository compares **TabPFN-based S-, T-, X-, R-, DR-, and Z-learners** against conventional baselines such as **linear models**, **LightGBM**, **Causal Forests**, and **CausalPFN**.

## 📊 Evaluation

Model performance is evaluated using metrics that match the data setting and the causal objective.

For **semi-synthetic benchmarks**, where ground-truth treatment effects are available, we evaluate:
- **root-PEHE**
- **ATE error**

For **real-world RCT experiments**, where the objective is treatment prioritization rather than direct recovery of unobserved individual effects, we evaluate:
- **AUQC**
- **Top-$k$\% policy gain**
- standard supervised metrics where relevant for base-model tuning

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
