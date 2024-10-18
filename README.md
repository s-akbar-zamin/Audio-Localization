# Audio Localization

This project was inspired by my friend Conner.

I did this project between research to develop my programming and machine learning skills. This project focused on classifying and localizing sounds in stereo audio by mimicking how humans differentiate sound direction through phase shift and amplitude. I converted raw audio data into mel spectrograms, which are interpretable images of sound. These audio channels were fed into a simple neural network to output direction and sound class. Keeping it simple allowed me to test and modify layers freely to see how they impacted prediction and make sense of what the model "sees"; all of this helped me improve my understanding and intuition surrounding neural networks.

# From theory to signal to data

I used Microsoft Paint to explain the project to another friend. I've shared the image here.

![Background](https://github.com/user-attachments/assets/36139fbf-a454-4165-b47f-20e3b8937f2b)

In summary:
  1. A person (left) can localize the source (left or right) of a sound depending on each ear's processing of amplitude and the difference in time they process the sound
  2. A continuous, audio waveform (middle top, in blue) is sampled at 48 kHz by our headset / audio device (red dots on blue waveform) to produce a waveform of discrete arbitrary values (red waveform with volume and 48,000 on the y and x-axis, respectively)
  3. This complex, audio waveform is composed of several different waveforms of a single frequency. It can be decomposed into these frequencies and plotted as a frequency distribution using short time fourier transforms
  4. This frequency distribution is a description of the sound at one instant. Performing this operation for a longer duration of time and plotting them together as an array, where higher values indicate more frequencies in the bin, produces an interpretable image of sound
  5. This image, or spectrogram, can be scaled appropriately to the human hearing scale
  6. This is done for both left and right audio channels

Below, I've included some mel spectrograms and a few comments justifying what is seen in the image.

https://github.com/user-attachments/assets/07d389ae-36c7-4fe0-833e-8894a287acc0

Vertical bars may represent noise or insignificant values compared to the hyperintense signal at the appropriate frequency

https://github.com/user-attachments/assets/9708f1f4-f8c3-4a03-9b11-1a87d49422fa

Vertical resolution is kept low to improve processing speed of model for use in real-time.

https://github.com/user-attachments/assets/2c9ce539-a231-4512-a4d0-ddffdac84116

Scattered, diffuse alternating color represent low, non-zero values due to normalization
