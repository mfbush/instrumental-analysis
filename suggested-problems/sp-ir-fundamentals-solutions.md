# Solutions to Suggested Problems: Fundamentals of Infrared Spectroscopy
*Prof. Matthew F. Bush, University of Washington*

## Question 1: Michelson Interferometer and Signal Modulation

**a) Calculate the frequency (in Hz) of infrared radiation at 1720 cm⁻¹**

The relationship between wavenumber ($\tilde{\nu}$) and frequency ($\nu$) is:

$$\nu = c \cdot \tilde{\nu}$$

where $c$ is the speed of light and $\tilde{\nu}$ is the wavenumber.

Substituting values:
$$\nu = (3.0 \times 10^{10} \text{ cm/s}) \times (1720 \text{ cm}^{-1})$$

$$\nu = 5.16 \times 10^{13} \text{ Hz}$$

**Answer: $5.16 \times 10^{13}$ Hz** (or $5.2 \times 10^{13}$ Hz with appropriate sig figs)

---

**b) Calculate the modulated frequency in the interferogram**

Using the given relationship:
$$f_{\text{mod}} = \frac{2\nu v}{c}$$

Substituting values:
$$f_{\text{mod}} = \frac{2 \times (5.16 \times 10^{13} \text{ Hz}) \times (0.25 \text{ cm/s})}{3.0 \times 10^{10} \text{ cm/s}}$$

$$f_{\text{mod}} = \frac{2.58 \times 10^{13}}{3.0 \times 10^{10}} \text{ Hz}$$

$$f_{\text{mod}} = 860 \text{ Hz}$$

**Answer: 860 Hz** (or 8.6 × 10² Hz)

**Note:** The factor of 2 arises because the optical path difference changes by twice the mirror displacement (the beam makes a round trip to the moving mirror).

---

**c) Explain how the Michelson interferometer creates the interference pattern**

**Sample Answer:**

The Michelson interferometer splits the incoming IR beam into two paths using a beamsplitter. One beam travels to a fixed mirror while the other travels to a moving mirror; when the beams recombine, they create constructive or destructive interference depending on the path length difference. As the moving mirror continuously changes position, this produces a time-varying interferogram that encodes all wavelengths as a function of mirror displacement.

**Key points students should include:**
- Beam is split into two paths (beamsplitter)
- One path has variable length (moving mirror)
- Beams recombine and interfere
- Interference pattern varies with mirror position
- Result is an interferogram

---

**d) Effect of doubling mirror velocity on modulated frequency**

From the equation: $f_{\text{mod}} = \frac{2\nu v}{c}$

The modulated frequency is directly proportional to mirror velocity $v$.

If $v$ doubles, then $f_{\text{mod}}$ also doubles.

**Answer: It would be doubled**

---

**e) Convert 3.0 μm to wavenumbers and frequency**

**i) Wavenumbers:**

The relationship between wavelength ($\lambda$) and wavenumber ($\tilde{\nu}$) is:
$$\tilde{\nu} = \frac{1}{\lambda}$$

First convert wavelength to cm:
$$\lambda = 3.0 \text{ μm} = 3.0 \times 10^{-4} \text{ cm}$$

Then:
$$\tilde{\nu} = \frac{1}{3.0 \times 10^{-4} \text{ cm}} = 3333.3 \text{ cm}^{-1}$$

**Answer: 3333 cm⁻¹** (or 3.3 × 10³ cm⁻¹)

**Note:** Both 3333 cm⁻¹ and 3.3 × 10³ cm⁻¹ are acceptable depending on significant figure treatment.

**ii) Frequency:**

Using $\nu = c \cdot \tilde{\nu}$:
$$\nu = (3.0 \times 10^{10} \text{ cm/s}) \times (3333 \text{ cm}^{-1})$$

$$\nu = 1.0 \times 10^{14} \text{ Hz}$$

**Answer: $1.0 \times 10^{14}$ Hz**

---

## Question 2: FT-IR Instrumentation and Performance

**a) Three distinct advantages of FT-IR compared to dispersive IR**

**Sample Answer:**

1. **Fellgett (Multiplex) Advantage:** All wavelengths are measured simultaneously rather than sequentially, resulting in much faster data collection and improved signal-to-noise ratio for a given measurement time.

2. **Jacquinot (Throughput) Advantage:** FT-IR uses circular apertures rather than narrow slits, allowing much more light to reach the detector, which improves sensitivity and signal-to-noise ratio.

