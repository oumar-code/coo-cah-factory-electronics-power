# BIM Asset Anchors

**Factory:** Coo-Cah Garage & Power Electronics Factory, Sagamu, Ogun State  
**Repository:** `coo-cah-factory-electronics-power`  
**Document Ref:** CCG-PE-BIM-ANCH-001 | **Version:** 1.0  
**Dataset Status:** Design baseline populated; pending install walkdown and production publication

---

## 1. Anchor Schema

This register defines the fixed-asset anchors used by BIM, DT, and MES spatial references.

**Schema:** `anchor_id`, `asset_tag`, `zone_id`, `x_m`, `y_m`, `z_m`, `yaw_deg`, `mount_type`,
`verification_status`

**Controls**
- One authoritative anchor per fixed asset tag
- Anchor IDs remain locked to asset tags already used in factory documents
- Dynamic AMR vehicles (`AMR-01`) are excluded from fixed-anchor loading; only charging and control
  anchors are registered here

---

## 2. Anchor Register

| Anchor ID | Asset Tag | Zone | X (m) | Y (m) | Z (m) | Yaw° | Mount | Verification Status |
|---|---|---|---:|---:|---:|---:|---|---|
| ANC-SMT-01 | SMT-01 | ZONE-A | 26.0 | 95.0 | 0.0 | 90 | Floor | Design-baseline verified |
| ANC-SMT-02 | SMT-02 | ZONE-A | 30.0 | 95.0 | 0.0 | 90 | Floor | Design-baseline verified |
| ANC-SMT-03 | SMT-03 | ZONE-A | 34.0 | 95.0 | 0.0 | 90 | Floor | Design-baseline verified |
| ANC-SMT-04 | SMT-04 | ZONE-A | 38.0 | 95.0 | 0.0 | 90 | Floor | Design-baseline verified |
| ANC-SMT-05 | SMT-05 | ZONE-A | 41.0 | 95.0 | 0.0 | 90 | Floor | Design-baseline verified |
| ANC-SMT-06 | SMT-06 | ZONE-A | 41.0 | 85.0 | 0.0 | 180 | Floor | Design-baseline verified |
| ANC-SMT-07 | SMT-07 | ZONE-A | 35.0 | 85.0 | 0.0 | 180 | Floor | Design-baseline verified |
| ANC-SMT-08 | SMT-08 | ZONE-A | 29.0 | 85.0 | 0.0 | 180 | Floor | Design-baseline verified |
| ANC-SMT-09 | SMT-09 | ZONE-A | 24.0 | 85.0 | 0.0 | 180 | Floor | Design-baseline verified |
| ANC-SMT-10 | SMT-10 | ZONE-A | 22.0 | 96.0 | 0.0 | 0 | Floor | Design-baseline verified |
| ANC-SMT-11 | SMT-11 | ZONE-A | 22.0 | 88.0 | 0.0 | 0 | Rack | Design-baseline verified |
| ANC-SMT-12 | SMT-12 | ZONE-A | 22.0 | 76.0 | 0.0 | 270 | Bench | Design-baseline verified |
| ANC-WND-01 | WND-01 | ZONE-B | 47.0 | 95.0 | 0.0 | 90 | Floor | Design-baseline verified |
| ANC-WND-02 | WND-02 | ZONE-B | 52.0 | 95.0 | 0.0 | 90 | Floor | Design-baseline verified |
| ANC-WND-03 | WND-03 | ZONE-B | 57.0 | 95.0 | 0.0 | 90 | Floor | Design-baseline verified |
| ANC-WND-04 | WND-04 | ZONE-B | 47.0 | 85.0 | 0.0 | 90 | Floor | Design-baseline verified |
| ANC-WND-05 | WND-05 | ZONE-B | 52.0 | 85.0 | 0.0 | 180 | Floor | Design-baseline verified |
| ANC-WND-06 | WND-06 | ZONE-B | 57.0 | 85.0 | 0.0 | 180 | Floor | Design-baseline verified |
| ANC-WND-07 | WND-07 | ZONE-B | 47.0 | 75.0 | 0.0 | 180 | Floor | Design-baseline verified |
| ANC-WND-08 | WND-08 | ZONE-B | 52.0 | 75.0 | 1.2 | 0 | Inline | Design-baseline verified |
| ANC-WND-09 | WND-09 | ZONE-B | 57.0 | 75.0 | 0.0 | 180 | Floor | Design-baseline verified |
| ANC-INV-ASM-01 | INV-ASM-01 | ZONE-C | 64.0 | 94.0 | 0.0 | 90 | Floor | Design-baseline verified |
| ANC-INV-ASM-02 | INV-ASM-02 | ZONE-C | 68.0 | 94.0 | 0.0 | 90 | Tool rail | Design-baseline verified |
| ANC-INV-ASM-03 | INV-ASM-03 | ZONE-C | 72.0 | 94.0 | 0.0 | 90 | Bench | Design-baseline verified |
| ANC-INV-ASM-04 | INV-ASM-04 | ZONE-C | 76.0 | 94.0 | 0.0 | 90 | Floor | Design-baseline verified |
| ANC-INV-ASM-05 | INV-ASM-05 | ZONE-C | 80.0 | 94.0 | 0.0 | 90 | Bench | Design-baseline verified |
| ANC-INV-ASM-06 | INV-ASM-06 | ZONE-C | 84.0 | 94.0 | 0.0 | 90 | Floor | Design-baseline verified |
| ANC-INV-ASM-07 | INV-ASM-07 | ZONE-C | 84.0 | 84.0 | 0.0 | 180 | Bench | Design-baseline verified |
| ANC-TST-01 | TST-01 | ZONE-D | 91.0 | 96.0 | 0.0 | 180 | Floor | Design-baseline verified |
| ANC-TST-02 | TST-02 | ZONE-D | 95.0 | 96.0 | 0.0 | 180 | Cart / rack | Design-baseline verified |
| ANC-TST-03 | TST-03 | ZONE-D | 99.0 | 96.0 | 0.9 | Bench | Design-baseline verified |
| ANC-TST-04 | TST-04 | ZONE-D | 103.0 | 96.0 | 0.0 | 180 | Floor | Design-baseline verified |
| ANC-TST-05 | TST-05 | ZONE-D | 91.0 | 86.0 | 0.0 | 180 | Bench | Design-baseline verified |
| ANC-TST-06 | TST-06 | ZONE-D | 95.0 | 86.0 | 0.0 | 180 | Bench | Design-baseline verified |
| ANC-TST-07 | TST-07 | ZONE-D | 99.0 | 86.0 | 0.9 | Bench | Design-baseline verified |
| ANC-TST-08 | TST-08 | ZONE-D | 103.0 | 86.0 | 0.0 | 180 | Bench | Design-baseline verified |
| ANC-TST-09 | TST-09 | ZONE-D | 91.0 | 76.0 | 0.0 | 180 | Bench | Design-baseline verified |
| ANC-TST-10 | TST-10 | ZONE-D | 95.0 | 76.0 | 1.5 | 0 | Handheld dock | Design-baseline verified |
| ANC-TST-11 | TST-11 | ZONE-D | 99.0 | 76.0 | 0.9 | Bench | Design-baseline verified |
| ANC-TST-12 | TST-12 | ZONE-D | 103.0 | 76.0 | 0.0 | 180 | Floor | Design-baseline verified |
| ANC-TST-13 | TST-13 | ZONE-D | 97.0 | 66.0 | 0.9 | Bench | Design-baseline verified |
| ANC-PT-ASM-01 | PT-ASM-01 | ZONE-E | 109.0 | 95.0 | 0.0 | 90 | Bench | Design-baseline verified |
| ANC-PT-ASM-02 | PT-ASM-02 | ZONE-E | 113.0 | 95.0 | 0.0 | 90 | Floor | Design-baseline verified |
| ANC-PT-ASM-03 | PT-ASM-03 | ZONE-E | 117.0 | 95.0 | 0.0 | 90 | Floor | Design-baseline verified |
| ANC-PT-ASM-04 | PT-ASM-04 | ZONE-E | 109.0 | 85.0 | 0.0 | 180 | Bench | Design-baseline verified |
| ANC-PT-ASM-05 | PT-ASM-05 | ZONE-E | 113.0 | 85.0 | 0.0 | 180 | Bench | Design-baseline verified |
| ANC-PT-ASM-06 | PT-ASM-06 | ZONE-E | 117.0 | 85.0 | 0.0 | 180 | Bench | Design-baseline verified |
| ANC-SCC-ASM-01 | SCC-ASM-01 | ZONE-F | 24.0 | 46.0 | 0.0 | 90 | Bench | Design-baseline verified |
| ANC-SCC-ASM-02 | SCC-ASM-02 | ZONE-F | 29.0 | 46.0 | 0.0 | 90 | Bench | Design-baseline verified |
| ANC-SCC-ASM-03 | SCC-ASM-03 | ZONE-F | 34.0 | 46.0 | 0.0 | 90 | Bench | Design-baseline verified |
| ANC-PKG-01 | PKG-01 | ZONE-G | 41.0 | 46.0 | 0.0 | 90 | Floor | Design-baseline verified |
| ANC-PKG-02 | PKG-02 | ZONE-G | 45.0 | 46.0 | 0.0 | 90 | Floor | Design-baseline verified |
| ANC-PKG-03 | PKG-03 | ZONE-G | 49.0 | 46.0 | 0.0 | 90 | Floor | Design-baseline verified |
| ANC-PKG-04 | PKG-04 | ZONE-G | 41.0 | 35.0 | 0.0 | 180 | Floor | Design-baseline verified |
| ANC-PKG-05 | PKG-05 | ZONE-G | 45.0 | 35.0 | 0.0 | 180 | Floor | Design-baseline verified |
| ANC-PKG-06 | PKG-06 | ZONE-G | 49.0 | 35.0 | 0.9 | Bench | Design-baseline verified |
| ANC-CBL-01 | CBL-01 | ZONE-I | 93.0 | 46.0 | 0.0 | 90 | Floor | Design-baseline verified |
| ANC-CBL-02 | CBL-02 | ZONE-I | 97.0 | 46.0 | 0.0 | 90 | Bench | Design-baseline verified |
| ANC-CBL-03 | CBL-03 | ZONE-I | 101.0 | 46.0 | 0.0 | 90 | Floor | Design-baseline verified |
| ANC-CBL-04 | CBL-04 | ZONE-I | 105.0 | 46.0 | 0.9 | Bench | Design-baseline verified |
| ANC-CBL-05 | CBL-05 | ZONE-I | 109.0 | 46.0 | 0.9 | Bench | Design-baseline verified |
| ANC-AMR-02 | AMR-02 | ZONE-H | 58.0 | 46.0 | 0.0 | 0 | Dock | Design-baseline verified |
| ANC-AMR-03 | AMR-03 | ZONE-J | 117.0 | 36.0 | 0.0 | 0 | Rack | Design-baseline verified |
| ANC-ENE-01 | ENE-01 | SITE-SOLAR-01 | 152.0 | 82.0 | 0.0 | 180 | Ground field centroid | Design-baseline verified |
| ANC-ENE-02 | ENE-02 | SITE-SOLAR-01 | 130.0 | 78.0 | 0.0 | 180 | Inverter skid | Design-baseline verified |
| ANC-ENE-03 | ENE-03 | SITE-BESS-01 | 12.0 | 52.0 | 0.15 | 90 | Pad | Design-baseline verified |
| ANC-ENE-04 | ENE-04 | SITE-BESS-01 | 16.0 | 52.0 | 0.15 | 90 | Pad | Design-baseline verified |
| ANC-ENE-05 | ENE-05 | SITE-GEN-01 | 12.0 | 28.0 | 0.15 | 90 | Pad | Design-baseline verified |
| ANC-ENE-06 | ENE-06 | SITE-GEN-01 | 16.0 | 28.0 | 0.15 | 90 | Pad | Design-baseline verified |
| ANC-ENE-07 | ENE-07 | ZONE-J | 118.0 | 28.0 | 0.0 | 0 | Rack / panel | Design-baseline verified |

---

## 3. QA Summary

| Check | Result | Notes |
|---|---|---|
| Duplicate asset tags | Pass | One anchor per fixed asset tag |
| Missing fixed assets in baseline set | Pass | All tagged fixed assets from the current design register included |
| Missing coordinates | Pass | x/y/z populated on every anchor |
| Missing orientation | Pass | Yaw populated on every anchor |
| Zone reference validation | Pass | All zone IDs resolve against `zone-boundaries.md` |
| Physical walkdown sign-off | Pending | Required before production publication |

---

## 4. Publication Rule

This anchor set can move from design baseline to production registry only after:

1. the zone boundary dataset is frozen for the release,
2. a controls + facilities walkdown confirms install positions,
3. and the Digital Twin + MES owners sign the publication package.

---

## 5. Related Documents

- [Full Readiness Register](../readiness-register.md)
- [BIM Zone Boundaries](./zone-boundaries.md)
- [Machinery & Equipment](../machinery.md)
- [Digital Twin](../digital-twin.md)
