# Solutions to Suggested Problems: Gas Chromatography and GC-MS
*Prof. Matthew F. Bush, University of Washington*

---

## Question 1 Solutions

### Part a) Retention Factors

The retention factor $k$ is the ratio of the time a solute spends in the stationary phase to the time it spends in the mobile phase:

$$k = \frac{t_r - t_m}{t_m}$$

The void time is read from the unretained solvent peak: $t_m = 0.80$ min.

**Benzene** (worked example):

$$k_\text{benz} = \frac{4.00 - 0.80}{0.80} = \frac{3.20}{0.80} = 4.00$$

**Toluene:**

$$k_\text{tol} = \frac{5.60 - 0.80}{0.80} = \frac{4.80}{0.80} = 6.00$$

**Ethylbenzene:**

$$k_\text{eth} = \frac{8.00 - 0.80}{0.80} = \frac{7.20}{0.80} = 9.00$$

Note that $k$ is dimensionless — the units of time cancel. As expected, ethylbenzene has the largest $k$, reflecting its longest residence in the stationary phase.

---

### Part b) Selectivity Factors

$$\alpha = \frac{k_2}{k_1} \quad (k_2 > k_1,\ \text{so}\ \alpha \geq 1)$$

**Benzene/toluene pair:**

$$\alpha_{\text{tol/benz}} = \frac{6.00}{4.00} = 1.50$$

**Toluene/ethylbenzene pair:**

$$\alpha_{\text{eth/tol}} = \frac{9.00}{6.00} = 1.50$$

Both pairs have identical selectivity factors despite ethylbenzene having a substantially longer absolute retention time. This illustrates that $\alpha$ reflects *differential* interaction with the stationary phase, not absolute retention. The consistent $\alpha = 1.50$ across the series is characteristic of a homologous series — each additional $-\text{CH}_2-$ group contributes a comparable increment to London dispersion interactions with the PDMS phase.

---

### Part c) Peak-to-Peak Resolution

$$R_{pp} = \frac{t_{r,2} - t_{r,1}}{\dfrac{w_{b,1} + w_{b,2}}{2}}$$

**Benzene/toluene:**

$$R_{pp} = \frac{5.60 - 4.00}{\dfrac{0.60 + 0.72}{2}} = \frac{1.60}{0.66} = 2.4$$

**Toluene/ethylbenzene:**

$$R_{pp} = \frac{8.00 - 5.60}{\dfrac{0.72 + 0.88}{2}} = \frac{2.40}{0.80} = 3.0$$

Both pairs are baseline resolved. Baseline separation requires $R_{pp} \geq 1.5$, so values of 2.4 and 3.0 indicate good separation with comfortable margin — both peaks can be reliably integrated and quantified without overlap.

---

### Part d) Boiling Point and Retention Time

On a nonpolar stationary phase like PDMS, the dominant analyte–stationary phase interaction is **London dispersion forces**. These forces arise from transient, induced dipoles and scale with molecular polarizability — larger molecules with more electrons are more polarizable and therefore experience stronger interactions with the stationary phase.

Boiling point also reflects the strength of intermolecular attractions: a higher boiling point means stronger intermolecular forces and lower volatility. Because both boiling point and GC retention time on a nonpolar column are governed by the same underlying London dispersion interactions, they correlate strongly for a homologous series like benzene → toluene → ethylbenzene. Each additional $-\text{CH}_2-$ group increases polarizability, strengthening interaction with PDMS and raising both the boiling point and the retention time.

---

### Part e) Effect of Switching to a Polar Stationary Phase

Switching to a polar stationary phase would **decrease** $\alpha$ for these three nonpolar analytes.

By the *like dissolves like* principle, solutes interact most strongly with a stationary phase of similar polarity. All three analytes are nonpolar aromatics — none carries a permanent dipole, and none engages in hydrogen bonding. On a polar (cyanopropyl-modified) phase, all three would interact weakly and *similarly*; the phase cannot discriminate among them on the basis of polarity because none of them is polar. The small differences in London dispersion interactions that produce $\alpha = 1.50$ on PDMS would be diminished on a polar phase, driving $\alpha$ toward 1 and potentially worsening the separation.

A polar stationary phase is better suited to mixtures containing analytes with *different* polarities (e.g., alcohols vs. hydrocarbons), where it selectively retains the polar components.

---

### Part f) Methanol Elution Relative to Benzene

Methanol will elute **before** benzene. Two independent factors both favor early elution:

1. **Volatility.** Methanol (bp 65 °C) is more volatile than benzene (bp 80 °C). In GC, more volatile compounds prefer the gas-phase mobile phase, spending proportionally less time in the stationary phase and eluting sooner.

