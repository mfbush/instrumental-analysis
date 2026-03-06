# Solution Guide: Liquid Chromatography–Mass Spectrometry
*Prof. Matthew F. Bush, University of Washington*

---

## Question 1: Targeted Quantitation of Neonicotinoid Pesticides in Drinking Water

### Part a)

Two properties of imidacloprid that make it incompatible with GC-MS:

**1. Thermal lability.** Imidacloprid contains a nitroguanidine substituent and a chloropyridinylmethyl group that are prone to thermal decomposition. GC requires analytes to survive vaporization at temperatures that may exceed 200–300 °C. Imidacloprid would decompose before or during vaporization, producing degradation products rather than the intact analyte.

**2. Low volatility.** Imidacloprid is a highly polar compound (logP ≈ 0.57), with multiple hydrogen bond acceptors (five nitrogen atoms, two oxygens) and a formal charge under acidic conditions. Polar functional groups create strong intermolecular interactions in the condensed phase, greatly reducing vapor pressure. The compound has insufficient volatility to exist as a stable gas at practical GC operating temperatures.

---

### Part b)

**Elution order: imidacloprid elutes before acetamiprid.**

Reversed-phase retention is driven by hydrophobic interactions between the analyte and the C18 stationary phase. The more nonpolar (hydrophobic) an analyte, the more strongly it partitions into the C18 layer and the longer it is retained.

- **Imidacloprid** contains a nitroguanidine group (–NH–C(=N–NO₂)–NH–) that is strongly electron-withdrawing and highly polar, as well as a ring nitrogen that contributes polarity. These polar groups stabilize the molecule in the aqueous mobile phase through hydrogen bonding and dipole interactions → imidacloprid spends more time in the mobile phase → elutes first.

- **Acetamiprid** lacks the ring nitrogen oxide, and its cyano group (–CN) is less polar than the nitroguanidine moiety. Acetamiprid is therefore more hydrophobic than imidacloprid, partitions more strongly into the C18 chains, and elutes later.

---

### Part c)

**Same retention time:** Retention in RPLC is governed by the chemical polarity and molecular shape of the analyte, which determine its partitioning between the aqueous mobile phase and the nonpolar C18 stationary phase. Replacing five ¹²C atoms with ¹³C does not change the number or type of functional groups, the molecular geometry, or the hydrogen bonding capacity of the molecule. The labeled and unlabeled compounds therefore have identical polarity and identical retention factors, $k$, and co-elute.

**Distinction by the mass spectrometer:** The ¹³C₅ label adds $5 \times (13.003 - 12.000) = 5.017$ Da to the molecular mass. The [M+H]⁺ ion of imidacloprid appears at $m/z\ 256.1$, while that of ¹³C₅-imidacloprid appears at $m/z\ 261.1$. The QqQ uses separate MRM transitions for each compound (e.g., $256.1 \rightarrow 175.1$ for imidacloprid and $261.1 \rightarrow 180.1$ for the labeled IS), and the two signals are detected independently.

---

### Part d)

**i)** The ion at $m/z\ 256.1$ is a protonated molecule — the $[\text{M+H}]^+$ adduct formed when a proton is added to neutral imidacloprid during positive-mode ESI. The ionic formula is $[\text{C}_9\text{H}_{11}\text{ClN}_5\text{O}_2]^+$.

*Calculation check:* Monoisotopic neutral mass ($^{35}$Cl isotopologue) = $9(12.000) + 10(1.008) + 34.969 + 5(14.003) + 2(15.995) = 255.052$ Da; $[\text{M+H}]^+ = 255.052 + 1.007 = 256.059 \approx 256.1$ Da. ✓

