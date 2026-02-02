# Suggested Problems: UV-Vis

## Question 1: Beer's Law and Instrumental Noise

An environmental laboratory is validating a UV-Vis method for determining nitrate ($\text{NO}_3^-$) in groundwater samples. The nitrate ion absorbs strongly at 220 nm with a molar absorptivity of 715 M$^{-1}$cm$^{-1}$. A series of standard solutions were prepared and analyzed using a 1.00 cm pathlength cell.

**Given:**
- The spectrophotometer has a fixed noise level of $\sigma_T = 0.002$ in transmittance
- Maximum permissible contaminant level for nitrate: 10.0 mg/L (as nitrogen)
- Molecular weight of $\text{NO}_3^- = 62.0$ g/mol
- Atomic weight of N = 14.0 g/mol

**a)** Calculate the absorbance that would correspond to a nitrate solution at the maximum permissible contaminant level.

**b)** Using the relationship $\sigma_A = \frac{0.434\sigma_T}{T}$, calculate the absolute uncertainty in absorbance ($\sigma_A$) at the following transmittance values. Which transmittance range provides the lowest relative uncertainty in concentration? (circle one)

| $T$ | $\sigma_A$ |
|---|-----|
| 0.95 | |
| 0.50 | |
| 0.10 | |

**Circle one:**
- $T \approx 0.95$ (low absorbance) provides lowest relative uncertainty
- $T \approx 0.50$ (mid-range absorbance) provides lowest relative uncertainty
- $T \approx 0.10$ (high absorbance) provides lowest relative uncertainty

**c)** A groundwater sample gives an absorbance reading of 0.850 at 220 nm. However, the laboratory director notes that groundwater often contains dissolved organic matter that also absorbs at 220 nm. Describe how this interference would affect the Beer's law relationship for nitrate. Does this represent a chemical or instrumental deviation from Beer's law? (circle one)

- Chemical deviation
- Instrumental deviation

**d)** At very high nitrate concentrations (>0.01 M), analysts observe negative deviations from Beer's law—the measured absorbance is lower than predicted by the linear relationship established at lower concentrations. Which limitation to Beer's law most likely explains this observation? (circle one)

- Stray light reaching the detector
- Changes in refractive index affecting molar absorptivity
- Analyte association/aggregation at high concentration
- Detector saturation effects

**e)** Would the deviation described in part (d) cause a positive or negative bias in the calculated nitrate concentration?

**f)** A second groundwater sample is found to contain one-third the concentration of nitrate as the first sample analyzed in part (c). Predict the absorbance expected for this second sample.

---

## Question 2: Chemical Speciation and Absorbance

Bromocresol green (HIn) is a pH indicator that exists in two forms: the protonated yellow form (HIn, $\lambda_{\text{max}} = 444$ nm) and the deprotonated blue form ($\text{In}^-$, $\lambda_{\text{max}} = 616$ nm). The indicator has a $pK_a$ of 4.90.

**Given:**
- $\varepsilon_{\text{HIn}}$ at 616 nm = 800 M$^{-1}$cm$^{-1}$
- $\varepsilon_{\text{In}^-}$ at 616 nm = 28,000 M$^{-1}$cm$^{-1}$
- Total indicator concentration = $2.0 \times 10^{-5}$ M
- Pathlength = 1.00 cm
- Henderson-Hasselbalch equation: $\text{pH} = pK_a + \log\left(\frac{[\text{In}^-]}{[\text{HIn}]}\right)$

**a)** Calculate the fraction of indicator in the $\text{In}^-$ form ($\alpha_{\text{In}^-}$) at pH 6.00.

**b)** Calculate the expected absorbance of the indicator solution at 616 nm and pH 6.00, assuming both forms contribute to the total absorbance.

**c)** A student measures the absorbance of the indicator solution at 616 nm across a range of pH values. Sketch the expected shape of a plot of absorbance (y-axis) vs. pH (x-axis) from pH 3 to pH 7. Label key features including the approximate absorbance at the $pK_a$.

**d)** The student accidentally prepares a buffer at pH 4.90 (equal to the $pK_a$) instead of pH 6.00. Compared to your answer in part (b), will the measured absorbance at 616 nm be: (circle one)

- Higher
- Lower
- The same
- Cannot be determined without additional information

**e)** At very low pH (pH < 3), essentially all the indicator exists as HIn. If a student uses Beer's law with the molar absorptivity of $\text{In}^-$ (28,000 M$^{-1}$cm$^{-1}$) to calculate the indicator concentration from measurements at 616 nm and pH 2.0, would this cause a positive or negative bias in the calculated concentration? In 1-2 sentences, explain your reasoning using the relationship $C = A/(\varepsilon b)$.

---

## Question 3: Multicomponent Analysis

A water quality laboratory needs to simultaneously determine iron(II) and iron(III) in industrial wastewater using UV-Vis spectrophotometry. 

**Background:** A traditional sequential method uses 1,10-phenanthroline: Fe$^{2+}$ reacts immediately to form an orange complex, then hydroxylamine reduces Fe$^{3+}$ to Fe$^{2+}$ for total iron determination. However, this requires two separate measurements. For faster analysis, you propose using thiocyanate complexation for simultaneous determination of both species.

**Thiocyanate method:**

Iron(II) and iron(III) form colored complexes with thiocyanate (SCN$^-$) with different absorption characteristics:

| Wavelength | $\varepsilon_{\text{Fe}^{2+}}$ (M$^{-1}$cm$^{-1}$) | $\varepsilon_{\text{Fe}^{3+}}$ (M$^{-1}$cm$^{-1}$) |
|------------|------------------|-------------------|
| 480 nm | 90 | 5,200 |
| 580 nm | 50 | 180 |

A wastewater sample is treated with excess SCN$^-$ and analyzed in a 1.00 cm cell:
- $A_{480} = 0.624$
- $A_{580} = 0.158$

**a)** Write the matrix equation in the form $\mathbf{A} = b\boldsymbol{\varepsilon}\mathbf{c}$, where $b$ is the pathlength (1.00 cm). Define each matrix and vector, including their dimensions.

**b)** Using classical least-squares analysis, calculate the concentrations of Fe$^{2+}$ and Fe$^{3+}$ in the sample. Show your work.

**c)** In this analysis, why is it important to measure absorbance at two wavelengths rather than just at 480 nm where Fe$^{3+}$ has maximum absorbance? (circle one)

- To improve precision by averaging two measurements
- Because the detector is more sensitive at two wavelengths
- To mathematically resolve the contributions of both species to the total absorbance
- To verify that Beer's law is followed

**d)** If the sample actually contained a third colored species that absorbed at both wavelengths, how would this affect your calculated concentrations? (circle one)

- No effect, because Beer's law applies additively to all absorbing species
- Positive bias in both Fe$^{2+}$ and Fe$^{3+}$ concentrations, with magnitude depending on the third species' absorptivities
- Negative bias in both Fe$^{2+}$ and Fe$^{3+}$ concentrations
- The effect cannot be predicted without knowing the third species' molar absorptivities at both wavelengths

**e)** Explain in 1-2 sentences why the simultaneous thiocyanate method is preferred over the sequential phenanthroline method for routine wastewater monitoring.

## Acknowledgements

This documented was created with assistance from Claude 4.5 Sonnet.