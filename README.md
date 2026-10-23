# SAP2000 Projects

Structural models analysed in **SAP2000** (versions 24–26): reinforced-concrete building frames with IS 1893 seismic loading, and truss/arch concepts for a spaghetti-bridge design.

| Project | What it covers | Status |
|---|---|---|
| [sap you1: 5-storey RC frame](sap%20you1) | Practice RC frame with IS 1893:2016 seismic loads and 24 design combinations | ✅ Analysed |
| [sap you2: 3-storey RC frame](sap%20you2) | Practice RC frame under gravity loads | ✅ Analysed |
| [spaghetti bridge](spaghetti%20bridge) | Truss and arch concepts for a spaghetti model bridge | 🚧 Concept stage |

## sap you1: 5-storey RC frame with seismic loading

| Item | Value (from `sap you1.$2k`) |
|---|---|
| Software | SAP2000 25.3 |
| Geometry | 5 storeys at 3.0 m (15 m high), plan ≈ 11 m × 9 m, 9 columns, 150 frame members |
| Sections | Columns 300 × 500 mm, beams 300 × 400 mm (M25); 150 mm M30 slab (thin shell) |
| Supports | Fixed |
| Loads | Self-weight; 24.3 kN/m wall load on beams; 2.0 kN/m² additional dead load; 3.5 kN/m² live load |
| Seismic | IS 1893:2016 static method in X and Y, Z = 0.10, soil type II, I = 1.0, R = 5, 5 % eccentricity, program-calculated period |
| Combinations | 10 user combinations + 14 IS 456 design combinations (1.5DL, 1.5(DL + LL), 1.2(DL + LL ± EQ), 1.5(DL ± EQ), 0.9DL ± 1.5EQ) |
| Design codes set | IS 456:2000 (concrete) |

## sap you2: 3-storey RC frame

| Item | Value (from `sap you2.$2k`) |
|---|---|
| Software | SAP2000 24.0 |
| Geometry | 3 storeys at 3.0 m (9 m high), 12 columns, 87 frame members |
| Sections | Columns 300 × 300 mm, beams 230 × 300 mm (M30); 125 mm slab |
| Loads | Self-weight; 24.3 kN/m wall load on beams; 2.0 kN/m² additional dead load; 3.0 kN/m² live load |
| Combinations | 1.4DL · 1.2DL + 1.6LL · 1.5DL · 1.5(DL + LL) |

## spaghetti bridge: concept models

Concept models for a spaghetti model-bridge design, comparing a flat truss with an arch truss.

![Arch truss concept with axial forces](spaghetti%20bridge/images/arch-truss-axial.png)

| Model | Description |
|---|---|
| `basic.$2k` | 0.8 m span, 0.2 m deep flat truss with 75 members, modelled as Ø5.5 mm spaghetti rods (custom material: E = 5 GPa, γ = 12.75 kN/m³) under a single point load |
| `arch.$2k` | 0.7 m span arch truss (rise ≈ 0.17 m) with a distributed deck load; members still use a placeholder steel section |
| `arch 2.$2k` | The arch geometry scaled to a 70 m span for comparison |

**Next steps:** assign the spaghetti section to the arch model, check member forces against the tensile and buckling capacity of spaghetti, and compare the two concepts by load-to-self-weight ratio.

## Opening the files

Open the `.sdb` models in **SAP2000 24 or later** (or import the `.$2k` text files). Analysis output files are not stored in the repository, so run the analysis after opening a model.
