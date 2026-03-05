# Suggested Problems: Mass Spectrometry
*Prof. Matthew F. Bush, University of Washington*

## Question 1 — Instrument Architecture, Mass Definitions, and Isotope Distributions

Acetaminophen (C₈H₉NO₂, the active ingredient in Tylenol) is a widely used over-the-counter analgesic. Its mass spectrum is collected by GC-MS with electron ionization (EI).

*Masses for this question:* H: nominal 1, monoisotopic 1.00783 Da; C: nominal 12, monoisotopic 12.00000 Da; N: nominal 14, monoisotopic 14.00307 Da; O: nominal 16, monoisotopic 15.99491 Da.

**(a)** Draw a labeled block diagram of a mass spectrometer. Identify the ion source, mass analyzer, and detector, and write one sentence describing the function of each component.

**(b)** The *x*-axis of a mass spectrum reports *m*/*z*. Define the *m*/*z* ratio in physical terms. A peak in the EI spectrum of acetaminophen appears at *m*/*z* = 151 and is the most intense peak in the spectrum (the base peak). If this ion carries a single positive charge, what is its mass in daltons?

**(c)** Calculate the nominal mass and monoisotopic mass of neutral acetaminophen (C₈H₉NO₂). Show your work. How does the monoisotopic mass of the neutral molecule compare to the mass of the singly charged molecular ion you identified in part (b)?

**(d)** Under EI conditions, the molecular ion M⁺• is observed at the *m*/*z* value you calculated in part (c). For a different analyte — a thermally labile pharmaceutical — the GC-MS spectrum shows abundant fragment ions but *no* molecular ion peak. Propose a mechanistic explanation for the absence of the molecular ion under EI conditions.

**(e)** A polystyrene standard with approximately 200 styrene repeat units is analyzed by MALDI. The repeat unit of polystyrene is C₈H₈ (104 Da), giving an approximate formula of C₁₆₀₀H₁₆₀₂ and an average molecular weight of approximately 20,800 Da. Predict quantitatively whether the monoisotopic peak will be the most intense peak in the isotope distribution. Support your prediction with a calculation.

---

## Question 2 — Ionization Sources and the Relationship Between *m*/*z* and Neutral Mass

A surfactant manufacturer uses mass spectrometry to characterize a new poly(ethylene oxide)-based nonionic surfactant intended for use as an industrial detergent additive.

*Proton mass for this question:* 1.00728 Da.

**(a)** Explain why ESI is more appropriate than EI for characterizing this surfactant. Your answer should address (i) the physical state of the analyte required by each technique, (ii) the mechanism by which each technique produces ions, and (iii) how each technique is classified with respect to the energy deposited in the analyte.

**(b)** The positive-mode ESI spectrum of the surfactant shows two prominent peaks at *m*/*z* = 748.6 and *m*/*z* = 936.0. Both peaks arise from the same neutral PEO oligomer. Determine the charge state *z* of each peak and the neutral mass *M* of the oligomer. Show your work.

**(c)** In contrast to ESI, MALDI of the same PEO sample produces predominantly singly charged [M + H]⁺ ions. Provide a mechanistic explanation for why MALDI produces mainly singly charged ions while ESI produces multiply charged ions of the same analyte.

**(d)** A colleague proposes using MALDI instead of EI to analyze a small (MW ≈ 150 Da), volatile fragrance compound by GC-MS. The colleague argues that MALDI's soft ionization will simplify the spectrum. Critically evaluate this proposal. Is MALDI compatible with gas chromatography? Which ionization technique is more appropriate here, and why?

**(e)** For a large analyte analyzed by ESI, a [M + 3H]³⁺ ion is observed at *m*/*z* = 612.4. Calculate the neutral mass *M* of this analyte.

---

## Question 3 — Mass Analyzers, Resolving Power, and Mass Accuracy

Bisphenol A (BPA, C₁₅H₁₆O₂) is an industrial monomer used in polycarbonate plastics and epoxy resins. It is routinely monitored as an environmental contaminant by LC-MS. In positive-ion ESI, BPA forms a prominent [M + H]⁺ ion.

*Masses for this question:* H: monoisotopic 1.00783 Da; C: monoisotopic 12.00000 Da; O: monoisotopic 15.99491 Da; proton: 1.00728 Da.

**(a)** Calculate the expected monoisotopic *m*/*z* of the [M + H]⁺ ion of BPA (C₁₅H₁₆O₂). Show your work. Note: the [M + H]⁺ ion is formed by adding a proton (mass 1.00728 Da) to the neutral molecule, not a hydrogen atom.

