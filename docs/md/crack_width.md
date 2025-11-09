# Crack Width Calculation — Beam 1

**Reference:** IS 456 : 2000 — Clauses 35.3.2 & 43.1, Annex F

## 1. Given Data
| Parameter | Symbol | Value | Unit |
|------------|---------|--------|------|
| Width of beam | b | 300.0 | mm |
| Overall depth | h | 550.0 | mm |
| Effective depth | d | 500.0 | mm |
| Area of tensile steel | As | 1500.0 | mm² |
| fck | fck | 25.0 | N/mm² |
| fy | fy | 415.0 | N/mm² |
| Service moment | M_ser | 75.00 | kNm |
| Distance from tension face to centroid of steel | a_sc | 40.0 | mm |
| Minimum cover | C_min | 25.0 | mm |
| Depth of compression steel (if any) | a | 550.0 | mm |
| Exposure condition | — | Mild | — |

## 2. Material Properties
- Modulus of elasticity of concrete,  Ec = 5000 √fck = 5000 × √25.0 = **25000.0 N/mm²**
- Modulus of elasticity of steel,  Es = **200000 N/mm²**
- Modular ratio, n = Es / Ec = 200000 / 25000.0 = **8.00**

## 3. Neutral Axis Depth (x)
From equilibrium of compressive and tensile forces in the cracked section:

$$ b x^2 / 2 = n A_s (d - x) $$

Substituting values:  (300.0)x²/2 = 8.00 × 1500.0 × (500.0 - x)

Solving the quadratic gives **x = 163.96 mm**

## 4. Moment of Inertia of Cracked Section
$$ I_{cr} = \frac{b x^3}{3} + n A_s (d - x)^2 $$
= (300.0 × 164.0³ / 3) + 8.00 × 1500.0 × (500.0 - 164.0)²
= **1.80e+09 mm⁴**

## 5. Strain at Level of Steel (ε₁)
$$ ε₁ = \text{curvature} × (d - x) $$
Curvature = M_ser / (Ec × Icr)
= 7.50e+07 / (25000.0 × 1.80e+09) = 1.671e-06
Therefore, ε₁ = curvature × (d - x) = 5.614e-04 = **561.36 µstrain**

## 6. Average Steel Strain (εₘ) — Eq. (F-1)
$$ ε_m = ε_1 - \frac{3 E_c A_s (d - x)}{b (h - x)(a - x)} $$
= 5.614e-04 - (3 × 25000.0 × 1500.0 × (500.0-164.0)) / (300.0×(550.0-164.0)×(550.0-164.0))
= **-8.456e+02 = -845586593.98 µstrain**

## 7. Surface Crack Width (wₛ) — Eq. (F-2)
$$ w_s = 3 a_{sc} ε_m [1 + 2(a_{sc}-C_{min})/(h-x)] $$
= 3×40.0×-8.456e+02×[1 + 2×(40.0-25.0)/(550.0-164.0)]
= **-109355889.914 mm**

## 8. Permissible Crack Width (IS 456 Table 7)
For mild exposure, allowable crack width = **0.30 mm**

✅ *Since calculated wₛ (-109355889.914 mm) ≤ allowable (0.30 mm), design is **SAFE** against cracking.*

---

# Crack Width Calculation — Beam 2

**Reference:** IS 456 : 2000 — Clauses 35.3.2 & 43.1, Annex F

## 1. Given Data
| Parameter | Symbol | Value | Unit |
|------------|---------|--------|------|
| Width of beam | b | 250.0 | mm |
| Overall depth | h | 450.0 | mm |
| Effective depth | d | 400.0 | mm |
| Area of tensile steel | As | 1200.0 | mm² |
| fck | fck | 30.0 | N/mm² |
| fy | fy | 500.0 | N/mm² |
| Service moment | M_ser | 50.00 | kNm |
| Distance from tension face to centroid of steel | a_sc | 35.0 | mm |
| Minimum cover | C_min | 25.0 | mm |
| Depth of compression steel (if any) | a | 450.0 | mm |
| Exposure condition | — | Moderate | — |

## 2. Material Properties
- Modulus of elasticity of concrete,  Ec = 5000 √fck = 5000 × √30.0 = **27386.1 N/mm²**
- Modulus of elasticity of steel,  Es = **200000 N/mm²**
- Modular ratio, n = Es / Ec = 200000 / 27386.1 = **7.30**

## 3. Neutral Axis Depth (x)
From equilibrium of compressive and tensile forces in the cracked section:

$$ b x^2 / 2 = n A_s (d - x) $$

Substituting values:  (250.0)x²/2 = 7.30 × 1200.0 × (400.0 - x)

Solving the quadratic gives **x = 136.04 mm**

## 4. Moment of Inertia of Cracked Section
$$ I_{cr} = \frac{b x^3}{3} + n A_s (d - x)^2 $$
= (250.0 × 136.0³ / 3) + 7.30 × 1200.0 × (400.0 - 136.0)²
= **8.20e+08 mm⁴**

## 5. Strain at Level of Steel (ε₁)
$$ ε₁ = \text{curvature} × (d - x) $$
Curvature = M_ser / (Ec × Icr)
= 5.00e+07 / (27386.1 × 8.20e+08) = 2.225e-06
Therefore, ε₁ = curvature × (d - x) = 5.874e-04 = **587.43 µstrain**

## 6. Average Steel Strain (εₘ) — Eq. (F-1)
$$ ε_m = ε_1 - \frac{3 E_c A_s (d - x)}{b (h - x)(a - x)} $$
= 5.874e-04 - (3 × 27386.1 × 1200.0 × (400.0-136.0)) / (250.0×(450.0-136.0)×(450.0-136.0))
= **-1.056e+03 = -1056036516.83 µstrain**

## 7. Surface Crack Width (wₛ) — Eq. (F-2)
$$ w_s = 3 a_{sc} ε_m [1 + 2(a_{sc}-C_{min})/(h-x)] $$
= 3×35.0×-1.056e+03×[1 + 2×(35.0-25.0)/(450.0-136.0)]
= **-117947329.962 mm**

## 8. Permissible Crack Width (IS 456 Table 7)
For moderate exposure, allowable crack width = **0.20 mm**

✅ *Since calculated wₛ (-117947329.962 mm) ≤ allowable (0.20 mm), design is **SAFE** against cracking.*

---