**ii)** The sequence of events in QqQ MRM mode:
1. Q1 is fixed to transmit only $m/z\ 256.1$. The precursor ion $[\text{M+H}]^+$ passes through; all other ions strike the rods and are neutralized.
2. The selected precursor enters the RF-only collision cell q2, where it is accelerated into an inert collision gas (N₂ or Ar). Energetic collisions transfer internal energy to the ion, causing collision-induced dissociation (CID) and generating product ions, including the fragment at $m/z\ 175.1$.
3. Q3 is fixed to transmit only $m/z\ 175.1$. Only this product ion passes through to the detector; all other fragment ions are discarded.

**iii)** Three independent criteria that must all be satisfied simultaneously:
1. **Retention time:** the signal arrives within the expected LC retention time window for imidacloprid.
2. **Precursor $m/z$:** Q1 transmits the correct precursor ion ($m/z\ 256.1$).
3. **Product $m/z$:** Q3 transmits the correct product ion ($m/z\ 175.1$).

---

### Part e)

**Linear regression setup:**

$$\bar{x} = \frac{0 + 1.0 + 2.5 + 5.0 + 10.0}{5} = 3.70 \text{ ng/mL}$$

$$\bar{y} = \frac{0.010 + 0.511 + 1.260 + 2.510 + 5.012}{5} = 1.861$$

$$S_{xx} = \sum(x_i - \bar{x})^2 = (-3.7)^2 + (-2.7)^2 + (-1.2)^2 + (1.3)^2 + (6.3)^2 = 13.69 + 7.29 + 1.44 + 1.69 + 39.69 = 63.80$$

$$S_{xy} = \sum(x_i - \bar{x})(y_i - \bar{y}) = (-3.7)(-1.851) + (-2.7)(-1.350) + (-1.2)(-0.601) + (1.3)(0.649) + (6.3)(3.151) = 6.85 + 3.64 + 0.72 + 0.84 + 19.85 = 31.90$$

$$\text{slope} = \frac{S_{xy}}{S_{xx}} = \frac{31.90}{63.80} = 0.500$$

$$\text{intercept} = \bar{y} - \text{slope} \cdot \bar{x} = 1.861 - 0.500 \times 3.70 = 0.011 \approx 0.010$$

$$\boxed{y = 0.500\, x + 0.010}$$

**Unknown concentration:**

$$1.26 = 0.500\, x + 0.010$$

$$x = \frac{1.26 - 0.010}{0.500} = \frac{1.250}{0.500} = \boxed{2.50 \text{ ng/mL}}$$

---

### Part f)

**i) Ion suppression.** Co-eluting matrix components in the surface water extract — inorganic salts, dissolved organic matter — partition into the same ESI droplets as imidacloprid. As solvent evaporates from the droplets, these matrix species compete with imidacloprid for the limited number of available charges. Because fewer charges reach imidacloprid molecules, the ionization efficiency of the analyte is reduced. The same concentration of analyte therefore produces a smaller signal in the complex matrix than in clean solvent.

**ii)** Both imidacloprid and the ¹³C₅-IS are suppressed by the same factor because they are chemically identical and co-elute into the same droplets. From the data:

$$\text{Suppression factor} \approx \frac{171{,}000}{285{,}000} = 0.600 \quad \text{(analyte)} \qquad \frac{68{,}200}{113{,}800} = 0.599 \quad \text{(IS)}$$

Both signals are reduced by $\approx$40%. When the ratio is computed, this factor cancels exactly:

$$\frac{\text{analyte signal}}{\text{IS signal}} = \frac{f \cdot [\text{analyte}] \cdot k}{f \cdot [\text{IS}] \cdot k} = \frac{[\text{analyte}]}{[\text{IS}]}$$

The peak area ratios in both matrices are essentially identical (2.505 vs. 2.507), yielding the same calculated concentration (4.99 ng/mL) despite a 40% difference in raw signal.

**iii)** If the internal standard is added before extraction, it experiences all of the same sample preparation losses as the analyte (e.g., incomplete recovery from solid-phase extraction, losses during filtration or evaporation). These losses reduce both the analyte and IS signals by the same factor, which again cancels in the ratio. Adding the IS only at the point of injection would correct for ESI ion suppression but would not account for analyte losses that occurred during sample preparation — leaving those losses as an uncorrected systematic error in the final result.

