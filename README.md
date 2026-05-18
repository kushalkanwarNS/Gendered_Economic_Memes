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
Mail me for the password email id: kushalneo@gmail.com
```

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
source_root = "size_based_batches"

# Final merged folder
merged_folder = "merged_images"

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
