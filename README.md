# Transfer-learning-for-Music-Emotion-Prediction
## Music Preprocessing
### Mel-spectrogram (Input for 2D CNN)
  * Audio data is very high-dimensional and comes from a mixture of frequencies.
#### Step 1. Windowing (framing)
  * Audio is sequential and time dependent.
  * Dividing the signal into very short sections that allow time-invariant assumptions.
![image](https://user-images.githubusercontent.com/67357059/123906225-bb9b8300-d9ae-11eb-8b09-5d04c4f87537.png)
#### Step 2. Short Time Fourier Transform
 * Fourier Transfrom
   * It translates the waveform from time domain to frequency domain.
   * It can represent the sum of different frequencies.
   * The problem is It disappears time domain.
![image](https://user-images.githubusercontent.com/67357059/123907642-39608e00-d9b1-11eb-82ac-b21234fead44.png)
 * STFT is a method for saving the time domain.
 * Stacking each frame by taking Fourier transforms for each frame cut earlier.
![image](https://user-images.githubusercontent.com/67357059/123907730-56955c80-d9b1-11eb-91eb-318f48fc7688.png)
#### Step 3. Mel Filter Bank
 * Human hearing is less sensitive to frequencies above 1000 Hz.
 * Converting linearly up to 1000 Hz, and then multiplying it by making a Melscale filter.
![image](https://user-images.githubusercontent.com/67357059/123907918-9bb98e80-d9b1-11eb-92a1-1b236a524b34.png)
#### Step 4. Mel spectrogram
 * Apply a Mel-filter bank to the spectrogram
 * The average amplitude values of the mel-frequency interval per unit time are input for 2D CNN.
![image](https://user-images.githubusercontent.com/67357059/123908006-c4da1f00-d9b1-11eb-9a54-5126d83642da.png)