---

### Part g)

**Correct answer: option 2.**

*"By fixing Q1 and Q3 at specific m/z values, the instrument dwells on the target transition for nearly 100% of acquisition time, greatly increasing the duty cycle for those ions."*

In full-scan mode, the quadrupole ramps through $N$ successive $m/z$ values and spends only $\sim 1/N$ of its time at any given value. The duty cycle for the target ion is therefore $\sim 1/N$, which may be 0.1–1% for a typical scan range. In MRM, Q1 and Q3 are both fixed at the target transition, so the instrument collects signal from that transition for essentially 100% of acquisition time. This dramatic increase in duty cycle directly translates to lower detection limits.

---

## Question 2: Discovery LC-MS of Unknown Impurities in a Pharmaceutical Intermediate

### Part a)

**i) The interface challenge.** ESI operates at atmospheric pressure. The analyte solution is sprayed into a warm atmospheric-pressure region where solvent evaporates, assisted by a flow of drying gas. The resulting desolvated gas-phase ions are then drawn through a series of differentially pumped stages (from atmospheric pressure, to rough vacuum, to high vacuum) before entering the mass analyzer. This means the large solvent load from the LC — typically 0.1–1 mL/min of liquid, which upon vaporization would produce roughly 0.1–1 L/min of gas — is removed at atmospheric pressure and never reaches the high-vacuum analyzer. No other common ionization method achieves this.

**ii) Why EI is inappropriate.** EI requires the analyte to be present as a stable vapor in the gas phase. These polar, non-volatile compounds with molecular weights of 200–600 Da have insufficient vapor pressure to be vaporized without thermal decomposition. Even if vaporization were possible, the internal energy deposited by 70-eV electrons would cause extensive fragmentation that could destroy the molecular ion, making identification ambiguous. EI is fundamentally incompatible with non-volatile, thermally labile analytes.

---

### Part b)

**i) A single DDA cycle proceeds as follows:**
1. The QTOF acquires an **MS¹ survey scan**: the full mass spectrum of all ions eluting from the LC column at that moment (e.g., $m/z$ 50–1200). This scan records the $m/z$ values and signal intensities of all precursor ions present.
2. The instrument software ranks all detected precursor ions by signal intensity and selects the top 10 that have not been fragmented recently (to avoid repeatedly fragmenting the same species).
3. For each selected precursor, the quadrupole is set to isolate that $m/z$ value, the precursor is accelerated into the collision cell and fragmented by CID, and the TOF records the full **MS² product ion spectrum**.
4. Steps 3 is repeated for all 10 selected precursors.
5. The instrument returns to step 1 to begin the next MS¹ survey scan.

**ii)** Number of DDA cycles across the peak:

$$\text{Cycles} = \frac{18\ \text{s}}{1.1\ \text{s/cycle}} \approx 16\ \text{cycles}$$

This is sufficient. In practice, $\geq$10 complete DDA cycles across a chromatographic peak is generally considered adequate — it ensures that multiple independent MS² spectra are acquired for the compound, allows the apex region (where signal is strongest and spectra are least contaminated by co-eluting species) to be sampled many times, and provides enough spectral averaging to produce a reliable fragmentation pattern for identification.

**iii)** The isotope peaks are separated by 1.0 $m/z$ unit ($315.1 \rightarrow 316.1 \rightarrow 317.1$). For a multiply charged ion with charge state $z$, adjacent isotope peaks are separated by $1/z$ mass units. A spacing of 1.0 units is therefore diagnostic of $z = 1$ — a singly charged ion. The absence of any peak at $m/z\ 314.1$ confirms that this is the monoisotopic peak (the lightest isotopologue), not a higher-charge isotope peak. This pattern is fully consistent with a singly charged $[\text{M+H}]^+$ ion from a compound with a molecular weight of approximately 314 Da, which is within the stated 200–600 Da range.

---

### Part c)

