# Automatic Folk Music Generation

This project explores the use of deep learning to generate melodies inspired by selected folk music traditions of Assam, focusing on **Mising Oi Nitom and Bihu**. It also examines the melodic characteristics of the real and generated music through pitch, interval, and Hindustani thaat-level analysis.

## About the Project

The project uses a style-conditioned Bidirectional Long Short-Term Memory (BiLSTM) model to learn patterns from symbolic pitch and duration sequences. The trained model generates new melodies for the two folk styles, which are then compared with the original data using statistical and melodic features.

The work also investigates similarities between the pitch-class distributions of the folk melodies and the pitch sets associated with Hindustani thaats. These comparisons are intended to study broad melodic affinities rather than assign an exact raag identity.

## Main Components

* Symbolic pitch and duration sequence processing
* Style-conditioned BiLSTM model training and evaluation
* Autoregressive melody generation
* MIDI and WAV rendering of generated melodies
* Comparison of real and generated melody characteristics
* Pitch-class, interval, and thaat-level analysis

## Dataset

The experiments use 70 songs: 45 Mising Oi Nitom songs and 25 Bihu songs. The prepared dataset is divided into training, validation, and test sets and represents melodies using symbolic pitch and duration sequences.

The notebook uses prepared dataset files and model artifacts stored in Google Drive. The original audio recordings are not included in this repository. Please check the relevant permissions and source terms before redistributing any recordings or derived data.

## Results

On the held-out test set, the model achieved 30.08% next-pitch accuracy and 40.02% duration accuracy. The thaat-level pitch-affinity rankings of real and generated melodies showed Spearman correlations of 0.9394 for Mising Oi Nitom and 0.9515 for Bihu.

These results suggest that the generated melodies preserve some broad statistical and pitch-affinity characteristics of the selected folk styles, while differences in melodic movement and repetition remain.

## Running the Notebook

Open `Automatic_Folk_Music_Generation_Code.ipynb` in Google Colab. The notebook expects the prepared dataset, vocabulary, and any required model checkpoints to be available in the corresponding Google Drive folders. Update the file paths if your folder structure differs.

Install the required Python packages before running the cells. Some cells are experimental and may need to be run in sequence with the required files available.

## Technologies

Python, PyTorch, NumPy, Pandas, Librosa, Matplotlib, and MIDI/WAV rendering tools.

## Acknowledgement

This work was carried out as part of the IKS Internship Program 2026 at the National Institute of Technology Silchar.

