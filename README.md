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
│   ├── induction_head_identification.ipynb
│   ├── local_repetition_analysis.ipynb
│   ├── entropy_analysis.ipynb
│   └── activation_patching.ipynb
│
├── figures/
│   └── ...
│
├── paper/
│   └── paper.pdf
│
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

Run notebooks in the following order:

1. `induction_head_identification.ipynb`
2. `local_repetition_analysis.ipynb`
3. `entropy_analysis.ipynb`
4. `activation_patching.ipynb`

Google Colab was used for all experiments.

## Paper

The accompanying paper is available in:

```text
paper/paper.pdf
```

## License

MIT License
