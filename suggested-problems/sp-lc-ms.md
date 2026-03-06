# Suggested Problems: Liquid Chromatography–Mass Spectrometry
*Prof. Matthew F. Bush, University of Washington*

---

## Question 1: Targeted Quantitation of Neonicotinoid Pesticides in Drinking Water

A municipal water authority is developing a validated LC-QqQ-MS method to quantify [imidacloprid](https://en.wikipedia.org/wiki/Imidacloprid), a neonicotinoid insecticide, in drinking water. Imidacloprid ($\text{C}_9\text{H}_{10}\text{ClN}_5\text{O}_2$, average MW = 255.66 Da) is a polar, thermally labile compound with limited volatility. Its structure is provided on the exam.

**a)** A colleague proposes using GC-MS rather than LC-MS for this analysis. Identify **two** properties of imidacloprid that make it a poor candidate for GC-MS, and explain in each case why that property is problematic for gas chromatographic analysis.

**b)** The method uses a C18 reversed-phase column. Two compounds — imidacloprid and [acetamiprid](https://en.wikipedia.org/wiki/Acetamiprid), a structurally related neonicotinoid that lacks the ring nitrogen oxide substituent present in imidacloprid — are injected simultaneously. Predict the elution order of these two compounds from the C18 column, and explain your reasoning in terms of the dominant intermolecular interactions that govern reversed-phase retention.

**c)** The analyst uses $^{13}$C$_5$-imidacloprid (five carbon atoms replaced with $^{13}$C) as an internal standard. This compound co-elutes exactly with imidacloprid on the C18 column, despite having a molecular weight 5 Da higher. Explain why the labeled and unlabeled compounds have the same retention time, and explain how the mass spectrometer distinguishes them despite their co-elution.

**d)** The method uses MRM detection. The primary MRM transition for imidacloprid is $m/z\ 256.1 \rightarrow 175.1$.

- **i)** Identify what type of ion gives rise to the precursor at $m/z\ 256.1$, and write its ionic formula. *(Hint: the monoisotopic mass of imidacloprid, using the $^{35}$Cl isotopologue, is 255.05 Da.)*
- **ii)** Describe the sequence of instrumental events that occur between the ion source and the detector in a QqQ operating in MRM mode that result in detection of the product ion at $m/z\ 175.1$.
- **iii)** A signal is recorded only when three independent criteria are simultaneously satisfied. List all three.

**e)** Calibration standards are prepared by spiking known concentrations of imidacloprid into Milli-Q water, with a fixed concentration of $^{13}$C$_5$-imidacloprid internal standard added to each. The analytical response is the **peak area ratio** (imidacloprid signal ÷ internal standard signal). The following data are obtained:

| Imidacloprid Concentration (ng/mL) | Peak Area Ratio |
|---|---|
| 0.0 | 0.010 |
| 1.0 | 0.511 |
| 2.5 | 1.260 |
| 5.0 | 2.510 |
| 10.0 | 5.012 |

Using linear regression through all five data points, determine the calibration equation (slope and intercept). Then calculate the imidacloprid concentration in a drinking water sample that yields a peak area ratio of 1.26. Show your work.

**f)** To evaluate the effect of matrix composition on quantitation, the analyst prepares spiked samples in two matrices. All samples contain 5.0 ng/mL imidacloprid; $^{13}$C$_5$-IS was added at the same concentration to all samples.

| Matrix | Imidacloprid Signal (counts) | IS Signal (counts) | Peak Area Ratio | Calculated Concentration (ng/mL) |
|---|---|---|---|---|
| Milli-Q water | 285,000 | 113,800 | 2.505 | 4.99 |
| Surface water | 171,000 | 68,200 | 2.507 | 4.99 |

- **i)** The imidacloprid signal is approximately 40% lower in the surface water matrix than in Milli-Q water at the same analyte concentration. What phenomenon explains this reduction, and what is its mechanistic basis in ESI?
- **ii)** Despite the large difference in raw signal, the calculated concentrations are essentially identical in both matrices. Using the data in the table, explain quantitatively why the peak area ratio approach corrects for this effect.
- **iii)** Why is it essential that the internal standard be added to the sample **before** any sample preparation steps (e.g., solid-phase extraction, filtration), rather than immediately before injection?

**g)** Which statement **best** describes why MRM detection achieves lower detection limits than full-scan acquisition for a targeted analyte? *(circle one)*