2. **Weak stationary-phase interaction.** Methanol is polar and capable of hydrogen bonding, but nonpolar PDMS cannot act as a hydrogen-bond acceptor and engages in only weak London dispersion interactions with methanol — much weaker than with the aromatic $\pi$-system of benzene. Because methanol interacts weakly with PDMS, its distribution constant $D = [\text{solute}]_\text{stat}/[\text{solute}]_\text{mobile}$ is small, and it spends little time retained in the phase.

Both effects independently predict that methanol elutes before benzene.

---

### Part g) Multiple Choice

**Correct answer: second option.**

> All analytes spend the same total time in the mobile phase regardless of their interactions with the stationary phase; $t_m$ is simply the time it takes the carrier gas to traverse the column.

The void time is a property of the instrument — the time required for carrier gas to flow from injector to detector at a given flow rate. Every analyte, regardless of polarity or size, is swept along at exactly the carrier-gas velocity when it is in the mobile phase. A strongly retained analyte spends *additional* time immobilized in the stationary phase on top of $t_m$; it does not slow down while in the mobile phase.

**Why the distractors are wrong:**
- *Option 1*: Molecular weight influences diffusion coefficients and peak width, but analytes all travel at carrier-gas velocity when in the mobile phase, regardless of MW.
- *Option 3*: Column temperature affects partitioning equilibria (and therefore $k$), but does not change that $t_m$ is fixed by column dimensions and flow rate.
- *Option 4*: Carrier-gas flow rate is held constant; it does not adjust per analyte.

---

## Question 2 Solutions

### Part a) Injection Mode

**Splitless injection** should be used.

At ~5 ppb, chlorpyrifos is present at trace levels near the regulatory threshold. Splitless injection directs nearly all vaporized sample onto the column, maximizing the analyte mass reaching the detector. Split injection would divert most of the sample to waste, reducing sensitivity and potentially preventing reliable detection at this concentration.

---

### Part b) Block Diagram

The instrument chain, in order:

$$\boxed{\text{Injector}} \xrightarrow{\ \text{capillary column (oven)}\ } \boxed{\text{Transfer Line}} \longrightarrow \boxed{\text{EI Ion Source}} \longrightarrow \boxed{\text{Quadrupole}} \longrightarrow \boxed{\text{Detector}}$$

**Transfer line:** A short, heated capillary connecting the GC column exit (near atmospheric pressure) to the MS ion source (~$10^{-5}$–$10^{-6}$ torr). It is maintained at elevated temperature to prevent analyte condensation. No enrichment interface is required because capillary-column carrier-gas flow rates (~1 mL/min) are directly compatible with the MS vacuum system.

---

### Part c) Hard Ionization — Limitation and Advantage

EI is a **hard ionization** technique because the primary electrons (70 eV) deposit far more energy into the analyte than is required for ionization (~10 eV). The excess energy drives extensive fragmentation of the molecular ion $M^{+\cdot}$:

$$M + e^-_1(70\ \text{eV}) \rightarrow M^{+\cdot} + e^-_2 + e^-_1(\ll 70\ \text{eV}) \rightarrow \text{fragment ions}$$

**Limitation:** The molecular ion may be weak or absent for compounds that fragment readily. For chlorpyrifos, the molecular ion at $m/z$ = 314 contributes only 35% relative abundance, making direct molecular-weight confirmation less prominent than in a soft-ionization spectrum.

**Advantage:** Fragmentation is highly reproducible because the 70 eV standard was established specifically to ensure consistent spectra across instruments and laboratories. This reproducibility underpins the NIST and Wiley spectral libraries, enabling confident identification of unknowns in a complex food matrix by library searching — which would not be possible with soft ionization techniques that yield only intact molecular ions.

---

### Part d) Ion Selection

| Role | Ion ($m/z$) | Justification |
|---|---|---|
| **Quantifier** | 197 | Base peak (100% relative abundance); highest signal-to-noise ratio for building the calibration curve |
| **Qualifier** | 314 | Molecular ion; confirms molecular weight and provides structural specificity alongside retention time |
| **Exclude** | 97 | Low-mass fragment; most susceptible to interference from co-extracted matrix compounds in a complex apple extract |

The quantifier should be the most abundant ion to maximize sensitivity. The molecular ion ($m/z$ 314) serves effectively as a qualifier — its presence and ratio to the quantifier confirm identity beyond retention time alone. Low-mass fragments like $m/z$ 97, while reasonably abundant (62%), are less structurally specific because many unrelated compounds produce ions in the low-mass range, increasing the risk of interference.

---

