# Chromatography: An Introduction — Solution Guide for Students

*Matthew Bush, University of Washington*

> **How to use this guide.**
> This guide is posted after you have submitted the activity. Work through each question and compare your reasoning — not just your numbers — to what is written here. For measurement-based questions (Q4, Q5, Q8, Q10–12), small differences from the values below are expected and acceptable; the key is whether your reasoning and your conclusions are correct.

---

## Section 1: A Gas Chromatography Separation

### Q1. Qualitative observations in Figure 1

A complete group list should capture all three of the following. Check whether your list addressed each:

**Band separation.** At $t = 0$, both bands are co-located at the column inlet. As time progresses, the two bands separate spatially — the purple band (benzene) moves ahead of the yellow band (toluene). By $t \approx 5$ min, benzene has exited the right end of the column and only toluene remains.

**Band broadening.** Both bands become wider (more spread out along the column axis) as they travel. This is not an artifact — it reflects real physical processes (diffusion and resistance to mass transfer) and is directly responsible for the finite width of peaks in the chromatogram.

**Different average speeds.** Benzene travels faster on average than toluene. The separation visible in Figure 1 is entirely a consequence of this speed difference.

---

## Section 2: A Gas Chromatography Instrument

### Q2. Role of the carrier gas; constraints of GC

**Carrier gas role.** Helium is the mobile phase. It flows continuously through the column and physically carries vaporized analytes from the injector to the detector. Helium is chemically inert — it does not interact with analytes or the stationary phase, and contributes nothing to the chemical basis of separation.

**Constraints imposed by the gas phase.** Because analytes must exist as gases inside the column, two properties are required:

1. **Sufficient volatility** — the analyte must vaporize at the inlet temperature (typically 200–300 °C). Large, involatile molecules (proteins, ionic compounds, most polymers) cannot be analyzed by conventional GC.
2. **Thermal stability** — the analyte must not decompose at the temperatures required for volatilization. Thermally labile molecules fragment before they can be separated.

### Q3. Predicting elution order from molecular structure

Both benzene ($\text{C}_6\text{H}_6$) and toluene ($\text{C}_7\text{H}_8$) are non-polar aromatic hydrocarbons that interact with the non-polar PDMS stationary phase through **London dispersion forces**. Toluene is larger and more polarizable due to its additional methyl group, so it experiences stronger dispersion interactions with PDMS. By *like dissolves like*, toluene should be retained longer.

**Does Figure 1 support this?** Yes. The yellow band (toluene) moves more slowly and exits the column later, consistent with a stronger stationary-phase interaction.

---

## Section 3: The Chromatogram

### Q4. Retention times and the most consistent measurement feature

Reading peak apices from Figure 4:

| Analyte | $t_r$ |
|---------|-------|
| Benzene | $\approx 4.0$ min |
| Toluene | $\approx 6.1$ min |

Values within $\pm 0.1$ min are acceptable.

**Most consistent feature: the peak apex.** The peak maximum is unambiguous — every analyst identifies the same point regardless of baseline noise or how they draw tangent lines. The leading or trailing edge of a peak depends on arbitrary threshold decisions, and therefore, values will vary between analysts and for data acquired with different signal-to-noise ratios.

### Q5. Void time

The **solvent peak** (hexane) is the first peak in Figure 4, eluting at approximately:

$$t_m \approx 0.8 \text{ min}$$

Hexane is essentially unretained under these conditions — it has very low affinity for PDMS and travels through the column at nearly the speed of the carrier gas.

> **Propagation note.** Your value of $t_m$ flows into every calculation of $k$ in this activity. If your $t_m$ differs slightly from 0.8 min, your $k$ values will shift by a constant offset — but their *ratio* (and therefore $\alpha$) will be largely preserved. The key check is that $k_\text{toluene} > k_\text{benzene} > 0$.

### Q6. Why $t_m$ is the same for every solute

While a solute molecule is in the **mobile phase**, it is carried at the same velocity as the helium flow, regardless of its chemical identity. The stationary phase cannot influence a molecule that is not in contact with it. Therefore every solute — no matter how strongly it partitions into PDMS — accumulates exactly $t_m$ minutes of mobile-phase travel time. What differs between solutes is how much *additional* time each molecule spends immobilized in the stationary phase on top of that shared $t_m$.

### Q7. Time spent only in the stationary phase

$$t_r = t_m + t_s \implies t_s = t_r - t_m$$

### Q8. Retention factor $k$

$$k = \frac{t_r - t_m}{t_m}$$

