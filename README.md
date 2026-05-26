# The Effect of Induction Head Ablation on Repetition Dynamics in Large Language Models}

# Induction Heads and Local Repetition in GPT-2

This repository contains the code and experiments accompanying a mechanistic interpretability study investigating the role of induction heads in controlling local repetition behavior in transformer language models.

The project examines how induction head ablation affects repetition dynamics and entropy in GPT-2 models and validates causal mechanisms through activation patching.

## Main Results

- Global induction head ablation increases local repetition in GPT-2
- Local repetition effects are stronger than entropy effects
- Ablation effects are non-additive
- Induction head ablation exhibits non-linear behavior
- Activation patching provides causal evidence for the role of induction heads in repetition control with:

```text
Mean Recovery Rate ≈ 0.965 ± 0.15
```

- Primary findings generalize from GPT-2 Small to GPT-2 Medium

## Repository Structure

```text
.
├── notebooks/
│   ├── Ablated_Head_vs_LRR.ipynb
│   ├── Activation_Patching.ipynb
│   ├── GPT2Medium_Generalization.ipynb
│   ├── LRR_Entropy_Control_Trial.ipynb
│   └── LRR_post_ablation.ipynb
│
├── paper/
|   ├── Figure_1.png
│   ├── Figure_2.png
│   ├── Figure_3.png
│   ├── Figure_4.png
|   ├── Figure_5.png
│   ├── Figure_6.png
│   ├── main.tex
│   └── references.bib
│
├── paper.pdf
|
├── requirements.txt
│
└── README.md
```

## Models Used

Experiments were conducted on:

- GPT-2 Small
- GPT-2 Medium

using the TransformerLens framework.

## Running the Project

Install dependencies:

```bash
pip install -r requirements.txt
```


Google Colab was used for all experiments.

## Notebooks

- **`Ablated_Head_vs_LRR.ipynb`** – Analyzes the relationship between the number of ablated induction heads and changes in the Local Repetition Rate (LRR), investigating potential non-linear effects of progressive ablation.

- **`Activation_Patching.ipynb`** – Implements activation patching experiments to verify the causal contribution of induction heads by measuring recovery of model behavior after restoring patched activations.

- **`GPT2Medium_Generalization.ipynb`** – Extends the analysis to GPT-2 Medium to evaluate whether induction head behavior and repetition dynamics generalize across model scales.

- **`LRR_Entropy_Control_Trial.ipynb`** – Performs control experiments examining only the Local Repetition Rate (LRR) and includes additional analysis with entropy to further contextualize the results.

- **`LRR_post_ablation.ipynb`** – Measures final LRR changes due to ablation, summarizing the reported outcomes of induction head removal on repetition behavior across sequences.


## License

MIT License