3. **Connes Advantage:** The internal He-Ne laser provides an extremely precise wavelength reference for the interferometer mirror position, resulting in excellent wavelength accuracy and precision without need for external calibration.

**Other acceptable advantages:**
- No stray light issues (no diffraction from gratings)
- Higher resolution achievable with same-sized optical components
- Fewer moving parts (only one moving mirror)
- Easy signal averaging for S/N improvement
- Better dynamic range

---

**b) Signal-to-noise ratio after averaging 16 scans**

Signal-to-noise ratio improves with the square root of the number of scans averaged:

$$\text{S/N}_{\text{final}} = \text{S/N}_{\text{initial}} \times \sqrt{n}$$

where $n$ is the number of scans.

$$\text{S/N}_{\text{final}} = 3 \times \sqrt{16} = 3 \times 4 = 12$$

**Answer: 12:1**

**Note:** This assumes the noise is random and uncorrelated between scans, which is the typical case for detector noise.

---

**c) Time comparison**

**FT-IR time:**
$$\text{Time} = 16 \text{ scans} \times 1 \text{ s/scan} = 16 \text{ seconds}$$

**Dispersive IR time:**
$$\text{Time} = 5 \text{ minutes} = 300 \text{ seconds}$$

**Comparison:**
The FT-IR collects 16 scans in 16 seconds, which is **18.75 times faster** than a single scan with the dispersive instrument (300 s). 

Alternatively: The FT-IR is 300/16 ≈ 19× faster, or the dispersive instrument takes 300/16 ≈ 19× longer.

This dramatic speed advantage demonstrates the Fellgett (multiplex) advantage of FT-IR.

---

**d) Best description of the Fellgett (multiplex) advantage**

**Answer: All wavelengths are measured simultaneously, improving speed and signal-to-noise ratio**

**Explanation:** This is the correct definition of the multiplex advantage. In FT-IR, all wavelengths pass through the interferometer and reach the detector simultaneously, whereas a dispersive instrument scans through wavelengths sequentially. This provides both a speed advantage and, for the same total measurement time, an improved signal-to-noise ratio.

**Why the other options are incorrect:**
- "The interferometer has no moving parts" – FALSE: The interferometer has a moving mirror that is essential to its operation
- "The instrument can measure both near-IR and mid-IR simultaneously" – FALSE: This would require different detectors and beamsplitters; it's not related to the multiplex advantage
- "The Fourier transform algorithm removes all noise" – FALSE: The FT is a mathematical transformation that converts the interferogram to a spectrum; it doesn't remove noise, though it does help distribute noise evenly across all frequencies

---

**e) Why FT-IR is still better even for high-concentration, non-time-critical analyses**

**Concise Answer (3-4 sentences):**

Even for routine high-concentration samples, FT-IR offers superior wavelength accuracy and precision due to the Connes advantage (internal laser reference), which provides more reliable and reproducible spectra for compound identification and spectral library searching. The Jacquinot advantage ensures better energy throughput, which is beneficial when using sampling accessories like ATR or working with difficult sample matrices that inherently reduce signal. Additionally, the ability to quickly collect and average multiple scans improves spectral quality—allowing better discrimination of weak features, more accurate integration of bands, and superior baseline correction—even when speed is not the primary concern.

**Extended Answer (for deeper understanding):**

Even for routine high-concentration samples where sensitivity and speed are not limiting factors, FT-IR provides several important advantages. First, the Connes advantage—arising from the internal He-Ne laser wavelength reference—ensures exceptional wavelength accuracy and precision. This is critical for reliable spectral library matching and for comparing spectra between instruments or over time. Second, the Jacquinot advantage (higher throughput due to circular apertures vs. slits) means that even if you don't need the extra sensitivity for detection, you have more photons available for averaging, which improves spectral quality and reduces noise. This is particularly valuable when using ATR accessories or other sampling techniques that inherently reduce signal. Third, the ease of collecting and averaging multiple scans in FT-IR means that even when you have time, you can improve spectral quality by signal averaging—this helps with accurate band integration for quantitation, better resolution of overlapping peaks, and more reliable baseline correction. Finally, FT-IR systems generally have better resolution capabilities than dispersive instruments of similar cost, and they don't suffer from stray light issues that can affect dispersive systems. These factors combine to make FT-IR the superior choice even in applications where the classical speed and sensitivity advantages are not the primary drivers.

## Acknowledgements
This documented was created with assistance from Claude 4.5 Sonnet.