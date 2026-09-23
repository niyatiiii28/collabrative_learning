# Collaborative Learning

A multimodal analysis project exploring collaborative learning through speech, eye gaze, facial emotion, and hand-movement features.

The repository contains Jupyter notebooks for preprocessing and analyzing interaction data, along with presentation and research materials. The notebooks combine behavioral and affective signals from participant pairs to create normalized feature representations, reduce dimensionality, and identify patterns in collaborative interaction.

## Repository contents

### Analysis notebooks

- [`Untitled59.ipynb`](Untitled59.ipynb) — Integrates speech, eye-gaze, emotion, and hand-movement features. The workflow standardizes numeric features, applies principal component analysis (PCA), and uses clustering-related analysis.
- [`eye_gaze.ipynb`](eye_gaze.ipynb) — Eye-gaze feature analysis.
- [`face-emotions (1).ipynb`](face-emotions%20(1).ipynb) — Facial emotion feature analysis.
- [`hand_movement.ipynb`](hand_movement.ipynb) — Hand-movement and object-interaction feature analysis.
- [`speech-2.ipynb`](speech-2.ipynb) — Speech feature processing and analysis.
- [`speech-eval (1).ipynb`](speech-eval%20(1).ipynb) — Speech evaluation experiments.

### Research and presentation materials

- [`collaborative learning.pdf`](collaborative%20learning.pdf)
- [`AIED_2026_T4E2026_collab_making (1).pdf`](AIED_2026_T4E2026_collab_making%20(1).pdf)
- [`Poster Presentation_final.pdf`](Poster%20Presentation_final.pdf)

### Data

- [`final_normalized_data_before_PCA.numbers`](final_normalized_data_before_PCA.numbers) — Normalized feature data prepared for downstream analysis.

> **Note:** Some notebooks refer to input files stored outside this repository, such as CSV and Excel files under `/content/`. You will need to provide those files locally and update the paths before running the notebooks.

## Analysis workflow

The combined-analysis notebook follows these general steps:

1. Load speech, eye-gaze, emotion, and hand-movement feature tables.
2. Standardize column names and merge tables using `pair_id`.
3. Select numeric features and apply standard scaling.
4. Use PCA to retain approximately 90% of the variance.
5. Explore pair-level interaction patterns using clustering and evaluation metrics.

The feature set includes conversational measures such as turn-taking, pauses, pitch, and energy; affective measures such as valence and arousal; gaze/attention measures; and hand-interaction measures such as interaction frequency, object switching, simultaneous touches, and workspace coverage.

## Requirements

The notebooks are written for Python 3 and use common data-science libraries, including:

- Jupyter Notebook or Google Colab
- pandas
- NumPy
- scikit-learn
- matplotlib/seaborn, where required by individual notebooks

A typical environment can be installed with:

```bash
pip install jupyter pandas numpy scikit-learn matplotlib seaborn openpyxl
```

## Getting started

1. Clone the repository:

   ```bash
   git clone https://github.com/niyatiiii28/collabrative_learning.git
   cd collabrative_learning
   ```

2. Open a notebook in Jupyter:

   ```bash
   jupyter notebook
   ```

   Alternatively, upload the notebooks to [Google Colab](https://colab.research.google.com/).

3. Add the required input datasets and update any `/content/` paths in the notebooks.
4. Run the notebook cells in order.

## Reproducibility notes

- Confirm that all source datasets use the expected `pair_id` values and column names.
- Keep the feature-preparation and normalization steps consistent when comparing experiments.
- The notebooks contain exploratory outputs from previous runs; rerunning them may produce different results depending on the input data and preprocessing choices.
- Raw participant data is not included in this repository unless explicitly provided in the repository files.

## Project status

This repository is an ongoing research and analysis workspace. The notebooks and supporting documents represent exploratory work on multimodal indicators of collaborative learning.

## License

No license has been specified for this repository. Unless a license is added, the contents should not be reused, modified, or redistributed without permission from the repository owner.
