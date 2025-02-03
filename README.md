## Custom classes and functions to analyze analogic data from photosensors

Read_Data, Filter_Data and Analyze_Data are three classes that contains a whole set of functions I used to use to analyze a whole kind of analogic data with a fixed set of formats.
Functions.py contains another set of functions to analyze and plot data.
Other files are example notebooks that use these functions contained in the files cited above with custom quantities to plot useful histogram required for APC and DUNE team meeting.

#### Test-bench equipment
The data acquisition (DAQ) is done with CAEN Digitizer DT5730SB (2 Vpp, 14 bits, 500 MSamples/s), specially customized for the DAQ in the Coldbox at CERN, the test-bench was composed by the digitizer, 
an LED pulser, Silicon-PhotoMultipiers (SiPMs), custom electronic boards, ecroy WaveRunner 625Zi oscilloscope and a dual chamber vacuum cryostat with a capability of ∼85 litres.
<img width="354" alt="image" src="https://github.com/user-attachments/assets/c24a019d-1846-4758-bcc7-d0139199e50f" />

#### Brief explanation of the tests
The prototypes of custom electronic boards, which was our objective to characterize (SNR etc.), capture the differential signals coming from the SiPMs, unify them in a single positive signal, 
amplify it and transforming it into a light signal carried out the cryostat by optical fibers (already characterized) inside the digitizer which recontruct the signal, already amplified, of the photons emitted by the pulser.
Since there were suspects of leakage of photons inside the cryostat, random triggers tests were conducted in order to understand the source of light leakage, 
which source was then confirmed to be optical fibers (then black coated from that moment on). My contributions are a full library of functions to help detect random peaks (determined then to be light peaks) and various manual hardware test
to modify the configuration of the test-bench in order to exclude hypothesis, fundamental over the final determination of the leakage source.
More details can be found in my master thesis uploaded on my (LinkedIn profile)[https://www.linkedin.com/-davide-moretti].

#### Various plots
Here below I attach some plots that are made through all the classes and functions contained in this repository.

Charge histogram (fit):
<img width="440" alt="image" src="https://github.com/user-attachments/assets/19866b58-2127-490f-b846-893f5248441e" />


Waveforms 3D plot and recontruction of the mean waveform:
<img width="604" alt="image" src="https://github.com/user-attachments/assets/21c0a5ba-014e-43f8-9ef9-72aa29986337" />


Example of LED waveform:
<img width="607" alt="image" src="https://github.com/user-attachments/assets/2d064890-29e8-4ff4-aaa9-fb11fe4935c9" />


Random trigger waveform and peaks detection:
<img width="705" alt="image" src="https://github.com/user-attachments/assets/3faf8853-4c80-4de3-b5f7-9b4311236242" />



