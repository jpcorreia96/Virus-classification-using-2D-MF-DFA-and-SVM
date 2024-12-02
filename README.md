# Classification of Coronaviruses and SARS-CoV-2 Variants

This repository contains the code used to classify genomic sequences of coronaviruses and SARS-CoV-2 variants using **Chaos Game Representation (CGR)**, **2D Multifractal Detrended Fluctuation Analysis (2D MF-DFA)**, and **Support Vector Machine (SVM)**.

## Repository Structure

The repository is organized into three main directories, each representing a step in the analysis pipeline:

1. **`chaosGameRepresentation/`**: Contains the code for generating CGR representations of DNA sequences as images.
2. **`2dMFDFA/`**: Includes the code to compute fractal parameters from CGR images using 2D MF-DFA.
3. **`SVM/`**: Implements the Support Vector Machine (SVM) algorithm to classify the samples based on the computed fractal parameters.

## Step Descriptions

### Chaos Game Representation (CGR)

The code in the `chaos_game/` directory performs the following tasks:
- **Input**: A file containing DNA sequences in FASTA format.
- **Output**: CGR images representing DNA subsequences (k-mers).
- **Dependencies**: Python, `numpy`, `matplotlib`.

### 2D Multifractal Detrended Fluctuation Analysis (2D MF-DFA)

The code in the `2d_mf_dfa/` directory performs:
- **Input**: CGR images generated in the previous step.
- **Output**: Fractal parameters such as $\Delta h$, $\Delta \alpha$, $\alpha_{\min}$, among others.
- **Dependencies**: Python, `numpy`, `pandas`, `scipy`.

### Support Vector Machine (SVM)

The code in the `svm/` directory performs:
- **Input**: A file containing the fractal parameters calculated in the previous step.
- **Processing**: Classification of samples using cross-validation with `StratifiedKFold`.
- **Output**: Performance metrics such as average accuracy.
- **Dependencies**: Python, `pandas`, `scikit-learn`, `numpy`.

