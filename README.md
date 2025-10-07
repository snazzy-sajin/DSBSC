# DSBSC


EX NO: 2	DSB-SC-AM MODULATOR AND DEMODULATOR

AIM:

To write a program to perform DSBSC modulation and demodulation using SCI LAB and study its spectral characteristics

EQUIPMENTS REQUIRED

•	Computer with i3 Processor
•	SCI LAB

Note: Keep all the switch faults in off position

Algorithm:

1.	Define Parameters:
•	Fs: Sampling frequency.
•	T: Duration of the signal.
•	Fc: Carrier frequency.
•	Fm: Frequency of the message signal.
•	Amplitude: Maximum amplitude of the message signal.
2.	Generate Signals:
•	Message Signal: A sinusoidal signal that will be modulated.
•	Carrier Signal: A high-frequency sinusoidal signal used for modulation.
3.	DSBSC Modulation:
•	Modulated Signal: Multiply the message signal by the carrier signal to produce the DSBSC signal.
4.	DSBSC Demodulation:
•	Multiplication: Multiply the modulated signal by the carrier signal to get the product of the message signal with itself (i.e., the original message signal plus high-frequency components).
•	Low-pass Filtering: Apply a Butterworth low-pass filter to remove the high- frequency components and recover the original message signal.
5.	Visualization:
Plot the message signal, carrier signal, DSBSC modulated signal, and the recovered signal after demodulation.
PROCEDURE

•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
 
•	Execute the code
•	If any Error, correct it in code and execute again
•	Verify the generated waveform using Tabulation and Model Waveform

Model Waveform

<img width="703" height="679" alt="image" src="https://github.com/user-attachments/assets/e7c7c7f8-ccf2-41ac-b1f3-325989941a6f" />

Program <br>
Am=6.6; <br>
fm=519; <br>
Ac=13.86; <br>
fc=5190;<br>
fs=519000;<br>
t=0:1/fs:2/fm;<br>
m=Am*cos(2*%pi*fm*t);<br>
subplot(3,1,1);<br>
plot(t,m);<br>
c=Ac*cos(2*%pi*fc*t);<br>
subplot(3,1,2);<br>
plot(t,c);<br>
s1 = (Ac + m).*cos(2*%pi*fc*t);<br>
s2 = (Ac - m).*cos(2*%pi*fc*t);<br>
S= s1 - s2;<br>
subplot(3,1,3);<br>
plot(t,S);<br>

Output Graph
<img width="1529" height="988" alt="image" src="https://github.com/user-attachments/assets/cb5876fe-21cb-4e0b-86c0-f6012a05f205" />


Tablular Column
![Exp - 2](https://github.com/user-attachments/assets/41e76a24-4b7c-4114-82f0-64e8590490eb)


Result

Thus the DSB-SC-AM Modulation and Demodulation is generated.

