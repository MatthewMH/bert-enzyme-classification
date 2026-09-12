# Implementation of Fine-Tuned BERT for Enzyme Classification Based on Gene Ontology

This directory contains the implementation and data used in the study:

**Implementation of Fine-Tuned BERT for Enzyme Classification Based on Gene Ontology**  
ICAICTA 2024.

The study investigates enzyme classification using Gene Ontology (GO)-derived text and a fine-tuned BERT model.

## Methodology

Gene Ontology annotation names and definitions are used as textual representations of enzyme function.

The text is encoded and classified using:

- `bert-base-uncased`
- Fine-tuning for enzyme classification
- Enzyme Commission (EC) labels as classification targets

The experiments evaluate the ability of BERT to learn enzyme-function representations from GO-derived textual information.

## Data

The dataset contains enzyme records associated with Gene Ontology annotations and corresponding Enzyme Commission labels.

GO names and definitions are concatenated into text inputs before being passed to the BERT classifier.

## Environment

Install the required dependencies from the repository root:

```bash
pip install -r ../requirements.txt
```

GPU acceleration is recommended for BERT fine-tuning.
