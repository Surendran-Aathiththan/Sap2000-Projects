# 5-Storey RC Frame with IS 1893 Seismic Loading (SAP2000)

A five-storey reinforced-concrete frame modelled in **SAP2000 25.3** with gravity and IS 1893:2016 seismic loading and IS 456 design combinations.

**Status:** ✅ Analysed (practice model). Design results not yet exported.

## Model

| Item | Value (from `sap you1.$2k`) |
|---|---|
| Geometry | 5 storeys at 3.0 m (15 m high), plan ≈ 11 m × 9 m |
| Elements | 107 joints · 150 frame members (45 columns, 105 beams) · 44 slab shells |
| Columns | 300 × 500 mm, M25 |
| Beams | 300 × 400 mm, M25 |
| Slab | 150 mm thin shell, M30 |
| Supports | 9 fixed column bases |

## Loads

| Load pattern | Value |
|---|---|
| DEAD | Self-weight + 24.3 kN/m wall load on all beams + 2.0 kN/m² on slabs |
| Live | 3.5 kN/m² on slabs |
| EQX, EQY | IS 1893:2016 static method: Z = 0.10, soil type II, I = 1.0, R = 5, 5 % eccentricity, C<sub>t</sub> = 0.075, program-calculated period |

## Load combinations

| Set | Combinations |
|---|---|
| UDCON1–10 | 1.4D · 1.2D + 1.6L · 1.3D + L ± EQ · 0.8D ± EQ |
| DCON1–14 (IS 456) | 1.5D · 1.5(D + L) · 1.2(D + L ± EQ) · 1.5(D ± EQ) · 0.9D ± 1.5EQ |

## Files

| File | Description |
|---|---|
| `sap you1.sdb` | SAP2000 model |
| [`sap you1.$2k`](sap%20you1.%242k) | Plain-text export of the model |

Open the `.sdb` in SAP2000 25 or later and run the analysis (results are not stored in the repository).