**i) Mass accuracy with the proposed (incorrect) formula, C₁₈H₂₂N₂O₃:**

Monoisotopic mass of $[\text{M+H}]^+$:
$$18(12.000) + 22(1.008) + 2(14.003) + 3(15.995) + 1.007 = 315.170\ \text{Da}$$

$$\text{mass accuracy} = \left|\frac{315.1340 - 315.1703}{315.1703}\right| \times 10^6 = \frac{0.0363}{315.170} \times 10^6 = \mathbf{115\ \text{ppm}}$$

This far exceeds the $\leq$5 ppm specification of a well-calibrated QTOF, so the proposed formula is **incorrect**.

**ii) Mass accuracy with the correct formula, C₁₇H₁₈N₂O₄:**

Monoisotopic mass of $[\text{M+H}]^+$:
$$17(12.000) + 18(1.008) + 2(14.003) + 4(15.995) + 1.007 = 315.134\ \text{Da}$$

$$\text{mass accuracy} = \left|\frac{315.1340 - 315.1339}{315.1339}\right| \times 10^6 = \frac{0.0001}{315.134} \times 10^6 \approx \mathbf{0.3\ \text{ppm}}$$

This is excellent agreement, fully consistent with a well-calibrated QTOF.

**Could a quadrupole distinguish the two formulas?** No. Both candidate formulas have a nominal (integer) $[\text{M+H}]^+$ mass of 315 Da. Their exact masses differ by only 36.4 mDa = 0.036 Da, which is far smaller than the $\approx$1 Da unit resolution of a quadrupole mass filter. A quadrupole would report both as $m/z\ 315$ and could not determine which formula is correct. High mass accuracy from a QTOF (or other high-resolution analyzer) is essential to discriminate between these candidates.

---

### Part d)

**i) Recommendation: QqQ in MRM mode.**

The analytical goal has shifted from identification (unknown characterization) to routine targeted quantitation at trace levels. This is precisely the application for which MRM on a triple quadrupole is optimized. MRM provides detection limits 100–1,000× lower than full-scan acquisition by focusing dwell time entirely on the target transitions. The three-criteria selectivity of MRM (retention time + precursor $m/z$ + product $m/z$) ensures confident identification even in a complex pharmaceutical matrix. A QTOF in DDA mode would provide lower sensitivity for these known, trace-level targets and is not the appropriate tool for routine quantitative monitoring.

**ii)** The QTOF-DDA experiment provides all the information needed to build the MRM method:
- **Precursor $m/z$** for each impurity (from the MS¹ exact mass): converted to the nominal $m/z$ value used in Q1.
- **Product ion $m/z$ values** and relative abundances (from the MS² spectra): used to select the most abundant and most specific fragment ion as the quantifier transition, and secondary fragments as qualifier transitions.
- **LC retention times**: used to define narrow MRM acquisition windows, which reduces background and allows the instrument to cycle through many transitions within a single run.
- **Relative collision energy** from the DDA fragmentation: provides a starting point for optimizing CID conditions in q2.

---

### Part e)

**Correct answer: option 2.**

*"The TOF analyzer detects all ions simultaneously in every acquisition cycle, providing complete spectral data at every time point without the sensitivity penalty of scanning."*

A quadrupole filter is a scanning instrument: it transmits one $m/z$ value at a time and discards all others. In full-scan mode, it spends only $\sim 1/N$ of its time at any given $m/z$ value, resulting in a significant sensitivity penalty for discovery experiments. The TOF, by contrast, is a multichannel instrument: all ions are accelerated simultaneously and separated by flight time, so a complete mass spectrum is recorded in every acquisition event. This means no ions are discarded, full spectral information is available at every time point across the chromatogram, and the sensitivity for full-scan experiments is substantially higher than a scanning quadrupole. This property is the primary reason TOF (and Orbitrap) instruments are preferred for discovery LC-MS.

---

## Acknowledgements

This document was created with assistance from Claude Sonnet 4.6.