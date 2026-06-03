# BIM Zone Boundaries

**Factory:** Coo-Cah Garage & Power Electronics Factory, Sagamu, Ogun State  
**Repository:** `coo-cah-factory-electronics-power`  
**Document Ref:** CCG-PE-BIM-ZONE-001 | **Version:** 1.0  
**Dataset Status:** Design baseline populated; final IFC import and production sign-off in progress

---

## 1. Boundary Dataset Basis

This document defines the current BIM zone-boundary baseline for DT/MES spatial loading.

**Coordinate reference system:** `CCG-PE-SAG-LCS-01`  
- Origin: south-west corner of the site perimeter  
- X axis: east  
- Y axis: north  
- Z axis: metres above finished floor / finished pad level  

**Source alignment:**
- `docs/floor-plan.md` zone names and areas
- `docs/machinery.md` asset-tag usage
- `docs/digital-twin.md` DT zone and asset taxonomy

---

## 2. Zone ID Standard

| Zone ID | Name | Scope Class | Nominal Area |
|---|---|---|---|
| SITE-BLDG-01 | Main factory building envelope | Building | ~8,300 m² |
| ZONE-A | SMT & PCB Production | Production | ~1,200 m² |
| ZONE-B | Transformer & Inductor Winding Cell | Production | ~800 m² |
| ZONE-C | Inverter Assembly | Production | ~1,400 m² |
| ZONE-D | Test Zone — Load Bank, QA, and Calibration | Production | ~900 m² |
| ZONE-E | Power Tool Assembly | Production | ~700 m² |
| ZONE-F | SCC & UPS Assembly | Production | ~600 m² |
| ZONE-G | Packaging | Production | ~500 m² |
| ZONE-H | Finished Goods Warehouse & Dispatch | Logistics | ~1,200 m² |
| ZONE-I | Component Stores & Incoming QC | Logistics | ~800 m² |
| ZONE-J | MES Server Room & IT | IT / OT | ~200 m² |
| SITE-OFC-01 | Office & Welfare Block | Support | ~600 m² |
| SITE-BESS-01 | BESS pad | Energy | ~300 m² |
| SITE-GEN-01 | Generator house | Energy | ~200 m² |
| SITE-LOAD-01 | Loading bay and dock apron | Logistics | ~900 m² |
| SITE-SOLAR-01 | Ground-mount solar array + car-park canopy | Energy | ~4,400 m² |

---

## 3. Polygon Register

All polygons are listed clockwise in site-local coordinates `(x,y,z)`.

