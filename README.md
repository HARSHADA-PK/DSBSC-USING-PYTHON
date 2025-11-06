# DSBSC-USING-PYTHON

# Aim

To implement and analyze Double Sideband Suppressed Carrier (DSB-SC) modulation using Python's NumPy and Matplotlib libraries.

# Apparatus Required

Software: Python with NumPy and Matplotlib libraries
Hardware: Personal Computer

# Theory

Double Sideband Suppressed Carrier (DSB-SC) modulation is a type of amplitude modulation in which the carrier is suppressed, and only the two sidebands containing the information are transmitted. The DSB-SC signal is produced by multiplying the message signal with the carrier signal.The general equation of a DSB-SC signal is:

# Algorithm

1.Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and amplitudes.

2.Generate Time Axis: Create a time vector for the signal duration.

3.Generate Message Signal: Define the message signal as a cosine wave.

4.Generate Carrier Signal: Define the carrier signal as a high-frequency cosine wave.

5.Generate DSB-SC Signal: Multiply the message signal and carrier signal to obtain the modulated signal.

6.Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and DSB-SC modulated signal.

# PROGRAM:
```
import numpy as np
import matplotlib.pyplot as plt
Am=2.4
Ac=4.8
fm=218
fc=2180
fs=21800
t=np.arange(0,2/fm,1/fs)
m=Am*np.cos(2*np.pi*fm*t)
c=Ac*np.cos(2*np.pi*fc*t)
s1=(Ac+m)*np.cos(2*np.pi*fc*t)
s2=(Ac-m)*np.cos(2*np.pi*fc*t)
s=s1-s2
plt.subplot(3,1,1)
plt.plot(t,m)
plt.subplot(3,1,2)
plt.plot(t,c)
plt.subplot(3,1,3)
plt.plot(t,s)

```

# OUTPUT WAVEFORM:

<img width="782" height="540" alt="image" src="https://github.com/user-attachments/assets/0d54d405-482e-44e6-9ef2-862c0c802c69" />

# TABULAR COLUMN:

![WhatsApp Image 2025-11-06 at 10 52 57_f3941fc2](https://github.com/user-attachments/assets/a4b3c31b-4f6b-415b-bfb0-d5bff9065d41)

# RESULT:

The message signal, carrier signal, and DSB-SC modulated signal were successfully generated and displayed.The DSB-SC modulated waveform shows sidebands representing the frequency components of the message signal.

