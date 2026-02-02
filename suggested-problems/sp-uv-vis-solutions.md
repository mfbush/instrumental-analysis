# Solutions to Suggested Problems: UV-Vis

## Question 1: Beer's Law and Instrumental Noise

### Solution (a): Calculate absorbance at maximum permissible contaminant level

**Step 1:** Convert from mg/L as nitrogen to mg/L as nitrate

$$\text{mg/L NO}_3^- = 10.0 \text{ mg/L N} \times \frac{62.0 \text{ g/mol NO}_3^-}{14.0 \text{ g/mol N}} = 44.3 \text{ mg/L NO}_3^-$$

**Step 2:** Convert to molarity

$$C = 44.3 \frac{\text{mg}}{\text{L}} \times \frac{1 \text{ g}}{1000 \text{ mg}} \times \frac{1 \text{ mol}}{62.0 \text{ g}} = 7.14 \times 10^{-4} \text{ M}$$

**Step 3:** Apply Beer's law: $A = \varepsilon bc$

$$A = (7150 \text{ M}^{-1}\text{cm}^{-1})(1.00 \text{ cm})(7.14 \times 10^{-4} \text{ M}) = 5.10$$

**Answer:** $A = 5.10$

**Note:** This absorbance is extremely high and outside the linear range of most spectrophotometers (typically $A < 2$). This suggests the method would need modification (dilution or shorter pathlength) for practical use.

---

### Solution (b): Calculate uncertainty in absorbance at different transmittance values

Using the relationship: $\sigma_A = \frac{0.434\sigma_T}{T}$

Given: $\sigma_T = 0.002$

$$\sigma_A = \frac{0.434 \times 0.002}{T} = \frac{0.000868}{T}$$

| $T$ | $A = -\log(T)$ | $\sigma_A$ | $\sigma_A/A$ (Relative Uncertainty) |
|-----|----------------|------------|-------------------------------------|
| 0.95 | 0.0223 | 0.000914 | 0.041 (4.1%) |
| 0.50 | 0.301 | 0.001736 | 0.0058 (0.58%) |
| 0.10 | 1.00 | 0.00868 | 0.0087 (0.87%) |

**Answer:** $T \approx 0.50$ (mid-range absorbance) provides lowest relative uncertainty

The relative uncertainty in concentration is proportional to $\sigma_A/A$. The minimum occurs around $A \approx 0.434$ ($T \approx 0.37$), so the mid-range transmittance gives the best precision.

---

### Solution (c): Effect of dissolved organic matter interference

The dissolved organic matter (DOM) absorbs at 220 nm, contributing additional absorbance beyond that of nitrate. This causes the measured absorbance to be higher than the absorbance due to nitrate alone, violating the assumption that only the analyte absorbs at the measurement wavelength.

$$A_{\text{measured}} = A_{\text{nitrate}} + A_{\text{DOM}}$$

This represents a **chemical deviation** from Beer's law because it arises from the sample chemistry (presence of another absorbing species), not from instrumental limitations.

---

### Solution (d): Limitation causing downward curvature

**Answer:** Changes in refractive index affecting molar absorptivity

At very high concentrations, the solution's refractive index changes significantly, which affects the molar absorptivity ($\varepsilon$). This causes negative deviations from Beer's law (measured absorbance lower than predicted).

Other options:
- Stray light causes *upward* curvature (positive deviation) at high absorbance
- Analyte association/aggregation would be a chemical deviation (often mentioned separately)
- Detector saturation is less common with modern instruments

---

### Solution (e): Direction of bias

When the calibration curve shows downward curvature (absorbance lower than expected), using a linear Beer's law relationship will **underestimate** the concentration.

**Answer:** Negative bias (concentration will be calculated as lower than the true value)

If the true relationship gives lower absorbance at high concentration, but you assume linear Beer's law, you'll calculate a lower concentration from that absorbance reading.

---

## Question 2: Chemical Speciation and Absorbance

### Solution (a): Calculate fraction in In⁻ form at pH 6.00

Using the Henderson-Hasselbalch equation:

$$\text{pH} = pK_a + \log\left(\frac{[\text{In}^-]}{[\text{HIn}]}\right)$$

$$6.00 = 4.90 + \log\left(\frac{[\text{In}^-]}{[\text{HIn}]}\right)$$

$$1.10 = \log\left(\frac{[\text{In}^-]}{[\text{HIn}]}\right)$$

$$\frac{[\text{In}^-]}{[\text{HIn}]} = 10^{1.10} = 12.59$$

The fraction in the In⁻ form:

$$\alpha_{\text{In}^-} = \frac{[\text{In}^-]}{[\text{In}^-] + [\text{HIn}]} = \frac{12.59}{12.59 + 1} = \frac{12.59}{13.59} = 0.926$$

**Answer:** $\alpha_{\text{In}^-} = 0.926$ (92.6% deprotonated)

