# Suggested Problems: Gas Chromatography and GC-MS
*Prof. Matthew F. Bush, University of Washington*

---

## Question 1: Chromatographic Separations — Quantitative Analysis of a Fuel Sample

A quality control laboratory is analyzing a gasoline blend for three regulated aromatic hydrocarbons: benzene, toluene, and ethylbenzene. The sample was diluted 1:50 in hexane and injected onto a non-polar capillary column (30 m × 0.25 mm × 0.25 μm DB-5). The following data were read from the resulting chromatogram:

| Compound | Retention Time (min) | Peak Width at Base, $w_b$ (min) |
|---|---|---|
| Solvent (hexane, unretained) | 0.80 | — |
| Benzene | 4.00 | 0.60 |
| Toluene | 5.60 | 0.72 |
| Ethylbenzene | 8.00 | 0.88 |

**a)** Calculate the retention factor $k$ for each aromatic analyte. Show your work for benzene, then report values for toluene and ethylbenzene.

**b)** Calculate the selectivity factor $\alpha$ for each adjacent pair of analytes: benzene/toluene and toluene/ethylbenzene.

**c)** Calculate the peak-to-peak resolution $R_{pp}$ for the benzene/toluene pair and for the toluene/ethylbenzene pair. For each pair, state whether the peaks are baseline resolved.

**d)** All three analytes are nonpolar aromatics analyzed on a nonpolar stationary phase (DB-5), yet they elute at significantly different times. The boiling points are: benzene 80 °C, toluene 111 °C, ethylbenzene 136 °C. Explain why boiling point correlates with retention time on a nonpolar GC column. Your answer should reference the dominant intermolecular force and the concept of polarizability.

**e)** A colleague suggests switching to a more polar stationary phase (e.g., one modified with cyanopropyl groups) to improve the separation. Predict whether this change would *increase* or *decrease* $\alpha$ for these three nonpolar aromatics relative to the DB-5 column, and justify your answer using the *like dissolves like* principle.

**f)** The laboratory also needs to monitor a trace contaminant — methanol (bp 65 °C) — present at much lower concentrations than the aromatics. Methanol is significantly more polar than benzene or toluene. Predict whether methanol will elute *before* or *after* benzene on this nonpolar DB-5 column, and explain your reasoning in terms of both volatility and stationary phase interactions.

**g)** Which of the following best explains why the void time $t_m$ is the same for every analyte, regardless of how strongly it interacts with the stationary phase? (circle one)

- All analytes have the same molecular weight and therefore travel at the same speed in the gas phase
- All analytes spend the same total time in the mobile phase regardless of their interactions with the stationary phase; $t_m$ is simply the time it takes the carrier gas to traverse the column
- The column temperature is constant, so all analytes experience the same driving force
- The carrier gas flow rate adjusts automatically to ensure equal mobile-phase residence times

---

## Question 2: GC-MS Instrumentation and Quantitative Analysis of Pesticide Residues

A food safety laboratory is developing a GC-MS method to quantify chlorpyrifos, an organophosphate pesticide, in apple extracts. The method uses electron ionization with a quadrupole mass analyzer.

**a)** The analyst must choose between split and splitless injection. Chlorpyrifos is present at approximately 5 ppb in the extract, near the regulatory action level. Which injection mode should be used, and why?

**b)** Draw a block diagram of the complete GC-MS instrument, labeling: injector, capillary column (in oven), transfer line, EI ion source, mass analyzer, and detector. Include a brief annotation of the function of the transfer line.

**c)** Electron ionization is described as a *hard* ionization technique. Explain what this means and why this property is simultaneously a limitation and an advantage for the analysis of chlorpyrifos in a complex food matrix.

**d)** The analyst consults the NIST spectral library and identifies three candidate ions from the EI spectrum of chlorpyrifos, with the following relative abundances:

| Ion ($m/z$) | Identity | Relative Abundance |
|---|---|---|
| 97 | Low-mass fragment | 62% |
| 197 | Loss of diethyl thiophosphate | 100% (base peak) |
| 314 | Molecular ion (M$^{+\cdot}$) | 35% |

Which ion would you designate as the **quantifier** and which as a **qualifier**? Explain your reasoning, and identify which of the three ions you would **exclude** and why.

**e)** The analyst collects the following calibration data using SIM acquisition on the quantifier ion:

| Chlorpyrifos Concentration (ppb) | Quantifier Ion Signal (counts) |
|---|---|
| 0 (solvent blank) | 420 |
| 1.0 | 4,850 |
| 2.5 | 11,200 |
| 5.0 | 22,180 |
| 10.0 | 44,400 |

Using linear regression through all five blank-corrected data points, determine the chlorpyrifos concentration (in ppb) in an apple extract that gives a signal of 18,600 counts. Show your approach clearly.

**f)** A supervisor recommends using an isotopically labeled internal standard — specifically, $^{13}$C$_4$-chlorpyrifos — added to every sample and standard *before extraction*. Explain two distinct reasons why this strategy improves accuracy relative to external calibration. Why is it important that the internal standard be added before extraction rather than just before injection?

**g)** The laboratory is considering upgrading from the quadrupole to a time-of-flight (TOF) mass analyzer. Complete the following comparison table:

| Property | Quadrupole | Time-of-Flight |
|---|---|---|
| Typical acquisition speed (spectra/s) | | |
| Mass accuracy | | |
| SIM acquisition mode available? | | |
| Full-scan sensitivity | | |
| Compatibility with NIST EI spectral library | | |

**h)** The laboratory's existing regulatory compliance method explicitly requires SIM acquisition for chlorpyrifos quantitation. Based on your table, which analyzer is the more straightforward choice for this compliance application? Briefly justify your answer.

**i)** Which statement best describes the primary advantage of full-scan acquisition over SIM for an *exploratory* food safety screen of an unknown extract? (circle one)

- Full-scan acquisition is always more sensitive than SIM for all analytes
- Full-scan data can be searched retrospectively against spectral libraries to identify unexpected compounds not included in the original target list
- Full-scan acquisition eliminates the need for a transfer line between the GC and MS
- Full-scan mode is required when using a time-of-flight analyzer

---

## Acknowledgements

This document was created with assistance from Claude Sonnet 4.6.