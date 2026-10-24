# 3-Storey RC Frame under Gravity Loads (SAP2000)

A three-storey reinforced-concrete frame modelled in **SAP2000 24.0** under dead and live loads, with IS 456 design combinations.

**Status:** ✅ Analysed (practice model). Design results not yet exported.

## Model

| Item | Value (from `sap you2.$2k`) |
|---|---|
| Geometry | 3 storeys at 3.0 m (9 m high), plan ≈ 7 m × 13 m |
| Elements | 48 joints · 87 frame members (36 columns, 51 beams) · 12 slab shells |
| Columns | 300 × 300 mm, M30 |
| Beams | 230 × 300 mm, M30 |
| Slab | 125 mm thin shell, M30 |
| Supports | 12 fixed column bases |

## Loads and combinations

| Item | Value |
|---|---|
| DEAD | Self-weight + 24.3 kN/m wall load on all beams + 2.0 kN/m² on slabs |
| LL | 3.0 kN/m² on slabs |
| Combinations | 1.4D · 1.2D + 1.6L · 1.5D · 1.5(D + L) |

## Files

| File | Description |
|---|---|
| `sap you2.sdb` | SAP2000 model |
| [`sap you2.$2k`](sap%20you2.%242k) | Plain-text export of the model |

Open the `.sdb` in SAP2000 24 or later and run the analysis (results are not stored in the repository).
