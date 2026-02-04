# Solutions to Suggested Problems: Molecular Luminescence
*Prof. Matthew F. Bush, University of Washington*

## Question 2: Spectrofluorometry Instrumentation and Quantitative Analysis

### a) Calibration Curve

**Step 1: Blank correction**

| Concentration (ppm) | Raw Intensity | Corrected Intensity |
|---------------------|---------------|---------------------|
| 0 | 5.2 | 0 |
| 5.0 | 127.8 | 122.6 |
| 10.0 | 250.6 | 245.4 |
| 20.0 | 496.2 | 491.0 |

**Step 2: Calculate slope**

Using points (5.0, 122.6) and (20.0, 491.0):

$$m = \frac{I_2 - I_1}{C_2 - C_1} = \frac{491.0 - 122.6}{20.0 - 5.0} = \frac{368.4}{15.0} = 24.56 \text{ a.u./ppm}$$

**Verification** using points (10.0, 245.4) and (20.0, 491.0):
$$m = \frac{491.0 - 245.4}{20.0 - 10.0} = \frac{245.6}{10.0} = 24.56 \text{ a.u./ppm}$$ ✓

**Step 3: Calculate intercept**

Using point-slope form with (10.0, 245.4):
$$I = mC + b$$
$$245.4 = 24.56(10.0) + b$$
$$245.4 = 245.6 + b$$
$$b = -0.2 \approx 0$$

**Calibration equation:** 
$$I_{corrected} = 24.56 \times C \text{ (ppm)}$$

Or with intercept:
$$I_{corrected} = 24.56C - 0.2$$

### b) Concentration in Solution B

Unknown raw intensity: 373.6
Blank-corrected intensity: $373.6 - 5.2 = 368.4$ a.u.

$$C = \frac{I_{corrected}}{m} = \frac{368.4}{24.56} = 15.0 \text{ ppm}$$

### c) Concentration in Solution A

Solution B was prepared by diluting 1.00 mL of Solution A to 100.0 mL.

**Dilution factor:** $\frac{100.0 \text{ mL}}{1.00 \text{ mL}} = 100$

**Concentration in Solution A:**
$$C_A = C_B \times \text{dilution factor} = 15.0 \text{ ppm} \times 100 = 1500 \text{ ppm}$$

### d) Mass of Quinine in Tablet

Concentration in Solution A: 1500 ppm = 1500 mg/L

Volume of Solution A: 100.0 mL = 0.1000 L

**Mass calculation:**
$$\text{mass} = \text{concentration} \times \text{volume}$$
$$\text{mass} = 1500 \text{ mg/L} \times 0.1000 \text{ L} = 150 \text{ mg}$$

### e) Quality Control Decision

**Target:** 150 mg ± 10% = 135 mg to 165 mg

**Found:** 150 mg

**Answer: Yes** - The tablet contains exactly the target amount and is well within the acceptable range.

**Calculation:**
$$\text{Percent of target} = \frac{150}{150} \times 100\% = 100\%$$

This is within 135-165 mg specification.

### f) 90° Detection Geometry

**Correct answer:** To minimize detection of scattered excitation light that would increase background signal

**Detailed explanation:**

At 90° geometry:
- **Scattered excitation light** (Rayleigh and Raman scattering) travels straight through the sample
- Emission detector positioned perpendicular to excitation beam
- **Minimal scattered light** reaches detector
- Background ≈ dark current only (essentially zero)

**Why this matters for sensitivity:**
$$S/N = \frac{\text{Fluorescence signal}}{\text{Background noise}}$$

- Low background → high S/N ratio
- Can detect very weak fluorescence
- This is the fundamental reason fluorescence is so sensitive

**Alternative geometries:**
- **0° (transmission):** Detector would see mostly scattered light + small fluorescence signal → poor S/N
- **180° (front-face):** Used only for highly absorbing/scattering samples

---

## Question 3: Luminescence Instrumentation and Techniques

### a) Spectrofluorometer Block Diagram

```
                        ┌─────────────────┐
                        │ Emission        │
                        │ Monochromator   │
                        └────────┬────────┘
                                 │
                                 ↓
                        ┌─────────────────┐
                        │   Detector      │
                        │   (PMT/PD)      │
                        └─────────────────┘
                                 ↑
                                 │ 90°
                                 │
Light Source    ┌─────────────┐ │
(Xe lamp)  ───→ │ Excitation  │ │
                │ Monochromator│ │
                └──────┬──────┘ │
                       │        │
                       ↓        │
                  ┌────────────┐│
                  │  Sample    ││
                  │   Cell     ││
                  └────────────┘│
                       └────────┘
```

