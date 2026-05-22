This is the anonymous GitHub repository for the paper **"LeNS: "**, prepared for double-blind review. 

This repository contains the dataset subsets used in our evaluation and the codebase for the LeNS framework implementation, specifically focusing on the SARA dataset (both classification and regression tasks), as well as corresponding ablation studies.

## 📂 Repository Structure

The repository is organized into two main directories: `Datasets` and `Abductive_LR_for_SARA` (Code).

### 1. Datasets
Contains the datasets used to evaluate the LeNS framework: **SARA**, **LawBench**, **LawShift**, and **COLIEE**.

```text
Datasets/
├── COLIEE2025/
│   └── coliee_subset.json          # Subset data for COLIEE 2025
├── LawBench/
│   └── data/
│       └── LawBench_subset.json    # Subset data for LawBench
├── LawShift/
│   ├── term_down/
│   │   ├── original_all.json       # Original down-shift terms
│   │   └── poisoned_all.json       # Poisoned down-shift terms
│   └── term_up/
│       ├── original_all.json       # Original up-shift terms
│       └── poisoned_all.json       # Poisoned up-shift terms
└── Sara_v3/
    ├── Classification.json         # SARA Dataset for classification task (SARA_s)
    └── Tax.json                    # SARA Dataset for regression task (SARA_tax)


2. Code (Abductive_LR_for_SARA)
Contains the Python scripts to run the LeNS framework and reproduce our experiments across various LLMs (DeepSeek-V32, Gemini-3-Flash, GPT-5.4-mini, O4-mini).

Abductive_LR_for_SARA/
├── Ablation_SARA_s/                        # Ablation study scripts for SARA classification
│   ├── DeepSeek_V32_for_S...without_abstraction.py
│   ├── DeepSeek_V32_for_S...without_coherence.py
│   ├── Gemini3_flash_for_S...without_abstraction.py
│   └── Gemini3_flash_for_S...without_coherence.py
│
├── SARA_s/                                 # LeNS framework for SARA Classification Task
│   ├── DeepSeek_V32_for_SARA.py
│   ├── Gemini3_flash_for_SARA.py
│   ├── GPT5.4_mini_for_SARA.py
│   ├── O4_mini_for_SARA.py
│   └── Evaluate_results_SARA.py            # Evaluation script for classification outputs
│
└── SARA_tax/                               # LeNS framework for SARA Regression Task (Tax)
    ├── DeepSeek_V32_for_SARA_tax.py
    ├── Gemini3_flash_for_SARA_tax.py
    ├── GPT5.4_mini_for_SARA_tax.py
    ├── O4_mini_for_SARA_tax.py
    └── Evaluate_results_tax.py             # Evaluation script for regression outputs
