# Automatic Folk Music Generation

Research project on style-conditioned generation and thaat-level analysis of selected folk music traditions of Assam, focusing on Mising Oi Nitom and Bihu.

## Current research workflow

The accompanying Colab notebook contains code for:

- Loading the prepared symbolic pitch-duration dataset and vocabulary
- Defining/loading and evaluating a style-conditioned BiLSTM
- Generating folk-style symbolic melodies autoregressively
- Rendering generated melodies to MIDI/WAV
- Comparing real and generated melody statistics
- Pitch-class, interval, and thaat-level pitch-affinity analysis

## Dataset and prerequisites

The notebook expects the prepared files to be available in Google Drive at:

`MyDrive/Automatic_Folk_Music_Generation/`

Expected data files include:

- `bilstm_data/train.npz`
- `bilstm_data/validation.npz`
- `bilstm_data/test.npz`
- `bilstm_data/vocabulary.json`

Model checkpoints and experiment outputs are expected under the `models/` directory. These files are not embedded in this source-code notebook.

**Scope note:** This repository notebook starts from an already prepared symbolic dataset. It does not, by itself, reproduce the full raw-audio collection and preprocessing process from the original recordings.

## How to use

1. Open `Automatic_Folk_Music_Generation_Code.ipynb` in Google Colab.
2. Place the expected dataset and model artifacts in the Google Drive folder shown above, or update the paths in the notebook.
3. Run the cells in the required order, checking dependencies and input files first.
4. Review the evaluation and analysis outputs before interpreting results.

The notebook includes exploratory and repeated diagnostic cells from the research workflow; it has not been fully refactored into a minimal, clean pipeline.

## Dataset and audio rights

The project concerns 70 songs used in the experiments (45 Mising Oi Nitom and 25 Bihu). Before publicly redistributing source audio, verify permission and licensing. Do not assume that publicly accessible YouTube recordings can be republished. Share only data and derived materials that you have the right to redistribute, with appropriate source attribution.

## Reported experimental results

The project notes report overall held-out next-event accuracy of 30.08% for pitch and 40.02% for duration. The reported Spearman correlations between real and generated thaat-level pitch-affinity rankings are 0.9394 for Mising Oi Nitom and 0.9515 for Bihu. These are broad pitch-affinity comparisons, not proof of exact raag classification.

## Status

This is a research-code release based on the Colab notebook. For full reproducibility, the prepared dataset, exact dependency versions, and any required model checkpoints must be made available separately and documented.
