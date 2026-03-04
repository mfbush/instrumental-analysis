# Gas Chromatography/Mass Spectrometry

## Learning Objectives
*At the conclusion of in-class and outside learning, participants will be able to:*
- Explain the fundamental principles of gas chromatography and mass spectrometry as individual techniques and how they complement each other when combined.
- Describe the key components of a GC-MS instrument, including injection systems, columns, interfaces, ionization sources, mass analyzers, and detectors.
- Compare and contrast a quadrupole mass filter and a time-of-flight mass analyzer in the context of GC-MS.
- Describe the process of using a spectral library for qualitative applications of GC-MS.
- Select and justify the appropriate acquisition mode (full-scan vs. selected ion monitoring) for a given GC-MS application, and explain the tradeoff between spectral information content and sensitivity.
- Select appropriate ions for quantitation in GC-MS, distinguish between quantifier and qualifier ions, and explain how isotope dilution improves accuracy.

## Why Combine Gas Chromatography and Mass Spectrometry?

Although some analyses yield simple gas chromatograms (consider the analysis of benzene and toluene from petroleum, which was performed under conditions where most simple hydrocarbons were not retained), others yield complex chromatograms.

![complex-chromatograms](https://upload.wikimedia.org/wikipedia/commons/c/c9/NonBiodegradedAndBiodegraded.png)

**Figure 1.** Examples of non-biodegraded crude oil (top) and a heavily biodegraded one (bottom) with the unresolved complex mixture (UCM) area indicated. Both chromatograms have been normalized so that their integrals are equal to unity. Reproduced from [Wikipedia](https://en.wikipedia.org/wiki/Unresolved_complex_mixture).

### In congested chromatograms:
- Using a single channel detector, not all chromatographic features are adequately resolved.
- Using only retention time, it is often not possible to unambiguously identify the molecule associated with each feature.

## Mass Spectrometry Offers:
- **Fast detection**
    - In conventional GC, peaks have widths around 2 to 10 seconds.
    - Low-cost quadrupole mass filters typically support acquisition of 2–20 mass spectra per second.
    - Time-of-flight mass analyzers typically support acquisition of tens to hundreds of mass spectra per second.
    - Even for fast GC with sub-second peaks, it is possible to sample individual chromatographic peaks many times.
- **Multichannel, analyte-specific detection**
    - Even unit-mass resolution analyzers offer hundreds of channels per mass spectrum.
    - Mass spectra depend on the identity of the analyte.
- **Great sensitivity**
    - Detectors for mass spectrometry can be very sensitive. This is particularly advantageous for GC, since very little material can be loaded onto capillary columns.

## Instrument Architecture

![GC-MS schematic](https://upload.wikimedia.org/wikipedia/commons/b/bf/Electron_ionization_GC-MS.png)

**Figure 2.** Schematic of an electron ionization GC-MS instrument. Reproduced from [Wikipedia](https://en.wikipedia.org/wiki/Gas_chromatography%E2%80%93mass_spectrometry).

### Injection System
The sample is introduced as a solution via a syringe through a heated **injector port**, where it is vaporized instantly. Two common modes:
- **Split injection**: Most of the vaporized sample is vented; only a fraction enters the column. Used for concentrated samples to avoid overloading the column.
- **Splitless injection**: Nearly all vapor is directed onto the column. Used for trace analysis where sensitivity is critical.

### Capillary Column
GC-MS is almost exclusively performed with fused-silica capillary columns (typically 15–60 m long, 0.18–0.32 mm inner diameter). The column is housed in a temperature-programmable oven, allowing the carrier gas flow and temperature ramp to be optimized for the analyte mixture.

### Transfer Line (Interface)
The column exit must be connected to the mass spectrometer, which operates under high vacuum (~10⁻⁵ to 10⁻⁶ torr). The **transfer line** is a short, heated capillary that carries eluting analytes directly into the ion source while maintaining temperature to prevent condensation. Modern capillary GC-MS requires no additional enrichment interface — the low flow rates of capillary columns are directly compatible with the vacuum system.

### Ionization Source, Mass Analyzer, and Detector
Analyte vapors entering the source are ionized by electron ionization (reviewed below). The resulting ions are extracted into the mass analyzer (quadrupole or TOF) and detected, typically by a discrete dynode electron multiplier or multichannel plate detector.

## Recall from Recent Classes

### Gas Chromatography

The *retention factor* in gas chromatography is the ratio between the time that an analyte spends partitioned in the stationary phase to the time that analyte spends in the carrier gas. Therefore, the analyte must be stable as a gaseous vapor during experiments.
- **Volatility**: Analytes must have sufficient vapor pressure at GC operating temperatures. Generally, analytes should have boiling points below approximately 400–450 °C to be analyzed by conventional GC.
- **Thermal Stability**: Analytes must remain chemically stable at the temperatures required for vaporization and separation. Compounds that decompose or rearrange under heat are poor candidates.
- **Molecular Weight**: Typically, GC works best for compounds with molecular weights below 500–600 Da. Larger molecules often have insufficient volatility.
- **Functional Groups**: The presence of certain functional groups (like -OH, -COOH, -NH₂) can decrease volatility and create unwanted column interactions through hydrogen bonding.
- **Derivatization Potential**: Some non-volatile compounds can be chemically modified (derivatized) to increase volatility and improve GC performance.

### Electron Impact (EI) Ionization
In electron impact (EI) ionization, the analyte $M$ (specifically, the vapor of the analyte) is reacted with a high-energy electron (the primary electron, $e_{1}^{-}$). This yields the radical cation of the molecule and a secondary electron ($e_{2}^{-}$):

$M + e_{1}^{-}(70 \text{ eV}) \rightarrow M^{+\cdot} + e_{2}^{-} + e_{1}^{-}(\ll 70 \text{ eV})$

Some notes:
- This technique also analyzes gaseous vapors.
- EI is a **hard ionization** technique — it yields the molecular ion as well as fragment ions. In contrast, MALDI and ESI are soft ionization techniques that yield primarily the molecular ion.
- EI is a great match for analyzing the eluent of gas chromatography.

## Quadrupole vs. Time-of-Flight in GC-MS

Students entering this section have studied both analyzer types in detail. The question here is: *what does each choice mean for a GC-MS experiment?*

| Property | Quadrupole | Time-of-Flight |
|---|---|---|
| Acquisition speed | 2–20 spectra/s | Tens to hundreds of spectra/s |
| Mass accuracy | Unit resolution (~0.3 Da) | High resolution (low-ppm accuracy possible) |
| Full-scan sensitivity | Moderate (scanning instrument) | High (multichannel, all ions collected simultaneously) |
| SIM capability | Yes — well-established | Not typical; TOF collects full spectra by default |
| Cost | Lower | Higher |
| Library searching | Excellent — standard EI libraries built on unit-resolution spectra | Excellent plus elemental composition confirmation |

**Key synthesis questions to consider:**
- A quadrupole operated in SIM mode can achieve very low detection limits, but at the cost of spectral information. A TOF running in full-scan mode collects complete spectra at every time point — how does this change the analytical options available after data collection?
- EI spectral libraries (NIST, Wiley) were built predominantly from unit-resolution quadrupole data. Does high mass accuracy from a TOF improve library matching, or complicate it?
- For a targeted environmental method requiring compliance with a regulatory method that specifies SIM acquisition, which analyzer is the natural choice?

## Electron Impact Spectra

### Examples
- [Benzene](https://webbook.nist.gov/cgi/cbook.cgi?Name=benzene&Units=SI&cMS=on)
- [Toluene](https://webbook.nist.gov/cgi/cbook.cgi?Name=toluene&Units=SI&cMS=on)
- [Cholesterol](https://webbook.nist.gov/cgi/cbook.cgi?Name=cholesterol&Units=SI&cMS=on)
- [Dichlorvos](https://webbook.nist.gov/cgi/cbook.cgi?ID=62-73-7&Units=SI)

### Spectral Libraries

Although many electron impact spectra can be assigned based on features and fragmentation patterns, most spectra are assigned through comparisons with spectral libraries, which contain spectra obtained for pure standards.
- **NIST/EPA/NIH Mass Spectral Library (NIST).** Contains over 300,000 EI mass spectra; most widely used in commercial and research settings; includes retention indices for many compounds.
- **Wiley Registry of Mass Spectral Data.** Contains approximately 775,000 spectra; often combined with NIST as the "Wiley-NIST" combined library.

### Scoring Against Libraries

1. **Direct Matching Factor (MF)**: Calculates similarity between the unknown and library spectra using a weighted dot-product algorithm. Scores range from 0–999; scores >900 suggest excellent matches.
2. **Reverse Matching Factor (RMF)**: Similar to MF but ignores peaks present in the unknown but absent in the library spectrum. Useful when the unknown spectrum contains contaminants or co-eluting compounds.
3. **Probability Score**: Estimates the likelihood that the match is correct based on statistical analysis of similarity scores and the uniqueness of the spectral pattern.
4. **Retention Index Matching**: When available, compares the experimental retention index to library values. Can significantly improve identification confidence when combined with spectral matching.

## Acquisition Modes and Quantitative Applications of GC-MS

### Acquisition Mode Selection

The choice of acquisition mode is one of the most consequential decisions in method development:

- **Full-scan mode**: The mass analyzer scans across a defined *m*/*z* range (e.g., 50–500) repeatedly throughout the run. Every spectrum is recorded, enabling retrospective library searching and the detection of unexpected compounds. Sensitivity is lower because a scanning analyzer spends only a fraction of its time at any given *m*/*z*.
- **Selected Ion Monitoring (SIM)**: The quadrupole is fixed at one or a small number of *m*/*z* values. Because dwell time per ion is much longer, sensitivity can be 10–100× greater than full-scan. The tradeoff is that spectral information is sacrificed — only the monitored ions are recorded.

**Rule of thumb**: Use full-scan for unknowns, discovery, and library-searchable data. Use SIM when you know your targets and need maximum sensitivity in a complex matrix.

### Ion Selection for Quantitation

When quantifying a target analyte in SIM or when extracting ion chromatograms from full-scan data:

- **Quantifier ion**: The most abundant or characteristic fragment ion, used to build the calibration curve. Should be selected for high abundance and low background interference.
- **Qualifier ions**: Secondary ions monitored alongside the quantifier. The ratio of qualifier to quantifier ion intensities must fall within ±20% of reference standards to confirm identity — providing a second dimension of specificity beyond retention time.
- The molecular ion (M⁺·) is often avoided as a quantifier in EI because it may be weak or absent for many compound classes.
- Column bleed ions (e.g., *m*/*z* 73, 147, 207, 281, 355 for siloxane columns) should be excluded from quantitation ion lists.

### Calibration Approaches

- **External calibration**: Standard curves of analyte concentrations prepared in a clean solvent.
- **Standard addition**: Known amounts of target analyte are spiked into the sample matrix to account for matrix effects.
- **Isotope dilution**: An isotopically labeled analog (e.g., ²H or ¹³C) of the target is added as an internal standard before extraction. Because the labeled and unlabeled forms are chemically identical but distinguishable by mass, this approach compensates for losses during sample preparation and is the most accurate quantitative strategy available.

## Acknowledgements

These notes were revised for clarity and accessibility with assistance from Claude 4.6 Sonnet.