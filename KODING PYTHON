# Filter
import numpy as np
import matplotlib.pyplot as plt
from scipy.signal import butter, lfilter

#Data Sample
fs=100  #Sample in Hz
t=np.linspace(0,1,fs,endpoint=False)  #Array time
f1=5  #Frequency input
input_signal=np.sin(2*np.pi*f1*t)

#Lowpass code
cutoff_freq=5 #Frequency cutoff here
nyquist_freq =0.5*fs #Nyquist frequence
order=4
#Create the filter here
b,a=butter(order,cutoff_freq/nyquist_freq,btype='low')
#Apply the filter here
output_signal = lfilter(b,a,input_signal)

#Plot input and filtered signals
plt.figure(figsize=(10,6))
plt.subplot(2,2,1)
plt.plot(t, input_signal,'b-',label='Input Sinyal')
plt.xlabel('Waktu(s)')
plt.ylabel('Amplitudo')
plt.legend()

plt.subplot(2,2,2)
plt.plot(t,output_signal,'r-',label='Filtered Signal')
plt.xlabel('Waktu(s)')
plt.ylabel('Amplitudo')
