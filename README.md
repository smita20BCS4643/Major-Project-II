# Design and Implementation of a Real-Time ECG Monitoring System using Diligent analog Discovery Board and LabVIEW (Major-Project-II)
Final Year Project
## 
This Project is a cost-effective and accessible DIY Electrocardiogram (ECG) system using the Analog Discovery Studio and
LabVIEW. The ECG signal, representing the heart’s electrical activity, is amplified through external circuitry and processed in LabVIEW via WaveForms Virtual Instruments (VIs).
These VIs enable filtering, peak detection, and heart rate calculation. The system offers a
customizable solution for ECG acquisition, processing, and analysis, promoting hands-on
learning and experimentation in biomedical instrumentation and signal processing. This
project highlights the potential of utilizing accessible hardware and software tools for
practical healthcare technology applications

## INTRODUCTION 

### Problem Statement 
Develop a cost-effective and portable DIY ECG (Electrocardiogram) system using readily available
components and open-source software, addressing the lack of accessible and affordable
ECG monitoring solutions, particularly in resource-constrained settings or remote
areas

## Hardware Implementation

1. **Operational Amplifier Circuit**:
   - Connect the non-inverting input (+) of one op-amp in the LM324 quad op-amp package to ground using a 100kΩ resistor.
   - Connect the inverting input (-) of the same op-amp to the output through a 10kΩ resistor, forming a non-inverting amplifier configuration.
   - Connect the output of this op-amp to the non-inverting input (+) of another op-amp in the LM324 package.
   - Connect the inverting input (-) of the second op-amp to ground using a 100kΩ resistor.
   - Connect the output of the second op-amp to the inverting input (-) through a 10kΩ resistor, forming an inverting amplifier configuration.

2. **Filtering**:
   - Connect the output of the second op-amp to the positive terminal of the 1μF electrolytic capacitor.
   - Connect the negative terminal of the 1μF electrolytic capacitor to ground.
   - Connect the positive terminal of the 0.1μF ceramic capacitor (104M) to the output of the second op-amp.
   - Connect the negative terminal of the 0.1μF ceramic capacitor to ground.

3. **ECG Signal Acquisition**:
   - Connect one of the DIN ECG snap leads or alligator clips to the non-inverting input (+) of the first op-amp in the LM324 package.
   - Connect the other two DIN ECG snap leads or alligator clips to the right arm and left leg surface electrodes or pennies (use lotion if using pennies).

4. **Power Supply**:
   - Connect the positive voltage hub (V+) to the positive power supply terminal of the LM324 quad op-amp package.
   - Connect the negative voltage hub (V-) to the negative power supply terminal of the LM324 quad op-amp package.

5. **Analog Discovery Connections**:
   - Connect the orange wire with a white stripe (Scope Ch. 1 negative) to the ground of the Analog Discovery.
   - Connect the orange wire (Scope Ch. 1 positive) to the output of the second op-amp, which is the voltage output of the circuit.
   - Connect the white wire (V-) to the negative voltage hub.
   - Connect the red wire (V+) to the positive voltage hub.

6. **Diode Protection**:
   - Connect the anode (positive terminal) of one diode to the non-inverting input (+) of the first op-amp in the LM324 package, where the ECG signal from the right arm electrode is connected.
   - Connect the cathode (negative terminal) of the same diode to ground.
   - Connect the anode of another diode to the non-inverting input (+) of the first op-amp, where the ECG signal from the left leg electrode is connected.
   - Connect the cathode of this diode to ground.



## Flowchart

![pfinalroject io drawio](https://github.com/smita20BCS4643/Major-Project-II/assets/101444257/dd866266-3352-423c-8c09-13f806520cc7)

## Circuit Design
![circuit diagram](https://github.com/smita20BCS4643/Major-Project-II/assets/101444257/0cef59b1-d634-4b63-b2a6-eb003abc6e7d)


## Electrode Placement

![Picture1t - Copy](https://github.com/smita20BCS4643/Major-Project-II/assets/101444257/7ae32f19-f21d-4ff2-901e-ff32a1315d0c)

## LabVIEW Program

<img width="607" alt="circuitdaigrambackend" src="https://github.com/smita20BCS4643/Major-Project-II/assets/101444257/447c806e-d70b-4dbc-91b2-ea2c7f9101af">

### Initialiazation Block
![initial](https://github.com/smita20BCS4643/Major-Project-II/assets/101444257/33d7cd42-72a3-473a-a08c-2971045c8ef8)

### Enabling All Outputs

![Enabling all outputs](https://github.com/smita20BCS4643/Major-Project-II/assets/101444257/3743c1b1-9d6d-46ea-bf94-b086c7b947d1)

### Closing Block
<img width="682" alt="close" src="https://github.com/smita20BCS4643/Major-Project-II/assets/101444257/d8bf5f3e-29a7-4f56-b55c-e6391dac5316">


## Hardware Setup
![circuit](https://github.com/smita20BCS4643/Major-Project-II/assets/101444257/c734e781-5cfc-43c6-9cda-eade8f1437e1)

## Result / Output

![result](https://github.com/smita20BCS4643/Major-Project-II/assets/101444257/df6240e9-3eff-40c9-979d-ab8eadd9fc7f)




