# Speaker Classification from Speech Recordings

This repository contains an example of how to create a model that classifies speakers based on the frequency domain representation of speech recordings, obtained via Fast Fourier Transform (FFT).

## Overview

This example demonstrates the following:

- Using `tf.data` to load, preprocess, and feed audio streams into a model.
- Creating a 1D convolutional network with residual connections for audio classification.

## Process

1. **Dataset Preparation:**
   - Collect a dataset of speech samples from different speakers, with the speaker as the label.
   - Add background noise to these samples to augment the data.

2. **Data Preprocessing:**
   - Resample noise samples to a sampling rate of 16,000 Hz using `ffmpeg`.
   - Convert speech samples to their frequency domain representation using FFT.

3. **Model Training:**
   - Train a 1D convolutional neural network (convnet) to predict the correct speaker given a noisy FFT speech sample.

## Notes

- This example requires TensorFlow 2.3 or higher, or `tf-nightly`.
- Ensure all noise samples are resampled to a sampling rate of 16,000 Hz before using the provided code. `ffmpeg` is required for resampling.

## Requirements

- TensorFlow 2.3 or higher
- `tf-nightly` (optional)
- `ffmpeg` for resampling audio

## Usage

1. **Install Dependencies:**
   ```bash
   pip install tensorflow
   sudo apt-get install ffmpeg
   ```

2. **Prepare Dataset:**
   - Collect and label speech samples.
   - Add background noise and resample to 16,000 Hz using `ffmpeg`.

3. **Run the Example:**
   ```python
   # Load, preprocess, and augment data
   # Create and train the 1D convnet model
   ```

4. **Evaluate the Model:**
   - Test the model with noisy FFT speech samples to classify speakers.

This repository provides a comprehensive guide to build a robust speaker classification model using the FFT of speech recordings and a 1D convolutional neural network.