**Key components:**
1. **Light source:** Xenon arc lamp (continuous spectrum 200-1000 nm) or laser
2. **Excitation monochromator:** Selects $\lambda_{ex}$ (grating or prism)
3. **Sample cell:** Typically 1 cm quartz cuvette
4. **Emission monochromator:** Selects $\lambda_{em}$ (perpendicular to excitation)
5. **Detector:** Photomultiplier tube (PMT) or photodiode
6. **90° geometry:** Critical for minimizing stray light

### b) Comparison of Luminescence Techniques

| Technique | Energy Source for Excitation | External Light Source Required? | Typical Application |
|-----------|------------------------------|--------------------------------|---------------------|
| Fluorescence | Photon absorption (UV/visible light) | Yes | Quantitative analysis, imaging, sensing |
| Phosphorescence | Photon absorption (UV/visible light) | Yes | Low-temperature spectroscopy, glow-in-dark materials |
| Chemiluminescence | Chemical reaction energy | No | Immunoassays, ATP assays, forensic blood detection |

**Additional details:**

**Fluorescence:**
- Requires external excitation source matched to absorption spectrum
- Immediate emission (ns timescale)
- Most versatile - can be tuned for any fluorophore

**Phosphorescence:**
- Same excitation as fluorescence, but emission is delayed
- Often requires cooling to 77 K (liquid nitrogen) to observe
- Time-gated detection can eliminate fluorescence interference

**Chemiluminescence:**
- Energy from bond formation/breaking in chemical reaction
- Example: luminol + H₂O₂ + catalyst → excited state product → emission
- No excitation source needed → extremely low background

### c) Key Advantages

**Fluorescence:**
- **Versatility and tunability** - Can excite at any wavelength matched to the fluorophore's absorption. Can create excitation and emission spectra to characterize compounds. Compatible with wide range of analytes through derivatization or intrinsic fluorescence.

**Phosphorescence:**
- **Time-resolution eliminates interference** - Long lifetime (ms-s) allows time-gated detection after short-lived fluorescence has decayed. Can distinguish multiple phosphorescent species by lifetime differences. Reduces background from scattered light and autofluorescence.

**Chemiluminescence:**
- **Ultimate sensitivity with zero background** - No excitation source means no scattered light, no Raman scattering, no photodecomposition. Background limited only by detector dark current. Can achieve attomole (10⁻¹⁸ mol) detection limits for optimized systems like luminol.

### d) Properties of Good Fluorescent Probes

**Three essential properties:**

1. **High fluorescence quantum yield ($\Phi_f > 0.1$)**
   - Ratio of photons emitted to photons absorbed
   - Ensures bright signal for low concentrations
   - Example: Fluorescein $\Phi_f \approx 0.9$

2. **Large molar absorptivity ($\varepsilon > 10^4$ M⁻¹cm⁻¹)**
   - Strong absorption at excitation wavelength
   - Combined with high $\Phi_f$ gives intense emission
   - Brightness = $\varepsilon \times \Phi_f$

3. **Photostability (resistance to photobleaching)**
   - Maintains fluorescence under prolonged illumination
   - Critical for time-lapse imaging experiments
   - Example: Rhodamine dyes are very photostable

**Additional desirable properties:**
- Large Stokes shift (>50 nm) - reduces self-quenching and scatter interference
- Appropriate excitation/emission wavelengths - match available lasers and detectors
- Water solubility - for biological applications
- Biocompatibility and low toxicity - for live-cell imaging
- Functional groups for conjugation - can attach to antibodies, proteins, DNA

### e) Sensitivity Advantage of Fluorescence

**Correct answer:** Fluorescence measures signal against a near-zero background, while absorption measures a small difference between large signals

---

## Question 1: Luminescence Fundamentals and Jablonski Diagrams

### a) Jablonski Diagram

**Complete diagram should show:**

```
Energy ↑
        
    S₂ ──────────  v=2
       ──────────  v=1
       ──────────  v=0
        ↑ absorption    ↓ IC
         
    S₁ ──────────  v=2
       ──────────  v=1  ↓ VR (vibrational relaxation)
       ──────────  v=0  ──→ fluorescence (10⁻⁹ s)
        ↑                ↓     ↘
                        ISC     ↘
    T₁ ──────────  v=2          ↘
       ──────────  v=1           ↘
       ──────────  v=0 ───→ phosphorescence (10⁻³ s)
                              ↘
    S₀ ──────────  v=2         ↘
       ──────────  v=1          ↘
       ──────────  v=0 ←────────┘
```