Using $t_m = 0.8$ min, $t_{r,\text{benz}} = 4.0$ min, $t_{r,\text{tol}} = 6.1$ min:

$$k_\text{benzene} = \frac{4.0 - 0.8}{0.8} = \frac{3.2}{0.8} \approx 4.0$$

$$k_\text{toluene} = \frac{6.1 - 0.8}{0.8} = \frac{5.3}{0.8} \approx 6.6$$

**Units of $k$:** $k$ is **unitless**. The numerator $(t_r - t_m)$ and denominator $t_m$ both have units of time, which cancel. This is by design — $k$ should not depend on whether you work in minutes or seconds.

### Q9. Two strategies for improving separation

Both scenarios improve resolution, but through different mechanisms:

**Scenario A (peaks farther apart in time)** increases the numerator of $R_{pp}$. This is controlled by selectivity $\alpha$ and average retention $k$. Lowering the column oven temperature, for example, increases the time analytes spend in the stationary phase (higher $k$) and spreads peaks further apart — but also lengthens the total analysis time.

**Scenario B (narrower peaks)** decreases the denominator of $R_{pp}$. Peak width is governed by column efficiency $N$. Longer columns, thinner stationary-phase films, and carrier gas flow rates near the Van Deemter optimum all reduce band broadening.

**Can both be improved simultaneously?** Yes, in principle — a longer column narrows peaks without changing selectivity. In practice, longer columns increase analysis time, cost, and backpressure, so real method development involves balancing all three factors.

---

## Section 4: Peak-to-Peak Resolution

### Q10. Calculating $R_{pp}$

$$R_{pp} = \frac{t_{r,2} - t_{r,1}}{\dfrac{w_{b,1} + w_{b,2}}{2}}$$

Reading peak widths at base from Figure 4 by drawing tangent lines to the baseline:

| Analyte | $t_r$ (min) | $w_b$ (min) |
|---------|:-----------:|:-----------:|
| Benzene | 4.0 | $\approx 1.3$ |
| Toluene | 6.1 | $\approx 1.55$ |

$$R_{pp} = \frac{6.1 - 4.0}{\dfrac{1.3 + 1.55}{2}} = \frac{2.1}{1.425} \approx 1.47$$

**Qualitative assessment using Figure 5.** $R_{pp} \approx 1.48$ exceeds the $R_{pp} = 1.0$ threshold shown in Figure 5 and is similar to the conventional "baseline resolution" criterion of $R_{pp} = 1.5$. The two peaks in Figure 4 are well resolved and have neglible overlap — more than adequate for reliable identification and quantification of both analytes.

> **Acceptable range.** Peak width measurement depends on where you draw your tangent lines. Values of $R_{pp}$ between 1.3 and 1.7 are likely defensible. Whatever value you obtained, the conclusion — that the separation is adequate — should be the same.

---

## Section 5: Selectivity Factor

### Q11. Selectivity factor $\alpha$ and its relationship to $R_{pp}$

$$\alpha = \frac{k_\text{toluene}}{k_\text{benzene}} = \frac{6.6}{4.0} \approx 1.65$$

**Relationship between $\alpha$ and $R_{pp}$.** Both quantities describe separation quality, but they capture different things:

- $\alpha$ reflects only the **chemical selectivity** of the stationary phase — how differently the two analytes partition between phases. It tells you whether separation is *chemically possible* at all, independent of peak width.
- $R_{pp}$ captures the *actual observed* separation quality in a given experiment, incorporating both selectivity and how much the peaks have broadened.

A system where $\alpha = 1.0$ cannot separate two analytes no matter how efficient the column is, because both analytes spend identical fractions of their time in each phase. Increasing $\alpha$ is usually the most powerful lever for a difficult separation.

**Using stationary phase choice to improve resolution.** If two analytes co-elute on a non-polar column ($\alpha \approx 1$), they likely differ in polarity or hydrogen-bonding ability. Switching to a polar stationary phase (such as polyethylene glycol) that exploits that chemical difference can dramatically increase $\alpha$ — and therefore $R_{pp}$ — without changing any hardware.

---

## Section 6: A Microscopic View

### Q12. Estimating $D$ from Figure 6

Molecule counts from Figure 6:

|         | Mobile phase | Stationary phase | $D = N_\text{stat} / N_\text{mobile}$ |
|---------|:---:|:---:|:---:|
| Benzene | 2 | 8 | $8/2 = 4$ |
| Toluene | 2 | 13 | $13/2 = 6.5$ |

