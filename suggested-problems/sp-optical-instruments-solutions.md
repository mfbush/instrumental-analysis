# Solutions: Components of Optical Instruments

## Question 1: Detector Response and Beer's Law Calculations

### Given Information
- $P_0 = 82.5$ μA (pure water, 100% transmittance)
- $P_{\text{std}} = 23.8$ μA (5.00 ppm Fe³⁺ standard)
- $P_{\text{unk}} = 48.6$ μA (unknown sample)
- $\lambda = 480$ nm
- $b = 1.00$ cm

### Solutions

**a) Percent transmittance of the standard solution**

The transmittance is the ratio of transmitted power to incident power:

$$T = \frac{P}{P_0}$$

$$T_{\text{std}} = \frac{23.8 \text{ μA}}{82.5 \text{ μA}} = 0.288$$

$$\%T = T \times 100 = 28.8\%$$

**Answer: 28.8%**

---

**b) Absorbance of the standard solution**

Absorbance is related to transmittance by:

$$A = -\log_{10}(T)$$

$$A_{\text{std}} = -\log_{10}(0.288) = 0.540$$

**Answer: 0.540** (or 0.54)

---

**c) Concentration of Fe³⁺ in the unknown sample**

First, calculate the absorbance of the unknown:

$$T_{\text{unk}} = \frac{48.6 \text{ μA}}{82.5 \text{ μA}} = 0.589$$

$$A_{\text{unk}} = -\log_{10}(0.589) = 0.230$$

Using Beer's law, $A = \varepsilon b c$. Since $\varepsilon$ and $b$ are constant for both measurements:

$$\frac{A_{\text{std}}}{c_{\text{std}}} = \frac{A_{\text{unk}}}{c_{\text{unk}}}$$

$$c_{\text{unk}} = c_{\text{std}} \times \frac{A_{\text{unk}}}{A_{\text{std}}}$$

$$c_{\text{unk}} = 5.00 \text{ ppm} \times \frac{0.230}{0.540} = 2.13 \text{ ppm}$$

**Answer: 2.13 ppm Fe³⁺**

---

**d) Expected current for 7.50 ppm Fe³⁺**

Calculate the expected absorbance:

$$A_{7.50} = A_{\text{std}} \times \frac{7.50 \text{ ppm}}{5.00 \text{ ppm}} = 0.540 \times 1.50 = 0.810$$

Convert to transmittance:

$$T_{7.50} = 10^{-A} = 10^{-0.810} = 0.155$$

Calculate the current:

$$P_{7.50} = T_{7.50} \times P_0 = 0.155 \times 82.5 \text{ μA} = 12.8 \text{ μA}$$

**Answer: 12.8 μA**

---

**e) Color of the Fe(SCN)₂⁺ complex**

The complex absorbs maximally at 480 nm, which is in the blue-green region of the visible spectrum (approximately 475-495 nm). 

According to the principle of complementary colors, a solution will appear the color complementary to the color it absorbs. The complement of blue-green is red-orange.

Therefore, the Fe(SCN)₂⁺ complex appears **red** (which is consistent with the problem statement describing it as "the red Fe(SCN)₂⁺ complex").

**Answer: Red. The solution absorbs blue-green light (480 nm), so it transmits/reflects the complementary color, which is red.**

---

## Question 2: Light Sources and Instrument Components

### Solutions

**a) Block diagram for UV-Vis absorption spectrophotometer**

```
[Light Source] → [Monochromator] → [Sample Cell] → [Detector] → [Signal Processor/Readout]
```

**Components:**
1. **Light Source**: Provides radiation (deuterium for UV, tungsten for visible)
2. **Monochromator**: Selects specific wavelength(s) from the light source
3. **Sample Cell**: Holds the sample in the light path
4. **Detector**: Converts radiant power to electrical signal (photodiode or PMT)
5. **Signal Processor/Readout**: Amplifies and displays the signal

*Note: Some instruments use a double-beam configuration where the beam is split before the sample, with one beam passing through a reference.*

---

**b) Light source selection**

**i. Quantitative determination of aspirin at 276 nm**

**Light source: Deuterium discharge lamp**

**Justification:** 276 nm is in the UV region (below 350 nm). Deuterium lamps produce intense continuum emission in the UV range (~160-375 nm), making them ideal for UV absorption measurements.

---

