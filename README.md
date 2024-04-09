# DSP-sliding-dft
The Sliding Discrete Fourier Transform (SDFT) is a signal processing 
technique that allows for the real-time computation of the Discrete 
Fourier Transform (DFT) as a signal evolves over time. It is particularly 
useful in applications where there is a need for continuous monitoring 
and analysis of a changing signal, such as in audio processing, 
communication systems, and various other time-series data analysis 
tasks.



The traditional DFT computes the frequency components of an entire 
signal or a fixed-length window. In contrast, the Sliding DFT 
continuously updates the frequency representation of the signal as it 
moves through time. This is achieved by applying the DFT to 
overlapping windows of the signal, incrementally shifting the window 
through the signal samples.
