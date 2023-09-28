# Digital-Comm-Lab-1

In this lab GNURadio was used in concert with an SDR to scan AM radio frequencies using a given recording. All files used in the lab can be found in the above folder.
## Flowchart
![image](https://github.com/blee0730/Digital-Comm-Lab-1/assets/130094173/156fd18f-3daf-4ef1-8300-4607a5aaaa07)
This is the start of the flowchart that captures the message and multiplies it with a carrier. In the actual flowgraph the three blocks shown on the left are done in the single SDR source block on the right.
### Low Pass Filter
![image](https://github.com/blee0730/Digital-Comm-Lab-1/assets/130094173/9398ec91-670e-41ed-a4cf-323f869a87b5)
Afterwards the new analog signal with the modulated message and carrier are put through a low pass filter.
### Demodulator
![image](https://github.com/blee0730/Digital-Comm-Lab-1/assets/130094173/0f6d6146-5212-4f67-99a2-b59eb62604a0)
Right after the low pass filter the signal is demodulated as shown on the right capturing only a single side (SSB).
### Transition Width
![image](https://github.com/blee0730/Digital-Comm-Lab-1/assets/130094173/e04079f2-5356-48f5-96f8-72292f31c853)
The transition width of the demodulator is smaller than that of the low pass filter to reduce the noise from the signal.
### Resampler
![image](https://github.com/blee0730/Digital-Comm-Lab-1/assets/130094173/2a309b5f-2f32-45f4-90c3-26f0d7c3d14b)
Finally the signal is resampled so that the sampling rate is compatable with the computer's. The signal is decimated and interpolated by the sampling rates of the computer (32) and the system (400).
### Output
(picture pending)
The output shows the audio in frequency and as a waterfall.

