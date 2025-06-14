# HMM-based-Named-Entity-Recognition-for-Biomedical-Text

# Medical Named Entity Recognition using Hidden Markov Models

## Project Overview
This project implements a Hidden Markov Model (HMM) for identifying medical entities in text, specifically focusing on:
- Diseases (labeled as 'D')
- Treatments (labeled as 'T')
- Other text (labeled as 'O')

The system combines statistical machine learning with rule-based enhancements to improve recognition of medical terms.

## Key Features
- **Hybrid HMM Approach**: Combines probabilistic modeling with dictionary-based rules
- **Unknown Word Handling**: Uses POS tagging and medical dictionaries for better generalization
- **Evaluation Framework**: Includes precision, recall, and F1-score metrics
- **Medical Domain Focus**: Pre-configured with common treatment terms (e.g., ibuprofen, antibiotics)

## Dataset
The model is trained on the `ner.txt` dataset from IIT Delhi's CSL772 course, containing annotated medical text with:
- One word per line followed by its label
- Sentences separated by blank lines
- Three label types: D (Disease), T (Treatment), O (Other)

## Implementation Details

### Model Architecture
1. **HMM Core**:
   - Trained using NLTK's HMM implementation
   - Lidstone smoothing (γ=0.1) for probability estimation
   - Learns transition and emission probabilities

2. **Enhancements**:
   - Predefined treatment dictionary
   - POS-based fallback for unknown words
   - Context-sensitive rules

### Performance
The model achieves:
- **Precision**: 0.7647
- **Recall**: 0.7554
- **F1-score**: 0.7284


## How to Use

### Requirements
- Python 3.6+
- NLTK
- NumPy
- scikit-learn

### Installation
1. Install dependencies:
```bash
pip install nltk numpy scikit-learn
python -m nltk.downloader punkt averaged_perceptron_tagger
