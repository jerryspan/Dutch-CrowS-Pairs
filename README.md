## 📂 Repository Overview

This repository contains materials for the paper:  
**"Dutch CrowS-Pairs: Adapting a Challenge Dataset for Measuring Social Biases in Language Models for Dutch"**

---

## 📑 Contents

### 📁 Datasets

Located in the `datasets/` folder.

Includes versions of the CrowS-Pairs dataset in:
- **English**
- **French**
- **Dutch** (newly created)

Each version contains **1,463 sentence pairs** covering **9 bias categories**:
- Race/Color  
- Gender  
- Nationality  
- Socioeconomic Status  
- Religion  
- Age  
- Sexual Orientation  
- Physical Appearance  
- Disability

---

### 🧠 Model Evaluation Scripts

#### 🔹 `arlm_evaluation.py`
- Evaluates **autoregressive language models (ARLMs)**.
- Prompting was performed via **LM Studio**.
- Output results are located in the `results/` folder.

#### 🔹 `mlm_metric.py`
- Evaluates **masked language models (MLMs)**.
- Adapted from the original CrowS-Pairs study (Nangia et al., 2020).

**Usage:**
```bash
python mlm_metric.py \
    --input_file [crows_pairs_dataset] \
    --lm_model [mlm_name] \
    --output_file [output_filename]