---

### Solution (b): Calculate absorbance at 616 nm and pH 6.00

Both forms contribute to the total absorbance:

$$A_{\text{total}} = \varepsilon_{\text{HIn}} \cdot b \cdot [\text{HIn}] + \varepsilon_{\text{In}^-} \cdot b \cdot [\text{In}^-]$$

Express in terms of total concentration and fractions:

$$A_{\text{total}} = \varepsilon_{\text{HIn}} \cdot b \cdot C_{\text{total}} \cdot (1 - \alpha_{\text{In}^-}) + \varepsilon_{\text{In}^-} \cdot b \cdot C_{\text{total}} \cdot \alpha_{\text{In}^-}$$

Substitute values:

$$A = (800)(1.00)(2.0 \times 10^{-5})(0.074) + (28{,}000)(1.00)(2.0 \times 10^{-5})(0.926)$$

$$A = 0.00118 + 0.519 = 0.520$$

**Answer:** $A = 0.520$

---

### Solution (c): Sketch of absorbance vs. pH

The plot should show:
- **Sigmoid (S-shaped) curve**
- Low absorbance at pH 3 (mostly HIn, which has low $\varepsilon$ at 616 nm)
- High absorbance at pH 7 (mostly In⁻, which has high $\varepsilon$ at 616 nm)
- **Inflection point at pH = pK_a = 4.90** (50% of each form)
- Approximately linear region around the pK_a

```
A
|
0.56 |                    ___________
     |                   /
     |                  /
0.28 |                 /  ← Inflection at pH 4.90
     |                /
     |               /
0.00 |______________/
     |----+----+----+----+----+
         3    4    5    6    7    pH
```

---

### Solution (d): Absorbance at pH = pK_a

At pH = pK_a = 4.90, the ratio $[\text{In}^-]/[\text{HIn}] = 1$, so $\alpha_{\text{In}^-} = 0.50$

$$A = (800)(1.00)(2.0 \times 10^{-5})(0.50) + (28{,}000)(1.00)(2.0 \times 10^{-5})(0.50)$$

$$A = 0.00800 + 0.280 = 0.288$$

Compared to $A = 0.520$ at pH 6.00:

**Answer:** Lower

---

### Solution (e): Bias from incorrect molar absorptivity

At pH 2.0, essentially all indicator is in the HIn form ($\alpha_{\text{In}^-} \approx 0$).

**Actual absorbance:**
$$A_{\text{actual}} = (800)(1.00)(2.0 \times 10^{-5}) = 0.016$$

**Student's calculation using $\varepsilon_{\text{In}^-} = 28{,}000$:**
$$C_{\text{calculated}} = \frac{A}{\varepsilon b} = \frac{0.016}{(28{,}000)(1.00)} = 5.7 \times 10^{-7} \text{ M}$$

True concentration: $2.0 \times 10^{-5}$ M

**Answer:** This would cause a **negative bias** (calculated concentration much lower than true concentration) because the student is using a molar absorptivity that is 35 times larger than the actual molar absorptivity of the species present.

---

## Question 3: Multicomponent Analysis

### Solution (a): Matrix equation

The general form for a two-component, two-wavelength system is:

$$\mathbf{A} = \boldsymbol{\varepsilon} \cdot b \cdot \mathbf{c}$$

Where:
- $\mathbf{A}$ = absorbance vector (2×1): $\begin{bmatrix} A_{480} \\ A_{580} \end{bmatrix}$
- $\boldsymbol{\varepsilon}$ = molar absorptivity matrix (2×2): $\begin{bmatrix} \varepsilon_{\text{Fe}^{2+}, 480} & \varepsilon_{\text{Fe}^{3+}, 480} \\ \varepsilon_{\text{Fe}^{2+}, 580} & \varepsilon_{\text{Fe}^{3+}, 580} \end{bmatrix}$
- $b$ = pathlength (scalar): 1.00 cm
- $\mathbf{c}$ = concentration vector (2×1): $\begin{bmatrix} C_{\text{Fe}^{2+}} \\ C_{\text{Fe}^{3+}} \end{bmatrix}$

**Specific equation:**

$$\begin{bmatrix} 0.624 \\ 0.158 \end{bmatrix} = \begin{bmatrix} 90 & 5{,}200 \\ 50 & 180 \end{bmatrix} \times 1.00 \times \begin{bmatrix} C_{\text{Fe}^{2+}} \\ C_{\text{Fe}^{3+}} \end{bmatrix}$$

---

### Solution (b): Calculate concentrations using classical least-squares

**Method 1: Algebraic solution**

From the matrix equation:
$$0.624 = 90 C_{\text{Fe}^{2+}} + 5{,}200 C_{\text{Fe}^{3+}} \quad \text{(Equation 1)}$$
$$0.158 = 50 C_{\text{Fe}^{2+}} + 180 C_{\text{Fe}^{3+}} \quad \text{(Equation 2)}$$

