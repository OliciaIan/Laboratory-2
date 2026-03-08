<details>
<summary>Experiment 9: FM Modulation</summary>

Content for experiment 9 goes here.

- Introduction
- Circuit diagram(refer to the file)
- Circuit Set Up(refer to the file)
- Results(refer to the file)
- File(https://github.com/OliciaIan/Laboratory-2/blob/main/Experiment%209.pdf)
- Conclusion

Introduction:
Frequency Modulation (FM)


Frequency Modulation (FM) is a type of analog modulation technique in which the **frequency of a carrier signal is varied according to the amplitude of the message (modulating) signal**, while the amplitude of the carrier remains constant. FM is widely used in communication systems because of its strong resistance to noise and signal interference.

In an FM system, a high-frequency carrier wave is combined with a low-frequency information signal such as voice or music. The instantaneous frequency of the carrier changes in proportion to the instantaneous amplitude of the modulating signal. This allows the original information to be transmitted over long distances through radio frequency channels.

FM is commonly used in radio broadcasting, television sound transmission, and two-way radio communication systems. Compared to Amplitude Modulation (AM), FM provides better sound quality and higher immunity to electrical noise, making it suitable for high-fidelity audio applications.

The main parameters used to describe frequency modulation include **carrier frequency, frequency deviation, modulating frequency, and modulation index**. These parameters determine how much the carrier frequency varies in response to the input signal.

In this experiment, the principles of frequency modulation are studied by generating an FM signal using a telecommunications trainer system and observing the resulting waveform using measurement instruments such as an oscilloscope.

Conclusion:

The Emona telecommunications trainer was used in this experiment to study the idea and workings of frequency modulation (FM). The experiment showed how a carrier signal's frequency varies in response to the input modulating signal's amplitude while the carrier amplitude stays constant.

It was verified that the carrier's instantaneous frequency fluctuates proportionately to the message signal by looking at the circuit configuration and output waveforms. The experiment also demonstrated the impact of varying modulating signal amplitudes on the FM signal's frequency deviation.

The underpinnings of frequency modulation were confirmed by the circuit and oscilloscope measurements. The creation of FM signals and their properties in real-world communication systems were better understood thanks to this experiment.

</details>

<details>
<summary>Experiment 10: FM Modulation</summary>

Content for experiment 10 goes here.

- Introduction
- Circuit diagram(refer to the file)
- Circuit Set Up(refer to the file)
- Results(refer to the file)
- File()
- Conclusion

Introduction:
FM Demodulation (Using an Emona Kit)

Frequency Modulation (FM) is a technique in communication systems where the frequency of a carrier signal varies according to the amplitude of the input (message) signal, while the carrier amplitude remains constant. FM is widely used in radio broadcasting, wireless communications, and audio transmission because it offers better noise immunity and higher sound quality compared to amplitude modulation (AM).

FM demodulation is the process of recovering the original message signal from the frequency-modulated carrier wave. In other words, it converts the frequency variations of the FM signal back into the corresponding voltage or amplitude variations of the original information signal (such as voice or music).

In laboratory experiments, the Emona Telecommunications Trainer 101 (Emona Telecoms‑Trainer 101) is commonly used to demonstrate FM communication systems. This training kit allows students to generate, modulate, and demodulate signals using modular blocks.

Conclusion:
The FM demodulation experiment using the Emona Trainer 101 demonstrates how a frequency-modulated signal can be successfully converted back into its original message signal. The experiment shows that by using circuits such as frequency discriminator, the frequency variations of the FM carrier can be detected and transformed into amplitude variations corresponding to the original information signal.

</details>

<details>
<summary>Experiment 11: Sampling and Reconstruction</summary>

## Introduction
Digital transmission is rapidly replacing analog systems due to its superior resistance to electrical noise interference. Before an analog signal, such as speech or music, can be transmitted digitally, it must be converted through a process called **sampling**.

Sampling involves measuring the analog signal's voltage at regular intervals. This experiment explores **natural sampling**, where the voltage can change during the measurement period, and **sample-and-hold schemes**, where the voltage is fixed at the instant of measurement.

Reconstructing the original message from these samples is achieved by passing the sampled signal through a **low-pass filter**.

## Objectives
- Sample a message using **natural sampling** and a **sample-and-hold scheme**
- Reconstruct the message from the sampled signal
- Examine the effects of **aliasing**

## Materials Used
- Emona Telecoms-Trainer 101 (plus power-pack)
- Dual-channel 20MHz oscilloscope
- Two Emona Telecoms-Trainer 101 oscilloscope leads
- Assorted Emona Telecoms-Trainer 101 patch leads

## Procedures

### Part A: Sampling a Simple Message
1. Gather the required equipment.
2. Connect the setup using the **Dual Analog Switch module** to sample the **2kHz SINE output** from the Master Signals module, controlled by the **8kHz DIGITAL output**.
3. Set the oscilloscope:
   - Trigger Source: **CH1**
   - Mode: **CH1**
4. Adjust the **Timebase** to view approximately two cycles of the **2kHz sine wave**.
5. Set the scope to **DUAL mode** to view both the original message and the sampled output.
6. Adjust **Vertical Attenuation** as needed and draw the two waveforms to scale.
7. Modify the setup to substitute the switch for a **sample-and-hold circuit** using the Dual Analog Switch module.
8. Draw the new sampled message to scale.

### Part B: Sampling Speech
1. Disconnect the **Master Signals module**.
2. Connect the **Speech module output**.
3. Set the scope **Timebase to 2ms/div**.
4. Observe the sampled signal while **talking, singing, or humming** into the microphone.

### Part C: Reconstructing a Sampled Message
1. Return the scope **Timebase to 0.1ms/div**.
2. Set the **Tuneable Low-pass Filter gain** to the middle.
3. Turn the **cut-off frequency fully anti-clockwise**.
4. Connect the sampled message to the filter input.
5. Slowly turn the **cut-off frequency clockwise** until the original message signal is reconstructed.

### Part D: Aliasing
1. Connect the **VCO module** (set to **"Lo" range**) to provide a variable sampling frequency.
2. Slowly reduce the **VCO frequency** while observing distortion in the reconstructed signal.
3. Increase the frequency until distortion disappears.
4. Measure the sampling signal's **period** to calculate the **actual minimum sampling frequency**.

## Answers to Questions

**Question 1:** What type of sampling is this an example of?  
**Answer:** Natural sampling.

**Question 2:** What two features confirm this?  
- The tops of the samples follow the shape of the message signal.  
- The signal only exists during the **high periods** of the sampling pulse.

**Question 3:** What features confirm the sample-and-hold scheme?  
- The tops of the samples are **flat**.  
- The sampled voltage is **held until the next sampling instant**.

**Question 4:** What distortion appears when the VCO frequency is reduced enough?  
**Answer:** Aliasing.

**Question 5:** What is the theoretical minimum sampling frequency for a 2kHz message?  
**Answer:** **4kHz** (Nyquist rate).

**Question 6:** Why is the actual minimum sampling frequency higher than the theoretical value?  
**Answer:** Because practical filters are not ideal; their rejection of higher frequencies is gradual.

## Overall Conclusion
This experiment demonstrates that analog signals can be converted into digital samples using **natural sampling or sample-and-hold methods**. The original signal can be reconstructed using a **low-pass filter**, provided the sampling rate meets the **Nyquist criterion**. If the sampling rate is too low, **aliasing distortion** occurs.

</details>

---

<details>
<summary>Experiment 12: PCM Encoding</summary>

## Introduction
**Pulse Code Modulation (PCM)** converts analog signals into a **serial stream of binary digits (0s and 1s)**.

The process involves:
1. Sampling the signal
2. Quantizing the samples
3. Encoding them into binary numbers

The **Emona PCM Encoder** uses an **8-bit system**, providing **256 quantization levels** for voltages between **-2V and +2V**.

Because most samples do not perfectly match a quantization level, **quantization error** occurs.

## Objectives
- Convert fixed and variable **DC voltages** to PCM
- Convert a **continuously changing signal** to PCM
- Investigate **quantization error**

## Materials Used
- Emona Telecoms-Trainer 101 (plus power-pack)
- Dual-channel 20MHz oscilloscope
- Emona Telecoms-Trainer 101 patch leads
- Oscilloscope leads

## Procedures
1. Set up the **PCM Encoder module** on the Emona Telecoms-Trainer 101.
2. Input a **fixed DC voltage** and observe the **8-bit binary output** on the oscilloscope.
3. Use the **Frame Synchronisation (FS)** signal to trigger the scope so the **8-bit frame** can be seen.
4. Verify that the **most significant bit (bit-7)** is transmitted first.
5. Input a **variable DC voltage** and observe the binary changes when quantization levels are crossed.
6. Input a **continuously changing analog signal** to observe **real-time PCM encoding**.

## Answers to Questions

**Question 1:** What is the purpose of the Frame Synchronisation (FS) signal?  
**Answer:**  
It indicates the **start of each 8-bit data frame** and aligns the receiver or oscilloscope with the transmitted bits.

**Question 2:** How many quantization levels exist in an 8-bit PCM system?  
**Answer:**  
256 levels (2⁸).

**Question 3:** What happens to quantization error if the number of bits increases?  
**Answer:**  
Increasing the number of bits increases quantization levels and **reduces quantization error**.

## Overall Conclusion
The experiment demonstrates the **PCM encoding process**, converting analog signals into **digital binary data**. It also shows that **quantization error is unavoidable**, but increasing the **bit depth** improves signal accuracy.

</details>
