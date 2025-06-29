# Padeye Design Report

## 1. Introduction

This report summarizes the padeye design checks, including geometric, bearing, and shear stress verifications, using the provided dimensions and material properties. All calculations are shown in plain text and equations for clarity.

## 2. Input Data

- Shackle Pin Diameter: $D = 95\ \mathrm{mm}$
- Shackle Jaw Opening Width: $B = 147\ \mathrm{mm}$
- Shackle Inside Length: $H = 329\ \mathrm{mm}$
- Sling Diameter: $D_s = 80\ \mathrm{mm}$
- Yield Strength of Material: $F_y = 345\ \mathrm{MPa}$
- Young's Modulus: $E = 210,000\ \mathrm{MPa}$
- Poisson's Ratio: $\nu = 0.3$
- Padeye Hole Diameter: $d = 100\ \mathrm{mm}$
- Main Plate Thickness: $t = 40\ \mathrm{mm}$
- Cheek Plate Thickness: $t_c = 30\ \mathrm{mm}$
- Provided Main Plate Radius: $R_p = 200\ \mathrm{mm}$
- Provided Cheek Plate Radius: $R_c = 160\ \mathrm{mm}$
- Total Plate Thickness: $t_p = 100\ \mathrm{mm}$
- Padeye Length: $L = 658\ \mathrm{mm}$
- Number of Stiffeners: $n_{stiff} = 4$
- Distance Between Stiffener Centers: $H_s = 478\ \mathrm{mm}$
- Sling Load: $S_l = 86\ \mathrm{MT}$
- Acceleration due to Gravity: $g = 9.81\ \mathrm{m/s^2}$
- Calculated Sling Load: $SSL = S_l \times g \times 1,000 = 86 \times 9.81 \times 1,000 = 843,660\ \mathrm{N}$

## 3. Geometric Checks

### 3.1 Clearance Between Hole and Pin

- Pin Diameter: $d = 95\ \mathrm{mm}$
- Hole Diameter: $D = 100\ \mathrm{mm}$
- Clearance: $C_1 = D - d = 100 - 95 = 5\ \mathrm{mm}$

### 3.2 Clearance Between Shackle Jaw and Plate

- Shackle Jaw Opening: $B = 147\ \mathrm{mm}$
- Total Plate Thickness: $t_p = 100\ \mathrm{mm}$
- Clearance: $C_2 = \frac{B - t_p}{2} = \frac{147 - 100}{2} = 23.5\ \mathrm{mm}$

### 3.3 Sling Clearance

- Sling Clearance: $SC = H - (D_s + R_p - 0.5 \cdot d) = 329 - (80 + 200 - 0.5 \times 100) = 329 - 280 = 49\ \mathrm{mm}$

### 3.4 Minimum and Maximum Hole Sizes

- Minimum Hole: $\text{Minimum Hole} = \max(D + 3.18,\ 1.05 \cdot D) = \max(95 + 3.18,\ 1.05 \times 95) = \max(98.18,\ 99.75) = 99.75\ \mathrm{mm}$
- Maximum Hole: $\text{Maximum Hole} = D + 9.53 = 95 + 9.53 = 104.53\ \mathrm{mm}$

### 3.5 Minimum and Maximum Clearances

- Minimum Clearance: $\text{Minimum Clearance} = 0.05 \times t_p = 0.05 \times 100 = 5\ \mathrm{mm}$
- Maximum Clearance: $\text{Maximum Clearance} = \max(0.1 \times t_p,\ 20) = \max(10,\ 20) = 20\ \mathrm{mm}$

## 4. Bearing Stress Check

- Applied Load: $F = SSL = 843,660\ \mathrm{N}$
- Padeye Hole Diameter: $d = 100\ \mathrm{mm}$
- Main Plate Thickness: $t = 40\ \mathrm{mm}$
- Bearing Stress: $\sigma_b = \frac{F}{d \cdot t} = \frac{843,660}{100 \times 40} = 210.92\ \mathrm{MPa}$
- Permissible Bearing Stress: $\sigma_{b,\text{perm}} = 0.9 \times F_y = 0.9 \times 345 = 310.5\ \mathrm{MPa}$
- Check: $210.92\ \mathrm{MPa} < 310.5\ \mathrm{MPa} \implies \text{PASS}$

## 5. Shear Stress Check (Pin Hole Through Main/Cheek Plate)

- Applied Load: $F = SSL = 843,660\ \mathrm{N}$
- Main Plate Radius: $R_p = 200\ \mathrm{mm}$
- Cheek Plate Radius: $R_c = 160\ \mathrm{mm}$
- Shackle Hole Diameter: $d = 100\ \mathrm{mm}$
- Main Plate Thickness: $t = 40\ \mathrm{mm}$
- Cheek Plate Thickness: $t_c = 30\ \mathrm{mm}$
- Resisting Area:
> $A_{p1} = (R_p - \frac{d}{2}) \times 2t + (R_c - \frac{d}{2}) \times 4t_c
  = 25,200\ \mathrm{mm}^2$
- Shear Stress: $\sigma_s = \frac{F}{A_{p1}} = \frac{843,660}{25,200} = 33.49\ \mathrm{MPa}$
- Permissible Shear Stress: $\sigma_{s,\text{perm}} = 0.4 \times F_y = 0.4 \times 345 = 138\ \mathrm{MPa}$
- Check: $33.49\ \mathrm{MPa} < 138\ \mathrm{MPa} \implies \text{PASS}$

## 6. Summary Table

| Check                       | Calculated Value | Permissible Value | Result |
| --------------------------- | ---------------- | ----------------- | ------ |
| Bearing Stress ($\sigma_b$) | 210.92 MPa       | 310.5 MPa         | PASS   |
| Shear Stress ($\sigma_s$)   | 33.49 MPa        | 138 MPa           | PASS   |
| Hole Size                   | 100 mm           | 99.75 - 104.53 mm | PASS   |
| Clearance ($C_2$)           | 23.5 mm          | 5 - 20 mm         | FAIL   |

## 7. Conclusion

All checks except the shackle jaw clearance ($C_2$) are within permissible limits. The clearance between the shackle jaw and the plate exceeds the maximum allowed value and should be reviewed in the design.