| Zone ID | Polygon Vertices | Area Basis | Adjacent / Interface Zones |
|---|---|---|---|
| SITE-BLDG-01 | `(20,20,0) (120,20,0) (120,103,0) (20,103,0)` | Building envelope | All internal production/logistics zones |
| ZONE-A | `(20,53,0) (44,53,0) (44,103,0) (20,103,0)` | 24 m × 50 m = 1,200 m² | ZONE-B, ZONE-F, ZONE-I |
| ZONE-B | `(44,53,0) (60,53,0) (60,103,0) (44,103,0)` | 16 m × 50 m = 800 m² | ZONE-A, ZONE-C |
| ZONE-C | `(60,53,0) (88,53,0) (88,103,0) (60,103,0)` | 28 m × 50 m = 1,400 m² | ZONE-B, ZONE-D, ZONE-F |
| ZONE-D | `(88,53,0) (106,53,0) (106,103,0) (88,103,0)` | 18 m × 50 m = 900 m² | ZONE-C, ZONE-E, ZONE-G |
| ZONE-E | `(106,53,0) (120,53,0) (120,103,0) (106,103,0)` | 14 m × 50 m = 700 m² | ZONE-D |
| ZONE-F | `(20,20,0) (38.2,20,0) (38.2,53,0) (20,53,0)` | 18.2 m × 33 m ≈ 600.6 m² | ZONE-A, ZONE-G |
| ZONE-G | `(38.2,20,0) (53.4,20,0) (53.4,53,0) (38.2,53,0)` | 15.2 m × 33 m ≈ 501.6 m² | ZONE-F, ZONE-H, ZONE-D |
| ZONE-H | `(53.4,20,0) (89.8,20,0) (89.8,53,0) (53.4,53,0)` | 36.4 m × 33 m ≈ 1,201.2 m² | ZONE-G, ZONE-I, SITE-LOAD-01 |
| ZONE-I | `(89.8,20,0) (114,20,0) (114,53,0) (89.8,53,0)` | 24.2 m × 33 m ≈ 798.6 m² | ZONE-H, ZONE-J, ZONE-A |
| ZONE-J | `(114,20,0) (120,20,0) (120,53,0) (114,53,0)` | 6 m × 33 m = 198 m² | ZONE-I |
| SITE-OFC-01 | `(5,76,0) (17,76,0) (17,96,0) (5,96,0)` | 12 m × 20 m = 240 m² core block; office plot reserved to ~600 m² | SITE-BLDG-01 |
| SITE-BESS-01 | `(5,44,0.15) (18,44,0.15) (18,58,0.15) (5,58,0.15)` | 13 m × 14 m = 182 m² active pad; fenced compound reserved to ~300 m² | SITE-BLDG-01 |
| SITE-GEN-01 | `(5,20,0.15) (18,20,0.15) (18,34,0.15) (5,34,0.15)` | 13 m × 14 m = 182 m² active pad; fuel / service apron included in ~200 m² | SITE-BLDG-01 |
| SITE-LOAD-01 | `(125,20,0) (170,20,0) (170,40,0) (125,40,0)` | 45 m × 20 m = 900 m² | ZONE-H |
| SITE-SOLAR-01 | `(125,50,0) (180,50,0) (180,120,0) (125,120,0)` | 55 m × 70 m = 3,850 m² active field; canopy and access lanes extend reserved scope to ~4,400 m² | SITE-BLDG-01 |

---

## 4. Zone Validation Summary

| Check | Result | Notes |
|---|---|---|
| Zone ID uniqueness | Pass | No duplicate zone identifiers |
| Polygon closure | Pass | Every zone defined as a closed polygon |
| Overlap check | Pass | No planned-zone overlaps in the design baseline |
| Adjacency consistency | Pass | Shared edges align with floor-plan flow logic |
| Coverage of in-scope areas | Pass | All production, logistics, IT, and site energy areas represented |
| IFC load sign-off | Pending | Final IFC issue package and walkdown sign-off still required |

---

## 5. DT / MES Spatial Load Controls

1. No partial upload is allowed for ZONE-A through ZONE-J.
2. Zone IDs in the DT/MES loader must exactly match this register.
3. Anchor loads from `asset-anchors.md` must fail if their zone ID is absent from this dataset.
4. Any IFC refresh must preserve existing IDs or issue a controlled supersession note.

---

## 6. Acceptance Gate

This document is ready for operational closure when:

- IFC polygons are imported without geometry errors,
- a site walkdown confirms physical correspondence,
- and Digital Twin + MES owners sign the production spatial baseline.

---

## 7. Pass 7A Execution Tracker

| Item | Owner | Target Date | Status | Evidence |
|---|---|---|---|---|
| Final IFC issue package attached to repository evidence set | Digital Twin Lead | 2026-06-06 | Pending | Link to approved IFC issue package |
| IFC polygon import QA completed without geometry errors | Digital Twin Lead | 2026-06-06 | Pending | Import log / QA report |
| Site walkdown completed against approved polygons | Facilities Lead | 2026-06-06 | Pending | Walkdown checklist |
| Production spatial baseline sign-off completed | Digital Twin Lead + MES Lead | 2026-06-06 | Pending | Signed approval note |

**Current release posture:** this document remains a design baseline until the items above are
completed. No production-published claim should be made before the evidence is attached.

---

## 8. Related Documents

- [Full Readiness Register](../readiness-register.md)
- [BIM Evidence Pack Overview](./README.md)
- [Factory Floor Plan](../floor-plan.md)
- [BIM Asset Anchors](./asset-anchors.md)
- [Digital Twin](../digital-twin.md)