Both $D$ values are greater than 1, consistent with both analytes preferring the non-polar PDMS over the inert helium mobile phase. $D_\text{toluene} > D_\text{benzene}$, consistent with toluene's longer retention time in Figure 4.

> **On precision.** These estimates come from a single snapshot of a dynamic, stochastic process. Small differences in your counts are expected. The rank order ($D_\text{toluene} > D_\text{benzene}$) is what matters.

### Q13. Preferential partitioning when mobile-phase interactions dominate

The solute partitions **preferentially into the mobile phase**.

$$D = \frac{[\text{solute}]_\text{stat}}{[\text{solute}]_\text{mobile}} < 1$$

$D < 1$ means the mobile phase is the preferred environment at equilibrium. Analytes with $D \ll 1$ on a given column elute near the void time with $k \approx 0$ — the column provides essentially no retention for them.

### Q14. Connecting $D$ to $k$

Both $D$ and $k$ describe how a solute distributes between the two phases, just from different perspectives:

- $D$ is an **equilibrium concentration ratio** — it describes the molecular-level snapshot in Figure 6: at any given instant, what fraction of the molecules are in the stationary phase?
- $k$ is a **time ratio** — it describes the chromatogram: on average, what fraction of its total column time does a molecule spend in the stationary phase?

These two quantities are measuring the same underlying tendency (affinity for the stationary phase) from different angles, so they must be consistent with each other. A solute with a high $D$ — many molecules in the stationary phase at equilibrium — will also spend more of its time in the stationary phase on average, producing a high $k$ and a long retention time.

**Consistency check.** Your $D$ values from Q12 and $k$ values from Q8 should rank in the same order. For this separation: $D_\text{toluene} > D_\text{benzene}$ and $k_\text{toluene} > k_\text{benzene}$. If your values disagree, recheck either your molecule counts or your $t_r$ readings.

### Q15. Boiling point prediction

Toluene elutes later because it experiences stronger London dispersion interactions with the PDMS stationary phase — the same type of forces that determine boiling point. Larger, more polarizable molecules have higher boiling points and interact more strongly with a non-polar stationary phase.

**Prediction:** Toluene has the higher boiling point.

**Bonus check:**

| Analyte | Boiling point |
|---------|:---:|
| Benzene | $80\ ^\circ\text{C}$ |
| Toluene | $111\ ^\circ\text{C}$ |

Prediction confirmed. For structurally similar, non-polar compounds on a non-polar GC column, elution order reliably tracks boiling point order.

---

## Section 7: Synthesis

### Q16. The journey of a single benzene molecule

Rather than a model answer, here are the five elements your narrative must contain. Check each off in your response:

- [ ] The molecule is **vaporized** at the hot inlet and enters the column carried by the **mobile phase** (helium)
- [ ] The molecule undergoes repeated **partitioning** between the mobile phase and the **stationary phase** (PDMS film), governed by its **distribution constant** $D$
- [ ] While in the mobile phase it travels at the carrier gas velocity; while in the stationary phase it is temporarily immobilized
- [ ] After many thousands of adsorption–desorption events along the 30 m column, the molecule exits at **retention time** $t_r \approx 4.0$ min — recorded as the **peak** apex in the chromatogram
- [ ] The response explicitly connects the molecular picture (Figure 6) to the macroscopic chromatogram (Figure 4)

A response that addresses all five elements in 3–5 coherent sentences fully satisfies this question.

---

## Common Errors

| Error | What went wrong |
|---|---|
| Reporting the leading edge of a peak as $t_r$ | Retention time is defined at the **peak apex**. The leading edge depends on signal threshold and varies between analysts. |
| Negative $k$ | You likely read $t_r < t_m$. Confirm that your void time comes from the first (solvent) peak, not one of the analyte peaks. |
| Units on $k$ (e.g., "min") | $k$ is **unitless** — numerator and denominator both carry units of time that cancel. |
| $\alpha < 1$ | By convention, $\alpha = k_2/k_1$ where $k_2 > k_1$. Always place the *larger* $k$ in the numerator. |
| Concluding $R_{pp} = 1.0$ is sufficient | $R_{pp} \geq 1.5$ is the conventional threshold for *baseline resolution*. At $R_{pp} = 1.0$, there is still ~6% peak overlap — often unacceptable for quantitative work. |
| Treating Figure 6 as a static picture | The caption states explicitly that this is "a single instant in a dynamic process." Molecules exchange between phases continuously and rapidly. |

## Acknowledgements

This guide was developed with assistance from Claude Sonnet 4.6.