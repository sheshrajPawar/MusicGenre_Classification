# Music Genre Classification using K-Nearest Neighbors

## Overview

This project focuses on automatically classifying musical genres from audio files based on their low-level frequency and time-domain features. We use the K-nearest neighbors (KNN) algorithm for classification, leveraging Mel Frequency Cepstral Coefficients (MFCC) as our feature extraction method.

The dataset used is the **GTZAN genre classification dataset**, which consists of 1000 audio tracks of 30-second duration each, categorized into 10 genres: Blues, Classical, Country, Disco, Hiphop, Jazz, Metal, Pop, Reggae, and Rock. Each genre contains 100 tracks.

## Key Features
- **Algorithm**: K-nearest neighbors (KNN)
- **Dataset**: GTZAN Genre Classification Dataset
- **Audio Features**: Mel Frequency Cepstral Coefficients (MFCC)
- **Genres**: 10 music genres (Blues, Classical, Country, Disco, Hiphop, Jazz, Metal, Pop, Reggae, Rock)
  
## Project Approach

### Feature Extraction: Mel Frequency Cepstral Coefficients (MFCC)
MFCCs are widely used in audio and speech processing. They help in identifying the core linguistic content of an audio signal while discarding background noise. The key steps for feature extraction using MFCC are:
1. Divide audio signals into smaller frames (20-40 ms).
2. Identify different frequencies present in each frame.
3. Separate linguistic frequencies from noise.
4. Apply Discrete Cosine Transform (DCT) to focus on high-probability information sequences and discard noise.

### Classification Approach
- The K-nearest neighbors (KNN) algorithm classifies data points based on their similarity to others. By computing the distance between audio features (MFCCs), it identifies the genre of a track.
- KNN has proven effective for music genre classification tasks in various research studies.

## Requirements
- Python 3.x
- NumPy
- SciPy
- Python Speech Features (`python_speech_features`)
- Scikit-learn
- GTZAN Dataset (can be downloaded from [Marsyas website](http://marsyas.info/downloads/datasets.html))

## Usage

1. **Install Dependencies**:
   ```
   pip install numpy scipy python_speech_features scikit-learn
   ```
2. **Download the Dataset**: Download the GTZAN dataset and place the files in the appropriate directory.

3. **Run the Classifier**:
   ```python
   python music_genre_classifier.py
   ```

4. **Testing with New Audio Files**:
   You can also test the classifier with new audio files using the provided functions.

## Results
The model predicts the genre of a given audio file with the help of the K-nearest neighbors algorithm based on extracted MFCC features.


