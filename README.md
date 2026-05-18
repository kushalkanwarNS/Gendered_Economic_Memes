# Gendered Economic Memes Dataset

This repository contains the dataset resources associated with the paper:

**“Addressing Overcommitment in the Reasoning of Gendered Economic Memes under Multimodal Ambiguity”**  
Accepted at IJCAI 2026.

---

# Dataset Access

Due to the potentially sensitive and harmful nature of meme content included in this dataset, the images are distributed as password-protected compressed batches.

The dataset contains:
- Gendered economic memes
- Ambiguous multimodal content
- Harmful and stereotype-driven narratives
- Socially sensitive meme content

The dataset is released strictly for:
- Academic research
- Educational use
- Fairness and bias analysis
- Harmful content detection research
- Explainable and trustworthy AI research

---

# Download Structure

```text
protected_batches/
├── batch_1.zip
├── batch_2.zip
├── batch_3.zip
└── ...
```

Each ZIP file is password protected.

---

# Password

```
# Dataset Password Request

To obtain the password for accessing the dataset batches, please contact:

```
kushalneo@gmail.com
```

By requesting or using the dataset, you agree to the following conditions:

- The dataset will be used strictly for academic, educational, and non-commercial research purposes.
- The dataset will not be redistributed, re-uploaded, mirrored, or publicly shared in any form without explicit permission from the authors.
- The dataset will not be used to generate, promote, or disseminate harmful, hateful, abusive, or discriminatory content.
- Users must comply with institutional ethical guidelines, copyright regulations, and responsible AI research practices.
- The authors do not endorse any offensive, harmful, or stereotypical viewpoints present in the dataset.
- If requested by the authors or copyright holders, users agree to remove the dataset and any derived unauthorized redistributions.

By requesting the password, you acknowledge and agree to the above ethical usage and non-redistribution conditions.
---

# Reconstructing the Dataset

After downloading all ZIP files:

## Step 1: Extract all batches

Example:

```bash
unzip batch_1.zip
unzip batch_2.zip
...
```

---

## Step 2: Merge all extracted folders

Use the following Python script:

```python
import os
import shutil

# Folder containing extracted batch folders
source_root = "protected_batches"

# Final merged folder
merged_folder = "images"

# Create merged folder
os.makedirs(merged_folder, exist_ok=True)

# Traverse all batch folders
for batch_name in sorted(os.listdir(source_root)):

    batch_path = os.path.join(source_root, batch_name)

    if not os.path.isdir(batch_path):
        continue

    for file_name in os.listdir(batch_path):

        src_path = os.path.join(batch_path, file_name)
        dst_path = os.path.join(merged_folder, file_name)

        shutil.copy2(src_path, dst_path)

print("All batches merged successfully!")
```
---
## Step 3: Use `memes.csv` for Labels and Metadata

The file `memes.csv` contains the labels and associated metadata required for using the dataset.

After merging all image batches (name it as images), keep the dataset in the following structure:

```text
project/
├── images/
│   ├── image1.jpg
│   ├── image2.jpg
│   └── ...
│
├── memes.csv
└── README.md
```

The `memes.csv` file should be used to map each image to its corresponding label and other dataset-specific information.

Users should not modify the original `memes.csv` file unless required for preprocessing or experimental setup. Any preprocessing changes should be clearly documented for reproducibility.
---

# Ethical Usage Guidelines

By using this dataset, you agree to the following conditions:

1. The dataset must only be used for legitimate research and educational purposes.

2. The dataset must NOT be used for:
   - Harassment
   - Hate speech propagation
   - Targeted abuse
   - Discriminatory profiling
   - Offensive content generation
   - Commercial exploitation of harmful content

3. The dataset may contain:
   - Misogynistic memes
   - Offensive humor
   - Gender stereotypes
   - Sensitive social narratives
   - Ambiguous multimodal content

   These are included solely for scientific analysis and benchmarking.

4. The authors do not endorse any harmful, offensive, or stereotypical viewpoints represented in the dataset.

5. Users are responsible for complying with:
   - Institutional ethics policies
   - Copyright regulations
   - Fair use provisions
   - Responsible AI guidelines

6. If any copyright holder requests removal of specific content, reasonable efforts should be made to comply.

---

# Citation

If you use this dataset, please cite:

```bibtex
@inproceedings{kanwar2026gendered,
  title={Addressing Overcommitment in the Reasoning of Gendered Economic Memes under Multimodal Ambiguity},
  author={Kanwar, Kushal and Chauhan, Dushyant Singh and Rana, Kapil and Singh, Gopendra Vikram and Lukas, Nils},
  booktitle={International Joint Conference on Artificial Intelligence (IJCAI)},
  year={2026}
}
```

---

# Research Scope

This repository supports research in:
- Multimodal reasoning
- Harmful meme detection
- Explainable AI
- Bias-aware AI systems
- Context-sensitive multimodal understanding
- Epistemic uncertainty and abstention modeling

---

# Disclaimer

This repository may contain offensive or disturbing content.

Viewer discretion is advised.

The dataset is released exclusively for responsible research and educational purposes.
