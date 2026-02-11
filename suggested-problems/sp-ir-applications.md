# Suggested Problems: Applications of Infrared Spectroscopy
*Prof. Matthew F. Bush, University of Washington*

---

## Question 1: Spectral Library Matching and Near-IR Analysis

A pharmaceutical quality control laboratory is implementing IR spectroscopy for raw material identification and tablet content uniformity testing.

**Part A: Spectral Library Matching (Qualitative Analysis)**

The laboratory uses FT-IR with a commercial spectral library to verify incoming shipments of excipients. A sample labeled as "microcrystalline cellulose" is analyzed, and the library search returns the following top three matches:

| Rank | Compound | HQI | p-value |
|------|----------|-----|---------|
| 1 | Microcrystalline cellulose | 0.9985 | 0.152 |
| 2 | Hydroxypropyl cellulose | 0.9912 | 0.00018 |
| 3 | Methyl cellulose | 0.9845 | 0.000031 |

**a)** Using a significance level of $\alpha = 0.05$, evaluate whether you can confidently identify this sample as microcrystalline cellulose based on the spectral library match. Explain your reasoning using both the HQI value and p-value.

**b)** Explain why the HQI values for all three cellulose variants are very similar (all > 0.98), yet the p-values differ by several orders of magnitude. What does this tell you about using HQI alone for compound identification?

**c)** In 2-3 sentences, explain how the Connes advantage of FT-IR (discussed in the Fundamentals lecture) specifically enables reliable spectral library matching.

**Part B: Near-IR vs Mid-IR Selection**

The same laboratory needs to develop a method for measuring the API (active pharmaceutical ingredient) content in finished tablets. They are deciding between mid-IR and near-IR spectroscopy.

**Given information:**
- Target: 100 mg API per 500 mg tablet (20% w/w)
- Tablets also contain microcrystalline cellulose, starch, and magnesium stearate
- Required precision: ±2% relative error
- Analysis rate: >100 tablets/hour
- Laboratory budget allows for either approach

**d)** List three distinct advantages of near-IR over mid-IR for this specific application.

**e)** The API shows a strong carbonyl absorption at 1680 cm⁻¹ in the mid-IR. Would you expect to see this same absorption in the near-IR spectrum? Explain what type of transition you might observe instead in the near-IR region.

**f)** The laboratory plans to use Partial Least Squares (PLS) regression for quantitative analysis. Explain in 2-3 sentences why PLS is better suited than Classical Least Squares (CLS) for analyzing intact tablets with this complex matrix.

---

## Question 2: Sampling Techniques and Quantitative Analysis

An environmental laboratory needs to analyze samples using different IR sampling approaches depending on the sample type.

**Part A: Gas Analysis**

The laboratory uses a portable IR photometer with a Herriott cell for measuring CO in workplace air. The cell has two configurations:

**Configuration A:** 28 passes, effective path length = 10.4 m  
**Configuration B:** 80 passes, effective path length = 31.2 m

The detection limit for CO using Configuration A is 5.0 ppm.

**a)** Assuming the detection limit is inversely proportional to path length, what would be the expected detection limit when using Configuration B?

**b)** Compare this IR photometer approach (measuring at a single wavelength) to a multichannel FT-IR measurement (measuring across a range of wavelengths). In 2-3 sentences, explain one advantage of each approach for gas analysis.

**Part B: Cavity Ring-Down Spectroscopy**

The laboratory is considering purchasing a CRDS instrument for trace gas analysis. In an empty cavity, the ring-down time constant is $\tau_0 = 45$ μs. When a trace gas sample is introduced, the ring-down time decreases to $\tau = 38$ μs.

**c)** Does the decrease in ring-down time from 45 μs to 38 μs indicate that the sample absorbs the laser wavelength being used? Explain your reasoning.

**d)** Calculate the percent change in the ring-down time: $\frac{\tau_0 - \tau}{\tau_0} \times 100\%$

**e)** In 2-3 sentences, explain the fundamental mechanism that makes CRDS more sensitive than conventional absorption spectroscopy. What creates the long effective path length?

**Part C: ATR Sampling**

The laboratory receives a polymer film sample that is too thick and opaque for conventional transmission IR measurements.

**f)** Describe the mechanism of Attenuated Total Reflection (ATR):

   **i)** What phenomenon occurs at the crystal-sample interface, and what does it create?
   
   **ii)** How deep does the evanescent wave penetrate into the sample?
   
   **iii)** Why does this shallow penetration allow analysis of thick or strongly absorbing samples?

**g)** The analyst notices that the ATR spectrum of the polymer shows the same peak positions as a transmission spectrum of a thin film of the same polymer, but some peak intensities differ. In 1-2 sentences, suggest a reason why ATR and transmission spectra might show different relative peak intensities for the same material.

## Acknowledgements
This documented was created with assistance from Claude 4.5 Sonnet.