# Improving BioBERT Performance in Multi-Level Enzyme Classification

This directory contains the implementation and data used in the study:

**Improving BioBERT Performance in Multi-Level Enzyme Classification**  
ISITIA 2025.

The study extends enzyme classification to all four levels of the Enzyme Commission hierarchy using BioBERT and multi-task classification.

## Methodology

Gene Ontology annotation names and definitions are concatenated into textual inputs and encoded using BioBERT.

A shared BioBERT encoder is connected to four independent linear classification heads for:

- EC main class
- EC subclass
- EC sub-subclass
- EC serial number

The experiments compare:

- Cross-entropy loss
- Focal loss with `gamma = 2` and `alpha = 0.25`

The enzyme data are separated into:

- IEA — electronically inferred annotations
- NONIEA — manually curated annotations

Model performance is evaluated using per-level classification metrics and hierarchical accuracy.

Prediction confidence is also analyzed for correctly classified enzyme sequences.

## Data

The datasets are derived from Swiss-Prot enzyme records and Gene Ontology annotations.

GO annotation names and definitions are concatenated into text inputs, while the corresponding four-level EC hierarchy is used as the classification target.

## Environment

Install the required dependencies from the repository root:

```bash
pip install -r ../requirements.txt
```

GPU acceleration is strongly recommended for BioBERT fine-tuning.
