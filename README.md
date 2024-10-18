# Audio Localization

This project was inspired by my friend Conner.

I did this project between research to develop my programming and machine learning skills. This project focused on classifying and localizing sounds in stereo audio by mimicking how humans differentiate sound direction through phase shift and amplitude. I converted raw audio data into mel spectrograms, which are interpretable images of sound. These audio channels were fed into a simple neural network to output direction and sound class. Keeping it simple allowed me to test and modify layers freely to see how they impacted prediction and visualize what the model "sees" when making predictions (using GradCAM or Gradient-weighted Class Activation Mapping) - all of this helped me improve my understanding and intuition surrounding neural networks.

Below, I've included some mel spectrograms and a few comments justifying what is seen in the image.

https://github.com/user-attachments/assets/07d389ae-36c7-4fe0-833e-8894a287acc0

Vertical bars may represent noise or insignificant values compared to the hyperintense signal at the appropriate frequency

https://github.com/user-attachments/assets/9708f1f4-f8c3-4a03-9b11-1a87d49422fa

Vertical resolution is kept low to improve processing speed of model for use in real-time.

https://github.com/user-attachments/assets/2c9ce539-a231-4512-a4d0-ddffdac84116

Scattered, diffuse alternating color represent low, non-zero values due to normalization