**(b)** The [M + H]⁺ peak of BPA is measured on a quadrupole instrument at *m*/*z* = 229.1 with a full width at half maximum (FWHM) of 0.23 Da. Calculate the resolving power *R*ₚ of the quadrupole for this peak. A TOF instrument measures the same peak with a FWHM of 0.023 Da; calculate its resolving power. A suspected structural isomer has an exact [M + H]⁺ mass of 229.0869 Da. Which instrument, if either, can distinguish BPA (exact [M + H]⁺ = 229.1224 Da) from this isomer? Justify your answer quantitatively.

**(c)** The TOF instrument measures the [M + H]⁺ of BPA at *m*/*z* = 229.1235. Using the expected value from part (a), calculate the mass accuracy of the measurement in parts per million (ppm). Is this result consistent with a well-calibrated TOF instrument?

**(d)** A quadrupole mass filter is described as a *scanning* analyzer, while a TOF is described as a *multichannel* analyzer. Explain what these terms mean in terms of how each instrument acquires a mass spectrum. What is the practical consequence of this distinction for sensitivity in a full-scan experiment?

**(e)** A high-molecular-weight polyethylene glycol sample (MW ≈ 25,000 Da) is analyzed at low resolving power, such that individual isotope peaks are unresolved. Explain why the measured peak center corresponds to the average mass rather than the monoisotopic mass under these conditions.

---

## Question 4 — Acquisition Modes and Tandem Mass Spectrometry

An environmental testing laboratory is developing an LC-MS/MS method to quantify atrazine (a triazine herbicide, C₈H₁₄ClN₅, MW ≈ 215 Da) in drinking water samples at concentrations below 1 µg/L. In positive-ion ESI, atrazine forms a prominent [M + H]⁺ ion at *m*/*z* ≈ 216. Collision-induced dissociation (CID) of this precursor ion yields product ions at *m*/*z* = 174 and *m*/*z* = 132, among others.

**(a)** In a preliminary investigation, the laboratory collects a full-scan spectrum to confirm the presence of atrazine. For routine quantitative monitoring of hundreds of samples per day, they switch to selected ion monitoring (SIM) on a single-quadrupole instrument. Compare full-scan and SIM acquisition: describe how the quadrupole operates differently in each mode, and explain the tradeoff between spectral information content and sensitivity.

**(b)** To achieve even greater sensitivity and selectivity, the laboratory transitions to a triple-quadrupole instrument operated in multiple reaction monitoring (MRM) mode. Draw and label a block diagram of the triple-quadrupole instrument (Q1–q2–Q3). Describe the role of each component in one sentence.

**(c)** The primary MRM transition selected for atrazine is 216 → 174. Explain what the two *m*/*z* values represent physically. Describe how requiring *both* mass selection steps simultaneously increases analytical specificity compared to SIM, and propose one additional confirmatory MRM transition for atrazine.

**(d)** A chlorinated triazine degradation product present in some water samples has the same nominal precursor mass as atrazine (*m*/*z* = 216) but does not produce a product ion at *m*/*z* = 174 under CID. Explain why the 216 → 174 MRM transition allows the laboratory to accurately quantify atrazine in these samples, whereas SIM monitoring of *m*/*z* = 216 alone would not.

**(e)** The laboratory later acquires a quadrupole ion trap. A colleague proposes using it to perform MS³ experiments — three sequential stages of mass selection and fragmentation — to characterize the structures of unknown atrazine metabolites. Explain why the ion trap is well-suited for MS^n experiments (*n* ≥ 3) while the triple quadrupole is not. Identify one practical limitation of high-order MS^n experiments on an ion trap.

---

## Acknowledgements
This documented was created with assistance from Claude 4.5 Sonnet.