From Equation 2, solve for $C_{\text{Fe}^{2+}}$:
$$C_{\text{Fe}^{2+}} = \frac{0.158 - 180 C_{\text{Fe}^{3+}}}{50} = 0.00316 - 3.6 C_{\text{Fe}^{3+}}$$

Substitute into Equation 1:
$$0.624 = 90(0.00316 - 3.6 C_{\text{Fe}^{3+}}) + 5{,}200 C_{\text{Fe}^{3+}}$$
$$0.624 = 0.2844 - 324 C_{\text{Fe}^{3+}} + 5{,}200 C_{\text{Fe}^{3+}}$$
$$0.624 = 0.2844 + 4{,}876 C_{\text{Fe}^{3+}}$$
$$0.3396 = 4{,}876 C_{\text{Fe}^{3+}}$$
$$C_{\text{Fe}^{3+}} = 6.96 \times 10^{-5} \text{ M}$$

Back-substitute:
$$C_{\text{Fe}^{2+}} = 0.00316 - 3.6(6.96 \times 10^{-5}) = 0.00316 - 0.000251 = 2.91 \times 10^{-3} \text{ M}$$

**Verification:**
- $A_{480} = 90(2.91 \times 10^{-3}) + 5{,}200(6.96 \times 10^{-5}) = 0.262 + 0.362 = 0.624$ ✓
- $A_{580} = 50(2.91 \times 10^{-3}) + 180(6.96 \times 10^{-5}) = 0.146 + 0.0125 = 0.158$ ✓

**Method 2: Matrix inversion**

$$\mathbf{c} = \frac{1}{b} \boldsymbol{\varepsilon}^{-1} \mathbf{A}$$

$$\boldsymbol{\varepsilon}^{-1} = \frac{1}{(90)(180) - (5{,}200)(50)} \begin{bmatrix} 180 & -5{,}200 \\ -50 & 90 \end{bmatrix}$$

$$= \frac{1}{16{,}200 - 260{,}000} \begin{bmatrix} 180 & -5{,}200 \\ -50 & 90 \end{bmatrix} = \frac{1}{-243{,}800} \begin{bmatrix} 180 & -5{,}200 \\ -50 & 90 \end{bmatrix}$$

$$\mathbf{c} = \frac{1}{-243{,}800} \begin{bmatrix} 180 & -5{,}200 \\ -50 & 90 \end{bmatrix} \begin{bmatrix} 0.624 \\ 0.158 \end{bmatrix}$$

$$= \frac{1}{-243{,}800} \begin{bmatrix} 112.3 - 821.6 \\ -31.2 + 14.22 \end{bmatrix} = \frac{1}{-243{,}800} \begin{bmatrix} -709.3 \\ -16.98 \end{bmatrix}$$

$$\mathbf{c} = \begin{bmatrix} 2.91 \times 10^{-3} \\ 6.96 \times 10^{-5} \end{bmatrix} \text{ M}$$

**Answers:** 
- $C_{\text{Fe}^{2+}} = 2.91 \times 10^{-3}$ M (2.91 mM)
- $C_{\text{Fe}^{3+}} = 6.96 \times 10^{-5}$ M (69.6 μM)

---

### Solution (c): Why measure at two wavelengths?

**Answer:** To mathematically resolve the contributions of both species to the total absorbance

At any single wavelength, both Fe²⁺ and Fe³⁺ absorb, so the measured absorbance is the sum of contributions from both species. With measurements at two wavelengths, we have two equations and two unknowns, allowing us to solve for both concentrations simultaneously.

The other options are incorrect because:
- Averaging doesn't help when both species absorb at both wavelengths
- Detector sensitivity is wavelength-dependent but that's not the reason
- Beer's law verification requires multiple concentrations, not multiple wavelengths

---

### Solution (d): Effect of a third absorbing species

**Answer:** Unpredictable effect without knowing the third species' molar absorptivities

If a third species absorbs at 480 nm and/or 580 nm, it would contribute additional absorbance:
$$A_{480} = 90 C_{\text{Fe}^{2+}} + 5{,}200 C_{\text{Fe}^{3+}} + \varepsilon_{3,480} C_3$$
$$A_{580} = 50 C_{\text{Fe}^{2+}} + 180 C_{\text{Fe}^{3+}} + \varepsilon_{3,580} C_3$$

The two-component model would incorrectly attribute the third species' absorbance to Fe²⁺ and Fe³⁺. The direction and magnitude of the bias would depend on the third species' molar absorptivities at both wavelengths. However, in most practical cases, this would cause a **positive bias** (overestimation) in the calculated concentrations.

The calculation does NOT account for all absorbing species—it assumes only two components are present.

## Acknowledgements

This documented was created with assistance from Claude 4.5 Sonnet.