**ii. Measuring absorption spectrum of a blue dye from 400-700 nm**

**Light source: Tungsten-halogen lamp**

**Justification:** The wavelength range 400-700 nm is in the visible region. Tungsten-halogen lamps produce strong, stable continuum emission throughout the visible and near-IR regions (~320-2500 nm), making them ideal for visible spectroscopy.

---

**iii. Atomic absorption measurement of sodium at 589 nm**

**Light source: Hollow cathode lamp (sodium)**

**Justification:** Atomic absorption spectroscopy requires a line source that emits the specific wavelengths absorbed by the analyte atoms. A sodium hollow cathode lamp emits the characteristic sodium D-lines at 589.0 and 589.6 nm, providing the narrow-bandwidth radiation needed for selective sodium detection.

---

**c) Why deuterium produces a continuum spectrum**

In a deuterium discharge lamp, electrical discharge causes D₂ molecules to become excited to higher electronic states. When these excited molecules relax, many transitions result in dissociation of the D₂ molecule into two deuterium atoms:

$$\text{D}_2^* \rightarrow \text{D} + \text{D} + h\nu$$

During this dissociative transition, the molecule transitions from a bound excited electronic state to the dissociative continuum (unbound ground state). Because the two separated atoms can have any kinetic energy (continuous distribution), the emitted photons have a continuous range of energies, producing a continuum spectrum rather than discrete lines.

In contrast, hydrogen lamps at lower pressures show more discrete line emission from bound-to-bound electronic transitions in H atoms and H₂ molecules.

---

**d) Advantage of deuterium over hydrogen lamps**

**Advantage: Deuterium lamps produce 3-5 times higher intensity continuum radiation in the UV region compared to hydrogen lamps.**

The heavier deuterium molecule has different molecular properties that favor the continuum emission pathway. The increased intensity:
- Improves signal-to-noise ratio
- Allows for shorter measurement times
- Extends the useful lifetime of the lamp
- Provides better performance for routine analytical work

---

**e) Why PMTs cannot detect IR beyond 1100 nm**

Photomultiplier tubes operate via the photoelectric effect: incoming photons must have sufficient energy to eject electrons from the photocathode material.

The energy of a photon is:

$$E = \frac{hc}{\lambda}$$

IR radiation beyond ~1100 nm has photon energies less than ~1.1 eV. This is below the work function (minimum energy required to eject an electron) of typical photocathode materials (e.g., S-20 response, GaAs, multialkali cathodes).

Without sufficient photon energy to liberate electrons from the photocathode, the photoelectric effect cannot occur, and the PMT cannot generate a signal.

**Alternative IR detectors:** Thermal detectors (thermopiles, bolometers) or semiconductor detectors (InGaAs, PbS, MCT) must be used for IR detection.

---

## Question 3: Monochromators and Wavelength Selection

### Solutions

**a) Slit width selection**

**i. Recommended slit width for quantitative analysis**

**Answer: Narrow slit (1 nm)**

**ii. Justification:**

The spectral bandwidth (slit width) should be significantly smaller than the natural bandwidth of the absorption peak to avoid distortion of the measured absorbance. 

The general rule: **spectral bandwidth ≤ 1/10 of the natural bandwidth** for accurate measurements.

For a 12 nm natural bandwidth: maximum slit width ≈ 1.2 nm

Using a 1 nm slit ensures:
- No significant peak distortion
- Accurate absorbance measurements
- Adherence to Beer's law linearity

The 10 nm slit would be too close to the natural bandwidth and would cause significant band broadening and reduced peak absorbance, leading to quantitation errors.

**iii. For qualitative analysis (spectral acquisition):**

**Yes, use the narrow slit (1 nm).**

For qualitative analysis (obtaining detailed absorption spectra for compound identification), narrow slits are even more critical because:
- Better spectral resolution reveals fine structure
- Peak positions are more accurately determined
- Shoulder peaks and overlapping bands are better resolved
- The true shape of the absorption spectrum is preserved

Wide slits blur spectral features together, losing important structural information needed for identification.

---

**b) Diagram of grating monochromator**