### Part e) Quantitative Calibration

**Step 1: Subtract the blank signal from all standards and the unknown.**

$$S_\text{corrected} = S_\text{raw} - S_\text{blank} = S_\text{raw} - 420$$

| Concentration (ppb) | Raw Signal (counts) | Blank-corrected Signal (counts) |
|---|---|---|
| 0 | 420 | 0 |
| 1.0 | 4,850 | 4,430 |
| 2.5 | 11,200 | 10,780 |
| 5.0 | 22,180 | 21,760 |
| 10.0 | 44,400 | 43,980 |

**Step 2: Perform linear regression on the blank-corrected data.**

Linear regression through all five points yields:

$$S_\text{corrected} = 4396\, c - 75 \qquad (R^2 = 0.99995)$$

where $c$ is concentration in ppb. The near-zero intercept and excellent $R^2$ confirm that the response is linear across the calibration range.

**Step 3: Solve for the unknown concentration.**

$$S_\text{unknown, corrected} = 18{,}600 - 420 = 18{,}180 \text{ counts}$$

$$c = \frac{S_\text{corrected} + 75}{4396} = \frac{18{,}180 + 75}{4396} = \frac{18{,}255}{4396} \approx \boxed{4.2 \text{ ppb}}$$

---

### Part f) Isotope Dilution

**Two reasons isotope dilution improves accuracy over external calibration:**

1. **Corrects for sample preparation losses.** Extraction and cleanup steps inevitably lose some analyte. Because $^{13}$C$_4$-chlorpyrifos is chemically identical to the unlabeled compound, it experiences the same fractional losses at every step. Quantitation is based on the *ratio* of unlabeled to labeled signal, so proportional losses cancel.

2. **Corrects for matrix-induced signal variation.** Complex apple extracts contain co-extracted components that can suppress or enhance ionization. Because the labeled and unlabeled analytes co-elute and ionize together, any matrix effect shifts both signals by the same factor, leaving their ratio — and therefore the calculated concentration — unchanged.

**Why before extraction?** Adding the internal standard after extraction allows it to correct only for variability introduced at or after the injection step. Losses during extraction (e.g., incomplete partitioning, adsorption to glassware) would affect only the unlabeled analyte, biasing the ratio. Adding before extraction ensures the labeled standard tracks the unlabeled analyte through every step of sample preparation.

---

### Part g) Quadrupole vs. TOF Comparison Table

| Property | Quadrupole | Time-of-Flight |
|---|---|---|
| Typical acquisition speed (spectra/s) | 2–20 | Tens to hundreds |
| Mass accuracy | Unit resolution (~0.3 Da) | High resolution (low-ppm accuracy possible) |
| SIM acquisition mode available? | Yes — standard capability | Not typical; TOF collects full spectra by default |
| Full-scan sensitivity | Moderate (scanning — only one $m/z$ transmitted at a time) | High (all ions collected simultaneously) |
| Compatibility with NIST EI spectral library | Excellent — libraries built from unit-resolution data | Excellent; additionally enables elemental composition confirmation |

---

### Part h) Analyzer Choice for SIM Compliance Method

**The quadrupole** is the more straightforward choice.

SIM is a native operating mode of the quadrupole mass filter: the RF/DC voltages are held constant to transmit only the target $m/z$ values, maximizing dwell time and sensitivity. Regulatory methods that specify SIM acquisition were almost certainly developed and validated using quadrupole instruments. TOF analyzers do not offer a true SIM mode — they acquire full spectra by default and achieve targeted sensitivity by extracting specific ion chromatograms in software post-acquisition. Implementing a TOF-based workflow to satisfy a regulatory specification written for SIM requires additional method revalidation, making the quadrupole the lower-friction compliance option.

---

### Part i) Multiple Choice

**Correct answer: second option.**

> Full-scan data can be searched retrospectively against spectral libraries to identify unexpected compounds not included in the original target list.

Because a complete spectrum is recorded at every time point, full-scan data can be re-interrogated after collection to search for any compound in the NIST or Wiley library — including pesticides, adulterants, or contaminants that were not anticipated when the method was designed. This is the defining strength of full-scan acquisition for exploratory screening.

**Why the distractors are wrong:**
- *Option 1*: Full-scan is *less* sensitive than SIM for targeted analytes — this is the central tradeoff of the two modes.
- *Option 3*: The transfer line is a hardware interface required regardless of acquisition mode.
- *Option 4*: TOF analyzers collect full spectra by default, but full-scan mode is also available on quadrupole instruments; neither mode is exclusive to a particular analyzer type.

---

## Acknowledgements

This document was created with assistance from Claude Sonnet 4.6.