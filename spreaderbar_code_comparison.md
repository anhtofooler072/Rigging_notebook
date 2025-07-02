Comparison of Allowable Compressive Stress Solutions: AISC 2005 vs ASME BTH-1 2017
========================================================================================

This document summarizes and compares the allowable compressive stress calculations for the spreader bar as performed in `spreaderbar.ipynb`, following both AISC 2005 and ASME BTH-1 2017 codes.

---

1. **Parameters Used in Both Codes**
   - Outer diameter (Od): 588 mm
   - Thickness (t): 25 mm
   - Length (L): 6288 mm
   - Young's modulus (E): 210,000 MPa
   - Yield strength (Fy): 345 MPa
   - Effective length factor (K): 1
   - Safety factor (Nd): 4 (ASME BTH-1)

2. **ASME BTH-1 2017 Allowable Axial Compressive Stress**
   - The code uses a slenderness parameter $KL/r$ and a critical slenderness $C_c$.
   - For $KL/r \leq C_c$:
     $$
     F_a = \left[1 - \frac{(KL/r)^2}{2C_c^2}\right] \frac{F_y}{N_d} \left[1 + \frac{9 KL/r}{40 C_c} - \frac{3 (KL/r)^3}{40 C_c^4}\right]
     $$
   - For $KL/r > C_c$:
     $$
     F_a = \frac{\pi^2 E}{1.15 N_d (KL/r)^2}
     $$
   - **Result from notebook:**
     - Allowable axial compressive stress: **~44.13 MPa**
     - Applied compressive stress: **~31.99 MPa**
     - Conclusion: Applied stress is within allowable limits.

3. **AISC 2005 Allowable Compressive Stress**
   - The code uses the flexural buckling equations (E3-2 and E3-3):
   - For $KL/r \leq 4.71\sqrt{E/F_y}$:
     $$
     F_{cr} = [0.658^{F_y/F_e}] F_y
     $$
   - For $KL/r > 4.71\sqrt{E/F_y}$:
     $$
     F_{cr} = 0.877 F_e
     $$
   - Where $F_e = \frac{\pi^2 E}{(KL/r)^2}$
   - **Result from notebook:**
     - Critical stress $F_{cr}$: **~74.6 MPa**
     - Allowable compressive strength (ASD): **~44.7 MPa**
     - Applied compressive stress: **~31.99 MPa**
     - Conclusion: Applied stress is within allowable limits.

4. **Summary Table**

| Code             | Allowable Stress (MPa) | Applied Stress (MPa) | Pass/Fail |
|------------------|-----------------------|----------------------|-----------|
| ASME BTH-1 2017  | 44.13                 | 31.99                | Pass      |
| AISC 2005 (ASD)  | 44.7                  | 31.99                | Pass      |

5. **Discussion**
- Both codes yield very similar allowable compressive stresses for the given geometry and material.
- The calculation methods differ in their approach to slenderness and safety factors, but for this case, the results are nearly identical.
- In both cases, the applied compressive stress is well below the allowable, confirming the adequacy of the spreader bar design.

---

**References:**
- AISC 2005, Specification for Structural Steel Buildings
- ASME BTH-1 2017, Design of Below-the-Hook Lifting Devices
- See `spreaderbar.ipynb` for detailed calculation steps and code.