```
                         Diffraction
                           Grating
                              |
                              ↓
    Entrance    Collimating  /|\ Focusing    Exit
      Slit   →    Mirror    / | \  Mirror  →  Slit
       |            ↓      /  |  \    ↓         |
    [====]        (  )    /   |   \  (  )    [====]
                         /    |    \
                        /     |     \
    White light     λ₁   λ₂   λ₃   λ₄   λ₅    Selected
    enters                                    wavelength
                                              exits

    Rotation of grating selects which wavelength
    passes through exit slit
```

**Key components:**
- **Entrance slit**: Defines the input beam
- **Diffraction grating**: Disperses light by wavelength
- **Exit slit**: Selects specific wavelength range
- Mirrors (collimating and focusing) to direct the beam

---

**c) Function of entrance slit and effect of width**

**Function of entrance slit:**
The entrance slit serves as a well-defined light source for the monochromator. It:
- Limits the divergence of the entering beam
- Defines the spatial extent of the source
- Provides a sharp image that can be dispersed by the grating

**Effect of making entrance slit wider:**

Making the entrance slit wider **decreases spectral resolution**.

When the entrance slit is widened:
- The image of the slit at the exit plane becomes wider
- A broader range of wavelengths passes through the exit slit simultaneously
- The spectral bandwidth (bandpass) increases
- Fine spectral features become blurred together

**Trade-off:** 
- Narrow slits → better resolution but less light throughput (lower signal)
- Wide slits → more light throughput but poorer resolution

---

**d) Interference filters vs. monochromators**

**i. Which provides better wavelength selectivity?**

**Answer: Monochromators** provide better wavelength selectivity (narrower bandwidth).

- High-quality monochromators: 0.1-5 nm bandwidth
- Interference filters: typically 5-15 nm bandwidth (FWHM)

---

**ii. One advantage of interference filters:**

**Answer (choose one):**
- **Simplicity and ruggedness**: No moving parts, very stable
- **Higher light throughput**: Filters transmit 40-70% of incident light vs. 10-30% for monochromators
- **Lower cost**: Much less expensive than monochromators
- **Compactness**: Small size suitable for portable instruments
- **No stray light**: Filters don't suffer from stray light issues like gratings

---

**iii. One advantage of monochromators:**

**Answer (choose one):**
- **Continuously variable wavelength**: Can select any wavelength within the range, not fixed to one wavelength
- **Better wavelength selectivity**: Narrower bandwidth for better resolution
- **Single instrument for all wavelengths**: Don't need multiple filters for different applications
- **Essential for spectral scanning**: Required to obtain complete absorption spectra
- **Better for trace analysis**: Narrower bandwidth reduces background interference

---

**e) Single-beam vs. double-beam for routine analysis**

**Answer: Double-beam spectrophotometer would be more practical**

**Justification:**

For routine analysis of 50 samples per day at a fixed wavelength, a **double-beam instrument** offers significant advantages:

1. **Automatic compensation**: Double-beam instruments automatically correct for:
   - Drift in lamp intensity over time
   - Detector response changes
   - Optical component variations
   - Temperature fluctuations

2. **Reduced need for re-blanking**: Single-beam instruments require frequent re-zeroing and re-blanking between samples. With 50 samples/day, this becomes time-consuming and introduces potential errors.

3. **Better precision over time**: For all-day operation, the continuous referencing in double-beam mode provides more stable and reproducible measurements.

4. **Less operator intervention**: More suitable for routine, repetitive analyses with minimal downtime.

**Note:** For a very small number of samples or budget constraints, a single-beam instrument could suffice, but would require more careful attention to blanking and standardization procedures.

---

## Summary of Key Equations

**Transmittance:**
$$T = \frac{P}{P_0}, \quad \%T = T \times 100$$

**Absorbance:**
$$A = -\log_{10}(T) = -\log_{10}\left(\frac{P}{P_0}\right) = \log_{10}\left(\frac{P_0}{P}\right)$$

**Beer's Law:**
$$A = \varepsilon b c$$

where:
- $A$ = absorbance (unitless)
- $\varepsilon$ = molar absorptivity (M⁻¹ cm⁻¹)
- $b$ = path length (cm)
- $c$ = concentration (M or other units)

**Photon Energy:**
$$E = h\nu = \frac{hc}{\lambda}$$

where:
- $E$ = energy
- $h$ = Planck's constant
- $\nu$ = frequency
- $c$ = speed of light
- $\lambda$ = wavelength

## Acknowledgements

This documented was created with assistance from Claude 4.5 Sonnet.