**Labeled transitions:**
1. **Absorption**: Vertical upward arrows from $S_0$ (v=0) to vibrational levels of $S_1$ and $S_2$
2. **Vibrational relaxation (VR)**: Small downward arrows within electronic states (non-radiative)
3. **Internal conversion (IC)**: Horizontal arrow from $S_2$ to $S_1$ (non-radiative)
4. **Fluorescence**: Vertical downward arrow from $S_1$ (v=0) to vibrational levels of $S_0$
5. **Intersystem crossing (ISC)**: Horizontal arrow from $S_1$ to $T_1$ with spin flip notation
6. **Phosphorescence**: Vertical downward arrow from $T_1$ (v=0) to vibrational levels of $S_0$

### b) Why Fluorescence Emission is Longer Wavelength

**Energy-loss process:** Vibrational relaxation

**Mechanism:**
1. **Absorption** promotes molecule from $S_0$ (v=0) to higher vibrational levels of $S_1$ (or $S_2$)
2. **Vibrational relaxation** (~10⁻¹² s) rapidly dissipates energy as heat, bringing molecule to $v=0$ of $S_1$
3. **Fluorescence** emission occurs from $S_1$ (v=0) → vibrational levels of $S_0$

**Energy comparison:**
$$E_{absorbed} = E_{S_1(v=2)} - E_{S_0(v=0)}$$
$$E_{emitted} = E_{S_1(v=0)} - E_{S_0(v=0)}$$

Since $E_{S_1(v=2)} > E_{S_1(v=0)}$, we have $E_{absorbed} > E_{emitted}$

**Wavelength relationship:**
$$E = \frac{hc}{\lambda} \quad \text{so} \quad \lambda = \frac{hc}{E}$$

Lower energy → longer wavelength, therefore $\lambda_{emission} > \lambda_{excitation}$

This wavelength shift is called the **Stokes shift**.

### c) Fluorescence vs. Phosphorescence Comparison

| Property | Fluorescence | Phosphorescence |
|----------|--------------|-----------------|
| Electronic transition (specify states) | $S_1 \rightarrow S_0$ (singlet to singlet) | $T_1 \rightarrow S_0$ (triplet to singlet) |
| Spin multiplicity change? (yes/no) | No (singlet → singlet) | Yes (triplet → singlet) |
| Typical timescale | 10⁻⁹ to 10⁻⁶ seconds (nanoseconds) | 10⁻³ to 10² seconds (milliseconds to minutes) |
| Allowed or forbidden transition? | Allowed (spin-allowed) | Forbidden (spin-forbidden) |

### d) Conjugation and Fluorescence

**Role of conjugation in HOMO-LUMO gap:**

Aromatic compounds (anthracene):
- Extended π-conjugation delocalizes electrons over multiple atoms
- Creates **small HOMO-LUMO gap** (~3-4 eV)
- Transitions occur in **visible/near-UV region** (300-400 nm)
- Energy gap small enough that radiative decay can compete with non-radiative processes

Saturated hydrocarbons (hexane):
- Only σ-bonds, no π-system
- **Large HOMO-LUMO gap** (>6 eV)  
- Would require **far-UV excitation** (<200 nm)
- Not accessible with typical fluorometers

**Role of molecular rigidity:**

Aromatic compounds:
- **Rigid, planar structure** (constrained by aromaticity)
- Few vibrational/rotational modes available
- **Low non-radiative decay rate** ($k_{nr}$ is small)
- Fluorescence quantum yield: $\Phi_f = \frac{k_f}{k_f + k_{nr}}$ is high (0.3-0.9)

Saturated hydrocarbons:
- **Flexible structure** with free rotation around C-C bonds
- Many vibrational modes act as "energy sinks"
- **High non-radiative decay rate** ($k_{nr} >> k_f$)
- Excited state energy dissipated as heat via C-C bond vibrations/rotations
- $\Phi_f \approx 0$ (essentially no fluorescence)

### e) Fluorescence Excitation Spectra

**Correct answer:** Fluorescence excitation spectra closely resemble absorption spectra because both measure wavelengths that promote molecules to excited states

**Explanation:**
- **Excitation spectrum**: Scan $\lambda_{ex}$, monitor intensity at fixed $\lambda_{em}$
- **Absorption spectrum**: Scan $\lambda$, monitor absorbance
- Both measure the $S_0 \rightarrow S_1$ (and $S_0 \rightarrow S_2$) transitions
- They are nearly identical for molecules that fluoresce
- Minor differences: Excitation spectrum only sees molecules that emit (fluorescent species)

---

## Acknowledgements
This documented was created with assistance from Claude 4.5 Sonnet.