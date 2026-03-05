# Solutions to Suggested Problems: Mass Spectrometry
*Prof. Matthew F. Bush, University of Washington*

## Question 1 — Instrument Architecture, Mass Definitions, and Isotope Distributions

### Part (a)

A mass spectrometer contains three essential components arranged in series:

```
[Sample] → [Ion Source] → [Mass Analyzer] → [Detector] → [Mass Spectrum]
```

- **Ion source:** Converts the analyte from its native state (solution, solid, or gas) into gas-phase ions. This step is required because mass analyzers operate under high vacuum and manipulate ions using electric and/or magnetic fields.
- **Mass analyzer:** Separates or filters ions on the basis of their mass-to-charge ratio (*m*/*z*), allowing different ions to reach the detector at different times or positions.
- **Detector:** Generates a measurable electrical signal proportional to the number or total charge of ions arriving at a given instant.

---

### Part (b)

The *m*/*z* ratio is the mass of the ion (in unified atomic mass units, Da) divided by its charge number *z*, where *z* is a dimensionless integer equal to the number of elementary charges carried by the ion.

For a singly charged ion (*z* = 1):

$$\frac{m}{z} = \frac{m}{1} = m$$

Therefore, an ion at *m*/*z* = 151 with *z* = 1 has a mass of **151 Da**.

---

### Part (c)

**Nominal mass** (sum of integer masses of lightest stable isotopes):

$$m_{\text{nominal}} = 8(12) + 9(1) + 1(14) + 2(16) = 96 + 9 + 14 + 32 = \mathbf{151 \ \text{Da}}$$

**Monoisotopic mass** (sum of exact masses of lightest stable isotopes):

$$m_{\text{mono}} = 8(12.00000) + 9(1.00783) + 1(14.00307) + 2(15.99491)$$

$$= 96.00000 + 9.07047 + 14.00307 + 31.98982 = \mathbf{151.06336 \ \text{Da}}$$

*Comparison to part (b):* The molecular ion M⁺• in EI is formed by removing one electron from the neutral molecule. An electron has a mass of only ~0.00055 Da — negligible at nominal mass resolution. Therefore, the monoisotopic *m*/*z* of the molecular ion is also 151.06336 Da, and its nominal mass is 151 Da, consistent with the base peak at *m*/*z* = 151 observed in part (b).

---

### Part (d)

EI uses 70 eV electrons to produce the molecular ion by ejecting one electron from the analyte. The excess internal energy deposited in the molecular ion (~4–20 eV above ionization potential) far exceeds the bond dissociation energies of typical organic functional groups (3–5 eV). For a thermally labile compound — one with particularly weak bonds or an inherently unstable cation — the initially formed M⁺• undergoes rapid fragmentation before it can be detected. If the rate of fragmentation is much faster than the time scale of the measurement, the molecular ion population is depleted and no M⁺• peak is observed. Only fragment ions survive to reach the detector.

---

### Part (e)

The monoisotopic peak requires that every carbon atom be ¹²C (and similarly for all other elements). With 1,600 carbon atoms each having a 1.1% probability of being ¹³C, the probability that *all* carbons are ¹²C is:

$$P(\text{all } {}^{12}\text{C}) = (1 - 0.011)^{1600} = (0.989)^{1600}$$

Taking the natural logarithm:

$$\ln\left[(0.989)^{1600}\right] = 1600 \times \ln(0.989) = 1600 \times (-0.01106) = -17.7$$

$$P = e^{-17.7} \approx 2 \times 10^{-8}$$

The probability that a randomly chosen molecule in the sample contains only ¹²C atoms is approximately **2 × 10⁻⁸** — essentially zero. The monoisotopic peak is therefore undetectable. The isotope envelope is broad and centered near the average mass (~20,800 Da), not the monoisotopic mass.

---

## Question 2 — Ionization Sources and the Relationship Between *m*/*z* and Neutral Mass

### Part (a)

| Property | EI | ESI |
|:---|:---|:---|
| (i) Required analyte state | Vapor phase — analyte must be volatile and thermally stable | Solution — analyte is introduced as a liquid directly from an LC system or syringe pump |
| (ii) Ionization mechanism | Bombardment by 70 eV electrons ejects one electron from the analyte, producing a radical cation (M⁺•) | A high-voltage capillary forms a Taylor cone; charged droplets undergo repeated solvent evaporation and Coulombic fission until individual gas-phase ions are released as [M + *n*H]^*n*+ |
| (iii) Energy classification | **Hard** ionization — substantial excess energy is deposited, leading to extensive fragmentation | **Soft** ionization — little excess energy is deposited; the intact molecule is preserved |

A poly(ethylene oxide) surfactant is non-volatile and thermally labile. EI would require vaporizing the sample, which would cause thermal degradation before ionization. ESI operates from solution at atmospheric pressure and is well-matched to high-molecular-weight, non-volatile polymers.

---

### Part (b)

Both peaks arise from the same neutral molecule *M*. Let the peak at lower *m*/*z* (748.6) carry charge *z*₁ and the peak at higher *m*/*z* (936.0) carry charge *z*₂ = *z*₁ − 1. Setting the neutral mass expressions equal:

$$z_1\left(\frac{m}{z}\right)_1 - z_1 m_{\text{H}} = z_2\left(\frac{m}{z}\right)_2 - z_2 m_{\text{H}}$$

Solving for *z*₁:

$$z_1 = \frac{\left(\frac{m}{z}\right)_2 - m_{\text{H}}}{\left(\frac{m}{z}\right)_2 - \left(\frac{m}{z}\right)_1} = \frac{936.0 - 1.007}{936.0 - 748.6} = \frac{934.993}{187.4} \approx \mathbf{5}$$

Therefore: *z* at *m*/*z* = 748.6 is **5**; *z* at *m*/*z* = 936.0 is **4**.

**Neutral mass** from each peak:

$$M = z_1\left(\frac{m}{z}\right)_1 - z_1 m_{\text{H}} = 5(748.6) - 5(1.007) = 3743.0 - 5.0 = \mathbf{3738 \ \text{Da}}$$

$$M = z_2\left(\frac{m}{z}\right)_2 - z_2 m_{\text{H}} = 4(936.0) - 4(1.007) = 3744.0 - 4.0 = \mathbf{3740 \ \text{Da}}$$

The 2 Da discrepancy reflects rounding in the given *m*/*z* values; both results are consistent with a PEO oligomer of approximately **3,739 Da**.

---

### Part (c)

In MALDI, ionization occurs via gas-phase proton transfer from the acidic matrix to the analyte in the desorption plume. This is a one-step, low-energy proton transfer that typically adds a single proton to the analyte to give [M + H]⁺. There is no mechanism analogous to Coulombic charging that would simultaneously transfer multiple protons.

In ESI, the analyte is embedded in a highly charged droplet. As solvent evaporates, the surface charge density rises until Coulombic repulsion distributes charges across the molecule. For a flexible polymer like PEO, multiple ether oxygens are available as proton-acceptor sites distributed along the chain. Repeated cycles of Coulombic fission deposit multiple protons on the same molecule, yielding [M + *n*H]^*n*+. The number of charges acquired scales with the number of available basic or polar sites and the size of the analyte.

---

### Part (d)

The proposal is not viable. MALDI is fundamentally incompatible with gas chromatography. MALDI requires the analyte to be co-crystallized with a solid matrix on a target plate and is operated as a *batch* technique under high vacuum — it cannot accept a continuous flow of analyte in a carrier gas stream as GC requires. Additionally, the analyte must be in the condensed phase for matrix incorporation.

For a volatile, thermally stable compound with MW ≈ 150 Da, **EI is the appropriate technique**. EI is specifically designed for volatile analytes delivered in the gas phase, making it a natural match for GC. Furthermore, EI fragmentation produces a rich, reproducible spectrum that can be matched against the NIST library for compound identification — a key advantage for unknown small molecules that would be lost if soft ionization were used.

---

### Part (e)

For a [M + 3H]³⁺ ion, the neutral mass is:

$$M = z\left(\frac{m}{z}\right) - z \cdot m_{\text{H}} = 3(612.4) - 3(1.007) = 1837.2 - 3.0 = \mathbf{1834.2 \ \text{Da}}$$

---

## Question 3 — Mass Analyzers, Resolving Power, and Mass Accuracy

### Part (a)

The neutral BPA molecule is C₁₅H₁₆O₂. The [M + H]⁺ ion is formed by adding a proton (mass 1.00728 Da) to the neutral molecule — not a hydrogen *atom* (mass 1.00783 Da). The distinction matters because proton transfer, not hydrogen-atom transfer, is the mechanism in ESI.

**Step 1 — Monoisotopic mass of neutral BPA:**

$$M = 15(12.00000) + 16(1.00783) + 2(15.99491)$$

$$= 180.00000 + 16.12528 + 31.98982 = 228.11510 \ \text{Da}$$

**Step 2 — Add a proton to form [M + H]⁺:**

$$\frac{m}{z} = M + m_{\text{H}^+} = 228.11510 + 1.00728 = \mathbf{229.1224 \ \text{Da}}$$

---

### Part (b)

**Resolving power** from the FWHM definition, $R_p = (m/z) / \Delta(m/z)_\text{FWHM}$:

$$R_p(\text{quadrupole}) = \frac{229.1}{0.23} \approx \mathbf{996}$$

$$R_p(\text{TOF}) = \frac{229.1}{0.023} \approx \mathbf{9{,}960}$$

**Can either instrument distinguish BPA from the isomer?**

The two ions differ by:

$$\Delta(m/z) = 229.1224 - 229.0869 = 0.0354 \ \text{Da} = 35.4 \ \text{mDa}$$

The minimum resolvable peak separation equals the FWHM. For each instrument:

| Instrument | FWHM | Peak separation | Resolved? |
|:---|:---:|:---:|:---:|
| Quadrupole | 230 mDa | 35.4 mDa | **No** — FWHM >> separation |
| TOF | 23.0 mDa | 35.4 mDa | **Yes** — separation/FWHM ≈ 1.5 |

The TOF can resolve the two ions; the quadrupole cannot.

---

### Part (c)

$$\text{mass accuracy (ppm)} = \left\lvert \frac{(m/z)_{\text{measured}} - (m/z)_{\text{expected}}}{(m/z)_{\text{expected}}} \right\rvert \times 10^6$$

$$= \left\lvert \frac{229.1235 - 229.1224}{229.1224} \right\rvert \times 10^6 = \frac{0.0011}{229.1224} \times 10^6 \approx \mathbf{4.8 \ \text{ppm}}$$

This is well within the 1–10 ppm typical range for a well-calibrated TOF instrument (Table 4 of the notes). The result confirms that the instrument is performing as expected and that the measured *m*/*z* is consistent with BPA.

---

### Part (d)

A **scanning analyzer** (quadrupole filter) transmits only one *m*/*z* value at a time. To build up a full mass spectrum, it steps through successive *m*/*z* windows sequentially, spending only a fraction of the total acquisition time at each window. Ions arriving while the instrument is set to any other *m*/*z* are not transmitted and are lost.

A **multichannel analyzer** (TOF, Fourier transform) records all *m*/*z* values simultaneously in a single acquisition event. Every ion generated during that event contributes to the spectrum.

**Practical consequence for sensitivity:** In full-scan mode, the quadrupole discards the vast majority of ions — for a scan window of 1,000 Da with unit-mass steps, each mass is transmitted for only about 0.1% of the acquisition time. The TOF detects all ions in every cycle, giving it significantly higher sensitivity (by 1–3 orders of magnitude) for full-scan experiments. This advantage disappears in targeted experiments such as SIM or MRM, where the quadrupole dwells continuously on the ions of interest.

---

### Part (e)

For a high-molecular-weight polymer, the probability of observing the monoisotopic ion (all atoms as lightest isotopes) is astronomically small — effectively zero — as shown quantitatively in Q1(e) for polystyrene. The isotope distribution is therefore a broad envelope containing thousands of overlapping isotope peaks.

When the resolving power is too low to separate individual isotope peaks (peaks spaced ~1 Da apart), the instrument cannot distinguish them; instead, it measures the centroid of the unresolved envelope. The centroid of the isotope distribution corresponds to the **average mass** — the abundance-weighted mean over all isotope combinations — which is the same quantity reported on a periodic table as the molar mass. For PEG-25000, reporting the monoisotopic mass would be physically meaningless since the monoisotopic ion is not detectable, and even at high resolving power the monoisotopic peak is not the most abundant feature of the spectrum.

---

## Question 4 — Acquisition Modes and Tandem Mass Spectrometry

### Part (a)

In **full-scan** mode, the quadrupole ramps its DC and RF voltages continuously across a wide *m*/*z* range (e.g., *m*/*z* 50–500), transmitting each *m*/*z* window briefly in sequence. The result is a complete mass spectrum that can be used for compound identification — every ion present in the source is eventually detected. The limitation is sensitivity: at any instant, all ions except those in the narrow transmitted window are discarded. For atrazine at trace concentrations in a complex water matrix, the full-scan signal may be weak and the spectrum may be overwhelmed by matrix ions.

In **selected ion monitoring (SIM)**, the quadrupole is locked onto one (or a small number of) target *m*/*z* values. Because the instrument dwells continuously on the target ion rather than scanning past it, the duty cycle increases by roughly the ratio of the scan time to the dwell time — typically a factor of 100–1,000 in practice. This improvement in sensitivity comes at the cost of all spectral information for non-target ions: SIM cannot identify unknowns and provides no confirmation that the signal at the target *m*/*z* actually arises from atrazine rather than a co-eluting interferent.

---

### Part (b)

**Block diagram of the triple-quadrupole (QqQ) instrument:**

```
[Ion Source] ──→ [  Q1  ] ──→ [   q2   ] ──→ [  Q3  ] ──→ [Detector]
                  Precursor    Collision       Product
                  selection    cell (CID)      ion analysis
```

- **Q1 (mass-filtering quadrupole):** Selects only the precursor ion of interest (e.g., atrazine [M + H]⁺ at *m*/*z* = 216) by transmitting a narrow *m*/*z* window; all other ions are rejected.
- **q2 (RF-only collision cell):** An RF-only quadrupole (no DC voltage, so no mass filtering) that confines ions while an inert collision gas (nitrogen or argon) induces collision-induced dissociation (CID), fragmenting the precursor ion into structurally diagnostic product ions.
- **Q3 (mass-filtering quadrupole):** Filters the product ions generated in q2, transmitting only the selected product ion *m*/*z* to the detector.