- The quadrupole mass filter transmits ions more efficiently at all $m/z$ values in MRM mode
- By fixing Q1 and Q3 at specific $m/z$ values, the instrument dwells on the target transition for nearly 100% of acquisition time, greatly increasing the duty cycle for those ions
- MRM mode eliminates the need for chromatographic separation, increasing the amount of analyte reaching the detector
- MRM acquisition uses a longer drift tube, which increases the time-of-flight and therefore the signal intensity

---

## Question 2: Discovery LC-MS of Unknown Impurities in a Pharmaceutical Intermediate

A process chemist observes two unexpected peaks in the HPLC chromatogram of a synthetic intermediate. The masses and identities of the impurities are unknown. The analyst decides to use LC-QTOF-MS in data-dependent acquisition mode to characterize them.

**a)** The synthetic intermediate and its impurities are all polar, non-volatile compounds with molecular weights in the range 200–600 Da. Explain why ESI is the appropriate ionization method for this analysis. Your answer must address **both** of the following:

- **i)** Why ESI is compatible with liquid chromatography at the instrument-design level — specifically, how it solves the interface problem — not simply that it is a "soft" technique.
- **ii)** Why EI ionization would be inappropriate for these analytes.

**b)** The analyst sets up a DDA experiment in which the QTOF cycles between MS$^1$ survey scans and MS$^2$ fragmentation scans, selecting the top 10 most intense precursor ions per MS$^1$ cycle. Each complete DDA cycle takes 1.1 seconds.

- **i)** Describe, step by step, what the instrument does during a single DDA cycle. Be specific about what is measured in each scan type and how the instrument decides which precursors to fragment.
- **ii)** One of the unknown impurities produces an LC peak with a width at half-maximum (FWHM) of approximately 18 seconds. Estimate the number of complete DDA cycles acquired across this FWHM window. Is this sampling density sufficient for reliable data? Explain briefly.
- **iii)** The MS$^1$ spectrum of one impurity shows a dominant ion at $m/z\ 315.1$, a smaller peak at $m/z\ 316.1$, and a very small peak at $m/z\ 317.1$. No significant peak is observed at $m/z\ 314.1$. Based on this isotope pattern, what charge state does the dominant ion carry? Is it likely to be a singly charged $[\text{M+H}]^+$ ion or a multiply charged ion? Explain your reasoning.

**c)** The QTOF measures the dominant precursor ion at $m/z\ 315.1340$. The analyst proposes the molecular formula $\text{C}_{18}\text{H}_{22}\text{N}_2\text{O}_3$ for the neutral molecule, which gives a calculated monoisotopic $[\text{M+H}]^+$ mass of 315.1703 Da.

- **i)** Calculate the mass accuracy of this measurement in ppm. Is this result consistent with the proposed formula? Explain.

- **ii)** The analyst reconsiders and finds that the formula $\text{C}_{17}\text{H}_{18}\text{N}_2\text{O}_4$ (calculated monoisotopic $[\text{M+H}]^+$ = 315.1339 Da) gives a much better match. Recalculate the mass accuracy for this formula. The two candidate formulas have the same nominal mass (315 Da) and differ in exact mass by 36.4 mDa. Would a quadrupole mass filter operating at unit resolution be able to distinguish between these two formulas? Explain.

**d)** Having characterized the two impurities by QTOF-DDA, the process chemist now needs to routinely monitor their concentrations at trace levels ($<$0.1% relative to the main compound) in future batches.

- **i)** Which instrument platform and acquisition mode would you recommend for this routine monitoring application? Justify your recommendation.
- **ii)** List the specific information obtained from the QTOF-DDA experiment that is directly used to set up the routine monitoring method on the recommended instrument.

**e)** Which statement **best** describes the key advantage of a time-of-flight analyzer over a quadrupole filter in a discovery LC-MS experiment? *(circle one)*

- The TOF analyzer scans through each $m/z$ value sequentially and is therefore more thorough than a quadrupole
- The TOF analyzer detects all ions simultaneously in every acquisition cycle, providing complete spectral data at every time point without the sensitivity penalty of scanning
- The TOF analyzer is better suited for MRM acquisition because it can monitor many transitions simultaneously
- The TOF analyzer requires lower vacuum pressures than the quadrupole, reducing instrument cost

---

## Acknowledgements

This document was created with assistance from Claude Sonnet 4.6.