---

### Part (c)

**Physical meaning of 216 → 174:**

- **216** is the *m*/*z* of the **precursor ion** — the [M + H]⁺ ion of atrazine selected by Q1 for fragmentation in q2.
- **174** is the *m*/*z* of a specific **product ion** — a fragment formed from the precursor during CID in q2 (corresponding to loss of a 42 Da neutral fragment, likely loss of C₂H₂N from the triazine ring) and selected by Q3 for detection.

**Why two selection steps increase specificity:** A co-eluting interferent can produce a signal in SIM if it happens to have the same nominal precursor mass (*m*/*z* = 216). In MRM, the interferent must *also* fragment under CID to produce a product ion at exactly *m*/*z* = 174. Satisfying two independent mass criteria simultaneously — the correct precursor mass and the correct fragmentation chemistry — is a far more stringent requirement. Most interferents that happen to share the precursor *m*/*z* will not produce the same product ions and will therefore not generate a false-positive signal.

**Confirmatory MRM transition:** **216 → 132** (using the second product ion noted in the problem). Both transitions must agree quantitatively for an unambiguous identification; regulatory methods for pesticide monitoring typically require at least two MRM transitions.

---

### Part (d)

The degradation product has *m*/*z* = 216 — the same as atrazine — so **SIM** monitoring of *m*/*z* = 216 cannot distinguish the two compounds. Both would contribute equally to the SIM signal, causing a positive bias (overestimation) in the atrazine concentration.

In **MRM with the 216 → 174 transition**, Q1 transmits all ions at *m*/*z* = 216, including both atrazine and the degradation product. However, in q2, CID of the degradation product does *not* generate a product ion at *m*/*z* = 174 (as stated in the problem). Q3 therefore transmits no signal from the degradation product. Only atrazine produces the correct product ion and reaches the detector. The degradation product is invisible to this transition, and quantitation of atrazine is unaffected by its presence.

---

### Part (e)

**Why the ion trap is well-suited for MS^n:** The ion trap achieves tandem MS by performing all steps — ion accumulation, precursor isolation, fragmentation, and product ion detection — in **temporal sequence within the same physical device** (tandem-in-time). To perform MS³, the instrument simply executes an additional isolation-and-fragmentation step in time without requiring any new hardware. MS^n for arbitrarily large *n* requires only additional time steps in the same trap.

The triple quadrupole uses tandem-in-space: Q1, q2, and Q3 are physically separate regions. An additional stage of MS/MS would require a fourth and fifth physical component (another collision cell and another quadrupole mass filter), which would make the instrument larger and more expensive. Practically, this limits triple-quadrupole instruments to MS/MS (n = 2).

**Practical limitation of high-order MS^n on an ion trap:** Each isolation step selects a subset of ions from those currently in the trap, reducing the ion population available for the next stage. After several isolation and fragmentation steps, the number of product ions remaining may fall below the detection limit, and the spectrum becomes too noisy to interpret. Sensitivity therefore decreases progressively with each successive MS^n stage.

---

## Acknowledgements
This documented was created with assistance from Claude 4.5 Sonnet.